---
description: Especifica o número de campos a serem codificados.
ms.assetid: 5848493c-1f8e-4fe2-8261-dfdc8f61b265
title: Propriedade AVEncVideoNoOfFieldsToEncode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525deb0bbacf90eaffe2946ab569e419a68774f42390d6d2c85a355f2f390a7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119274976"
---
# <a name="avencvideonooffieldstoencode-property"></a>Propriedade AVEncVideoNoOfFieldsToEncode

Especifica o número de campos a serem codificados.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoNoOfFieldsToEncode**

## <a name="remarks"></a>Comentários

Para vídeo progressivo, defina essa propriedade como duas vezes o número de quadros a serem codificados.

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

 

 




