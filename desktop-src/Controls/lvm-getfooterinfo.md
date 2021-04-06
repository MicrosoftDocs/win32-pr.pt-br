---
title: Mensagem de LVM_GETFOOTERINFO (commctrl. h)
description: Obtém informações sobre o rodapé de um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro GetFooterInfo do ListView.
ms.assetid: 5734e151-50c0-46df-8f2c-220c4910a590
keywords:
- Controles de LVM_GETFOOTERINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718e6c165985981190b5a1d4c52e851d1a2d504d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917996"
---
# <a name="lvm_getfooterinfo-message"></a>\_Mensagem GETFOOTERINFO LVM

Obtém informações sobre o rodapé de um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a macro [**\_ GetFooterInfo do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado. Deve ser 0.

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) para receber informações dependendo do valor do membro **Mask** . O processo de chamada é responsável por alocar essa estrutura e definir o membro de **máscara** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





