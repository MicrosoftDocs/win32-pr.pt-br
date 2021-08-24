---
title: EM_SETTABLEPARMS mensagem (Richedit.h)
description: Altera os parâmetros de linhas em uma tabela.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- EM_SETTABLEPARMS controles de Windows mensagem
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
ms.openlocfilehash: bccb6258f03d76391bf2288331efb3d9ebde4fb903fe907eaa5e9d37e7497a74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576346"
---
# <a name="em_settableparms-message"></a>Mensagem EM \_ SETTABLEPARMS

Altera os parâmetros de linhas em uma tabela.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura TABLEROWPARMS.**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura TABLECELLPARMS.**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido ou um dos códigos de erro a seguir.



| Código de retorno                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Não é possível fazer alterações. Isso pode ocorrer se o controle for um controle de texto sem-texto ou de linha única ou se o ponto de inserção estiver dentro de um objeto matemático. Isso também ocorrerá se as tabelas estão desabilitadas ou se a mensagem [**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md) define o **valor SES EX \_ \_ NOTABLE.** <br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | O *wParam* ou *lParam* é NULL ou aponta para uma estrutura inválida. O **membro cCell** da estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve ser pelo menos 1 e não mais que 63. O **membro cbRow** deve ser igual `sizeof(TABLEROWPARMS)` ou `sizeof(TABLEROWPARMS)   2*sizeof(long)` . O último valor é o tamanho da estrutura **TABLEROWPARMS** richEdit 4.1. O **membro cbCell** de **TABLEROWPARMS** deve ser igual a `sizeof(TABLECELLPARMS)` . O ponto de inserção deve estar no início de uma tabela ou dentro de uma linha de tabela e o número de células só pode ser alterado em uma. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente disponível.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Comentários

Essa mensagem altera os parâmetros do número de linhas especificado pelo membro **cRow** da estrutura [**TABLEROWPARMS,**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) se a tabela tiver muitas linhas consecutivas. Se **cRow** for menor que 0, a mensagem será iterado até o final da tabela. Se a nova contagem de células for diferente da contagem de células atual em +1 ou 1, ela inserirá ou excluirá a célula no índice especificado pelo membro **iCell** de **TABLEROWPARMS.** A linha da tabela inicial é identificada por uma posição de caractere. Essa posição é especificada por membros **cpStartRow** com valores maiores ou iguais a zero. A posição deve estar dentro da linha da tabela, mas não dentro de uma tabela aninhada, a menos que você queira alterar os parâmetros dessa tabela. Se o **membro cpStartRow** for 1, a posição do caractere será dada pela seleção atual. Para isso, posicione a seleção em qualquer lugar dentro da linha da tabela ou selecione a linha com a extremidade ativa da seleção no final da linha da tabela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ GETTABLEPARMS**](em-gettableparms.md)
</dt> </dl>

 

 





