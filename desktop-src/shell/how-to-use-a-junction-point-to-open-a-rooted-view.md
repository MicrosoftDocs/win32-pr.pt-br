---
description: Você pode usar o registro para especificar que a navegação em um ponto de junção abrirá uma exibição com raiz em vez da exibição padrão do conteúdo da extensão associada.
title: Como abrir uma exibição com raiz de um ponto de junção no registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa51e87ccb541e995300cb010f82c79e33112e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169425"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a><span data-ttu-id="a0a44-103">Como abrir uma exibição com raiz de um ponto de junção no registro</span><span class="sxs-lookup"><span data-stu-id="a0a44-103">How to Open a Rooted View of a Junction Point Through the Registry</span></span>

<span data-ttu-id="a0a44-104">Você pode usar o registro para especificar que a navegação em um ponto de junção abrirá uma exibição com raiz em vez da exibição padrão do conteúdo da extensão associada.</span><span class="sxs-lookup"><span data-stu-id="a0a44-104">You can use the registry to specify that browsing into a junction point will open a rooted view rather than the default view of the contents of the associated extension.</span></span>

## <a name="instructions"></a><span data-ttu-id="a0a44-105">Instruções</span><span class="sxs-lookup"><span data-stu-id="a0a44-105">Instructions</span></span>


<span data-ttu-id="a0a44-106">Para especificar que a navegação em um ponto de junção deve abrir uma exibição com raiz , adicione o \\ **comando** Open e **Explore** as \\ subchaves de **comando** à subchave **CLSID** da extensão, com seus valores padrão atribuídos às linhas de comando mostradas aqui:</span><span class="sxs-lookup"><span data-stu-id="a0a44-106">To specify that browsing into a junction point should open a rooted view, add **Open**\\**Command** and **Explore**\\**Command** subkeys to your extension's **CLSID** subkey, with their default values assigned to the command lines shown here:</span></span>

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

<span data-ttu-id="a0a44-107">Depois de adicionar esses valores, uma instância do Explorer.exe é iniciada para exibir o conteúdo da extensão como uma exibição com raiz quando o usuário seleciona o ponto de junção.</span><span class="sxs-lookup"><span data-stu-id="a0a44-107">Once you've added those values, an instance of Explorer.exe is launched to display the contents of the extension as a rooted view when the user selects the junction point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0a44-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0a44-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0a44-109">Especificando o local de uma extensão de namespace</span><span class="sxs-lookup"><span data-stu-id="a0a44-109">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="a0a44-110">Como abrir uma exibição com raiz de um ponto de junção por meio de um arquivo de atalho</span><span class="sxs-lookup"><span data-stu-id="a0a44-110">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



