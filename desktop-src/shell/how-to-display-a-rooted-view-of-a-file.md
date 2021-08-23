---
description: Você pode usar uma extensão de namespace para permitir que os usuários naveguem pelo conteúdo de um arquivo em vez de que ele seja apresentado como uma pasta. Extensões dessa classificação normalmente são usadas para exibir o conteúdo dos membros de um tipo de arquivo.
title: Como exibir uma exibição raiz de um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c91e17ef12393b1a95316c37a18d51876cf988293c330610a3638c7995ab12a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596576"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a>Como exibir uma exibição raiz de um arquivo

Você pode usar uma extensão de namespace para permitir que os usuários naveguem pelo conteúdo de um arquivo em vez de que ele seja apresentado como uma pasta. Extensões dessa classificação normalmente são usadas para exibir o conteúdo dos membros de um [tipo de arquivo](fa-file-types.md). Por exemplo, os membros de um tipo de arquivo podem conter vários arquivos compactados ou imagens, organizados em uma hierarquia. Em vez de escrever um aplicativo para permitir que o usuário veja o conteúdo desse arquivo, você pode escrever uma extensão de namespace e permitir que Windows Explorer manipular a exibição.

Você deve usar uma exibição com raiz para que uma extensão exibir o conteúdo de um arquivo. A maneira mais comum de fornecer uma exibição com raiz dos membros de um tipo de arquivo é definir um verbo de [menu](context.md) de atalho que inicia uma instância do Explorer.exe. Ao tornar esse verbo o verbo padrão, um clique duplo também abrirá uma exibição com raiz do arquivo. Você pode definir um verbo para todos [](context.md)os membros do tipo de arquivo modificando o registro ou definir dinamicamente verbos em uma base arquivo a arquivo implementando um manipulador de [menu](context-menu-handlers.md)de atalho .

## <a name="instructions"></a>Instruções


O exemplo a seguir ilustra como usar o Registro para fornecer uma exibição com raiz dos membros de um tipo de arquivo modificando o Registro. A entrada de registro de exemplo é uma modificação de um dos exemplos em [Estendendo menus de atalho.](context.md) As entradas do Registro definem arquivos com uma extensão de nome  de arquivo .myp como um tipo de arquivo e usam o verbo procurar para iniciar uma exibição com raiz de membros desse tipo.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = browse
         browse
            command
               (Default) = %SYSTEMROOT%\explorer.exe /e,/root,{Extension CLSID}, "%1"
```

Você pode usar o mesmo verbo para iniciar programaticamente uma exibição com raiz de um membro do tipo de arquivo chamando a [**função ShellExecute.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificando o local de uma extensão de namespace](nse-junction.md)
</dt> <dt>

[Como abrir uma exibição raiz de um ponto de junção por meio do Registro](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[Como abrir uma exibição raiz de um ponto de junção por meio de um arquivo de atalho](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



