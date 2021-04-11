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
ms.openlocfilehash: 03ecde48ef3d68e30116cdd7fc8a77179f2282c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293800"
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

 

 




