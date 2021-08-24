---
description: Contém o link simbólico para uma transformação de Media Foundation baseada em hardware (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: Atributo MFT_ENUM_HARDWARE_URL_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7119ea4bde7900087f706cb6fbc77c845721debab54dfa05b48f5c0094b1e29e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722575"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a>\_Atributo de \_ atributo de URL de hardware de enumeração de \_ MFT \_

Contém o link simbólico para uma transformação de Media Foundation baseada em hardware (MFT).

## <a name="data-type"></a>Tipo de dados

**WCHAR\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentários

Esse atributo tem suporte de MFTs baseadas em hardware. O valor do atributo é o link simbólico para o driver de dispositivo. Esse atributo também é definido nos ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) alocados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , quando esses ponteiros representam MFTs baseadas em hardware.

O link simbólico deve ser considerado uma cadeia de caracteres opaca. Para obter o nome de exibição de um dispositivo, consulte o atributo [ \_ \_ nome amigável de MFT](mft-friendly-name-attribute.md) .

O MFTs de software não deve ter esse atributo definido.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Aplicativos de aplicativos de área de trabalho do servidor 2008 R2 \[ \| UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs de hardware](hardware-mfts.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




