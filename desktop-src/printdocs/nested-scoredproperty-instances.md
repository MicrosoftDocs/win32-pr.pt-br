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
# <a name="nested-scoredproperty-instances"></a>Instâncias ScoredProperty aninhadas

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Observe que você não está restrito a adicionar instâncias ScoredProperty como elementos filho de uma instância de opção. As instâncias de ScoredProperty também podem ser aninhadas em outras instâncias de ScoredProperty. Isso é útil quando uma propriedade de dispositivo é complexa e é melhor representada por várias subpropriedades. Adicionar subpropriedades a uma propriedade existente (ou pública) ou ScoredProperty é uma boa maneira de aprimorar uma opção, enquanto mantém a portabilidade com as instâncias de opção existentes. Por exemplo, as instâncias de opção padrão para o recurso MediaType contêm um ScoredProperty que descreve o peso da mídia como Light, Medium, Heavy ou ExtraHeavy. Se você quiser descrições mais precisas do peso, poderá adicionar um subpropriedade (GramsPer100Sheets no exemplo a seguir) que contém o peso real (em gramas) de 100 folhas de mídia. A opção avançado pode ser semelhante ao exemplo a seguir.

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

Uma comparação das instâncias de opção original e avançada produz uma correspondência quase perfeita, pois a opção avançada é um superconjunto do original, e os locais e valores de cada uma das instâncias ScoredProperty originais são preservados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



