---
title: DRM_SAPLEVEL (preterido)
description: Especifica o nível de caminho de áudio seguro (SAP) com suporte do seu aplicativo.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (preterido) formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80b43cfcf0c89283237f8ff2d3e4f8612050296d7462f54890c3efa908fa9be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930886"
---
# <a name="drm_saplevel-deprecated"></a>\_SAPLEVEL DRM (preterido)

\[**DRM \_ o SAPLEVEL** não está mais disponível para uso a partir do Windows Vista. Em vez disso, use o PUMA (áudio do modo de usuário protegido) na biblioteca Media Foundation. \]

A propriedade **DRM \_ SAPLEVEL** especifica o nível de caminho de áudio seguro (SAP) com suporte do seu aplicativo.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ SAPLEVEL

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

Essa é uma propriedade somente gravação que é definida chamando [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty). O valor é uma representação de cadeia de caracteres de caracteres largos do nível do SAP, como L "200". Os valores atuais com suporte são 200 e 300.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|--------------------------------|
| Fim do suporte do cliente<br/> | Windows XP<br/>          |
| Fim do suporte do servidor<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> </dl>

 

 





