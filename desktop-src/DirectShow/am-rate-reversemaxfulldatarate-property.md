---
description: Propriedade AM_RATE_ReverseMaxFullDataRate – aplica-se ao Windows Vista e posterior.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: Propriedade AM_RATE_ReverseMaxFullDataRate (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e70a330433c8ea6e8116db944d8fb3d2ffff4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099964"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a>Propriedade de ReverseMaxFullDataRate da \_ taxa de am \_

Aplica-se ao Windows Vista e posterior.

Retorna a taxa máxima de reprodução inversa do decodificador. O valor da propriedade é o valor absoluto da velocidade de inversa máxima x 10000. Por exemplo, se a velocidade inversa máxima for-2,0, o valor dessa propriedade será 20000.

O tipo de dados para essa propriedade **é \_ MaxFullDataRate**, que é um `typedef` para **longo**.

Esta propriedade é somente para leitura.



| Label | Valor |
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Conjunto de propriedades de alteração de taxa**](rate-change-property-set.md)
</dt> </dl>

 

 




