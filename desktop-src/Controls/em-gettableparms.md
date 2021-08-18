---
title: Mensagem de EM_GETTABLEPARMS (RichEdit. h)
description: Recupera os parâmetros de tabela para uma linha de tabela e os parâmetros de célula para o número especificado de células.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- controles de Windows de mensagem de EM_GETTABLEPARMS
topic_type:
- apiref
api_name:
- EM_GETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ddca96ce29a0f7b7076580b48cfeceecf1f638830b7c77bc9406a39e97de57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545026"
---
# <a name="em_gettableparms-message"></a>\_Mensagem em GETTABLEPARMS

Recupera os parâmetros de tabela para uma linha de tabela e os parâmetros de célula para o número especificado de células.


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



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

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se for bem-sucedido ou um dos seguintes códigos de erro.



| Código de retorno                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FALHA**</dt> </dl>        | Não é possível fazer alterações. Isso pode ocorrer se o controle for um controle de linha simples ou de texto sem formatação ou se o ponto de inserção estiver dentro de um objeto matemático. Isso também ocorrerá se as tabelas estiverem desabilitadas se a mensagem em [**\_ SETEDITSTYLEEX**](em-seteditstyleex.md) definir o valor de **ses \_ ex \_ notável** . <br/>                                                                                                                                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *WParam* ou *lParam* é nulo ou aponta para uma estrutura inválida. O membro **cbRow** da estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve ser igual `sizeof(TABLEROWPARMS)` ou sizeof (TABLEROWPARMS) 2 \* sizeof (Long). O último valor é o tamanho da estrutura RichEdit 4,1 **TABLEROWPARMS** . O membro **cbCell** da estrutura **TABLEROWPARMS** deve ser igual `sizeof(TABLECELLPARMS)` . A posição do caractere de consulta deve estar em um delimitador de linha de tabela. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente disponível.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentários

Essa mensagem obtém os parâmetros de tabela para a linha na posição de caractere especificada pelo membro **cpStartRow** da estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) e o número de células especificado pelo membro **cCells** da estrutura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .

A posição do caractere especificada pelo membro **cpStartRow** da estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve estar no início da linha da tabela ou no delimitador final da linha da tabela. Se **cpStartRow** for definido como 1, a posição do caractere será fornecida pela seleção atual. Nesse caso, posicione a seleção no final da linha (entre a marca de célula e o delimitador final da linha da tabela) ou selecione a linha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SETTABLEPARMS**](em-settableparms.md)
</dt> </dl>

 

 





