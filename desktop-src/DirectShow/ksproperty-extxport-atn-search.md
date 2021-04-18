---
description: Essa propriedade envia um comando para o dispositivo para pesquisar um número de faixa absoluto (ATN). O driver de dispositivo UVC dá suporte a essa propriedade.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc8ff454386c444ed6b55bfbeede60196a75127c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105767673"
---
# <a name="ksproperty_extxport_atn_search"></a>KSPROPERTY \_ EXTXPORT \_ ATN \_ Search

Essa propriedade envia um comando para o dispositivo para pesquisar um número de faixa absoluto (ATN). O driver de dispositivo UVC dá suporte a essa propriedade.



|                   |                                       |
|-------------------|---------------------------------------|
| GUID do Conjunto de Propriedades | transporte de extensão propsetid \_ \_             |
| ID da propriedade       | KSPROPERTY \_ EXTXPORT \_ ATN \_ Search     |
| Tipo de Dados         | **KSPROPERTY \_ Estrutura EXTXPORT \_ S** |



 

## <a name="remarks"></a>Comentários

Defina o membro **dwAbsTrackNumber** da estrutura **KSPROPERTY \_ EXTXPORT \_** como o seguinte valor:


```
(absolute track number << 1) + continuity bit
```



A especificação UVC não define como o dispositivo usa o bit de continuidade. A estrutura **KSPROPERTY \_ EXTXPORT \_ S** é descrita no Windows DDK.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Conjunto de propriedades de transporte de dispositivo externo](external-device-transport-property-set.md)
</dt> </dl>

 

 



