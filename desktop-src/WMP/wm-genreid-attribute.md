---
title: Atributo WM/Gêneroid
description: O atributo WM/Gêneroid é um identificador de gênero compatível com a marca TCON em ID3v2.
ms.assetid: 9b68f9be-1f02-4b14-b052-90657b8800e3
keywords:
- Atributo WM/Gêneroid Windows Media Player
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d31e54805f778a51f345c84654056391ec4052e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780282"
---
# <a name="wmgenreid-attribute"></a>Atributo WM/Gêneroid

O atributo **WM/gêneroid** é um identificador de gênero compatível com a marca Tcon em ID3v2.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado somente no arquivo de mídia digital.

ID3 versão 2 é uma Convenção de marcação que foi originalmente projetada para MP3. Para obter mais informações, consulte o [site da organização ID3](https://id3.org/).

A constante do Windows Media Format SDK para esse atributo é g \_ wszGenreID.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Versão<br/> | O Windows Media Player 9 Series Windows Media Player 10 ou posterior não oferece suporte a esse atributo<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





