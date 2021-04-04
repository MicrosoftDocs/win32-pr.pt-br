---
title: DRM_Flags
description: A \_ propriedade de sinalizadores DRM é usada com o conteúdo do DRM versão 1 somente para especificar os direitos que estarão contidos na licença local.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916987"
---
# <a name="drm_flags"></a>Sinalizadores de DRM \_

A propriedade de **\_ sinalizadores DRM** é usada com o conteúdo do DRM versão 1 somente para especificar os direitos que estarão contidos na licença local. Os direitos são especificados com valores definidos pelo tipo de enumeração **\_ direitos de WMT** . Mais de um valor pode ser selecionado combinando-os com o **operador OR**

## <a name="global-constant"></a>Constante global

\_sinalizadores g wszWMDRM \_

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Comentários

Ao acessar a interface **IWMHeaderInfo3** do objeto gravador, você pode adicionar ou alterar esse valor. Em outros objetos (editor de metadados, leitor e leitor síncrono), esse valor é somente leitura. Use [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) para definir essa propriedade ao criar o conteúdo do DRM versão 1.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




