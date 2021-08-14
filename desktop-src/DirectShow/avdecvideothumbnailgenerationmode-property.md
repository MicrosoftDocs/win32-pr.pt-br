---
description: Habilita ou desabilita o modo de geração de miniaturas em um decodificador de vídeo.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Propriedade AVDecVideoThumbnailGenerationMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb10b4996a88c8d2e62180edcbfaba8f71b6738d7dc7e3019a0b8ee4b44462d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159987"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a>Propriedade AVDecVideoThumbnailGenerationMode

Habilita ou desabilita o modo de geração de miniaturas em um decodificador de vídeo.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecVideoThumbnailGenerationMode**

## <a name="remarks"></a>Comentários

Se o valor for **VARIANT \_ TRUE**, o decodificador usará uma configuração otimizada para gerar imagens em miniatura rapidamente. (Por exemplo, ele pode ignorar quadros B ou P.) Caso contrário, se o valor for **VARIANT \_ FALSE**, o decodificador usará suas configurações normais de decodificação.

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

 

 




