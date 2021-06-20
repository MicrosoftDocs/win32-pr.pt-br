---
description: As instâncias de ScoredProperty também podem ser aninhadas em outras instâncias de ScoredProperty ou como elementos filho de uma instância de opção.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Instâncias ScoredProperty aninhadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a80d291fa59b2f36191f42b2f99ea9d22789a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408599"
---
# <a name="nested-scoredproperty-instances"></a><span data-ttu-id="37cc9-103">Instâncias ScoredProperty aninhadas</span><span class="sxs-lookup"><span data-stu-id="37cc9-103">Nested ScoredProperty Instances</span></span>

<span data-ttu-id="37cc9-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="37cc9-104">This topic is not current.</span></span> <span data-ttu-id="37cc9-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="37cc9-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="37cc9-106">Observe que você não está restrito a adicionar instâncias ScoredProperty como elementos filho de uma instância de opção.</span><span class="sxs-lookup"><span data-stu-id="37cc9-106">Notice that you are not restricted to adding ScoredProperty instances as child elements of an Option instance.</span></span> <span data-ttu-id="37cc9-107">As instâncias de ScoredProperty também podem ser aninhadas em outras instâncias de ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="37cc9-107">ScoredProperty instances may also be nested within other ScoredProperty instances.</span></span> <span data-ttu-id="37cc9-108">Isso é útil quando uma propriedade de dispositivo é complexa e é melhor representada por várias subpropriedades.</span><span class="sxs-lookup"><span data-stu-id="37cc9-108">This is useful when a device property is complex and is best represented by multiple subproperties.</span></span> <span data-ttu-id="37cc9-109">Adicionar subpropriedades a uma propriedade existente (ou pública) ou ScoredProperty é uma boa maneira de aprimorar uma opção, enquanto mantém a portabilidade com as instâncias de opção existentes.</span><span class="sxs-lookup"><span data-stu-id="37cc9-109">Adding subproperties to an existing (or public) Property or ScoredProperty is a good way to enhance an Option, while retaining portability with existing Option instances.</span></span> <span data-ttu-id="37cc9-110">Por exemplo, as instâncias de opção padrão para o recurso MediaType contêm um ScoredProperty que descreve o peso da mídia como Light, Medium, Heavy ou ExtraHeavy.</span><span class="sxs-lookup"><span data-stu-id="37cc9-110">For example, the standard Option instances for the MediaType Feature contain a ScoredProperty describing the weight of the media as Light, Medium, Heavy, or ExtraHeavy.</span></span> <span data-ttu-id="37cc9-111">Se você quiser descrições mais precisas do peso, poderá adicionar um subpropriedade (GramsPer100Sheets no exemplo a seguir) que contém o peso real (em gramas) de 100 folhas de mídia.</span><span class="sxs-lookup"><span data-stu-id="37cc9-111">If you want more precise descriptions of the weight, you can add a subproperty (GramsPer100Sheets in the following example) that contains the actual weight (in grams) of 100 sheets of media.</span></span> <span data-ttu-id="37cc9-112">A opção avançado pode ser semelhante ao exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="37cc9-112">The enhanced Option might look like the following example.</span></span>

``` syntax
<!-- Note: The following ScoredProperty is not a Public Print Schema ScoredProperty -->
<!-- This example shows a nested ScoredProperty defined by a Private namespace-->
<!-- It is included for illustration purposes. -->

<psf:ScoredProperty name="FabrikamES500:PaperWeight">
  <psf:Value xsi:type="xs:string">Medium</psf:Value>
  <psf:ScoredProperty name="FabrikamES500:GramsPerSheet">
    <Value xsi:type="decimal">109.5</Value>
  </psf:ScoredProperty>
</psf:ScoredProperty>
```

<span data-ttu-id="37cc9-113">Uma comparação das instâncias de opção original e avançada produz uma correspondência quase perfeita, pois a opção avançada é um superconjunto do original, e os locais e valores de cada uma das instâncias ScoredProperty originais são preservados.</span><span class="sxs-lookup"><span data-stu-id="37cc9-113">A comparison of the original and enhanced Option instances produces a near-perfect match, because the enhanced Option is a superset of the original, and the locations and values of each of the original ScoredProperty instances is preserved.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37cc9-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="37cc9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37cc9-115">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="37cc9-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



