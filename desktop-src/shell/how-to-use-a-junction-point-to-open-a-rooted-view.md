---
description: Você pode usar o registro para especificar que a navegação em um ponto de junção abrirá uma exibição com raiz em vez da exibição padrão do conteúdo da extensão associada.
title: Como abrir uma exibição com raiz de um ponto de junção no registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f575d4265a207e97c20f0c2a42456ddbf55cebbe5a0d42664c1fdfa9f5986d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593156"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a>Como abrir uma exibição com raiz de um ponto de junção no registro

Você pode usar o registro para especificar que a navegação em um ponto de junção abrirá uma exibição com raiz em vez da exibição padrão do conteúdo da extensão associada.

## <a name="instructions"></a>Instruções


Para especificar que a navegação em um ponto de junção deve abrir uma exibição com raiz , adicione o \\ **comando** Open e **Explore** as \\ subchaves de **comando** à subchave **CLSID** da extensão, com seus valores padrão atribuídos às linhas de comando mostradas aqui:

```
HKEY_CLASSES_ROOT
   CLSID
      {Extension CLSID}
         Shell
            Open
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
            Explore
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
```

Depois de adicionar esses valores, uma instância do Explorer.exe é iniciada para exibir o conteúdo da extensão como uma exibição com raiz quando o usuário seleciona o ponto de junção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificando o local de uma extensão de namespace](nse-junction.md)
</dt> <dt>

[Como abrir uma exibição com raiz de um ponto de junção por meio de um arquivo de atalho](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



