---
title: Mensagem de TVM_SETAUTOSCROLLINFO (commctrl. h)
description: Define informações usadas para determinar as características de rolagem automática. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetAutoScrollInfo.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- Controles de TVM_SETAUTOSCROLLINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETAUTOSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa1f7920d2ec8c443b2ec5f1ff9189c22c5f21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754369"
---
# <a name="tvm_setautoscrollinfo-message"></a>\_Mensagem TVM SETAUTOSCROLLINFO

Define informações usadas para determinar as características de rolagem automática. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetAutoScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Especifica pixels por segundo. O deslocamento para a rolagem é dividido pelo *wParam* para determinar a duração total da rolagem automática.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Especifica o intervalo de tempo de redesenho. Redesenhe a cada intervalo de ELASPED até que o item seja rolado para a exibição. Determinado *wParam*, o local do item é calculado e um redesenho ocorre. Defina esse valor para criar uma rolagem suave.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true**.

## <a name="remarks"></a>Comentários

As informações de AutoScroll são usadas para rolar um item não visível para a exibição. O controle deve ter o estilo estendido de [**TVs \_ ex \_ AUTOHSCROLL**](tree-view-control-window-extended-styles.md) . Para obter informações sobre estilos estendidos, consulte Tree-View estilos estendidos de controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





