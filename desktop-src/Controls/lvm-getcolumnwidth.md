---
title: Mensagem de LVM_GETCOLUMNWIDTH (commctrl. h)
description: Obtém a largura de uma coluna no modo de exibição de relatório ou de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetColumnWidth do ListView.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- Controles de LVM_GETCOLUMNWIDTH de mensagens do Windows
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
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085173"
---
# <a name="lvm_getcolumnwidth-message"></a>\_Mensagem GETCOLUMNWIDTH LVM

Obtém a largura de uma coluna no modo de exibição de relatório ou de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetColumnWidth do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice da coluna. Esse parâmetro é ignorado na exibição de lista.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a largura da coluna se for bem-sucedida ou zero caso contrário. Se essa mensagem for enviada a um controle de exibição de lista com o estilo de [**\_ relatório LVS**](list-view-window-styles.md) e a coluna especificada não existir, o valor de retorno será indefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





