---
title: DRM_IndividualizedVersion
description: O \_ atributo DRM IndividualizedVersion é armazenado no cabeçalho DRM e contém a versão individual, necessária para acessar o conteúdo.
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- DRM_IndividualizedVersion o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d7c9f64a7d4d00e95f8e877e7f33c9e6a8177977eff3b523c25cc1432ac57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704678"
---
# <a name="drm_individualizedversion"></a>\_INDIVIDUALIZEDVERSION DRM

O atributo **DRM \_ IndividualizedVersion** é armazenado no cabeçalho DRM e contém a versão individual, necessária para acessar o conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ IndividualizedVersion

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

Esse atributo está presente somente com conteúdo do DRM versão 7. Ele pode ser definido usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). O mesmo atributo de arquivo pode ser recuperado usando [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




