---
tags:
  - whatsapp
  - backup
  - depuração
  - usb
  - android
---
Esta documentação descreve o procedimento técnico para habilitar a **Depuração USB** em dispositivos Android. Este recurso é essencial para desenvolvedores, permitindo a comunicação entre o dispositivo e uma estação de trabalho via **Android Debug Bridge (ADB)**.

---

## 1. Visão Geral

Por questões de segurança, a depuração USB está oculta dentro do menu **Opções do Desenvolvedor**, que, por sua vez, vem desabilitado por padrão no sistema operacional Android. O processo consiste em duas etapas: desbloquear o menu de desenvolvedor e ativar a chave de depuração.

## 2. Pré-requisitos

- Dispositivo Android com bateria acima de 10%.
    
- Cabo de dados USB íntegro.
    

---

## 3. Passo a Passo

### Etapa 1: Desbloquear as "Opções do Desenvolvedor"

1. Acesse as **Configurações** (ícone de engrenagem) do seu aparelho.
    
2. Role até o fim e toque em **Sobre o telefone** ou **Sobre o dispositivo**.
    
3. Localize o item **Informações do software** (em alguns modelos, como Samsung).
    
4. Procure pelo **Número de compilação** (ou _Build Number_).
    
5. Toque rapidamente **7 vezes** seguidas sobre o "Número de compilação".
    
    - _Nota:_ O sistema solicitará sua senha de bloqueio de tela (PIN ou Padrão) para confirmar a ação.
        
6. Uma mensagem aparecerá dizendo: _"Você agora é um desenvolvedor!"_.
    

### Etapa 2: Ativar a Depuração USB

1. Volte à tela principal das **Configurações**.
    
2. Dependendo da marca do seu aparelho, o novo menu estará em locais diferentes:
    
    - **Geral:** Logo abaixo de "Sobre o telefone".
        
    - **Samsung:** No final da lista de configurações.
        
    - **Xiaomi/Motorola:** Dentro de **Sistema** > **Avançado** (ou Configurações Adicionais).
        
3. Toque em **Opções do desenvolvedor**.
    
4. Role a tela até encontrar a seção **Depuração**.
    
5. Ative a chave **Depuração USB**.
    
6. Uma janela de confirmação será exibida. Leia o aviso de segurança e toque em **OK**.
    

---

## 4. Autorizando o Computador

Ao conectar o celular ao computador pela primeira vez com a depuração ativa:

1. Um pop-up aparecerá na tela do celular perguntando: **"Permitir depuração USB?"**.
    
2. Aparecerá a **impressão digital da chave RSA** do computador.
    
3. Marque a opção **"Sempre permitir a partir deste computador"** e toque em **Permitir**.
    

---

## 5. Resolução de Problemas Comuns

|**Problema**|**Causa Provável**|**Solução**|
|---|---|---|
|**Opção cinza/desabilitada**|Cabo conectado em modo "Apenas Carga"|Desconecte o cabo, mude o modo USB para "Transferência de Arquivos" e tente ativar novamente.|
|**Menu não aparece**|Etapa 1 não concluída|Repita os 7 toques no Número de Compilação.|
|**PC não reconhece**|Driver ausente ou cabo ruim|Instale os drivers OEM do fabricante ou o Google USB Driver no Windows.|

---

> **Aviso de Segurança:** Mantenha a depuração USB desativada quando não estiver em uso para fins de desenvolvimento. Com ela ativa, qualquer pessoa com acesso físico ao seu aparelho e um computador pode extrair dados sensíveis mais facilmente.

Gostaria que eu explicasse como instalar os drivers necessários no seu computador para que ele reconheça o celular via comando no terminal?