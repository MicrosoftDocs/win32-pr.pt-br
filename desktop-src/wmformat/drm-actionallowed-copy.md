---
title: DRM_ActionAllowed_Copy
description: O atributo ActionAllowed Copy do DRM indica se o conteúdo tem permissão para ser copiado para um dispositivo, como \_ \_ um player portátil.
ms.assetid: 3a391a14-ccbb-43c6-b362-0db53d93ab79
keywords:
- DRM_ActionAllowed_Copy formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_Copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437dba087a336322fe1574112dce0b6b5805d05778613924f577c16343d33604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704777"
---
# <a name="drm_actionallowed_copy"></a>Ação \_ drmProvação \_ permitido

O **atributo \_ ActionAllowed \_ Copy** do DRM indica se o conteúdo tem permissão para ser copiado para um dispositivo, como um player portátil.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ Copy

## <a name="data-type"></a>Tipo de Dados

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Comentários

No Windows DRM de Mídia 10, todas as operações de cópia são restritas usando a ação Copiar.

Essa é uma propriedade somente leitura que é recuperada usando [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do DRM**](drm-properties.md)
</dt> </dl>

 

 




