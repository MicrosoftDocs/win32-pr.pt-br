---
title: DRM_BaseLicenseAcqURL
description: O \_ atributo DRM BaseLicenseAcqURL contém uma URL base parcial para a qual um aplicativo de Player deve navegar para obter uma licença para o conteúdo.
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 128a65eb51d9051243dd439e208207aaf98d5caf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084346"
---
# <a name="drm_baselicenseacqurl"></a>\_BASELICENSEACQURL DRM

O atributo **DRM \_ BaseLicenseAcqURL** contém uma URL base parcial para a qual um aplicativo de Player deve navegar para obter uma licença para o conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ BaseLicenseAcqURL

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

Essa é uma propriedade opcional de leitura/gravação que é definida e recuperada usando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Ele é fornecido para habilitar os sistemas de distribuição de licenças para usarem caminhos relativos nas propriedades da URL de aquisição de licença.

Depois de definir essa propriedade, todas as URLs de aquisição de licença parcial nos cabeçalhos de conteúdo terão a URL base adicionada à frente da URL parcial para formar uma URL completa para o aplicativo de Player navegar. Chamar **IWMDRMReader:: GetDRMProperty** para **DRM \_ BaseLicenseAcqURL** só funcionará na mesma sessão que foi definido. A propriedade não é armazenada no cabeçalho de conteúdo; Ele é dinâmico e apenas a URL relativa é armazenada no conteúdo.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




