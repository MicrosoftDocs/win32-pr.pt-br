---
title: DRM_ActionAllowed_CopyToCD
description: O atributo \_ ActionAllowed CopyToCD do DRM indica se o conteúdo tem permissão para \_ ser copiado para um CD.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852d44a4c812aed0d2f188b5ab18e9b74a1813bd9605bf348ca23b96b72f7d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809406"
---
# <a name="drm_actionallowed_copytocd"></a>Ação do \_ DRMProvado \_ Permitido CopyToCD

O **atributo \_ ActionAllowed \_ CopyToCD** do DRM indica se o conteúdo tem permissão para ser copiado para um CD.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD

## <a name="data-type"></a>Tipo de Dados

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Comentários

Windows As licenças de DRM de mídia 10 usam a ação Copiar para restringir a cópia para CD. Você deve verificar a [**propriedade \_ ActionAllowed \_ Copy**](drm-actionallowed-copy.md) do DRM para determinar se a cópia é permitida.

Essa é uma propriedade somente leitura que é recuperada usando [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do DRM**](drm-properties.md)
</dt> </dl>

 

 




