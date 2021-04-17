---
title: Identificadores de propriedade/pares de deslocamento
description: A seguir a contagem do valor do conjunto de propriedades da propriedade é uma matriz de valores de conjunto de propriedades de identificadores de propriedade/pares de deslocamento.
ms.assetid: 341608a1-3ab1-4fa9-ab9a-4124c63c78a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b55ed20aef2c76dc97fcb3f4acfe981b9800308
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754097"
---
# <a name="property-identifiersoffset-pairs"></a><span data-ttu-id="5436b-103">Identificadores de propriedade/pares de deslocamento</span><span class="sxs-lookup"><span data-stu-id="5436b-103">Property Identifiers/Offset Pairs</span></span>

<span data-ttu-id="5436b-104">A seguir a contagem do valor do conjunto de propriedades da propriedade é uma matriz de valores de conjunto de propriedades de identificadores de propriedade/pares de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="5436b-104">Following the Count of Properties property set value is an array of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="5436b-105">Os identificadores de propriedade são valores de 32 bits que identificam exclusivamente uma propriedade dentro de uma seção.</span><span class="sxs-lookup"><span data-stu-id="5436b-105">Property Identifiers are 32-bit values that uniquely identify a property within a section.</span></span> <span data-ttu-id="5436b-106">Os pares de deslocamento indicam a distância desde o início da seção até o início do par de tipo/valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="5436b-106">The Offset Pairs indicate the distance from the start of the section to the start of the property Type/Value Pair.</span></span> <span data-ttu-id="5436b-107">Como os deslocamentos são relativos à seção, as seções podem ser copiadas como uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="5436b-107">Because the offsets are relative to the section, sections can be copied as an array of bytes.</span></span>

<span data-ttu-id="5436b-108">Os identificadores de propriedade não são classificados em nenhuma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="5436b-108">Property identifiers are not sorted in any particular order.</span></span> <span data-ttu-id="5436b-109">As propriedades podem ser omitidas do conjunto de propriedades armazenadas; os leitores não devem confiar em uma ordem específica ou um intervalo de identificadores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5436b-109">Properties can be omitted from the stored property set; readers must not rely on a specific order or range of property identifiers.</span></span>

 

 




