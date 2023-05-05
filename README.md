# Exercicio_Funcoes_mack
#inserido 4 notas de 4 alunos e o progama retorna a lista de medias e os alunos aprovados(nota>7)
li_nota=[]
li_aprovados=[]
li_media=[]
alunos_aprovados=['aluno1', 'aluno2', 'aluno3', 'aluno4']
def entrada():
    while len(li_media)!=4:
        for i in range(4):
            nota = float(input('digite: '))
            while nota < 0 or nota > 10:
                nota=float(input('digite apenas os valores permitidos: '))
            li_nota.append(nota)
        media=sum(li_nota)/4
        li_media.append(media)
        print(f'Média do aluno {len(li_media)}: {media}')       
        if media >7: li_aprovados.append(media)
        li_nota.clear()      
    return li_aprovados, li_media

def aprovados():
    nomes_aprovados=[]
    for i in range(len(li_media)):
        valor =li_media[i]
        if valor in li_aprovados:
            nomes_aprovados.append(alunos_aprovados[i])
    return nomes_aprovados
        
    

def chamada():
    li_aprovados, li_media = entrada()
    nomes_aprovados=aprovados()
    
    print(f'\nAlunos aprovados:')
    for aluno in nomes_aprovados:
        print(aluno)

    print(f'\n Lista das medias:')
    for nota in li_media:
        print(nota)

    print()
chamada()



