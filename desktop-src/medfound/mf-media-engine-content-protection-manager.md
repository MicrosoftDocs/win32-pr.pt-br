---
description: Permite que o mecanismo de mídia Reproduza conteúdo protegido.
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: Atributo MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb99d1df36c9b9adbf1c099d619df60e1144b87
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105784522"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a>\_Atributo do \_ \_ \_ \_ Gerenciador de mídia MF

Permite que o mecanismo de mídia Reproduza conteúdo protegido.

## <a name="data-type"></a>Tipo de dados

**IUnknown\***

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro para a interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) . O chamador deve implementar a interface.

Esse atributo pode ser um dos atributos passados para [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). Será necessário se o conteúdo protegido for reproduzido.

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

[**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




