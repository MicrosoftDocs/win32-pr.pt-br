---
description: Especifica o nível de qualidade da VBR do tipo de saída enumerado mais recentemente.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68e609f8dc7b95eb9cfd4bf537af47d1a11cb4ba625f0bbc65897b008ff03a31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689790"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a>Propriedade \_ \_ \_ VBRQUALITY ENUMERADA MAIS RECENTE \_ MFPKEY

Especifica o nível de qualidade da VBR do tipo de saída enumerado mais recentemente. Somente leitura.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

**VT \_ UI4**

## <a name="remarks"></a>Comentários

Quando o codificador está atuando como uma transformação Media Foundation (MFT) e enumera um tipo de saída em uma chamada para [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), você pode consultar o MFT para a propriedade **\_ \_ \_ \_ VBRQUALITY ENUMERADA** MAIS RECENTEMENTE. O valor retornado indica a qualidade da VBR do tipo de mídia de saída retornado mais recentemente. Em seguida, você pode usar esse valor para definir a [**propriedade MFPKEY \_ DESIRED \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) do codificador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista ou Windows 7<br/>                                                   |
| Cabeçalho<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[**MFPKEY \_ RESTRINGIR A \_ \_ VBRQUALITY ENUMERADA**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
