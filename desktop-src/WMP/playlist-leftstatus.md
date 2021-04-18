---
title: PLAYLIST. leftStatus
description: O atributo leftStatus especifica ou recupera o texto de status que é exibido no lado esquerdo e no final do elemento PLAYLIST.
ms.assetid: c83f4fd1-d0e6-4822-9208-8e968c409a78
keywords:
- PLAYLIST. leftStatus Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.leftStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33d4c3d235a7bba67219378063cb9811601e68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764547"
---
# <a name="playlistleftstatus"></a>PLAYLIST. leftStatus

O atributo **leftStatus** especifica ou recupera o texto de status que é exibido no lado esquerdo e no final do elemento **playlist** .

``` syntax
        elementID.leftStatus
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Esse atributo pode combinar qualquer texto com palavras-chave específicas que exibirão as informações desejadas, como a duração total da lista de reprodução. As palavras-chave são circundadas por símbolos percentuais (%) para mantê-los distintos do texto comum.

As palavras-chave a seguir podem ser usadas.



| Palavra-chave               | Descrição                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count                 | Número de itens na lista de reprodução.                                                                                                                                                                             |
| tamanho                  | Tamanho total da lista de reprodução.                                                                                                                                                                                  |
| duration              | Duração total da playlist.                                                                                                                                                                              |
| *XXX*                 | Faz um **getItemInfo** na playlist com *xxx* ser o item a receber.                                                                                                                                 |
| SelectedSize          | Tamanho total das entradas selecionadas na lista de reprodução.                                                                                                                                                          |
| SelectedCount         | Número total de entradas selecionadas na lista de reprodução.                                                                                                                                                            |
| SelectedDuration      | Duração total das entradas selecionadas na playlist.                                                                                                                                                      |
| CheckedCount          | Número total de faixas verificadas na lista de reprodução.                                                                                                                                                              |
| CheckedDuration       | Duração total das faixas verificadas na lista de reprodução.                                                                                                                                                        |
| CheckedSize           | Tamanho total das faixas marcadas na lista de reprodução.                                                                                                                                                            |
| Duraçãostring        | Exibe o texto que descreve a duração como "tempo total" ou "tempo estimado", dependendo se os valores totais são conhecidos. Este texto é seguido por "% Duration%".                                       |
| CheckedDurationString | Exibe o texto que descreve a duração de todos os itens marcados na lista de reprodução como "tempo total" ou "tempo estimado", dependendo se os valores totais são conhecidos. Este texto é seguido por "% Duration%". |



 

O valor "tempo total:% Duration%" para uma lista de reprodução que contém uma duração total de sete minutos exibirá "tempo total: 07:00".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





