---
title: Mensagem de LVM_SETTEXTBKCOLOR (commctrl. h)
description: Define a cor da tela de fundo do texto em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetTextBkColor do ListView.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- Controles de LVM_SETTEXTBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2247dfd04d90c2b9eacadcb1c38608f519540fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009200"
---
# <a name="lvm_settextbkcolor-message"></a>\_Mensagem SETTEXTBKCOLOR LVM

Define a cor da tela de fundo do texto em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetTextBkColor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Nova cor do plano de fundo do texto. Isso pode ser \_ nenhum CLR para nenhuma cor do plano de fundo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





