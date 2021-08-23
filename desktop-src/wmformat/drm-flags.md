---
title: DRM_Flags
description: A propriedade Sinalizadores DRM é usada com o conteúdo do DRM versão 1 apenas para especificar os direitos que estarão \_ contidos na licença local.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf4f1b2065eb1b251f0c555f8c33e424e43aefd04377ed894edb90c121aacb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086007"
---
# <a name="drm_flags"></a>Sinalizadores DRM \_

A **propriedade \_ Sinalizadores DRM** é usada com o conteúdo do DRM versão 1 apenas para especificar os direitos que estarão contidos na licença local. Os direitos são especificados com valores definidos pelo tipo de **enumeração WMT \_ RIGHTS.** Mais de um valor pode ser selecionado combinando-os com o operador **OR bit** a bit.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ Flags

## <a name="data-type"></a>Tipo de Dados

**WMT \_ TYPE \_ DWORD**

## <a name="remarks"></a>Comentários

Ao acessar a interface **IWMHeaderInfo3** do objeto writer, você pode adicionar ou alterar esse valor. Em outros objetos (editor de metadados, leitor e leitor síncrono), esse valor é somente leitura. Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) para definir essa propriedade ao criar conteúdo drm versão 1.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do DRM**](drm-properties.md)
</dt> </dl>

 

 




