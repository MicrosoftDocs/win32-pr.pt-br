---
title: Mensagem de CB_INITSTORAGE (WinUser. h)
description: Um aplicativo envia a \_ mensagem CB INITSTORAGE antes de adicionar um grande número de itens à parte da caixa de listagem de uma caixa de combinação. Essa mensagem aloca memória para armazenar itens da caixa de listagem.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- controles de Windows de mensagem de CB_INITSTORAGE
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be1aeccdde2c81c87956a42e72440732ff9eb2732cbd066f51308816c01f64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089086"
---
# <a name="cb_initstorage-message"></a>\_Mensagem de INITSTORAGE CB

Um aplicativo envia a mensagem **CB \_ INITSTORAGE** antes de adicionar um grande número de itens à parte da caixa de listagem de uma caixa de combinação. Essa mensagem aloca memória para armazenar itens da caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de itens a serem adicionados.

</dd> <dt>

*lParam* 
</dt> <dd>

A quantidade de memória a ser alocada para cadeias de caracteres de item, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem for bem-sucedida, o valor de retorno será o número total de itens para os quais a memória foi alocada previamente, ou seja, o número total de itens adicionados por todas as mensagens do **CB \_ INITSTORAGE** bem-sucedidas.

Se a mensagem falhar, o valor de retorno será CB \_ ERRSPACE.

A mensagem aloca memória e retorna os valores de êxito e erro descritos acima.

## <a name="remarks"></a>Comentários

A mensagem **CB \_ INITSTORAGE** ajuda a acelerar a inicialização de caixas de combinação que têm um grande número de itens (mais de 100). Ele reserva a quantidade especificada de memória para que as mensagens de [**\_ dir**](cb-dir.md) subsequentes [**CB \_**](cb-addstring.md), [**CB \_ InsertString**](cb-insertstring.md)e CB tenham o menor tempo possível. Você pode usar estimativas para os parâmetros *wParam* e *lParam* . Se você superestimar, a memória extra é alocada, se você subestimar, a alocação normal será usada para itens que excedem o valor solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**AddString CB \_**](cb-addstring.md)
</dt> <dt>

[**\_pasta CB**](cb-dir.md)
</dt> <dt>

[**inserção de CB \_**](cb-insertstring.md)
</dt> </dl>

 

 





