---
description: Contém um ponteiro para o Gerenciador de Dispositivos do Microsoft Direct3D para o leitor de origem.
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: Atributo MF_SOURCE_READER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828619"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a>\_Atributo de \_ Gerenciador de D3D do leitor de origem MF \_ \_

Contém um ponteiro para o Gerenciador de Dispositivos do Microsoft [Direct3D](direct3d-device-manager.md) para o [leitor de origem](source-reader.md).

## <a name="data-type"></a>Tipo de dados

**IDirect3DDeviceManager9 \* ou IMFDXGIDeviceManager \*** armazenado como **IUnknown \** _

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [_ *IMFAttributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentários

O valor desse atributo pode ser um ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) ou um [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).

Use este atributo para fornecer um dispositivo Direct3D para qualquer decodificador de vídeo carregado pelo leitor de origem. Se você definir esse atributo e o decodificador oferecer suporte ao Microsoft DirectX Video Acceleration (DXVA), o leitor de origem usará o dispositivo Direct3D para alocar buffers de vídeo. Esses buffers são compatíveis com o processador de vídeo DXVA 2. (Consulte [processamento de vídeo de DXVA](dxva-video-processing.md).)

Use este atributo com as seguintes funções:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Normalmente, você definiria esse atributo se estiver usando o leitor de origem para obter quadros de vídeo decodificados e usar o Direct3D para exibir os quadros. Definir esse atributo permite que o decodificador use DXVA.

Você não definirá esse atributo se:

-   Você está usando o leitor de origem para processar somente áudio e não vídeo.
-   Você está obtendo vídeo compactado do leitor de origem. Nesse caso, o leitor de origem não cria um decodificador.

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

[Leitor de origem](source-reader.md)
</dt> <dt>

[Atributos do leitor de origem](source-reader-attributes.md)
</dt> </dl>

 

 




