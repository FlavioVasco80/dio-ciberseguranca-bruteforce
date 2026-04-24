# Projeto de Cibersegurança: Simulação de Ataque de Força Bruta
Projeto prático de cibersegurança focado em ataques de força bruta com Medusa e Kali Linux, desenvolvido para o Bootcamp da DIO 

# Descrição do Projeto

Este projeto documenta a análise técnica e a simulação de ataques de força bruta (Brute Force) utilizando o Kali Linux e a ferramenta Medusa. O objetivo é demonstrar a vulnerabilidade de sistemas mal configurados ou legados e propor medidas de mitigação eficazes.

# Tecnologias e Ferramentas Estudadas 

Sistema Atacante: Kali Linux.  

Sistema Alvo (Cenário Proposto): Windows XP (Representando sistemas legados em ambientes corporativos e de logística).

Ferramenta de Ataque: Medusa (focada em força bruta paralela).  

Protocolo Analisado: SMB (Server Message Block).  
# Metodologia e Execução Teórica

Devido a limitações de hardware para virtualização simultânea, o projeto foi executado através do estudo profundo da sintaxe e lógica das ferramentas.  

1. Preparação de Wordlists
   
Foram estruturadas listas de usuários e senhas para simular a tentativa e erro do ataque.  

* Exemplo de comando para criar lista de usuários: echo -e "admin\nadministrador\nuser" > usuarios.txt.  

2. Comando de Execução (Medusa)
O comando abaixo ilustra como seria realizada a auditoria no protocolo SMB:

*medusa -h [IP_ALVO] -U usuarios.txt -P senhas.txt -M smb*

-h: Define o IP do host alvo.  
-U/-P: Caminhos para as listas de usuários e senhas.  
-M: Módulo do protocolo utilizado (SMB).  

# Medidas de Mitigação (Prevenção) 

Para evitar o sucesso desse tipo de ataque, as seguintes práticas são essenciais:  

* Políticas de Senha: Implementação de senhas complexas (letras, números e símbolos).

* Bloqueio de Conta: Configurar o sistema para travar após 3 ou 5 tentativas falhas de login.

* MFA (Múltiplo Fator de Autenticação): Adição de uma camada extra de segurança além da senha.

* Atualização de Sistemas: Migrar de sistemas legados (como o Windows XP) para versões modernas que corrigem falhas de segurança conhecidas.

# Conclusão 

O desafio permitiu compreender profundamente a lógica de ataques por força bruta e a importância de ferramentas clássicas como o Medusa na auditoria de segurança. A documentação clara do processo é o primeiro passo para uma defesa sólida em qualquer infraestrutura de TI. 
