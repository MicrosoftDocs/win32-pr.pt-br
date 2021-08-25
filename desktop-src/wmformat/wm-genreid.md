---
title: WM/GenreID
description: O atributo WM/GenreID contém um identificador de gênero em conformidade com o conteúdo da marca TCON em ID3v2.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- Formato de mídia do Windows WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9355a16196d386d4ec3f2a98588eced2981f8e62a3df96a9c0d094551a10a733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930436"
---
# <a name="wmgenreid"></a>WM/GenreID

O **atributo WM/GenreID** contém um identificador de gênero em conformidade com o conteúdo da marca TCON em ID3v2. Isso deve conter a ID de gênero entre parênteses, opcionalmente seguido por um refinamento que descreve ainda mais o gênero. Para obter mais informações, consulte a especificação ID3v2.

## <a name="global-constant"></a>Constante global

g \_ wszWMGenreID

## <a name="data-type"></a>Tipo de Dados

**CADEIA DE CARACTERES DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

O atributo preferencial para especificar um gênero é [**WM/Genre.**](wm-genre.md) Use-o como preferência para esse atributo.

Se você alterar **WM/Genre ou** **WM/GenreID** em um arquivo MP3, o outro atributo será alterado para corresponder.

### <a name="example"></a>Exemplo



| Tipo de arquivo | Valor de exemplo   |
|-----------|-----------------|
| Áudio     | "(4) Eurodisco" |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




