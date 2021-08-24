---
description: Especifica o número de campos a ignorar durante a codificação.
ms.assetid: 82f2a2c1-52ff-410d-b5da-b2419c0adfe3
title: Propriedade AVEncVideoNoOfFieldsToSkip (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 908a169b6f8ea868f7959afbd8fc90afa0b7a129b90674791990a156e67af948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342126"
---
# <a name="avencvideonooffieldstoskip-property"></a>Propriedade AVEncVideoNoOfFieldsToSkip

Especifica o número de campos a ignorar durante a codificação.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoNoOfFieldsToSkip**

## <a name="remarks"></a>Comentários

Para vídeo progressivo, de definido essa propriedade como duas vezes o número de quadros a ignorar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional aplicativos \[ UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




