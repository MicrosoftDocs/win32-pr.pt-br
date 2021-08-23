---
title: Use_Advanced_DRM
description: O atributo \_ Usar \_ DRM Avançado especifica se a versão 7 do DRM é usada para proteger o conteúdo.
ms.assetid: a385152f-d72e-473c-93a0-5697659df23c
keywords:
- Use_Advanced_DRM formato de mídia do Windows
topic_type:
- apiref
api_name:
- Use_Advanced_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a11731fbe212c8b87cd52300da1885206230c7329491a6512ab3c261923c74e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658216"
---
# <a name="use_advanced_drm"></a>Usar \_ \_ DRM Avançado

O **atributo \_ Usar \_ DRM** Avançado especifica se a versão 7 do DRM é usada para proteger o conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszWMUse \_ ADVANCED \_ DRM

## <a name="data-type"></a>Tipo de Dados

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Comentários

Essa é uma propriedade de leitura/gravação que é recuperada usando [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) e definida usando [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute). Essa propriedade não está acessível do objeto de leitor.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do DRM**](drm-properties.md)
</dt> </dl>

 

 




