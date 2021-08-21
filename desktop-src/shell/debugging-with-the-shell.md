---
description: Este tópico explica como depurar DLLs de extensão de namespace e shell.
title: Depuração com o Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 276023e5628ab7390398fd7bd367be32e45c13825fcf96625104be1ded8735de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032824"
---
# <a name="debugging-with-the-shell"></a>Depuração com o Shell

Este tópico explica como depurar DLLs de extensão de namespace e shell.

-   [Executando o shell em um depurador](#running-the-shell-under-a-debugger)
-   [Executando e testando extensões do Shell](#running-and-testing-shell-extensions)
-   [Descarregando a DLL](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a>Executando o shell em um depurador

Para depurar sua extensão, você precisa executar o Shell do depurador. Siga estas etapas:

1.  Carregue o projeto da extensão no depurador, mas não o execute.
2.  Desligue o Shell.

    -   Para Windows Vista e posterior:
        1.  Exibir **o** menu Iniciar.
        2.  Pressione CTRL+SHIFT e clique com o botão direito do mouse na parte de fundo da metade direita **do** menu Iniciar.
        3.  No menu exibido, escolha Sair **do Explorer.**
    -   Para Windows XP:
        1.  No menu **Iniciar,** escolha **Desligar**.
        2.  Pressione CTRL+ALT+SHIFT e clique **em Não** na **Desligar Windows** caixa de diálogo.

    O Shell agora está desligado, mas todos os outros aplicativos ainda estão em execução, incluindo o depurador.

3.  Depure o depurador para executar a DLL de extensão com Explorer.exe do **Windows** diretório.
4.  Execute o projeto no depurador. O Shell será lançado como de costume, mas o depurador será anexado ao processo do Shell.

## <a name="running-and-testing-shell-extensions"></a>Executando e testando extensões do Shell

Você pode executar e testar suas extensões em um processo Windows Explorer separado para evitar parar e reiniciar a área de trabalho e a barra de tarefas. A área de trabalho e a barra de tarefas ainda podem ser usadas enquanto você executar e testar as extensões.

Para habilitar esse recurso, adicione a seguinte entrada REG \_ DWORD ao Registro.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

Para que essa entrada entre em vigor, você deve fazer logoff e fazer logoff novamente. Essa configuração faz com que as janelas da área de trabalho e da barra de tarefas sejam criadas em um processo Explorer.exe e todas as outras janelas do Explorer e da pasta sejam abertas em um processo Explorer.exe diferente.

Além de tornar a execução e o teste de suas extensões mais convenientes, essa configuração também torna a área de trabalho mais robusta em relação às extensões do Shell. Muitas dessas extensões (extensões de menu de atalho, por exemplo) serão carregadas no processo de Explorer.exe nondesktop. Se esse processo for encerrado, a área de trabalho e a barra de tarefas não serão afetadas e a próxima janela do Explorer ou da pasta criará o processo encerrado.

## <a name="unloading-the-dll"></a>Descarregando a DLL

O Shell descarrega automaticamente qualquer DLL quando sua contagem de uso é zero, mas somente depois que a DLL não é usada por um período de tempo. Esse período inativo pode ser inaceitável às vezes, especialmente quando uma DLL de extensão do Shell está sendo depurada. Você pode reduzir o período inativo adicionando as informações a seguir ao Registro.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



