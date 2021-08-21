---
description: Essa propriedade envia um comando para o dispositivo para pesquisar um código de hora especificado. O driver de dispositivo UVC dá suporte a essa propriedade.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f49b8e71d664cf266428d33c99b87859765623ca8205843bbfee108da5f7d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153184"
---
# <a name="ksproperty_extxport_timecode_search"></a>KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH

Essa propriedade envia um comando para o dispositivo para pesquisar um código de hora especificado. O driver de dispositivo UVC dá suporte a essa propriedade.



| Rótulo | Valor |
|-------------------|----------------------------------------|
| GUID do Conjunto de Propriedades | PROPSETID \_ EXT \_ TRANSPORT              |
| ID da propriedade       | KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH |
| Tipo de Dados         | **KSPROPERTY \_ Estrutura EXTXPORT \_ S**  |



 

## <a name="remarks"></a>Comentários

Preencha o **membro timecode** da estrutura **\_ EXTXPORT \_ S da KSPROPERTY** com o quadro desejado, o segundo, o minuto e a hora desejados. A **estrutura \_ EXTXPORT \_ S da KSPROPERTY** é descrita no DDK Windows.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Conjunto de propriedades de transporte de dispositivo externo](external-device-transport-property-set.md)
</dt> </dl>

 

 



