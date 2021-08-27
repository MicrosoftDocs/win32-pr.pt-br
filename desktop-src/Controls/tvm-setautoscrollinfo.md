---
title: TVM_SETAUTOSCROLLINFO mensagem (Commctrl.h)
description: Define as informações usadas para determinar as características de rolagem automática. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetAutoScrollInfo.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- TVM_SETAUTOSCROLLINFO controles Windows mensagem
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
ms.openlocfilehash: d8840045900fdbd63930219d199889cde018406779426cd767b49ab41a399efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060156"
---
# <a name="tvm_setautoscrollinfo-message"></a>Mensagem TVM \_ SETAUTOSCROLLINFO

Define as informações usadas para determinar as características de rolagem automática. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetAutoScrollInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>

Especifica pixels por segundo. O deslocamento a rolar é dividido pelo *wParam* para determinar a duração total da rolagem automática.

</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

Especifica o intervalo de tempo de redesenhar. Redesenhar em cada intervalo elaspaixado, até que o item seja rolado para a exibição. Dado *wParam*, o local do item é calculado e ocorre uma nova repaint. De definir esse valor para criar rolagem suave.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE.**

## <a name="remarks"></a>Comentários

As informações de autoscroll são usadas para rolar um item nãovisível para a exibição. O controle deve ter o [**estilo estendido TVS \_ EX \_ AUTOHSCROLL.**](tree-view-control-window-extended-styles.md) Para obter informações sobre estilos estendidos, consulte Tree-View controle de estilos estendidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





