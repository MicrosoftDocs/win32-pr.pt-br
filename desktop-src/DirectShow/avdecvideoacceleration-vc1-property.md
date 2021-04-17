---
description: Habilita ou desabilita a aceleração de hardware para decodificação de vídeo VC-1.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: Propriedade AVDecVideoAcceleration_VC1 (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fcdbe265f5a65212a2846b724f570b024ea0ab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105755400"
---
# <a name="avdecvideoacceleration_vc1-property"></a>\_Propriedade AVDecVideoAcceleration VC1

Habilita ou desabilita a aceleração de hardware para decodificação de vídeo VC-1.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecVideoAcceleration \_ VC1**

## <a name="remarks"></a>Comentários

Se o valor for zero, o decodificador não usará a DXVA (aceleração de vídeo do DirectX) para decodificação de vídeo VC-1. Para filtros do DirectShow, defina essa propriedade antes que o pino de saída do decodificador seja conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




