---
description: Especifica os tipos de quadro (I, P ou B) aos quais o parâmetro de quantificação (QP) é aplicado.
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: Propriedade CODECAPI_AVEncVideoEncodeFrameTypeQP (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e68e0cb6cbdc076dbf523f3ae9dfd7b5870f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089784"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a>\_Propriedade CODECAPI AVEncVideoEncodeFrameTypeQP

Especifica os tipos de quadro (I, P ou B) aos quais o parâmetro de quantificação (QP) é aplicado.

## <a name="data-type"></a>Tipo de dados

**ULONGULONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoEncodeFrameTypeQP**

## <a name="remarks"></a>Comentários

Para codificadores que dão suporte à definição de um parâmetro de quantificação (QP) para tipos de quadro diferentes (I, P, B), eles devem expor essa API além de [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md). Se um codificador oferecer suporte a apenas uma única QP para todos os tipos de quadro, ele deverá dar suporte apenas a CODECAPI \_ AVEncVideoEncodeQP.

Essa é uma propriedade de codificação dinâmica que significa que um novo valor pode ser definido a qualquer momento durante a sessão de codificação.

**Codificadores H. 264/AVC:**

O codificador deve dar suporte a [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**DefinirValor**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Um conjunto de campos de 4 16 bits é usado para especificar o quadro QPs na codificação de QP fixa. Os campos são:

-   **Bits 0-15:** QP usado para quadros I, intervalo válido \[ 0, 51 \] .
-   **Bits 16-31:** QP usado para quadros P, intervalo válido \[ 0, 51 \] .
-   **Bits 32-47:** QP usado para quadros B, intervalo válido \[ 0, 51\]
-   **Bits 48-63:** reservado

Quando esse CodecAPI tem suporte, os codificadores devem dar suporte à configuração de QP no tipo de quadro de I, P e B.

O valor padrão deve ser 0x0000001a001a001a. QP igual a 26 para I, P e B.

Quando [CODECAPI \_ AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) seleciona uma camada temporal específica, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) of CODECAPI \_ AVEncVideoEncodeFrameTypeQP deve definir QP para os quadros I, P e B nessa camada temporal. Por padrão, ele define QP para quadros I, P e B na camada temporal de camada temporal base 0.

[CODECAPI \_ AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) e [CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md) devem ser usados para definir e limitar o intervalo de QP para qps de todos os tipos de imagem, I, P e B.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

