# Instalação do IBExpert no Linux usando Bottles

## **INSTALAÇÃO**
Instale o software **Bottles** no Linux usando qualquer repositório (o Flathub é recomendado).
---

## **CRIAR UMA NOVA GARRAFA**
Crie uma garrafa personalizada com as seguintes especificações:

- **Nome**: `IBExpert-x32`  
- **Arquitetura**: 32 bits  
- **Versão**: Windows 10/11  
- **Runner**: `soda-9.0.1` (ou `sys-wine-10`)

Em seguida, selecione a garrafa recém-criada `IBExpert-x32`, vá para a seção **Dependências** e adicione:

- `allfonts` (inclui fontes essenciais da Microsoft e Adobe)
- `consolas`
- `lucon`
- `vcredist2008`

> ⚠️ **Importante**: Evite instalar as seguintes dependências, pois podem quebrar sua garrafa:
> - `mdac28`
> - outra cópia de `vcredist2008` como `vcredist2005`, `vcredist2010`,...  
> 
> Se quiser testar outras dependências, **faça um backup** da sua garrafa antes.

Sua garrafa estará localizada em: `~/.var/app/com.usebottles.bottles/data/bottles/bottles/IBExpert-x32`.

Você já pode fechar a garrafa.

---

## **DOWNLOAD**
Coloque os seguintes instaladores na sua pasta `~/Downloads`:

- Cliente Firebird Database (versão 32 bits)  
- Instalador do IBExpert  

> ⚠️ Observação: Às vezes, a janela do instalador do Windows abre *atrás* da janela principal do Bottles — verifique com atenção.

---

## **INSTALAÇÃO DENTRO DA GARRAFA**
Reabra o Bottles, selecione `IBExpert-x32` e clique em **Iniciar Programa**.

Instale os seguintes pacotes a partir da pasta `~/Downloads`:

1. **Cliente Firebird Database (x86)**
   - Instalar em: `C:\fb5`
   - Desmarcar “Server Components”
   - Marcar “Don’t create a Start Menu Folder”
   - Desmarcar “Show What’s New after installation”

2. **IBExpert**
   - Usar a instalação padrão ou instalar no local de sua preferência.

---

## **IBEXPERT - PRIMEIRA CONFIGURAÇÃO**
Na primeira vez que executar o IBExpert, ele perguntará se deseja escolher entre o modo MDI ou SDI.  
**Escolha MDI**, pois o SDI pode não funcionar bem no Linux.

Quando tudo estiver funcionando, vá em **Preferências** no Bottles e ative **“Fechar garrafa após iniciar o programa”**.  
Isso evitará que você tenha que fechar a garrafa manualmente todas as vezes.

---

## **CONCLUSÃO**
Depois que tudo estiver instalado e funcionando na garrafa `IBExpert-x32`, **não altere** suas configurações nem adicione mais dependências.

Se quiser testar alterações, **use a opção “Clonar”** e modifique a garrafa clonada.
