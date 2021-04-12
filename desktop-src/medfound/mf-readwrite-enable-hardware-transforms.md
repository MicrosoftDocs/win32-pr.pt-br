---
description: Permite que o leitor de origem ou o gravador de coletor use transformações de Media Foundation baseadas em hardware (MFTs).
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: Atributo MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297150"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a>\_Atributo de \_ \_ \_ transformações de hardware MF ReadWrite

Permite que o leitor de origem ou o gravador de coletor use transformações de Media Foundation baseadas em hardware (MFTs).

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Por padrão, o leitor de origem e o gravador de coletor não usam codificadores de hardware ou codificadores. Para habilitar o uso de MFTs de hardware, defina esse atributo como **true** ao criar o leitor de origem ou o gravador de coletor.

Use este atributo com as seguintes funções:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Há uma exceção para o comportamento padrão. O leitor de origem e o gravador de coletor usam automaticamente MFTs que são registrados localmente no processo do chamador. Para registrar uma MFT localmente, chame [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ou [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid). Os MFTs de hardware registrados localmente são usados mesmo se o atributo **MF \_ ReadWrite habilitar as \_ \_ \_ transformações de hardware** não estiver definido.

Esse atributo não afeta a decodificação de vídeo acelerada por hardware que usa a DXVA (aceleração de vídeo do DirectX). Para habilitar a decodificação de DXVA no leitor de origem, defina o atributo [Gerenciador de D3D de \_ leitor de origem \_ \_ \_ MF](mf-source-reader-d3d-manager.md) .

Se esse atributo for **true**, não defina o atributo [MF \_ ReadWrite \_ Disable \_ Converters](mf-readwrite-disable-converters.md) .

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
</dt> <dt>

[Atributos do leitor de origem](source-reader-attributes.md)
</dt> </dl>

 

 




