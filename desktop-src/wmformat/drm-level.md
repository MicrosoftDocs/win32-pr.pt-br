---
title: DRM_Level
description: '\_o nível de DRM é um atributo de licença que o Windows SDK do formato de mídia define quando cria uma licença local para arquivos protegidos com o DRM versão 1.'
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
ms.openlocfilehash: a4767f839c5d21610e7e425aea4a20a52c3cb0d8658848f578a33ca403f4ad60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848678"
---
# <a name="drm_level"></a>Nível de DRM \_

**DRM \_ Level** é um atributo de licença que o Windows SDK do formato de mídia define quando cria uma licença local para arquivos protegidos com o DRM versão 1. Ele contém o nível de segurança que o aplicativo de chamada deve ter para acessar o conteúdo no arquivo. O valor padrão é 150.

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

 

 




