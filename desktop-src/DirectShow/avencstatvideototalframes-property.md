---
description: Retorna o número de quadros de vídeo recebidos pelo codificador.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Propriedade AVEncStatVideoTotalFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76adda51e6d16676a2a957fd16a5aac2a15691e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105747623"
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
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




