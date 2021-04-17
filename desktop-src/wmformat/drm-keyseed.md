---
title: DRM_KeySeed
description: A \_ Propriedade Keysemente de DRM contém a semente de chave que será usada em conjunto com o keyid para criar a chave.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 698db5fe5a1123af0a7b4623d304bf0569bbf253
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105754226"
---
# <a name="drm_keyseed"></a>Keysemente DRM \_

A **propriedade \_ Keysemente de DRM** contém a semente de chave que será usada em conjunto com o keyid para criar a chave.

## <a name="global-constant"></a>Constante global

\_wszWMDRM \_ keysemente

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

Essa propriedade pode ser definida usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute). Ele não pode ser acessado pelo objeto leitor.

Uma semente-chave normalmente é usada para proteger vários arquivos ou conjuntos de arquivos, por exemplo, todos os arquivos emitidos por um servidor de licença ou talvez todos os arquivos por um determinado artista. O KeyID, no entanto, é exclusivo para cada arquivo.

A semente de chave deve permanecer como um segredo que é compartilhado somente entre o criador de conteúdo e o distribuidor de licenças. Esse valor não é armazenado no cabeçalho DRM e não é necessário nem acessível aos aplicativos do Player DRM.

Uma nova semente de chave pode ser gerada usando o método [**IWMDRMWriter:: GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) ou por qualquer outro meio adequado.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




