---
title: DRM_LicenseID
description: A \_ Propriedade DRM licenseid contém uma cadeia de caracteres recuperada da licença associada ao arquivo aberto no momento que identifica exclusivamente essa licença.
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293796"
---
# <a name="drm_licenseid"></a>\_Licenseid DRM

A propriedade **DRM \_ licenseid** contém uma cadeia de caracteres recuperada da licença associada ao arquivo aberto no momento que identifica exclusivamente essa licença.

## <a name="global-constant"></a>Constante global

\_licença de wszWMDRM g \_

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

Esse atributo está presente somente com conteúdo do DRM versão 7. Ele pode ser definido usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

A ID da licença é armazenada em uma licença, não em um arquivo ASF. Cada licença individual tem uma ID exclusiva que é atribuída pelo gerador de licença no momento em que a licença é criada. Por exemplo, se você obtiver duas licenças para o mesmo conteúdo, cada uma terá um atributo Licenseid diferente. Normalmente, os aplicativos não precisam recuperar esse valor.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




