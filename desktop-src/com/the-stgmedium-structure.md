---
title: A estrutura STGMEDIUM
description: A estrutura STGMEDIUM
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86faf52ab93bab39b8413ea2eb6381da24b643b5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104008582"
---
# <a name="the-stgmedium-structure"></a><span data-ttu-id="bc26e-103">A estrutura STGMEDIUM</span><span class="sxs-lookup"><span data-stu-id="bc26e-103">The STGMEDIUM Structure</span></span>

<span data-ttu-id="bc26e-104">Assim como a estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) é um aprimoramento do identificador de formato da área de transferência do Windows, a estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) é uma melhoria do identificador de memória global usado para transferir os dados.</span><span class="sxs-lookup"><span data-stu-id="bc26e-104">Just as the [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) structure is an enhancement of the Windows clipboard format identifier, so the [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure is an improvement of the global memory handle used to transfer the data.</span></span> <span data-ttu-id="bc26e-105">A estrutura **STGMEDIUM** inclui um membro, **TYMED**, que indica o meio a ser usado, e uma União que compreende ponteiros e um identificador para obter qualquer meio especificado em **TYMED**.</span><span class="sxs-lookup"><span data-stu-id="bc26e-105">The **STGMEDIUM** structure includes a member, **tymed**, which indicates the medium to be used, and a union comprising pointers and a handle for getting whichever medium is specified in **tymed**.</span></span>

<span data-ttu-id="bc26e-106">A estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) permite que as fontes de dados e os consumidores escolham o meio de troca mais eficiente em uma base por renderização.</span><span class="sxs-lookup"><span data-stu-id="bc26e-106">The [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure enables both data sources and consumers to choose the most efficient exchange medium on a per-rendering basis.</span></span> <span data-ttu-id="bc26e-107">Se os dados forem tão grandes que devem ser mantidos no disco, a fonte de dados poderá indicar uma mídia baseada em disco em seu formato preferencial, usando apenas a memória global como um backup se essa for a única mídia que o consumidor compreende.</span><span class="sxs-lookup"><span data-stu-id="bc26e-107">If the data is so large that it should be kept on disk, the data source can indicate a disk-based medium in its preferred format, only using global memory as a backup if that's the only medium the consumer understands.</span></span> <span data-ttu-id="bc26e-108">Ser capaz de usar o melhor meio para trocas, pois o padrão melhora o desempenho geral da troca de dados entre aplicativos.</span><span class="sxs-lookup"><span data-stu-id="bc26e-108">Being able to use the best medium for exchanges as the default improves overall performance of data exchange between applications.</span></span> <span data-ttu-id="bc26e-109">Por exemplo, se alguns dos dados a serem transferidos já estiverem no disco, o aplicativo de origem poderá movê-lo ou copiá-lo para um novo destino, no mesmo aplicativo ou em outros, sem precisar primeiro carregar os dados na memória global.</span><span class="sxs-lookup"><span data-stu-id="bc26e-109">For example, if some of the data to be transferred is already on disk, the source application can move or copy it to a new destination, either in the same application or in some other, without having first to load the data into global memory.</span></span> <span data-ttu-id="bc26e-110">Na extremidade de recebimento, o consumidor dos dados não precisa gravá-lo de volta no disco.</span><span class="sxs-lookup"><span data-stu-id="bc26e-110">At the receiving end, the consumer of the data does not have to write it back to disk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc26e-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc26e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc26e-112">Formatos de dados e mídia de transferência</span><span class="sxs-lookup"><span data-stu-id="bc26e-112">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




