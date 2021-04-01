---
description: Contém um ponteiro para a interface de retorno de chamada de aplicativos para o gravador de coletor.
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: Atributo MF_SINK_WRITER_ASYNC_CALLBACK (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663178"
---
# <a name="mf_sink_writer_async_callback-attribute"></a>\_Atributo de \_ retorno de \_ chamada assíncrono do gravador de coletor MF \_

Contém um ponteiro para a interface de retorno de chamada do aplicativo para o gravador do coletor.

## <a name="data-type"></a>Tipo de dados

**[](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) IMFSinkWriterCallback \** _ armazenado como _*IUnknown \**_

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [_ *IMFAttributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro para a interface [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) do aplicativo.

Use este atributo com as seguintes funções:

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do gravador de coletor](sink-writer-attributes.md)
</dt> </dl>

 

 




