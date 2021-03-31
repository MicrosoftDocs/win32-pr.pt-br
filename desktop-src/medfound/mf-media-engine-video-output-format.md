---
description: Define o formato de destino de renderização para o mecanismo de mídia.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: Atributo MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004025da1ad5258e5b04a3afba4a359f50f7444c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663784"
---
# <a name="mf_media_engine_video_output_format-attribute"></a>\_Atributo de \_ \_ formato de saída de vídeo do mecanismo de \_ mídia MF \_

Define o formato de destino de renderização para o mecanismo de mídia.

## <a name="data-type"></a>Tipo de dados

**Dxgi \_ FORMATO** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Defina esse atributo se você criar o mecanismo de mídia no modo de servidor de quadro. Para obter mais informações, consulte [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). O valor do atributo é um valor [de \_ formato dxgi](../direct3d9/d3dformat.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
