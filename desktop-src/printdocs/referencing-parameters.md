---
description: Saiba mais sobre como referenciar parâmetros e o elemento ParameterDef. Um exemplo de uma Opção que inclui um elemento ParameterRef é a Opção de tamanho de mídia personalizada.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Parâmetros de referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def14223c2d1a4471582e28881a3784eb86239e8daec0e9ec63bff8bc8b7838a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112136"
---
# <a name="referencing-parameters"></a>Parâmetros de referência

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um exemplo concreto de uma Opção que inclui um elemento ParameterRef é a Opção de tamanho de mídia personalizada. Observe que ele faz referência a dois parâmetros: PageMediaSizeMediaSizeWidth e PageMediaSizeMediaSizeHeight. Cada instância ParameterRef refere-se a uma instância ParameterDef definida em outro lugar no documento PrintCapabilities. Para obter informações sobre o elemento ParameterDef, consulte [ParameterDef](parameterdef.md). Para obter informações conceituais sobre como definir parâmetros, consulte [ParameterDef e ParameterInit Elements](parameterdef-and-parameterinit-elements.md).

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

Simplesmente criar uma Opção parametrizada não é suficiente para garantir que a Opção seja tratada e processada corretamente. O provedor e os clientes PrintCapabilities/PrintTicket devem fornecer suporte adicional para implementar corretamente instâncias de Opção parametrizadas. Os comportamentos necessários são descritos nas seções a seguir.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



