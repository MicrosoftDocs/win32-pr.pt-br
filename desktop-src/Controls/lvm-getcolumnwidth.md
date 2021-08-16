---
title: LVM_GETCOLUMNWIDTH mensagem (Commctrl.h)
description: Obtém a largura de uma coluna na exibição de relatório ou lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro ListView GetColumnWidth.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- LVM_GETCOLUMNWIDTH controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 800ab7172ec489b84506cc55a342325527f38e447fc2bae635c2e5688a142b25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411502"
---
# <a name="lvm_getcolumnwidth-message"></a>Mensagem \_ GETCOLUMNWIDTH do LVM

Obtém a largura de uma coluna na exibição de relatório ou lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ ListView GetColumnWidth.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice da coluna. Esse parâmetro é ignorado na exibição de lista.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a largura da coluna se for bem-sucedida ou zero caso contrário. Se essa mensagem for enviada para um controle de exibição de lista com o estilo [**report LVS \_**](list-view-window-styles.md) e a coluna especificada não existir, o valor de retorno será indefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





