---
title: PLAYLIST.rightStatus
description: O atributo rightStatus especifica ou recupera o texto de status exibido no lado direito e na parte inferior do elemento PLAYLIST.
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- PLAYLIST.rightStatus Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29b79b0f4e3ad18ed4e044f894d63ec5059477f80999a8b96dc461d9499b29cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336559"
---
# <a name="playlistrightstatus"></a>PLAYLIST.rightStatus

O **atributo rightStatus** especifica ou recupera o texto de status exibido no lado direito e na parte inferior do elemento **PLAYLIST.**

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

Esse atributo pode combinar qualquer texto com palavras-chave específicas que exibirão as informações desejadas, como a duração total da playlist. As palavras-chave estão entre símbolos percentuais (%) para mantê-las distintas do texto comum.

As palavras-chave a seguir podem ser usadas.



| Palavra-chave               | Descrição                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count                 | Número de itens na playlist.                                                                                                                                                                             |
| tamanho                  | Tamanho total da playlist.                                                                                                                                                                                  |
| duration              | Duração total da playlist.                                                                                                                                                                              |
| *Xxx*                 | Faz um **getItemInfo na** playlist com *XXX* sendo o item a ser recebido.                                                                                                                                 |
| SelectedSize          | Tamanho total das entradas selecionadas na playlist.                                                                                                                                                          |
| SelectedCount         | Número total de entradas selecionadas na playlist.                                                                                                                                                            |
| SelectedDuration      | Duração total das entradas selecionadas na playlist.                                                                                                                                                      |
| CheckedCount          | Número total de faixas marcadas na playlist.                                                                                                                                                              |
| CheckedDuration       | Duração total das faixas marcadas na playlist.                                                                                                                                                        |
| CheckedSize           | Tamanho total das faixas marcadas na playlist.                                                                                                                                                            |
| DurationString        | Exibe texto que descreve a duração como "Tempo Total" ou "Tempo Estimado", dependendo se os valores totais são conhecidos. Esse texto é seguido por "%duration%".                                       |
| CheckedDurationString | Exibe texto que descreve a duração de todos os itens marcados na playlist como "Tempo Total" ou "Tempo Estimado", dependendo se os valores totais são conhecidos. Esse texto é seguido por "%duration%". |



 

O valor "Tempo Total: %duração%" para uma playlist que contém uma duração total de sete minutos exibirá "Tempo Total: 07:00".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





