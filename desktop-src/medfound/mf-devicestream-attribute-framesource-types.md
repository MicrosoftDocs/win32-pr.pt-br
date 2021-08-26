---
description: Representa o tipo de origem do quadro.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce2e7f90f4e5f23e99bac8e532455fac1309cc0e20177c5800d85f4580e20a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013186"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a>Atributo \_ \_ \_ FRAMESOURCE TYPES MF DEVICESTREAM \_

Representa o tipo de origem do quadro.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse valor desse atributo deve ser um bitmask de um ou mais valores da [**enumeração MFFrameSourceTypes.**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) Para dar suporte à compatibilidade com backward, quando esse atributo não é definido para um tipo de mídia, supõe-se que tenha o valor **MFFrameSourceTypes::Color**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1607 somente \[ para aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




