---
title: Escolhendo arquivos
description: Escolhendo arquivos
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- Criando capas, escolhendo arquivos
- Capas do Windows Media Player, escolhendo arquivos
- capas, escolhendo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160259"
---
# <a name="choosing-files"></a><span data-ttu-id="92a27-106">Escolhendo arquivos</span><span class="sxs-lookup"><span data-stu-id="92a27-106">Choosing Files</span></span>

<span data-ttu-id="92a27-107">Se você quiser escolher um arquivo, poderá usar um código semelhante ao exemplo de playlist, mas substitua o seguinte pela seção PLAYelement:</span><span class="sxs-lookup"><span data-stu-id="92a27-107">If you want to choose a file, you can use code similar to the Playlist example, but substitute the following for the PLAYELEMENT section:</span></span>


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



<span data-ttu-id="92a27-108">Essa linha usará o método **openDialog** de **Theme** para definir uma **URL** para o Player.</span><span class="sxs-lookup"><span data-stu-id="92a27-108">This line will use the **openDialog** method of **THEME** to define a **URL** for the player.</span></span> <span data-ttu-id="92a27-109">Você pode usar isso para escolher arquivos que não estão em listas de reprodução.</span><span class="sxs-lookup"><span data-stu-id="92a27-109">You can use this to choose files that are not in playlists.</span></span>

<span data-ttu-id="92a27-110">Você pode ver um exemplo de **openDialog** de trabalho semelhante na seção de exemplo do SDK.</span><span class="sxs-lookup"><span data-stu-id="92a27-110">You can see a similar working **openDialog** example in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92a27-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92a27-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92a27-112">**Guia de criação de capa**</span><span class="sxs-lookup"><span data-stu-id="92a27-112">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




