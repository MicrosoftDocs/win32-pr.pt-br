---
description: Você pode usar uma extensão de namespace para permitir que os usuários procurem o conteúdo de um arquivo em vez de serem apresentados como uma pasta. As extensões dessa classificação normalmente são usadas para exibir o conteúdo dos membros de um tipo de arquivo.
title: Como exibir uma exibição com raiz de um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ee16f3ce50cd79800dd98aa53256591d1f79d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828294"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a>Como exibir uma exibição com raiz de um arquivo

Você pode usar uma extensão de namespace para permitir que os usuários procurem o conteúdo de um arquivo em vez de serem apresentados como uma pasta. As extensões dessa classificação normalmente são usadas para exibir o conteúdo dos membros de um [tipo de arquivo](fa-file-types.md). Por exemplo, os membros de um tipo de arquivo podem conter vários arquivos compactados ou imagens, organizados em uma hierarquia. Em vez de escrever um aplicativo para permitir que o usuário exiba o conteúdo desse arquivo, você pode escrever uma extensão de namespace e deixar que o Windows Explorer manipule a exibição.

Você deve usar uma exibição com raiz para que uma extensão exiba o conteúdo de um arquivo. A maneira mais comum de fornecer uma exibição com raiz dos membros de um tipo de arquivo é definir um [verbo de menu de atalho](context.md) que inicia uma instância do Explorer.exe. Ao tornar esse verbo o verbo padrão, um clique duplo também abrirá uma exibição com raiz do arquivo. Você pode definir um verbo para todos os membros do tipo de arquivo [modificando o registro](context.md)ou definindo os verbos de forma dinâmica em uma base arquivo por arquivo implementando um [manipulador de menu de atalho](context-menu-handlers.md).

## <a name="instructions"></a>Instruções


O exemplo a seguir ilustra como usar o registro para fornecer uma exibição com raiz dos membros de um tipo de arquivo, modificando o registro. A entrada do registro de exemplo é uma modificação de um dos exemplos na [extensão de menus de atalho](context.md). As entradas do registro definem arquivos com uma extensão de nome de arquivo. MYP como um tipo de arquivo e usam o verbo **procurar** para iniciar uma exibição com raiz dos membros desse tipo.

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

Você pode usar o mesmo verbo para iniciar programaticamente uma exibição com raiz de um membro do tipo de arquivo chamando a função [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificando o local de uma extensão de namespace](nse-junction.md)
</dt> <dt>

[Como abrir uma exibição com raiz de um ponto de junção no registro](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[Como abrir uma exibição com raiz de um ponto de junção por meio de um arquivo de atalho](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



