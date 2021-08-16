---
title: Use_DRM
description: O \_ atributo usar DRM instrui o objeto gravador a aplicar a proteção DRM versão 1 ao arquivo atual.
ms.assetid: ad959e4a-faf7-4b61-9988-6878afcf3a90
keywords:
- Use_DRM o formato Windows Media
topic_type:
- apiref
api_name:
- Use_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b802a7bef777fab4ed835aa3a1770169deaa6eeea9a7eddeb802fb2e4b0a9dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845297"
---
# <a name="use_drm"></a>Usar \_ DRM

O atributo **usar \_ DRM** instrui o objeto gravador a aplicar a proteção DRM versão 1 ao arquivo atual.

## <a name="global-constant"></a>Constante global

\_wszWMUse \_ DRM

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

Use [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) para definir essa propriedade como **true** ao criar o conteúdo do DRM versão 1. Essa propriedade não pode ser acessada do objeto leitor.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




