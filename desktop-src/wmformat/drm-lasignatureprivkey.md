---
title: DRM_LASignaturePrivKey
description: A \_ Propriedade DRM LASignaturePrivKey contém a chave privada que é usada para criptografar o cabeçalho DRM.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- DRM_LASignaturePrivKey o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9354cc652bfce22183370b1183062d6cf7f27ce60b3681862f150f565d444a6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704320"
---
# <a name="drm_lasignatureprivkey"></a>\_LASIGNATUREPRIVKEY DRM

A propriedade **DRM \_ LASignaturePrivKey** contém a chave privada que é usada para criptografar o cabeçalho DRM.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ LASignaturePrivKey

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

Essa propriedade pode ser gerada usando o método [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) . Essa propriedade deve permanecer um segredo conhecido apenas pelo criador de conteúdo. Essa propriedade pode ser definida com o método [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) . Ele não está acessível ao objeto leitor.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




