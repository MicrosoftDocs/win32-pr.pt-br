---
description: Retorna o número de quadros de vídeo recebidos pelo codificador.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Propriedade AVEncStatVideoTotalFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 461708e9006db183992cf550bf7f98eeaeacbfe16c100675ab4992b54f0768d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663437"
---
# <a name="avencstatvideototalframes-property"></a>Propriedade AVEncStatVideoTotalFrames

Retorna o número de quadros de vídeo recebidos pelo codificador.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncStatVideoTotalFrames**

## <a name="remarks"></a>Comentários

Essa propriedade estará disponível após a conclusão da codificação.

O valor dessa propriedade é o número total de quadros enviados ao codificador, incluindo os quadros que foram descartados. Para obter o número de quadros codificados, leia a propriedade [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | aplicativos Windows 2000 Professional \[ desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows \[ aplicativos da área de trabalho do servidor 2000 \| aplicativo UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




