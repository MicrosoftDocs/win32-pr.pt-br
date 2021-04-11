---
title: Busca
description: O atributo pesquisável é um atributo de nível de arquivo que especifica se um aplicativo pode buscar pontos dentro do conteúdo.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Formato de mídia do Windows pesquisável
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4db701be363c194c75bd698062d79a0c0c407cc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104293847"
---
# <a name="seekable"></a>Busca

O atributo **pesquisável** é um atributo de nível de arquivo que especifica se um aplicativo pode buscar pontos dentro do conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszWMSeekable

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

Este é um atributo codificado.

Este atributo não pode ser duplicado no nível do arquivo. Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.

O valor desse atributo para um arquivo pode variar dependendo do objeto expondo a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) ou [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) usada para recuperá-lo. Isso ocorre porque os objetos do leitor (síncrono e assíncrono) executam uma verificação mais completa do que o objeto do editor de metadados, para verificar se você pode buscar um ponto em um arquivo. O valor de atributo **pesquisável** retornado por um objeto leitor é mais preciso.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




