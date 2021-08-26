---
title: LVM_ENSUREVISIBLE mensagem (Commctrl.h)
description: Garante que um item de exibição de lista seja totalmente ou parcialmente visível, rolando o controle de exibição de lista, se necessário. Você pode enviar essa mensagem explicitamente ou usando a macro ListView \_ EnsureVisible.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- LVM_ENSUREVISIBLE controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baeefaf90f0a4562fb187024b2c6f8676c68fb9d46377a4ced900bda6cfd3dfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920296"
---
# <a name="lvm_ensurevisible-message"></a>Mensagem LVM \_ ENSUREVISIBLE

Garante que um item de exibição de lista seja totalmente ou parcialmente visível, rolando o controle de exibição de lista, se necessário. Você pode enviar essa mensagem explicitamente ou usando a [**macro ListView \_ EnsureVisible.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice do item de exibição de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Um valor que especifica se o item deve estar totalmente visível. Se esse parâmetro for **TRUE,** nenhuma rolagem ocorrerá se o item estiver pelo menos parcialmente visível.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

A mensagem falhará se o estilo da janela incluir [**LVS \_ NOSCROLL.**](list-view-window-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





