---
description: Especifica se o fluxo de saída deve ser estruturado para que o fluxo codificado tenha uma baixa latência de decodificação.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Propriedade AVEncCommonLowLatency (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b53c4b0122e595c930828f400600fc22b5a03977a781adab0e3a2f42b1048ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690226"
---
# <a name="avenccommonlowlatency-property"></a>Propriedade AVEncCommonLowLatency

Especifica se o fluxo de saída deve ser estruturado para que o fluxo codificado tenha uma baixa latência de decodificação.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonLowLatency**

## <a name="remarks"></a>Comentários

A latência de decodificação é definida como a quantidade de dados que o decodificador deve ter em buffer. Por exemplo, definir essa propriedade como **VARIANT \_ TRUE** em um codificador de vídeo MPEG limita os tipos de estruturas GOP que o codificador pode usar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[ aplicativos UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




