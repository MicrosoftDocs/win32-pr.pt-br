---
title: DRM_HeaderSignPrivKey
description: A \_ Propriedade DRM HeaderSignPrivKey contém a chave privada usada para assinar o cabeçalho ASF.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af73ea90acca6c20817f35a035f8f297aa56e90b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640143"
---
# <a name="drm_headersignprivkey"></a>\_HEADERSIGNPRIVKEY DRM

A propriedade **DRM \_ HeaderSignPrivKey** contém a chave privada usada para assinar o cabeçalho ASF.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ HeaderSignPrivKey

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

Essa propriedade é gerada usando [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair). Mantenha esse segredo de chave e compartilhe a chave pública somente com o serviço de licença. Depois de definir essa chave, o componente DRM a usará para assinar o cabeçalho do arquivo ASF (não o cabeçalho DRM que é assinado com os valores do objeto de assinatura digital, como DRM \_ LASignaturePrivKey). Obviamente, o **DRM \_ HeaderSignPrivKey** não está incluído no cabeçalho do arquivo.

Essa propriedade não pode ser acessada do objeto leitor. Ele pode ser definido a partir do objeto Writer usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




