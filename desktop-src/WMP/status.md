---
title: Status (SDK do Windows Media Player)
description: Status
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Aparências móveis do Windows Media Player, exibição de status
- aparências, exibição de status
- referência para capas, exibição de status
- exibição de status em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008689"
---
# <a name="status-windows-media-player-sdk"></a><span data-ttu-id="e2a32-107">Status (SDK do Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="e2a32-107">Status (Windows Media Player SDK)</span></span>

<span data-ttu-id="e2a32-108">Talvez você queira usar uma exibição de status em sua capa.</span><span class="sxs-lookup"><span data-stu-id="e2a32-108">You may want to use a status display in your skin.</span></span> <span data-ttu-id="e2a32-109">Nesse caso, o elemento status deve ser definido no arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="e2a32-109">If so, the status element must be defined in the skin definition file.</span></span> <span data-ttu-id="e2a32-110">Como alternativa, você também pode exibir essas informações usando o atributo status no elemento Text.</span><span class="sxs-lookup"><span data-stu-id="e2a32-110">As an alternative, you may also display this information by using the Status attribute in the Text element.</span></span>

<span data-ttu-id="e2a32-111">A seção de status do arquivo de definição de capa começa com esta linha:</span><span class="sxs-lookup"><span data-stu-id="e2a32-111">The Status section of the skin definition file begins with this line:</span></span>


```C++
[ Status ]

```



<span data-ttu-id="e2a32-112">Em seguida, você deve adicionar uma ou mais linhas que contêm informações sobre a exibição de status em sua capa.</span><span class="sxs-lookup"><span data-stu-id="e2a32-112">You then must add one or more lines that contain information about the status display in your skin.</span></span>


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



<span data-ttu-id="e2a32-113">Você pode usar o modelo a seguir para a seção de status do arquivo de definição de capa:</span><span class="sxs-lookup"><span data-stu-id="e2a32-113">You can use the following template for the Status section of your skin definition file:</span></span>


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



<span data-ttu-id="e2a32-114">Você deve usar a ordem mostrada no modelo anterior para informações de exibição de status para cada linha na seção de status.</span><span class="sxs-lookup"><span data-stu-id="e2a32-114">You must use the order shown in the preceding template for status display information for each line in the Status section.</span></span> <span data-ttu-id="e2a32-115">Cada parte da linha é necessária.</span><span class="sxs-lookup"><span data-stu-id="e2a32-115">Each part of the line is required.</span></span> <span data-ttu-id="e2a32-116">As seções a seguir descrevem cada item:</span><span class="sxs-lookup"><span data-stu-id="e2a32-116">The following sections describe each item:</span></span>

-   [<span data-ttu-id="e2a32-117">Item de status</span><span class="sxs-lookup"><span data-stu-id="e2a32-117">Status Item</span></span>](status-item.md)
-   [<span data-ttu-id="e2a32-118">Local do status</span><span class="sxs-lookup"><span data-stu-id="e2a32-118">Status Location</span></span>](status-location.md)
-   [<span data-ttu-id="e2a32-119">Alinhamento de status</span><span class="sxs-lookup"><span data-stu-id="e2a32-119">Status Alignment</span></span>](status-alignment.md)
-   [<span data-ttu-id="e2a32-120">Fonte de status</span><span class="sxs-lookup"><span data-stu-id="e2a32-120">Status Font</span></span>](status-font.md)
-   [<span data-ttu-id="e2a32-121">Cor do status</span><span class="sxs-lookup"><span data-stu-id="e2a32-121">Status Color</span></span>](status-color.md)

<span data-ttu-id="e2a32-122">Para obter um exemplo de código de status, consulte a [seção status de exemplo](sample-status-section.md).</span><span class="sxs-lookup"><span data-stu-id="e2a32-122">For an example of Status code, see [Sample Status Section](sample-status-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2a32-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2a32-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2a32-124">**Referência de capa**</span><span class="sxs-lookup"><span data-stu-id="e2a32-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




