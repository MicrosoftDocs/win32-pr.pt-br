---
description: Especifica se o leitor de origem desliga a origem da mídia.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: Atributo MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323340a0b95fd6f52d4ac7e8db2e9ff53bf70edb30442369f1ffd8f2f2c55fa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663886"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a>\_ \_ \_ Arquivo de desconexão \_ do leitor \_ de origem MF no \_ atributo de desligamento

Especifica se o [leitor de origem](source-reader.md) desliga a origem da mídia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Esse atributo se aplica somente quando o aplicativo cria o leitor de origem de um objeto de origem de mídia existente chamando [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) ou chamando [**IMFReadWriteClassFactory:: CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).

Por padrão, quando o aplicativo libera o leitor de origem, o leitor de origem desliga a origem da mídia chamando [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) na origem da mídia. Nesse ponto, o aplicativo não poderá mais usar a origem da mídia.

No entanto, se o \_ atributo do leitor de origem MF \_ \_ Desconectar \_ MediaName \_ no \_ desligamento for **true**, o leitor de origem não desligará a origem da mídia. Isso significa que o aplicativo ainda poderá usar a origem de mídia depois que o aplicativo liberar o leitor de origem. Isso também significa que o aplicativo é responsável por chamar [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) na origem da mídia.

Se o aplicativo criar o leitor de origem de uma URL ou de um fluxo de bytes, o leitor de origem sempre desligará a origem da mídia. O \_ atributo de \_ desconexão do leitor de origem MF \_ \_ \_ em \_ desligamento é ignorado nesse caso.

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

 

 




