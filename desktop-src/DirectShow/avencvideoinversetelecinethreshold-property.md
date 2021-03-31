---
description: Define o limite no qual o codificador considera um campo de vídeo redundante.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Propriedade AVEncVideoInverseTelecineThreshold (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645689"
---
# <a name="avencvideoinversetelecinethreshold-property"></a>Propriedade AVEncVideoInverseTelecineThreshold

Define o limite no qual o codificador considera um campo de vídeo redundante.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoInverseTelecineThreshold**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade tem o seguinte intervalo.



| Valor | Descrição                                                    |
|-------|----------------------------------------------------------------|
| 0     | É menos provável que o codificador considere os campos de vídeo redundantes. |
| 100   | É mais provável que o codificador considere os campos de vídeo redundantes. |



 

## <a name="remarks"></a>Comentários

Defina essa propriedade se o codificador estiver executando um telecineon inverso com uma fonte de vídeo analógica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




