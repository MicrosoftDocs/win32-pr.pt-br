---
description: Especifica uma janela para que o mecanismo de mídia aplique as proteções do Gerenciador de proteção de saída (OPM).
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: Atributo MF_MEDIA_ENGINE_OPM_HWND (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930121"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a>\_ \_ \_ Atributo HWND de OPM do mecanismo de mídia MF \_

Especifica uma janela para que o mecanismo de mídia aplique as proteções do [Gerenciador de proteção de saída](output-protection-manager.md) (OPM).

## <a name="data-type"></a>Tipo de dados

**HWND** armazenado como **UINT64**

## <a name="remarks"></a>Comentários

Esse atributo é usado com o método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar o mecanismo de mídia.

Para habilitar as proteções de OPM para reprodução de vídeo, o aplicativo deve executar um dos seguintes procedimentos:

-   Defina o [atributo \_ \_ HWND de \_ reprodução \_ do mecanismo de mídia MF](mf-media-engine-playback-hwnd.md) ao criar o mecanismo de mídia.
-   Defina o \_ atributo HWND do mecanismo de mídia MF \_ \_ \_ para criar o mecanismo de mídia.
-   Chame [**IMFMediaEngineProtectedContent:: SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) em qualquer ponto depois de criar o mecanismo de mídia, mas antes que o conteúdo protegido seja exibido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do mecanismo de mídia](media-engine-attributes.md)
</dt> </dl>

 

 




