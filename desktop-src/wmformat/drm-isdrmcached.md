---
title: DRM_IsDRMCached
description: A propriedade ISDRMCached do DRM indica se as informações de licença do DRM versão 1 foram \_ armazenadas no computador local.
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- DRM_IsDRMCached formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9b5bbcf7e4e1c11c8ae992156b7541ac66c7a9d43f2cb1d52878d1ee6762d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709036"
---
# <a name="drm_isdrmcached"></a>DRM \_ IsDRMCached

A **propriedade \_ ISDRMCached** do DRM indica se as informações de licença do DRM versão 1 foram armazenadas no computador local.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ IsDRMCached

## <a name="data-type"></a>Tipo de Dados

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Comentários

Essa é uma propriedade somente leitura que é recuperada usando [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). É TRUE **quando a** URL de aquisição de licença corresponde a uma das duas URLs de conhecimento usadas para aquisição de licença local no DRM versão 1.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do DRM**](drm-properties.md)
</dt> </dl>

 

 




