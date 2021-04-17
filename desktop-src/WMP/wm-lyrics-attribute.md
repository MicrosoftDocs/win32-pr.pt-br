---
title: Atributo do WM/letras de música
description: O atributo WM/letras de música é a letra do conteúdo.
ms.assetid: 125a2a51-81f2-478a-a9e9-234662a17bc0
keywords:
- Atributo do WM/letras de música do Windows Media Player
topic_type:
- apiref
api_name:
- WM/Lyrics
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d4c88b9046a89e37c4e9b588ff52ed937ee80e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782555"
---
# <a name="wmlyrics-attribute"></a>Atributo do WM/letras de música

O atributo **WM/letras de música** é a letra do conteúdo.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

**Letras de música** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMLyrics.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





