---
title: Mensagem de EM_INSERTTABLE (RichEdit. h)
description: Insere uma ou mais linhas de tabela idênticas com células vazias.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- controles de Windows de mensagem de EM_INSERTTABLE
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
# <a name="em_inserttable-message"></a>\_Mensagem em InsertTable

Insere uma ou mais linhas de tabela idênticas com células vazias.


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
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

Retornará S \_ OK se a tabela for inserida ou um código de erro, se não for.

## <a name="remarks"></a>Comentários

Se o membro **cpStartRow** do [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) for 1, essa mensagem excluirá o texto selecionado (se houver) e, em seguida, inserirá linhas de tabela vazia com os parâmetros de linha e célula fornecidos por *wParam* e *lParam*. Ele deixa a seleção apontando para o início da primeira célula na primeira linha. Em seguida, o cliente pode preencher as células da tabela apontando a seleção (ou um [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) para as várias marcas de extremidade da célula e inserindo e Formatando o texto desejado. Esse texto pode incluir linhas de tabela aninhadas. Como alternativa, se o membro **cpStartRow** do **TABLEROWPARMS** for 0 ou maior, as linhas da tabela serão inseridas na posição do caractere fornecido pelo **cpStartRow**. Isso só alterará a seleção atual se a tabela for inserida dentro do texto selecionado.

Uma tabela de edição rica da Microsoft consiste em uma sequência de linhas de tabela que, por sua vez, consiste em sequências de parágrafos. Uma linha de tabela começa com o delimitador de dois caracteres especial do parágrafo U + FFF9 U + 000D e termina com o caractere delimitador de dois caracteres no parágrafo U + FFFB U + 000D. Cada célula é encerrada pela marca de célula U + 0007, que é tratada como uma marca de fim de parágrafo difícil, assim como U + 000D (CR). Os parâmetros de linha e célula da tabela são tratados como formatação de parágrafo especial dos delimitadores de linha de tabela. A formatação contém as informações na estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) . Os parâmetros de célula fornecidos pela estrutura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) são armazenados em uma versão expandida da matriz Tabs. Esse formato permite que as tabelas sejam aninhadas em outras tabelas, até quinze níveis de profundidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ INSERTIMAGE**](em-insertimage.md)
</dt> </dl>

 

 





