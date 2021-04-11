---
description: Especifica se o fluxo de saída deve ser estruturado para que o fluxo codificado tenha uma latência de decodificação baixa.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Propriedade AVEncCommonLowLatency (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163864"
---
# <a name="avenccommonlowlatency-property"></a>Propriedade AVEncCommonLowLatency

Especifica se o fluxo de saída deve ser estruturado para que o fluxo codificado tenha uma latência de decodificação baixa.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonLowLatency**

## <a name="remarks"></a>Comentários

A decodificação da latência é definida como a quantidade de dados que o decodificador deve armazenar em buffer. Por exemplo, definir essa propriedade como **Variant \_ true** em um codificador de vídeo MPEG limita os tipos de estruturas GOP que o codificador pode usar.

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

 

 




