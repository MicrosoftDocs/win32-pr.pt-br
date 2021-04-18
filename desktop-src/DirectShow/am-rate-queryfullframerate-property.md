---
description: Essa propriedade consulta o decodificador quanto à taxa máxima de quadro completo que o decodificador dá suporte. O tipo de dados para essa propriedade é uma \_ estrutura am QueryRate.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: Propriedade AM_RATE_QueryFullFrameRate (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2c99564caa09253198b101a3e2467ec88c7e34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785507"
---
# <a name="am_rate_queryfullframerate-property"></a>Propriedade de QueryFullFrameRate da \_ taxa de am \_

Essa propriedade consulta o decodificador quanto à taxa máxima de quadro completo que o decodificador dá suporte. O tipo de dados para essa propriedade é uma estrutura **am \_ QueryRate** .

Esta propriedade é definida para a versão 1,1 deste conjunto de propriedades; consulte [**a \_ taxa de \_ UseRateVersion**](am-rate-userateversion-property.md).



|                   |                                       |
|-------------------|---------------------------------------|
| GUID do Conjunto de Propriedades | \_KSPROPSETID \_ TSRateChange         |
| ID da propriedade       | Propriedade de QueryFullFrameRate da \_ taxa de am \_ |
| Tipo de Dados         | [**AM \_ QueryRate**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a>Comentários

Se a taxa de reprodução exceder a taxa máxima do decodificador, o filtro de origem enviará grupos de amostras contínuas separadas por descontinuidades. Os carimbos de data/hora saltam pelo descontinuidades. O filtro de origem pode fazer isso mesmo se a taxa de reprodução estiver dentro da taxa máxima do decodificador, porque pode haver outros fatores, como e/s de disco, que limitam a taxa de reprodução completa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DVDMedia. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Conjunto de propriedades de alteração de taxa**](rate-change-property-set.md)
</dt> </dl>

 

 




