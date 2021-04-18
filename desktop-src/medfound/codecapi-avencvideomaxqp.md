---
description: Especifica o máximo de QP com suporte pelo codificador.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: Propriedade CODECAPI_AVEncVideoMaxQP (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bcf23866da5530d2edc1203be359071e5e33e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763229"
---
# <a name="codecapi_avencvideomaxqp-property"></a>\_Propriedade CODECAPI AVEncVideoMaxQP

Especifica o máximo de QP com suporte pelo codificador.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoMaxQP**

## <a name="remarks"></a>Comentários

**Codificadores H. 264/AVC:**

O codificador deve dar suporte a [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**DefinirValor**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Essa é uma propriedade estática, o que significa que ela só pode ser definida antes do início da sessão de codificação.

O valor padrão deve ser o máximo QP permitido pelo padrão de codificação correspondente. Por exemplo, os codificadores H. 264 devem ter um valor padrão de 51.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md)
</dt> </dl>

 

