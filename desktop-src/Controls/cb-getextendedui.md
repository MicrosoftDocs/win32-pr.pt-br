---
title: Mensagem de CB_GETEXTENDEDUI (WinUser. h)
description: Determina se uma caixa de combinação tem a interface do usuário padrão ou a interface do usuário estendida.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- controles de Windows de mensagem de CB_GETEXTENDEDUI
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05201b0986b114e97523716edacc6fe391908d3ed2841d36bf7578a6455f42a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089216"
---
# <a name="cb_getextendedui-message"></a>\_Mensagem de GETEXTENDEDUI CB

Determina se uma caixa de combinação tem a interface do usuário padrão ou a interface do usuário estendida.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a caixa de combinação tiver a interface do usuário estendida, o valor de retorno será **true**; caso contrário, será **false**.

## <a name="remarks"></a>Comentários

Por padrão, a tecla F4 é aberta ou fecha a lista e a seta para baixo altera a seleção atual. Em uma caixa de combinação com a interface do usuário estendida, a tecla F4 é desabilitada e pressionar a tecla de seta para baixo abre a lista suspensa.

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

[**\_SETEXTENDEDUI CB**](cb-setextendedui.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Recursos da caixa de combinação](combo-box-features.md)
</dt> </dl>

 

 





