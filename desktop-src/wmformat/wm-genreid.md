---
title: WM/Gêneroid
description: O atributo WM/Gêneroid contém um identificador de gênero compatível com o conteúdo da marca TCON em ID3v2.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- Formato de mídia do Windows WM/Gêneroid
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a3b25dffe69471f47eaf20124af48141835540f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104365033"
---
# <a name="wmgenreid"></a>WM/Gêneroid

O atributo **WM/gêneroid** contém um identificador de gênero compatível com o conteúdo da marca Tcon em ID3v2. Isso deve conter a ID do gênero entre parênteses, opcionalmente seguido por um refinamento que descreve ainda mais o gênero. Para obter mais informações, consulte a especificação ID3v2.

## <a name="global-constant"></a>Constante global

g \_ wszWMGenreID

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

O atributo preferencial para especificar um gênero é [**WM/gênero**](wm-genre.md). Use-o em preferência a este atributo.

Se você alterar o **WM/gênero** ou o **WM/gêneroid** em um arquivo MP3, o outro atributo será alterado para coincidir.

### <a name="example"></a>Exemplo



| Tipo de arquivo | Valor de exemplo   |
|-----------|-----------------|
| Áudio     | "(4) Eurodisco" |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




