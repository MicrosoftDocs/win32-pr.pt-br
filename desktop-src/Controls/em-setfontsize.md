---
title: EM_SETFONTSIZE mensagem (Richedit.h)
description: Define o tamanho da fonte para o texto selecionado em um controle de edição rico.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- EM_SETFONTSIZE controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_SETFONTSIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e646d58626a034f4764d6b9636e5b4b3eedba5befd7986eade9979c1f4a4fd5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048456"
---
# <a name="em_setfontsize-message"></a>Mensagem EM \_ SETFONTSIZE

Define o tamanho da fonte para o texto selecionado em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Altere o tamanho do ponto do texto selecionado. O resultado será arredondado de acordo com os valores mostrados na tabela a seguir. Esse parâmetro deve estar no intervalo de -1637 a 1638. O tamanho da fonte resultante estará dentro do intervalo de 1 a 1638.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se nenhum erro tiver ocorrido, o valor de retorno será **TRUE.**

Se ocorrer um erro, o valor de retorno será **FALSE.**

## <a name="remarks"></a>Comentários

Você pode obter facilmente o tamanho da fonte enviando a [**mensagem EM \_ GETCHARFORMAT.**](em-getcharformat.md)

Rich Edit primeiro adiciona *wParam* ao tamanho da fonte atual e, em seguida, usa o tamanho resultante e a tabela a seguir para determinar o valor de arredondamento.



| Banda    | Valor de arredondamento |
|---------|----------------|
| <=12 | 1              |
| 28      | 2              |
| 36      | 0              |
| 48      | 0              |
| 72      | 0              |
| 80      | 0              |
| > 80 | 10             |



 

Se o tamanho da fonte resultante não for divisível de maneira semelhante pelo valor de arredondamento, o tamanho da fonte será arredondado para um número que pode ser divisível pelo valor de arredondamento. Portanto, se o tamanho da fonte for menor ou igual a 12, o valor de arredondamento será 1. Da mesma forma, se o tamanho da fonte for menor ou igual a 28, o valor de arredondamento será 2. Para valores maiores que 28, os tamanhos de fonte são arredondados para a próxima faixa. Portanto, o tamanho da fonte vai para 36, 48, 72, 80. Após 80, todo o arredondamento é feito em incrementos de dez pontos.

O tamanho da fonte é arredondado para cima ou para baixo, dependendo do sinal *de wParam*. Se *wParam* for positivo, o arredondamento será sempre para cima. Caso contrário, o arredondamento sempre será inobado. Portanto, se o tamanho atual da fonte for 10 e *wParam* for 3, o tamanho da fonte resultante será 14 (10 + 3 = 13, o que não é divisível por 2, portanto, o tamanho é até 14). Por outro lado, se o tamanho da fonte atual for 14 e *wParam* for -3, o tamanho da fonte resultante será 10 (14 - 3 = 11, o que não é divisível por 2, portanto, o tamanho é reversível para 10).

A alteração é aplicada a cada parte da seleção. Portanto, se parte do texto for 10pt e 20pt, após uma chamada com *wParam* definido como 1, os tamanhos de fonte se tornarão 11pt e 22pt, respectivamente.

Exemplos adicionais são mostrados na tabela a seguir.



| Tamanho da fonte original | *wParam* | Tamanho da fonte resultante |
|--------------------|----------|---------------------|
| 7                  | 1        | 8                   |
| 7                  | 3        | 10                  |
| 10                 | 3        | 14                  |
| 14                 | -3       | 10                  |
| 28                 | 1        | 36                  |
| 28                 | 3        | 36                  |
| 80                 | 1        | 90                  |
| 80                 | -1       | 72                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Redistribuível<br/>          | Rich Edit 3.0<br/>                                                              |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EM \_ GETCHARFORMAT**](em-getcharformat.md)
</dt> <dt>

[**Charformat2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Sobre controles de edição rich](about-rich-edit-controls.md)
</dt> </dl>

 

 





