---
title: Mensagem de CB_SETHORIZONTALEXTENT (WinUser. h)
description: Um aplicativo envia a \_ mensagem CB SETHORIZONTALEXTENT para definir a largura, em pixels, pela qual uma caixa de listagem pode ser rolada horizontalmente (a largura rolável).
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- Controles de CB_SETHORIZONTALEXTENT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51e505f36f7cfd3fa47644a288db4a97ba89ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455117"
---
# <a name="cb_sethorizontalextent-message"></a>\_Mensagem de SETHORIZONTALEXTENT CB

Um aplicativo envia a mensagem **CB \_ SETHORIZONTALEXTENT** para definir a largura, em pixels, pela qual uma caixa de listagem pode ser rolada horizontalmente (a largura rolável). Se a largura da caixa de listagem for menor que esse valor, a barra de rolagem horizontal rolará horizontalmente os itens na caixa de listagem. Se a largura da caixa de listagem for igual ou maior que esse valor, a barra de rolagem horizontal ficará oculta ou, se a caixa de combinação tiver o estilo [**CBS \_ DISABLENOSCROLL**](combo-box-styles.md) , será desabilitada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica a largura rolável da caixa de listagem, em pixels.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETHORIZONTALEXTENT CB**](cb-gethorizontalextent.md)
</dt> </dl>

 

 





