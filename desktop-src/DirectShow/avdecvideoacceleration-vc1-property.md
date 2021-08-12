---
description: Habilita ou desabilita a aceleração de hardware para decodificação de vídeo VC-1.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: Propriedade AVDecVideoAcceleration_VC1 (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1767206fab479dbcae1dec5e768b21d768440a66776b1f41610b75be4190d6c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663835"
---
# <a name="avdecvideoacceleration_vc1-property"></a>\_Propriedade AVDecVideoAcceleration VC1

Habilita ou desabilita a aceleração de hardware para decodificação de vídeo VC-1.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecVideoAcceleration \_ VC1**

## <a name="remarks"></a>Comentários

Se o valor for zero, o decodificador não usará a DXVA (aceleração de vídeo do DirectX) para decodificação de vídeo VC-1. para filtros de DirectShow, defina essa propriedade antes que o pino de saída do decodificador seja conectado.

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

 

 




