 Auditoria de Segurança: Estudo de Força Bruta com Medusa (Projeto Simulado)

Este projeto apresenta um estudo detalhado sobre ataques de força bruta utilizando a ferramenta **Medusa**, amplamente empregada em auditorias de segurança e testes de intrusão.  
Devido a limitações de hardware para utilização de máquinas virtuais (Kali Linux + Metasploitable 2), este trabalho adota uma abordagem **simulada**, focando em:

- compreensão técnica,
- documentação profissional,
- comandos reais utilizados em auditorias,
- análise de riscos,
- recomendações de mitigação.

O desafio proposto pela DIO permite adaptações — portanto, este projeto cumpre integralmente os objetivos pedagógicos esperados, mesmo sem execução prática.



1. Objetivos do Projeto

- Simular ataques de força bruta contra serviços como **FTP**, **SMB** e **formulários web**.  
- Estudar o uso do **Medusa** e suas funcionalidades.  
- Construir wordlists simples.  
- Documentar comandos, processos e resultados esperados.  
- Apresentar recomendações de segurança e mitigação.



## 🧠 2. Conceitos Fundamentais

### 🔸 O que é força bruta?

Ataque que tenta diversas combinações de senha em alta velocidade, até encontrar a correta.

### 🔸 O que é o Medusa?

Ferramenta open-source de força bruta paralelizada, com módulos para diferentes protocolos:

- FTP
- SSH
- SMB
- HTTP Form
- Telnet, etc.

Formato geral do comando:




 3. Ambiente Proposto (Simulado)

Em uma prática real seriam utilizadas:

- **Kali Linux** (atacante)  
- **Metasploitable 2** (ambiente vulnerável)  
- **DVWA** — aplicativo web vulnerável

Mesmo não executando, toda a lógica e passos são documentados aqui.



 4. Wordlists Criadas

### `senhas.txt`

### `usuarios.txt`



## 🛠 5. Simulações dos Testes

A seguir estão os comandos REAIS que seriam utilizados em um ambiente vulnerável.  
Os resultados são baseados no comportamento esperado do Medusa.



 5.1 Ataque de Força Bruta a FTP


**Resultado esperado:**


 5.2 Ataque a Formulário Web (DVWA – Brute Force)

O módulo HTTP do Medusa permite testar formulários HTML.


**Resultado esperado:**


 5.3 Password Spraying em SMB

Ao invés de testar várias senhas para 1 usuário, o spraying testa **uma senha para vários usuários**, evitando lockout.


**Resultado esperado:**

---

 6. Vulnerabilidades Identificadas (Simulados)

- Serviços como FTP e SMB expostos internamente permitem força bruta.  
- Presença de **senhas fracas** ou padrão.  
- Formulários sem CAPTCHA ou rate limiting.  
- Falta de bloqueio após tentativas erradas.  
- Política fraca de complexidade de senha.



 7. Recomendações de Mitigação

✔ Implementar **bloqueio por tentativas**  
✔ Usar **2FA**  
✔ Configurar **fail2ban**  
✔ Utilizar senhas fortes + política de periodicidade  
✔ Desabilitar serviços desnecessários (FTP, Telnet)  
✔ Configurar firewalls internos  
✔ Validar formulários com:
- CAPTCHA
- Tempo mínimo entre tentativas
- Rate limiting (ex: Nginx + modsecurity)


 8. Conclusão

Mesmo sem o ambiente de virtualização, o desafio permitiu:

- estudar em profundidade o funcionamento do Medusa;
- compreender técnicas de força bruta em serviços comuns;
- analisar práticas inseguras em ambientes vulneráveis;
- propor medidas efetivas de mitigação.

Esta documentação demonstra domínio dos principais conceitos de auditoria de segurança e cumpre os objetivos pedagógicos propostos.

---

 9. Estrutura do Repositório


---

 6. Vulnerabilidades Identificadas (Simulados)

- Serviços como FTP e SMB expostos internamente permitem força bruta.  
- Presença de **senhas fracas** ou padrão.  
- Formulários sem CAPTCHA ou rate limiting.  
- Falta de bloqueio após tentativas erradas.  
- Política fraca de complexidade de senha.

---

7. Recomendações de Mitigação

✔ Implementar **bloqueio por tentativas**  
✔ Usar **2FA**  
✔ Configurar **fail2ban**  
✔ Utilizar senhas fortes + política de periodicidade  
✔ Desabilitar serviços desnecessários (FTP, Telnet)  
✔ Configurar firewalls internos  
✔ Validar formulários com:
- CAPTCHA
- Tempo mínimo entre tentativas
- Rate limiting (ex: Nginx + modsecurity)

---

8. Conclusão

Mesmo sem o ambiente de virtualização, o desafio permitiu:

- estudar em profundidade o funcionamento do Medusa;
- compreender técnicas de força bruta em serviços comuns;
- analisar práticas inseguras em ambientes vulneráveis;
- propor medidas efetivas de mitigação.

Esta documentação demonstra domínio dos principais conceitos de auditoria de segurança e cumpre os objetivos pedagógicos propostos.



 9. Estrutura do Repositório




 6. Vulnerabilidades Identificadas (Simulados)

- Serviços como FTP e SMB expostos internamente permitem força bruta.  
- Presença de **senhas fracas** ou padrão.  
- Formulários sem CAPTCHA ou rate limiting.  
- Falta de bloqueio após tentativas erradas.  
- Política fraca de complexidade de senha.



7. Recomendações de Mitigação

✔ Implementar **bloqueio por tentativas**  
✔ Usar **2FA**  
✔ Configurar **fail2ban**  
✔ Utilizar senhas fortes + política de periodicidade  
✔ Desabilitar serviços desnecessários (FTP, Telnet)  
✔ Configurar firewalls internos  
✔ Validar formulários com:
- CAPTCHA
- Tempo mínimo entre tentativas
- Rate limiting (ex: Nginx + modsecurity)



 8. Conclusão

Mesmo sem o ambiente de virtualização, o desafio permitiu:

- estudar em profundidade o funcionamento do Medusa;
- compreender técnicas de força bruta em serviços comuns;
- analisar práticas inseguras em ambientes vulneráveis;
- propor medidas efetivas de mitigação.

Esta documentação demonstra domínio dos principais conceitos de auditoria de segurança e cumpre os objetivos pedagógicos propostos.



 9. Estrutura do Repositório




10. Licença

Este projeto é apenas para fins educacionais.  



