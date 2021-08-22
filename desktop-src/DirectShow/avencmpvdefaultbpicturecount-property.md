---
description: Especifica o número padrão de quadros B consecutivos entre quadros I e P.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Propriedade AVEncMPVDefaultBPictureCount (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95604d8b3849175e579d276fa006f5a8c4d2833a167228316c4cf830b01618b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276256"
---
# <a name="avencmpvdefaultbpicturecount-property"></a>Propriedade AVEncMPVDefaultBPictureCount

Especifica o número padrão de quadros B consecutivos entre quadros I e P.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncMPVDefaultBPictureCount**

## <a name="property-value"></a>Valor da propriedade

Essa propriedade tem um intervalo linear de valores. Para obter o intervalo com suporte, chame [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Comentários

Antes de Windows 8, essa propriedade se aplica aos codificadores de vídeo MPEG. Começando com Windows 8, essa propriedade é usada por codificadores de vídeo MPEG, WMV e H.264.

Se o codificador dá suporte a essa propriedade, ele pode ser usado para controlar a estrutura gop (grupo de imagens).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[ aplicativos UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




