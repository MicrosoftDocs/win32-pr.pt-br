---
title: DRM_HeaderSignPrivKey
description: A propriedade HeaderSignPrivKey do DRM contém a \_ chave privada usada para assinar o header ASF.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7f8cc90e509294d9de9d3577ad5a2d56b61eb3a471f9b493e555c0f1ecf824
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547606"
---
# <a name="drm_headersignprivkey"></a>\_HeaderSignPrivKey do DRM

A **propriedade \_ HeaderSignPrivKey** do DRM contém a chave privada usada para assinar o header ASF.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ HeaderSignPrivKey

## <a name="data-type"></a>Tipo de Dados

**CADEIA DE CARACTERES DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

Essa propriedade é gerada usando [**o IWMDRMWriter::GenerateSigningKeyPair.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) Mantenha esse segredo de chave e compartilhe a chave pública somente com o serviço de licença. Depois de definir essa chave, o componente DRM a usará para assinar o header do arquivo ASF (não o header DRM assinado com os valores de objeto de assinatura digital, como DRM \_ LASignaturePrivKey). Obviamente, **o \_ HeaderSignPrivKey** do DRM não está incluído no headert do arquivo.

Essa propriedade não está acessível do objeto de leitor. Ele pode ser definido do objeto writer usando [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do DRM**](drm-properties.md)
</dt> </dl>

 

 




