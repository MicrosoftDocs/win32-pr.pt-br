---
title: Atributo do WM/letras de música
description: O atributo WM/letras de música é a letra do conteúdo.
ms.assetid: 125a2a51-81f2-478a-a9e9-234662a17bc0
keywords:
- Windows Media Player de atributo do WM/letras de música
topic_type:
- apiref
api_name:
- WM/Lyrics
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f35f6b131fc41258dcce4490c731fde61ef8823cac164523b9b912c7d9586d9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122636"
---
# <a name="wmlyrics-attribute"></a>Atributo do WM/letras de música

O atributo **WM/letras de música** é a letra do conteúdo.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [atributos de arquivo de mídia Windows usados com frequência](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

**Letras de música** é um alias para este atributo.

a constante do SDK do formato de mídia Windows para esse atributo é g \_ wszWMLyrics.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





