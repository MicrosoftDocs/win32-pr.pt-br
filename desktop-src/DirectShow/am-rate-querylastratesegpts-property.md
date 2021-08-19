---
description: Essa propriedade consulta o decodificador para a hora de início da alteração de taxa que foi enfilada mais recentemente, independentemente de sua posição na fila de alteração de taxa.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: AM_RATE_QueryLastRateSegPTS propriedade (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e7b54e618829d9768b4d08a0a76defcf2c91758be6b916b6e570b368191e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824830"
---
# <a name="am_rate_querylastratesegpts-property"></a>Propriedade AM \_ RATE \_ QueryLastRateSegPTS

Essa propriedade consulta o decodificador para a hora de início da alteração de taxa que foi enfilada mais recentemente, independentemente de sua posição na fila de alteração de taxa.

Essa propriedade é definida para a versão 1.1 deste conjunto de propriedades; consulte [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).



| Rótulo | Valor |
|-------------------|-------------------------------|
| GUID do Conjunto de Propriedades | AM \_ KSPROPSETID \_ TSRateChange |
| ID da propriedade       | CONSULTA \_ RATE \_ AMLastRateSegPTS |
| Tipo de Dados         | **TEMPO \_ DE REFERÊNCIA**           |



 

## <a name="remarks"></a>Comentários

O filtro de origem pode usar essa propriedade para sincronizar alterações de taxa em vários fluxos de áudio e vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Conjunto de propriedades de alteração de taxa**](rate-change-property-set.md)
</dt> </dl>

 

 




