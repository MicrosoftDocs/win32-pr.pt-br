---
description: Contém um ponteiro para o Gerenciador de Dispositivos DXGI para o gravador do coletor.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: Atributo MF_SINK_WRITER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706287b6001ba52c8bf5ba8a19326948afcf4f7f7569c606507115f484c46f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714306"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a>\_Atributo de \_ Gerenciador de D3D do gravador de coletor MF \_ \_

Contém um ponteiro para o Gerenciador de Dispositivos DXGI para o [gravador do coletor](sink-writer.md).

## <a name="data-type"></a>Tipo de dados

**IMFDXGIDeviceManager \* *_ armazenado como _* IUnknown\***

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro para a interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

Use esse atributo para fornecer um dispositivo Direct3D para qualquer codificador de vídeo ou coletores de mídia carregados pelo gravador de coletor.

Use este atributo com as seguintes funções:

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Gravador do coletor](sink-writer.md)
</dt> </dl>

 

 




