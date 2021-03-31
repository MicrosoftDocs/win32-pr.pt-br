---
title: Considerações sobre o conjunto de propriedades
description: É altamente recomendável que os conjuntos de propriedades sejam mantidos pequenos porque o fluxo do conjunto de propriedades é lido na memória antes que uma única propriedade possa ser lida ou gravada.
ms.assetid: 520db05e-81cd-40ef-af89-471d7194c634
keywords:
- Considerações sobre o conjunto de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfd89140092b13d113122ffe1c1a2b576e654c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637255"
---
# <a name="property-set-considerations"></a><span data-ttu-id="c5cd6-104">Considerações sobre o conjunto de propriedades</span><span class="sxs-lookup"><span data-stu-id="c5cd6-104">Property Set Considerations</span></span>

<span data-ttu-id="c5cd6-105">É altamente recomendável que os conjuntos de propriedades sejam mantidos pequenos porque o fluxo do conjunto de propriedades é lido na memória antes que uma única propriedade possa ser lida ou gravada.</span><span class="sxs-lookup"><span data-stu-id="c5cd6-105">It is strongly recommended that property sets be kept small because the property set stream is read into memory before a single property can be read or written.</span></span> <span data-ttu-id="c5cd6-106">"pequeno" significa menos de 32 kilobytes de dados.</span><span class="sxs-lookup"><span data-stu-id="c5cd6-106">"small" means less than 32 kilobytes of data.</span></span> <span data-ttu-id="c5cd6-107">Isso raramente apresenta um problema porque, normalmente, as propriedades "embutidas" serão itens pequenos, como cadeias de caracteres descritivas, palavras-chave, carimbos de data/hora, contagens, nomes de autor, identificadores globais exclusivos (GUIDs), identificadores de classe (CLSIDs) e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c5cd6-107">This rarely presents a problem because typically, "in-line" properties will be small items such as descriptive strings, keywords, time stamps, counts, author names, globally unique identifiers (GUIDs), class identifiers (CLSIDs), and so forth.</span></span>

<span data-ttu-id="c5cd6-108">Para armazenar maiores partes de dados, ou em casos em que o tamanho total de um conjunto de propriedades relacionadas excede a quantidade recomendada, o uso de tipos não simples, como o **\_ armazenamento** VT e o **\_ streaming** do UT, é altamente recomendável.</span><span class="sxs-lookup"><span data-stu-id="c5cd6-108">To store larger chunks of data, or in cases where the total size of a set of related properties far exceeds the recommended amount, the use of nonsimple types such as **VT\_STREAM** and **VT\_STORAGE** are strongly recommended.</span></span> <span data-ttu-id="c5cd6-109">Eles não são armazenados no fluxo do conjunto de propriedades, portanto, eles não afetam significativamente a sobrecarga inicial do primeiro acesso e gravação de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="c5cd6-109">These are not stored within the property set stream, so they do not significantly affect the initial overhead of the first accessing and writing of a property.</span></span> <span data-ttu-id="c5cd6-110">Há uma sobrecarga mínima, pois o fluxo do conjunto de propriedades contém o nome do fluxo irmão ou da propriedade com valor de armazenamento e isso requer um pequeno período de tempo adicional para ser processado.</span><span class="sxs-lookup"><span data-stu-id="c5cd6-110">There is a minimal overhead as the property set stream contains the name of the sibling stream- or storage-valued property and this takes an additional small amount of time to process.</span></span>

<span data-ttu-id="c5cd6-111">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="c5cd6-111">For more information, see:</span></span>

-   [<span data-ttu-id="c5cd6-112">Considerações sobre implementação do IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="c5cd6-112">IPropertySetStorage Implementation Considerations</span></span>](ipropertysetstorage-implementation-considerations.md)
-   [<span data-ttu-id="c5cd6-113">Armazenando conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="c5cd6-113">Storing Property Sets</span></span>](storing-property-sets.md)
-   [<span data-ttu-id="c5cd6-114">Características de desempenho</span><span class="sxs-lookup"><span data-stu-id="c5cd6-114">Performance Characteristics</span></span>](performance-characteristics.md)
-   [<span data-ttu-id="c5cd6-115">Implementando o conjunto de propriedades de informações de resumo</span><span class="sxs-lookup"><span data-stu-id="c5cd6-115">Implementing the Summary Information Property Set</span></span>](implementing-the-summary-information-property-set.md)

 

 




