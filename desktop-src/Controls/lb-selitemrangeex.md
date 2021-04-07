---
title: Mensagem de LB_SELITEMRANGEEX (WinUser. h)
description: Seleciona um ou mais itens consecutivos em uma caixa de listagem de seleção múltipla.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- Controles de LB_SELITEMRANGEEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa3ca1335372b7a61c4dfcbc379c36e89ff933e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918980"
---
# <a name="lb_selitemrangeex-message"></a>SELITEMRANGEEX de mensagens de LB \_

Seleciona um ou mais itens consecutivos em uma caixa de listagem de seleção múltipla.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice de base zero do primeiro item a ser selecionado.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica o índice de base zero do último item a ser selecionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se ocorrer um erro, o valor de retorno será um erro de LB \_ .

## <a name="remarks"></a>Comentários

Se o parâmetro *wParam* for menor que o parâmetro *lParam* , o intervalo de itens especificado será selecionado. Se *wParam* for maior ou igual a *lParam*, o intervalo será removido do intervalo de itens especificado. Para selecionar apenas um item, selecione dois itens e, em seguida, desmarque o item indesejado.

Use essa mensagem somente com caixas de listagem de seleção múltipla.

Esta mensagem pode selecionar um intervalo somente dentro dos primeiros 65.536 itens.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_SELITEMRANGE lb**](lb-selitemrange.md)
</dt> <dt>

[**\_SETSEL lb**](lb-setsel.md)
</dt> </dl>

 

 





