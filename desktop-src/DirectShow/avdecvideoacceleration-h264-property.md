---
description: Habilita ou desabilita a aceleração de hardware para decodificação de vídeo H. 264.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: Propriedade AVDecVideoAcceleration_H264 (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84279c49e65586d07dbf1efa4c372a1b1f8770e19bd00eb827ba44b6ad43bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663960"
---
# <a name="avdecvideoacceleration_h264-property"></a>\_Propriedade AVDecVideoAcceleration H264

Habilita ou desabilita a aceleração de hardware para decodificação de vídeo H. 264.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecVideoAcceleration \_ H264**

## <a name="remarks"></a>Comentários

Se o valor for zero, o decodificador não usará a DXVA (aceleração de vídeo do DirectX) para decodificação de vídeo H. 264. para filtros de DirectShow, defina essa propriedade antes que o pino de saída do decodificador seja conectado.

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

 

 




