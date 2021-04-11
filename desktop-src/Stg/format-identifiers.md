---
title: Identificadores de formato
description: Os valores do conjunto de propriedades são armazenados em uma seção marcada com um FMTID exclusivo.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Identificadores de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0202cd1287c3b4fef6e9e2b56e272541a03425b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292075"
---
# <a name="format-identifiers"></a><span data-ttu-id="c0641-104">Identificadores de formato</span><span class="sxs-lookup"><span data-stu-id="c0641-104">Format Identifiers</span></span>

<span data-ttu-id="c0641-105">Os valores do conjunto de propriedades são armazenados em uma seção marcada com um FMTID exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c0641-105">Property set values are stored in a section tagged with a unique FMTID.</span></span> <span data-ttu-id="c0641-106">Por exemplo, o FMTID para o conjunto de propriedades de informações de resumo COM é **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.</span><span class="sxs-lookup"><span data-stu-id="c0641-106">For example, the FMTID for the COM Summary Information property set is **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.</span></span>

<span data-ttu-id="c0641-107">Para definir um FMTID para o conjunto de propriedades de informações de resumo, use a macro **definir \_ GUID** em um arquivo de inclusão para o código que manipula o conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c0641-107">To define a FMTID for the Summary Information property set, use the **DEFINE\_GUID** macro in an include file for the code that manipulates the property set.</span></span>


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



<span data-ttu-id="c0641-108">Qualquer código que exija o FMTID para o conjunto de propriedades de informações resumidas pode acessá-lo por meio da variável *\_ SummaryInformation do FMTID* .</span><span class="sxs-lookup"><span data-stu-id="c0641-108">Any code that requires the FMTID for the Summary Information property set, can access it through the *FMTID\_SummaryInformation* variable.</span></span>

<span data-ttu-id="c0641-109">Ao armazenar conjuntos de propriedades em instâncias [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , converta o FMTID em um nome de cadeia de caracteres para o objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c0641-109">When storing property sets in [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instances, convert the FMTID to a string name for the storage object.</span></span>

 

 




