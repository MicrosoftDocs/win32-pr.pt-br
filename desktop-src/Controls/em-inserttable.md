---
title: EM_INSERTTABLE mensagem (Richedit.h)
description: Insere uma ou mais linhas de tabela idênticas com células vazias.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- EM_INSERTTABLE controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_INSERTTABLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a015ae2b9a886ddfa24591944f3f70eca8cb192af771c821df9e4a403c837d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413054"
---
# <a name="em_inserttable-message"></a>Mensagem EM \_ INSERTTABLE

Insere uma ou mais linhas de tabela idênticas com células vazias.


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
```



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

Retornará S \_ OK se a tabela for inserida ou um código de erro, caso não seja.

## <a name="remarks"></a>Comentários

Se o membro **cpStartRow** do [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) for 1, essa mensagem excluirá o texto selecionado (se algum) e, em seguida, inserirá linhas de tabela vazias com os parâmetros de linha e célula dados por *wParam* e *lParam*. Ele deixa a seleção apontando para o início da primeira célula na primeira linha. O cliente pode preencher as células da tabela apontando a seleção (ou [**um ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) para as várias marcas de extremidade da célula e inserindo e formatando o texto desejado. Esse texto pode incluir linhas de tabela aninhadas. Como alternativa, se o membro **cpStartRow** do **TABLEROWPARMS** for 0 ou superior, as linhas da tabela serão inseridas na posição do caractere determinada por **cpStartRow**. Isso só altera a seleção atual se a tabela for inserida dentro do texto selecionado.

Uma tabela edição rica da Microsoft consiste em uma sequência de linhas de tabela que, por sua vez, consistem em sequências de parágrafos. Uma linha de tabela começa com o parágrafo especial de dois caracteres U+FFF9 U+000D e termina com o parágrafo de dois caracteres U+FFFB U+000D. Cada célula é encerrada pela marca de célula U+0007, que é tratada como uma marca de fim de parágrafo, assim como U+000D (CR). Os parâmetros de linha e célula da tabela são tratados como formatação de parágrafo especial dos delimitadores de linha de tabela. A formatação contém as informações na estrutura [**TABLEROWPARMS.**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) Os parâmetros de célula dados pela estrutura [**TABLECELLPARMS são**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) armazenados em uma versão expandida da matriz de guias. Esse formato permite que as tabelas sejam aninhadas em outras tabelas, até quinze níveis de profundidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ INSERTIMAGE**](em-insertimage.md)
</dt> </dl>

 

 





