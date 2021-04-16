---
description: Obtém a URL efetiva de um fluxo de bytes.
ms.assetid: 0A83CFC0-7EAA-464B-BA39-50DF220AF683
title: Atributo MF_BYTESTREAM_EFFECTIVE_URL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95e01238f04c30f72d55f940b3f3105863247ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758080"
---
# <a name="mf_bytestream_effective_url-attribute"></a>Atributo de URL de bytes de MF em \_ \_ vigor \_

Obtém a URL efetiva de um fluxo de bytes.

## <a name="data-type"></a>Tipo de dados

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Aplica-se a

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Comentários

A URL efetiva pode diferir da URL original se a URL original contiver informações adicionais, como cadeias de caracteres de pesquisa ou âncoras, ou se a solicitação tiver sido redirecionada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de fluxo de bytes](byte-stream-attributes.md)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




