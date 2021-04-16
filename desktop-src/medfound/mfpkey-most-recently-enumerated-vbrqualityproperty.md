---
description: Especifica o nível de qualidade de VBR do tipo de saída enumerado mais recentemente.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: Propriedade MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd3b5f3aae6dc5347672cf6697c3431163dcbd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750534"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a>\_ \_ \_ Propriedade VBRQUALITY enumerada mais recente do MFPKEY \_

Especifica o nível de qualidade de VBR do tipo de saída enumerado mais recentemente. Somente leitura.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**\_UI4 VT**

## <a name="remarks"></a>Comentários

Quando o codificador está agindo como uma Media Foundation transformação (MFT) e enumera um tipo de saída em uma chamada para [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), você pode consultar o MFT para a **propriedade \_ \_ \_ \_ VBRQUALITY enumerada mais recentemente do MFPKEY** . O valor retornado indica a qualidade de VBR do tipo de mídia de saída retornado mais recentemente. Em seguida, você pode usar esse valor para definir a propriedade [**MFPKEY \_ desejada \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) do codificador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista ou Windows 7<br/>                                                   |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[**MFPKEY \_ restringir \_ VBRQUALITY enumerado \_**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
