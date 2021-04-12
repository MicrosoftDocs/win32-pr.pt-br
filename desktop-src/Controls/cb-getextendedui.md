---
title: Mensagem de CB_GETEXTENDEDUI (WinUser. h)
description: Determina se uma caixa de combinação tem a interface do usuário padrão ou a interface do usuário estendida.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- Controles de CB_GETEXTENDEDUI de mensagens do Windows
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
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455126"
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

## <a name="return-value"></a>Retornar valor

Se a caixa de combinação tiver a interface do usuário estendida, o valor de retorno será **true**; caso contrário, será **false**.

## <a name="remarks"></a>Comentários

Por padrão, a tecla F4 é aberta ou fecha a lista e a seta para baixo altera a seleção atual. Em uma caixa de combinação com a interface do usuário estendida, a tecla F4 é desabilitada e pressionar a tecla de seta para baixo abre a lista suspensa.

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

[**\_SETEXTENDEDUI CB**](cb-setextendedui.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Recursos da caixa de combinação](combo-box-features.md)
</dt> </dl>

 

 





