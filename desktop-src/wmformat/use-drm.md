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
ms.openlocfilehash: 6fcb010855ac4660792a7c579556001d5d7c4c96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104498978"
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

 

 




