---
title: DRM_DRMHeader_IndividualizedVersion
description: O atributo \_ DRM DRMHeaderIndividualizedVersion contém a versão individualizada mínima necessária para reproduzir o arquivo.
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- DRM_DRMHeader_IndividualizedVersion formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5793fa81a7c6c57542991d582607edb0cf3e38b62b037ad46974a4211a7ef8ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931176"
---
# <a name="drm_drmheader_individualizedversion"></a>DRM \_ DRMHeader \_ IndividualizedVersion

O **atributo \_ DRM DRMHeaderIndividualizedVersion** contém a versão individualizada mínima necessária para reproduzir o arquivo.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion

## <a name="data-type"></a>Tipo de Dados

**CADEIA DE CARACTERES DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

Esse atributo está presente apenas com conteúdo drm versão 7. Ele pode ser recuperado com [**IWMDRMReader::GetDRMProperty.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) Para definir a versão individualizada (também chamada de versão de segurança) no arquivo usando [**IWMDRMWriter::SetDRMAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) você deve usar a [**propriedade DRM \_ IndividualizedVersion.**](drm-individualizedversion.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




