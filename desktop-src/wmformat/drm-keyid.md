---
title: DRM_KeyID
description: O \_ atributo keyid do DRM contém o identificador de chave.
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- DRM_KeyID o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a60afa330a7cf967b42a4d06009d9c921d8f56
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007144"
---
# <a name="drm_keyid"></a>\_Keyid DRM

O **atributo \_ keyid do DRM** contém o identificador de chave.

## <a name="global-constant"></a>Constante global

\_keyid g wszWMDRM \_

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

Este atributo está presente somente para conteúdo DRM versão 7. Ele pode ser definido usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). O mesmo atributo de arquivo pode ser recuperado usando o [**\_ \_ keyid DRMHeader do DRM**](drm-drmheader-keyid.md).

A ID da chave é usada em conjunto com a semente de chave para criar a chave de conteúdo que é usada para criptografar e descriptografar o arquivo. O aplicativo de gravador usa a ID de chave para criptografar o arquivo e, em seguida, armazena a ID da chave no cabeçalho do arquivo. Quando um aplicativo de Player solicita uma licença para um arquivo, o componente DRM envia a ID de chave (juntamente com o restante do cabeçalho DRM) para o servidor de licença. O servidor de licença, que tem a semente da chave secreta, usa-a e a ID da chave para criar uma chave para o arquivo, que ele insere em uma licença junto com os vários direitos que serão aplicados ao arquivo.

Normalmente, uma semente de chave é usada com muitas IDs de chave. A semente de chave é um segredo compartilhado somente pelo criador de conteúdo e pelo distribuidor de licenças. A ID da chave é usada por aplicativos cliente DRM e é armazenada no cabeçalho DRM em claro.

Esse atributo é o mesmo que [**o \_ \_ keyid DRMHeader do DRM**](drm-drmheader-keyid.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




