---
description: Contém um ponteiro para a interface de retorno de chamada de aplicativos para o leitor de origem.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: Atributo MF_SOURCE_READER_ASYNC_CALLBACK (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af4dedfcdcb426eb62a0ae14bec3fd75232c9a871d0bad10194860305c687fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605147"
---
# <a name="mf_source_reader_async_callback-attribute"></a>\_Atributo de \_ retorno de \_ chamada assíncrono do leitor de origem MF \_

Contém um ponteiro para a interface de retorno de chamada do aplicativo para o [leitor de origem](source-reader.md).

## <a name="data-type"></a>Tipo de dados

**IMFSourceReaderCallback \* *_ armazenado como _* IUnknown\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro para a interface [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) do aplicativo.

Use este atributo com as seguintes funções:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Aplicativos de aplicativos de área de trabalho do servidor 2008 R2 \[ \| UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Leitor de origem](source-reader.md)
</dt> <dt>

[Atributos do leitor de origem](source-reader-attributes.md)
</dt> </dl>

 

 




