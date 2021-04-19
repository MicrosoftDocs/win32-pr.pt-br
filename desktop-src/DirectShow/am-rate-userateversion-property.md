---
description: Essa propriedade é usada para sinalizar qual versão do conjunto de propriedades de alteração de taxa deve ser usada pelo decodificador.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: Propriedade AM_RATE_UseRateVersion (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab609d2d38dc28257d13994e6cd464094b714be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771677"
---
# <a name="am_rate_userateversion-property"></a>Propriedade de UseRateVersion da \_ taxa de am \_

Essa propriedade é usada para sinalizar qual versão do conjunto de propriedades de alteração de taxa deve ser usada pelo decodificador. O valor é um tipo de **palavra** . O byte de ordem superior contém o número de versão secundária e o byte de ordem inferior contém o byte de ordem inferior. Assim, a versão 1,1 é sinalizada com o valor 0x0101.

Se o decodificador não oferecer suporte à versão especificada, ele deverá falhar na chamada para [**IKsPropertySet:: Set**](ikspropertyset-set.md) e retornar e \_ nointerface. Se o filtro de origem não definir a versão, o decodificador deverá ser padronizado para a versão 1,0.



|                   |                               |
|-------------------|-------------------------------|
| GUID do Conjunto de Propriedades | \_KSPROPSETID \_ TSRateChange |
| ID da propriedade       | \_UseRateVersion de taxa de am \_      |
| Tipo de Dados         | **WORD**                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DVDMedia. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Conjunto de propriedades de alteração de taxa**](rate-change-property-set.md)
</dt> </dl>

 

 




