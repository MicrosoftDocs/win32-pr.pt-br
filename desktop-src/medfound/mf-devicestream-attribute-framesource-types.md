---
description: Representa o tipo de origem do quadro.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: Atributo MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8823a828a81290fe3b039c8959d694c62331622f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763280"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a>\_Atributo de \_ \_ tipos de framery de atributo MF DEVICESTREAM \_

Representa o tipo de origem do quadro.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse valor desse atributo deve ser um bitmask de um ou mais valores da enumeração [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) . Para dar suporte à compatibilidade com versões anteriores, quando esse atributo não está definido para um tipo de mídia, supõe-se que o valor é **MFFrameSourceTypes:: Color**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1607\]<br/>                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




