---
description: Aplica-se ao Windows Vista e posterior.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: Propriedade AM_RATE_ReverseMaxFullDataRate (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679e83038a74e64d7a39e8757a9ffaf61fc88c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749055"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a>Propriedade de ReverseMaxFullDataRate da \_ taxa de am \_

Aplica-se ao Windows Vista e posterior.

Retorna a taxa máxima de reprodução inversa do decodificador. O valor da propriedade é o valor absoluto da velocidade de inversa máxima x 10000. Por exemplo, se a velocidade inversa máxima for-2,0, o valor dessa propriedade será 20000.

O tipo de dados para essa propriedade **é \_ MaxFullDataRate**, que é um `typedef` para **longo**.

Esta propriedade é somente para leitura.



|                   |                                  |
|-------------------|----------------------------------|
| GUID do Conjunto de Propriedades | \_KSPROPSETID \_ TSRateChange    |
| ID da propriedade       | \_ReverseMaxFullDataRate de taxa de am \_ |
| Tipo de Dados         | **AM \_ MaxFullDataRate**          |



 

## <a name="remarks"></a>Comentários

Os decodificadores que dão suporte à reprodução reversa suave devem expor essa propriedade. Para obter mais informações, consulte [aprimoramentos de reprodução de DVD no Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DVDMedia. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Conjunto de propriedades de alteração de taxa**](rate-change-property-set.md)
</dt> </dl>

 

 




