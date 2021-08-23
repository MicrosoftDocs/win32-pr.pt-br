---
title: Mensagem de LB_ADDFILE (WinUser. h)
description: Adiciona o nome de arquivo especificado a uma caixa de listagem que contém uma listagem de diretório.
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- controles de Windows de mensagem de LB_ADDFILE
topic_type:
- apiref
api_name:
- LB_ADDFILE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8077bda3015fef36d6383f37f272ddaf25469fcb6930bb38bd0fa8122efc5b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434476"
---
# <a name="lb_addfile-message"></a>A \_ mensagem de ADDfile do lb

Adiciona o nome de arquivo especificado a uma caixa de listagem que contém uma listagem de diretório.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para um buffer que especifica o nome do arquivo a ser adicionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o índice de base zero do arquivo que foi adicionado, ou erro de LB \_ se ocorrer um erro.

## <a name="remarks"></a>Comentários

A caixa de listagem para a qual o *lParam* é adicionado deve ter sido preenchida pela função [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) .

A [**mensagem \_ INITSTORAGE de lb**](lb-initstorage.md) ajuda a acelerar a inicialização de caixas de listagem que têm um grande número de itens (mais de 100). Ele reserva a quantidade especificada de memória para que as mensagens do **lb \_ AddFile** tenham o menor tempo possível. Você pode usar estimativas para os parâmetros *wParam* e *lParam* . Se você superestimar, a memória extra é alocada; Se você subestimar, a alocação normal será usada para itens que excedem o valor solicitado.

Para um aplicativo ANSI, o sistema converte o texto em uma caixa de listagem para Unicode usando CP \_ ACP. Isso pode causar problemas. por exemplo, caracteres romanos acentuados em uma caixa de listagem não-Unicode em japonês Windows ficarão confusos. Para corrigir isso, compile o aplicativo como Unicode ou use uma caixa de listagem desenhada pelo proprietário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[**seqüência de caracteres de LB \_**](lb-addstring.md)
</dt> </dl>

 

 





