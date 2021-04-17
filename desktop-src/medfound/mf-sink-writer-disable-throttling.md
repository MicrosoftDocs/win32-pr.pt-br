---
description: Especifica se o gravador do coletor limita a taxa de dados de entrada.
ms.assetid: eb79bda7-ece0-4977-a0f9-d40bd5d220ab
title: Atributo MF_SINK_WRITER_DISABLE_THROTTLING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e01c34b51726135516fb6547679db3ba3d48ebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798541"
---
# <a name="mf_sink_writer_disable_throttling-attribute"></a>\_Atributo de \_ \_ limitação de desabilitação do gravador de coletor MF \_

Especifica se o gravador do coletor limita a taxa de dados de entrada.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Por padrão, o método [**IMFSinkWriter:: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) do gravador do coletor limita a taxa de dados bloqueando o thread de chamada. Isso impede que o aplicativo entregue amostras com muita rapidez. Para desabilitar esse comportamento, defina o \_ atributo de limitação do gravador de coletor MF \_ \_ \_ para **verdadeiro** ao criar o gravador de coletor.

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

 

 




