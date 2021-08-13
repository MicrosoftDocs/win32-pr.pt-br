---
description: Essa propriedade consulta o decodificador para a taxa máxima de quadros completos compatível com o decodificador. O tipo de dados para essa propriedade é uma estrutura \_ DE Taxa de Consulta AM.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: AM_RATE_QueryFullFrameRate propriedade (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ceb938ac3fd0ea5f7f58b340f4b57fd6a722650cd3225702cbb74b1644045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664100"
---
# <a name="am_rate_queryfullframerate-property"></a>Propriedade AM \_ RATE \_ QueryFullFrameRate

Essa propriedade consulta o decodificador para a taxa máxima de quadros completos compatível com o decodificador. O tipo de dados para essa propriedade é uma **estrutura DE Taxa de \_ Consulta** AM.

Essa propriedade é definida para a versão 1.1 deste conjunto de propriedades; consulte [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).



| Rótulo | Valor |
|-------------------|---------------------------------------|
| GUID do Conjunto de Propriedades | AM \_ KSPROPSETID \_ TSRateChange         |
| ID da propriedade       | Propriedade AM \_ RATE \_ QueryFullFrameRate |
| Tipo de Dados         | [**Taxa \_ de Consulta AM**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a>Comentários

Se a taxa de reprodução exceder a taxa máxima do decodificador, o filtro de origem enviará grupos de exemplos contínuos separados por descontinuidades. Os carimbos de data/hora atravessam as descontinuidades. O filtro de origem pode fazer isso mesmo se a taxa de reprodução estiver dentro da taxa máxima do decodificador, pois pode haver outros fatores, como E/S de disco, que limitam a taxa de reprodução completa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Conjunto de propriedades de alteração de taxa**](rate-change-property-set.md)
</dt> </dl>

 

 




