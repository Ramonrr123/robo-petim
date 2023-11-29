# robo-petim
robo de testes automatizados petim

from selenium import webdriver
from selenium.webdriver import Chrome
from selenium.webdriver.common.keys import Keys
from time import sleep

login = 14385854971
senha = 123456 

def digitar_como_pessoa(texto):
    texto_digitado = ''
    for letra in texto:
        texto_digitado += letra
        print(letra, end='', flush=True)
        sleep(0.05)
    print()
    return texto_digitado

def tv_marins(titulo, resumo):

    navegador = webdriver.Chrome()

    navegador.get('https://petim.pormadeonline.com.br/')
    sleep(4)

    digite_seu_usuario = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/div[1]/input')

    digite_seu_usuario.send_keys(login)

    campo_senha = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/div[2]/input')
    sleep(3)
    

    campo_senha.send_keys(senha)

    sleep(3)

    botao_acessar = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/button')
    sleep(3)

    botao_acessar.click()
    sleep(4)

    acessar_marins =navegador.find_element('xpath','/html/body/div/div/div[2]/div/div[2]/div[7]/a/button/h1')
    acessar_marins.click()
    sleep(3)

    campo_titulo = navegador.find_element('xpath','/html/body/div/div/div[2]/div[2]/div[1]/div/input')
    campo_titulo.click()
    sleep(2)
    campo_titulo.send_keys(digitar_como_pessoa(titulo))
    sleep(2)

    campo_resumo = navegador.find_element('xpath','/html/body/div/div/div[2]/div[2]/div[2]/div/div[2]/textarea')
    campo_resumo.click()
    sleep(2)
    campo_resumo.send_keys(digitar_como_pessoa(resumo))
    sleep(4)

def resumo_livro(resumosemanal):

    navegador = webdriver.Chrome()

    navegador.get('https://petim.pormadeonline.com.br/')
    sleep(4)

    digite_seu_usuario = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/div[1]/input')

    digite_seu_usuario.send_keys(login)

    campo_senha = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/div[2]/input')
    sleep(3)

    campo_senha.send_keys(senha)

    sleep(3)

    botao_acessar = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/button')
    sleep(3)

    botao_acessar.click()
    sleep(4)

    acessar_resumo_livro = navegador.find_element('xpath','/html/body/div/div/div[2]/div/div[2]/div[6]/a/button')
    sleep(1.2)
    acessar_resumo_livro.click()
    sleep(3)

    navegador.execute_script("window.scrollTo(3000, document.body.scrollHeight);")
    sleep(6)

    campo_resumo_livro = navegador.find_element('xpath','/html/body/div/div/div[2]/div/div[3]/div/div[2]/textarea')
    sleep(1)
    campo_resumo_livro.click()
    sleep(1)
    campo_resumo_livro.clear()
    sleep(0.5)

    campo_resumo_livro.send_keys(digitar_como_pessoa(resumosemanal))
    sleep(10)

def impossivell(resumo_impossivel):
    navegador = webdriver.Chrome()

    navegador.get('https://petim.pormadeonline.com.br/')
    sleep(4)

    digite_seu_usuario = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/div[1]/input')

    digite_seu_usuario.send_keys(login)

    campo_senha = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/div[2]/input')
    sleep(3)
    

    campo_senha.send_keys(senha)

    sleep(3)

    botao_acessar = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/button')
    sleep(3)

    botao_acessar.click()
    sleep(4)

    acessar_impossivel = navegador.find_element('xpath','/html/body/div/div/div[2]/div/div[2]/div[3]/a/button/h1')

    acessar_impossivel.click()
    sleep(3)

    situacao = navegador.find_element('xpath','/html/body/div/div/div[2]/div[1]/div/div[2]/div/div[2]/textarea')
    
    situacao.click()
    sleep(1)
    situacao.clear()
    sleep(3)
    situacao.send_keys(digitar_como_pessoa(resumo_impossivel))
    sleep(6)

    botao_enviar = navegador.find_element('xpath','/html/body/div/div/div[2]/div[1]/div/div[3]/button')
    sleep(1)
    botao_enviar.click()
    sleep(10)

def coisa_boa(texto):
    navegador = webdriver.Chrome()

    navegador.get('https://petim.pormadeonline.com.br/')
    sleep(4)

    digite_seu_usuario = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/div[1]/input')

    digite_seu_usuario.send_keys(login)

    campo_senha = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/div[2]/input')
    sleep(3)
    

    campo_senha.send_keys(senha)

    sleep(3)

    botao_acessar = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/button')
    sleep(3)

    botao_acessar.click()
    sleep(4)

    coisa_boa = navegador.find_element('xpath','/html/body/div/div/div[2]/div/div[2]/div[1]/a/button/h1')
    
    coisa_boa.click()
    sleep(4)

    campo_coisa_boa =navegador.find_element('xpath','/html/body/div/div/div[2]/div[1]/div[2]/div[1]/div/div[2]/textarea')
    campo_coisa_boa.click()
    sleep(0.5)
    campo_coisa_boa.clear()
    sleep(0.5)
    campo_coisa_boa.send_keys(digitar_como_pessoa(texto))
    sleep(4)

    botao_enviar = navegador.find_element('xpath','/html/body/div/div/div[2]/div[1]/div[2]/div[2]/button')
    
    botao_enviar.click()
    sleep(5)

def erros_tesouros(erro,solucao):
    navegador = webdriver.Chrome()

    navegador.get('https://petim.pormadeonline.com.br/')
    sleep(4)

    digite_seu_usuario = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/div[1]/input')

    digite_seu_usuario.send_keys(login)

    campo_senha = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/div[2]/input')
    sleep(3)
    

    campo_senha.send_keys(senha)

    sleep(3)

    botao_acessar = navegador.find_element('xpath','/html/body/div/div/div/div[1]/form/button')
    sleep(3)

    botao_acessar.click()
    sleep(4)

    acessar_erro =navegador.find_element('xpath','/html/body/div/div/div[2]/div/div[2]/div[2]/a/button/h1')
   
    acessar_erro.click()
    sleep(5)
    
    campo_erro = navegador.find_element('xpath','/html/body/div/div/div[2]/div[1]/div[2]/div/div/div[2]/textarea')
    campo_erro.click()
    sleep(1)
    campo_erro.clear()
    sleep(1)
    campo_erro.send_keys(digitar_como_pessoa(erro))
    sleep(5)

    campo_solucao = navegador.find_element('xpath','/html/body/div/div/div[2]/div[1]/div[3]/div[1]/div/div[2]/textarea')
    
    campo_solucao.click()
    sleep(0.5)
    
    campo_solucao.clear()
    sleep(0.5)
   
    campo_solucao.send_keys(digitar_como_pessoa(solucao))
    sleep(5)

    botao_enviar = navegador.find_element('xpath','/html/body/div/div/div[2]/div[1]/div[3]/div[2]/button')
    sleep(2)
    
    botao_enviar.click()
    sleep(7)





]
