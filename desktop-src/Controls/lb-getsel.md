---
title: LB_GETSEL mensagem (Winuser.h)
description: Obtém o estado de seleção de um item.
ms.assetid: f92c02e7-3c6d-4649-8798-42eb4a0c51b6
keywords:
- LB_GETSEL controles de Windows mensagem
topic_type:
- apiref
api_name:
- LB_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e27a1bcec021d7416e32d1bae4047f7b2705e347cc396a07dcf6c377ccb48f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085506"
---
# <a name="lb_getsel-message"></a>Mensagem \_ LB GETSEL

Obtém o estado de seleção de um item.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero do item.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um item for selecionado, o valor de retorno será maior que zero; caso contrário, será zero. Se ocorrer um erro, o valor de retorno será LB \_ ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> </dl>

 

 





