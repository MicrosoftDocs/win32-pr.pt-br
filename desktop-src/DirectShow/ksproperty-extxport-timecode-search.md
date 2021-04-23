---
description: Essa propriedade envia um comando para o dispositivo para procurar um código de tempo especificado. O driver de dispositivo UVC dá suporte a essa propriedade.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6852dc44e6ef10eebb59721f16a276ac5d4306a3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909434"
---
# <a name="ksproperty_extxport_timecode_search"></a>pesquisa de código de KSPROPERTY \_ EXTXPORT \_ \_

Essa propriedade envia um comando para o dispositivo para procurar um código de tempo especificado. O driver de dispositivo UVC dá suporte a essa propriedade.



| Label | Valor |
|-------------------|----------------------------------------|
| GUID do Conjunto de Propriedades | transporte de extensão propsetid \_ \_              |
| ID da propriedade       | pesquisa de código de KSPROPERTY \_ EXTXPORT \_ \_ |
| Tipo de Dados         | **KSPROPERTY \_ Estrutura EXTXPORT \_ S**  |



 

## <a name="remarks"></a>Comentários

Preencha o membro de **código** de tempo da estrutura **KSPROPERTY \_ EXTXPORT \_ S** com o quadro desejado, segundo, minuto e hora. A estrutura **KSPROPERTY \_ EXTXPORT \_ S** é descrita no Windows DDK.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Conjunto de propriedades de transporte de dispositivo externo](external-device-transport-property-set.md)
</dt> </dl>

 

 



