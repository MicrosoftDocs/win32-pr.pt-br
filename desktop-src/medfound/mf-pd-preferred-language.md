---
description: Contém o idioma preferencial RFC 1766 da fonte de mídia.
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: Atributo MF_PD_PREFERRED_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cd01a47002bf3cd9419579786ff37df1fc03af940f54b2d2a2bb859d5b97007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740707"
---
# <a name="mf_pd_preferred_language-attribute"></a>\_Atributo de \_ \_ idioma preferencial do MF PD

Contém o idioma preferencial RFC 1766 da fonte de mídia.

## <a name="data-type"></a>Tipo de dados

**WCHAR**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes:: setastring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Aplica-se a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Comentários

O \_ atributo de linguagem MF PD \_ preferencial \_ é opcional. Um aplicativo pode definir esse atributo em uma fonte de mídia (como uma fonte de rede) para especificar seu idioma preferencial.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Aplicativos de aplicativos de área de trabalho do servidor 2008 R2 \[ \| UWP\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




