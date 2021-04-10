---
title: DRM_Level
description: '\_O nível de DRM é um atributo de licença que o Windows Media Format SDK define ao criar uma licença local para arquivos protegidos com o DRM versão 1.'
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3177197b9c149c2fca2c7678a8fe03c6b412e2d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293797"
---
# <a name="drm_level"></a>Nível de DRM \_

**DRM \_ Nível** é um atributo de licença que o SDK do Windows Media Format define ao criar uma licença local para arquivos protegidos com o DRM versão 1. Ele contém o nível de segurança que o aplicativo de chamada deve ter para acessar o conteúdo no arquivo. O valor padrão é 150.

## <a name="global-constant"></a>Constante global

\_nível g wszWMDRM \_

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Comentários

O nível de segurança do DRM de um aplicativo é determinado pela biblioteca wmstubdrm específica a que ele se vincula no momento da compilação. Para obter mais informações sobre esses níveis de segurança, consulte [obtendo a biblioteca de DRM necessária](obtaining-the-required-drm-library.md). Use [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) para definir essa propriedade ao proteger arquivos ASF com o DRM versão 1.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




