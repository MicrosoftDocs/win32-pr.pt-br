---
description: Especifica a ID do fornecedor para um Microsoft Media Foundation.
ms.assetid: AA31639F-EF70-4454-AC61-60755CAA684A
title: MFT_ENUM_HARDWARE_VENDOR_ID_Attribute atributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff3a93abed968a26f8eead5be6a7d1872b9d4556b0d163632992cbcc21b1acd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973095"
---
# <a name="mft_enum_hardware_vendor_id_attribute-attribute"></a>Atributo MFT \_ ENUM \_ HARDWARE VENDOR \_ \_ ID \_ Attribute

Especifica a ID do fornecedor para uma transformação de Microsoft Media Foundation (MFT) baseada em hardware.

## <a name="data-type"></a>Tipo de dados

**Wchar\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentários

Esse atributo é informacional e opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Hardware MFTs](hardware-mfts.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




