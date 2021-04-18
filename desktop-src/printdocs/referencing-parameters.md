---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Referenciando parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815ec7cd412e158a73e2b760f9f6080d7b0326a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105796154"
---
# <a name="referencing-parameters"></a>Referenciando parâmetros

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um exemplo concreto de uma opção que inclui um elemento ParameterRef é a opção de tamanho de mídia personalizada. Observe que ele faz referência a dois parâmetros: PageMediaSizeMediaSizeWidth e PageMediaSizeMediaSizeHeight. Cada instância de ParameterRef refere-se a uma instância ParameterDef que é definida em outro lugar no documento PrintCapabilities. Para obter informações sobre o elemento ParameterDef, consulte [ParameterDef](parameterdef.md). Para obter informações conceituais sobre como definir parâmetros, consulte [ParameterDef e ParameterInit Elements](parameterdef-and-parameterinit-elements.md).

``` syntax
<!--Example of ParamterRef usage within a Feature-->
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
</psf:Option>
```

Simplesmente criar uma opção parametrizada não é suficiente para garantir que a opção seja manipulada e processada corretamente. O provedor de PrintCapabilities/PrintTicket e os clientes devem fornecer suporte adicional para implementar adequadamente instâncias de opção parametrizadas. Os comportamentos necessários são descritos nas seções a seguir.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



