---
title: Mensagem de EM_GETEXTENDEDSTYLE (commctrl. h)
description: Recupera o estilo estendido para um controle de edição. Envie essa mensagem explicitamente ou usando a macro ' Editar \_ Extended '.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Controles de EM_GETEXTENDEDSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455548"
---
# <a name="em_getextendedstyle-message-commctrlh"></a>Mensagem de EM_GETEXTENDEDSTYLE (commctrl. h)

Recupera o estilo estendido para um controle de exibição de árvore. Envie essa mensagem explicitamente ou usando a macro ' [**Editar \_ Extended**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) '.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor do estilo estendido. Para obter mais informações sobre estilos, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md).

## <a name="remarks"></a>Comentários

Os estilos estendidos para um controle de edição não têm nada a ver com os estilos estendidos usados com a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1809\]<br/>                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2019\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

