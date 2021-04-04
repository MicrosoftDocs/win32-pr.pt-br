---
title: Mensagem de EM_SETTABLEPARMS (RichEdit. h)
description: Altera os parâmetros de linhas em uma tabela.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- Controles de EM_SETTABLEPARMS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fa77774bd7fcf461fc74b479a57304a5f8ee3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918280"
---
# <a name="em_settableparms-message"></a>\_Mensagem em SETTABLEPARMS

Altera os parâmetros de linhas em uma tabela.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se for bem-sucedido ou um dos seguintes códigos de erro.



| Código de retorno                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FALHA**</dt> </dl>        | Não é possível fazer alterações. Isso pode ocorrer se o controle for um controle de linha simples ou de texto sem formatação ou se o ponto de inserção estiver dentro de um objeto matemático. Isso também ocorrerá se as tabelas estiverem desabilitadas ou se a mensagem em [**\_ SETEDITSTYLEEX**](em-seteditstyleex.md) definir o valor de **ses \_ ex \_ notável** . <br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *WParam* ou *lParam* é nulo ou aponta para uma estrutura inválida. O membro **cCell** da estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve ser pelo menos 1 e não mais que 63. O membro **cbRow** deve ser igual `sizeof(TABLEROWPARMS)` ou `sizeof(TABLEROWPARMS)   2*sizeof(long)` . O último valor é o tamanho da estrutura RichEdit 4,1 **TABLEROWPARMS** . O membro **cbCell** de **TABLEROWPARMS** deve ser igual `sizeof(TABLECELLPARMS)` . O ponto de inserção deve estar no início de uma tabela ou dentro de uma linha de tabela, e o número de células só pode ser alterado por um. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente disponível.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Comentários

Essa mensagem altera os parâmetros do número de linhas especificado pelo membro de **galinha** da estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) , se a tabela tiver várias linhas consecutivas. Se **galinha** for menor que 0, a mensagem será iterada até o final da tabela. Se a nova contagem de células for diferente da contagem de células atual por + 1 ou 1, ela inserirá ou excluirá a célula no índice especificado pelo membro **iCell** de **TABLEROWPARMS**. A linha de tabela inicial é identificada por uma posição de caractere. Essa posição é especificada por membros **cpStartRow** com valores maiores ou iguais a zero. A posição deve estar dentro da linha da tabela, mas não dentro de uma tabela aninhada, a menos que você queira alterar os parâmetros da tabela. Se o membro **cpStartRow** for 1, a posição do caractere será fornecida pela seleção atual. Para isso, posicione a seleção em qualquer lugar dentro da linha da tabela ou selecione a linha com a extremidade ativa da seleção no final da linha da tabela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETTABLEPARMS**](em-gettableparms.md)
</dt> </dl>

 

 





