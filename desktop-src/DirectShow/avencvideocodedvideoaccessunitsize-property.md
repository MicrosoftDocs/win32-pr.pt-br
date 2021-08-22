---
description: Especifica o tamanho das unidades de acesso ao vídeo, em bytes. Essa propriedade só se aplica a modos de controle de taxa de bits variável (VBR).
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: Propriedade AVEncVideoCodedVideoAccessUnitSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce45dbd232226aa5e0013cbead8e4ff2d8d82b5362d1d6a43cf45c2d030407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663160"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a>Propriedade AVEncVideoCodedVideoAccessUnitSize

Especifica o tamanho das unidades de acesso ao vídeo, em bytes. Essa propriedade só se aplica a modos de controle de taxa de bits variável (VBR).

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoCodedVideoAccessUnitSize**

## <a name="property-value"></a>Valor da propriedade

Essa propriedade é retornada como um intervalo de valores. Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

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

 

 




