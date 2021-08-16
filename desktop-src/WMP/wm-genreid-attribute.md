---
title: Atributo WM/GenreID
description: O atributo WM/GenreID é um identificador de gênero em conformidade com a marca TCON em ID3v2.
ms.assetid: 9b68f9be-1f02-4b14-b052-90657b8800e3
keywords:
- Atributo WM/GenreID Windows Media Player
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fdb409453bbdc6a30026b5d36cb35bbaeb2a21264e5049c9e5fff520aea08b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332322"
---
# <a name="wmgenreid-attribute"></a>Atributo WM/GenreID

O **atributo WM/GenreID** é um identificador de gênero em conformidade com a marca TCON em ID3v2.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de Windows mídia comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado somente no arquivo de mídia digital.

A ID3 versão 2 é uma convenção de marcação que foi originalmente projetada para MP3. Para obter mais informações, consulte o site da organização [ID3](https://id3.org/).

A Windows constante do SDK de Formato de Mídia para esse atributo é g \_ wszGenreID.

Para determinar se você pode alterar o valor desse atributo, use o [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 Windows Media Player 10 ou posterior não dá suporte a esse atributo<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





