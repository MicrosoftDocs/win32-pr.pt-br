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
ms.openlocfilehash: 43711c6c394761f599271809419a46311265d8b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751768"
---
# <a name="drm_saplevel-deprecated"></a>\_SAPLEVEL DRM (preterido)

\[**DRM \_ O SAPLEVEL** não está mais disponível para uso a partir do Windows Vista. Em vez disso, use o PUMA (áudio do modo de usuário protegido) na biblioteca Media Foundation. \]

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

 

 





