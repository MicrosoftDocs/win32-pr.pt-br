---
description: Contém um ponteiro para o Gerenciador de Dispositivos DXGI para o gravador do coletor.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: Atributo MF_SINK_WRITER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23dea964be1a0ff726a974deaf1949863331df1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798540"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a>\_Atributo de \_ Gerenciador de D3D do gravador de coletor MF \_ \_

Contém um ponteiro para o Gerenciador de Dispositivos DXGI para o [gravador do coletor](sink-writer.md).

## <a name="data-type"></a>Tipo de dados

**IMFDXGIDeviceManager \** _ armazenado como _*IUnknown \**_

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro para a interface [_ *IMFDXGIDeviceManager* *](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

Use esse atributo para fornecer um dispositivo Direct3D para qualquer codificador de vídeo ou coletores de mídia carregados pelo gravador de coletor.

Use este atributo com as seguintes funções:

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Gravador do coletor](sink-writer.md)
</dt> </dl>

 

 




