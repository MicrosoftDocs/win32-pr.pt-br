---
description: Este tópico explica como depurar Shell e DLLs de extensão de namespace.
title: Depuração com o Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ca6e30809565408454976e1b07ff37dcc8f8f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501431"
---
# <a name="debugging-with-the-shell"></a>Depuração com o Shell

Este tópico explica como depurar Shell e DLLs de extensão de namespace.

-   [Executando o Shell em um depurador](#running-the-shell-under-a-debugger)
-   [Executando e testando extensões do Shell](#running-and-testing-shell-extensions)
-   [Descarregando a DLL](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a>Executando o Shell em um depurador

Para depurar sua extensão, você precisa executar o Shell do depurador. Siga estas etapas:

1.  Carregue o projeto da extensão no depurador, mas não o execute.
2.  Desligue o Shell.

    -   Para o Windows Vista e posterior:
        1.  Exibir o menu **Iniciar** .
        2.  Pressione CTRL + SHIFT e clique com o botão direito do mouse no plano de fundo da metade direita do menu **Iniciar** .
        3.  No menu que aparece, escolha **sair do Gerenciador**.
    -   Para o Windows XP:
        1.  No menu **Iniciar** , escolha **desligar**.
        2.  Pressione CTRL + ALT + SHIFT e clique em **não** na caixa de diálogo **desligar o Windows** .

    O Shell agora está desligado, mas todos os outros aplicativos ainda estão em execução, incluindo o depurador.

3.  Defina o depurador para executar a DLL de extensão com Explorer.exe do diretório do **Windows** .
4.  Execute o projeto do depurador. O shell será iniciado como de costume, mas o depurador será anexado ao processo do Shell.

## <a name="running-and-testing-shell-extensions"></a>Executando e testando extensões do Shell

Você pode executar e testar suas extensões em um processo separado do Windows Explorer para evitar parar e reiniciar a área de trabalho e a barra de tarefas. A área de trabalho e a barra de tarefas ainda podem ser usadas enquanto você executa e testa as extensões.

Para habilitar esse recurso, adicione a seguinte \_ entrada reg DWORD ao registro.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

Para que essa entrada tenha efeito, você deve fazer logoff e logon novamente. Essa configuração faz com que as janelas da área de trabalho e da barra de tarefas sejam criadas em um Explorer.exe processo e todas as outras janelas de navegador e de pasta sejam abertas em um processo de Explorer.exe diferente.

Além de tornar a execução e o teste de suas extensões mais convenientes, essa configuração também torna a área de trabalho mais robusta, pois está relacionada às extensões do Shell. Muitas dessas extensões (extensões de menu de atalho, por exemplo) serão carregadas no processo não Explorer.exe da área de trabalho. Se esse processo for encerrado, a área de trabalho e a barra de tarefas não serão afetadas e a próxima janela de navegador ou pasta recriará o processo encerrado.

## <a name="unloading-the-dll"></a>Descarregando a DLL

O Shell descarregará automaticamente qualquer DLL quando sua contagem de uso for zero, mas somente depois que a DLL não tiver sido usada por um período de tempo. Esse período inativo pode ser muito demorado às vezes, especialmente quando um DLL de extensão de Shell está sendo depurado. Você pode encurtar o período inativo adicionando as informações a seguir ao registro.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



