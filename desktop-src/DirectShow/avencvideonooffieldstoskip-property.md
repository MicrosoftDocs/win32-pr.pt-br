---
description: Especifica o número de campos a serem ignorados durante a codificação.
ms.assetid: 82f2a2c1-52ff-410d-b5da-b2419c0adfe3
title: Propriedade AVEncVideoNoOfFieldsToSkip (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708ef409fb907520d6a582599da2050a1353636c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825687"
---
# <a name="avencvideonooffieldstoskip-property"></a>Propriedade AVEncVideoNoOfFieldsToSkip

Especifica o número de campos a serem ignorados durante a codificação.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoNoOfFieldsToSkip**

## <a name="remarks"></a>Comentários

Para vídeo progressivo, defina essa propriedade como duas vezes o número de quadros a serem ignorados.

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

 

 




