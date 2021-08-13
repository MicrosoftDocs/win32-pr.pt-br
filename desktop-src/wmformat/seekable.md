---
title: Pesquisável
description: O atributo Seekable é um atributo de nível de arquivo que especifica se um aplicativo pode buscar pontos dentro do conteúdo.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Formato de mídia do Windows que pode ser buscado
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a254d06b36230bb6920f2f13d646edc5f1cdac75efe15864e0c84ba847cf50f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699982"
---
# <a name="seekable"></a>Pesquisável

O **atributo Seekable** é um atributo de nível de arquivo que especifica se um aplicativo pode buscar pontos dentro do conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszWMSeekable

## <a name="data-type"></a>Tipo de Dados

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Comentários

Esse é um atributo codificado.

Esse atributo não pode ser duplicado no nível do arquivo. Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK Windows Formato de Mídia.

O valor desse atributo para um arquivo pode variar dependendo do objeto que expõe a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) ou [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) usada para recuperá-lo. Isso acontece porque os objetos de leitor (síncronos e assíncronos) executam uma verificação mais completa do que o objeto do editor de metadados, para determinar se você pode buscar um ponto em um arquivo. O **valor do atributo Seekable** retornado por um objeto de leitor é mais preciso.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




