---
title: Mensagem de EM_SETFONTSIZE (RichEdit. h)
description: Define o tamanho da fonte para o texto selecionado em um controle rich edit.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- Controles de EM_SETFONTSIZE de mensagens do Windows
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
ms.openlocfilehash: 8eb75276acbb86cbd452a8ad97698f1cd7382bd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455184"
---
# <a name="em_setfontsize-message"></a>\_Mensagem em SETfontize

Define o tamanho da fonte para o texto selecionado em um controle rich edit.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Alteração no tamanho do ponto do texto selecionado. O resultado será arredondado de acordo com os valores mostrados na tabela a seguir. Esse parâmetro deve estar no intervalo de-1637 a 1638. O tamanho da fonte resultante estará dentro do intervalo de 1 a 1638.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se nenhum erro tiver ocorrido, o valor de retorno será **true**.

Se ocorrer um erro, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

Você pode obter facilmente o tamanho da fonte enviando a mensagem em [**\_ GETCHARFORMAT**](em-getcharformat.md) .

A edição avançada primeiro adiciona *wParam* ao tamanho da fonte atual e, em seguida, usa o tamanho resultante e a tabela a seguir para determinar o valor de arredondamento.



| Banda    | Valor de arredondamento |
|---------|----------------|
| <= 12 | 1              |
| 28      | 2              |
| 36      | 0              |
| 48      | 0              |
| 72      | 0              |
| 80      | 0              |
| > 80 | 10             |



 

Se o tamanho da fonte resultante não for divisível igualmente pelo valor de arredondamento, o tamanho da fonte será arredondado para um número igualmente divisível pelo valor de arredondamento. Portanto, se o tamanho da fonte for menor ou igual a 12, o valor de arredondamento será 1. Da mesma forma, se o tamanho da fonte for menor ou igual a 28, o valor de arredondamento será 2. Para valores maiores que 28, os tamanhos de fonte são arredondados para a próxima faixa. Portanto, o tamanho da fonte vai para 36, 48, 72, 80. Após 80, todo o arredondamento é feito em incrementos de dez pontos.

O tamanho da fonte é arredondado para cima ou para baixo, dependendo do sinal de *wParam*. Se *wParam* for positivo, o arredondamento estará sempre ativo. Caso contrário, o arredondamento estará sempre inoperante. Portanto, se o tamanho da fonte atual for 10 e *wParam* for 3, o tamanho da fonte resultante será 14 (10 + 3 = 13, que não é divisível por 2, portanto, o tamanho será arredondado para até 14). Por outro lado, se o tamanho da fonte atual for 14 e *wParam* for-3, o tamanho da fonte resultante será 10 (14-3 = 11, que não é divisível por 2, portanto, o tamanho será arredondado para 10).

A alteração é aplicada a cada parte da seleção. Portanto, se algum texto for 10pt e algum 20pt, após uma chamada com *wParam* definido como 1, os tamanhos de fonte se tornarão 11pt e 22PT, respectivamente.

Exemplos adicionais são mostrados na tabela a seguir.



| Tamanho da fonte original | *wParam* | Tamanho de fonte resultante |
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| Redistribuível<br/>          | Edição avançada 3,0<br/>                                                              |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ GETCHARFORMAT**](em-getcharformat.md)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Sobre os controles de edição avançados](about-rich-edit-controls.md)
</dt> </dl>

 

 





