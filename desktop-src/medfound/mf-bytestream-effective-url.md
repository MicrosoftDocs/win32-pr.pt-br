---
description: Obtém a URL efetiva de um fluxo de byte.
ms.assetid: 0A83CFC0-7EAA-464B-BA39-50DF220AF683
title: MF_BYTESTREAM_EFFECTIVE_URL atributo (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f26ece6ef4b0c4b25629f6669296cec56e23a4bf28b7e284b343e16c0df512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941076"
---
# <a name="mf_bytestream_effective_url-attribute"></a>Atributo MF \_ BYTESTREAM \_ EFFECTIVE \_ URL

Obtém a URL efetiva de um fluxo de byte.

## <a name="data-type"></a>Tipo de dados

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Aplica-se a

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Comentários

A URL efetiva poderá ser diferente da URL original se a URL original contiver informações adicionais, como cadeias de caracteres de pesquisa ou âncoras, ou se a solicitação tiver sido redirecionada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de fluxo de byte](byte-stream-attributes.md)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




