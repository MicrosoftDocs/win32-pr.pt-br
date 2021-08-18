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
ms.openlocfilehash: d9dea32903de18dd1bde8f132b8acf993d3eba2deb0d45c814f0572ce8591ca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930946"
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

 

 




