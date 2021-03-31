---
title: Tamanho da seção
description: O tipo de dados de tamanho da seção indica o tamanho, em bytes, da seção.
ms.assetid: 6438fbce-42b9-4b16-a6b0-80c80246e546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b19df1c2f9a65f6952855a4ab325565c759af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160382"
---
# <a name="size-of-section"></a><span data-ttu-id="bbedb-103">Tamanho da seção</span><span class="sxs-lookup"><span data-stu-id="bbedb-103">Size of Section</span></span>

<span data-ttu-id="bbedb-104">O tipo de dados de tamanho da seção indica o tamanho, em bytes, da seção.</span><span class="sxs-lookup"><span data-stu-id="bbedb-104">The section size data type indicates the size, in bytes, of the section.</span></span> <span data-ttu-id="bbedb-105">Como o tamanho da seção é dos primeiros 4 bytes, as seções podem ser copiadas como uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="bbedb-105">Because the section size is the first 4 bytes, sections can be copied as an array of bytes.</span></span> <span data-ttu-id="bbedb-106">O tamanho da seção deve ser sempre um múltiplo de quatro.</span><span class="sxs-lookup"><span data-stu-id="bbedb-106">The section size should always be a multiple of four.</span></span>

<span data-ttu-id="bbedb-107">Por exemplo, uma seção vazia, ou seja, uma com zero propriedades, teria uma contagem de bytes de oito (a contagem de bytes **DWORD** e a contagem de propriedades **DWORD** ).</span><span class="sxs-lookup"><span data-stu-id="bbedb-107">For example, an empty section, that is, one with zero properties in it, would have a byte count of eight (the **DWORD** byte count and the **DWORD** count of properties).</span></span> <span data-ttu-id="bbedb-108">A seção em si conterá os 8 bytes: **08 00 00 00 00 00 00 00**.</span><span class="sxs-lookup"><span data-stu-id="bbedb-108">The section itself would contain the 8 bytes: **08 00 00 00 00 00 00 00**.</span></span>

 

 




