---
title: Mensagem de LVM_SETITEMINDEXSTATE (commctrl. h)
description: Define o estado de um item de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro SetItemIndexState do ListView.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- Controles de LVM_SETITEMINDEXSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMINDEXSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ce8f6847c733127053e2162dd785d52fb77cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009127"
---
# <a name="lvm_setitemindexstate-message"></a>\_Mensagem SETITEMINDEXSTATE LVM

Define o estado de um item de exibição de lista. Envie essa mensagem explicitamente ou usando a macro [**\_ SetItemIndexState do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) para o item. O processo de chamada é responsável por alocar essa estrutura e definir os membros.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . O processo de chamada é responsável por alocar memória para a estrutura. Defina o membro de **estado** como uma ou mais (como uma combinação bit a bit) dos sinalizadores de [Estados de item de exibição de lista](list-view-item-states.md) . Defina o membro **stateMask** da estrutura para indicar os bits válidos do membro de **estado** . Para obter mais informações, consulte o membro **stateMask** da estrutura **LVITEM** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes valores do tipo **HRESULT**.



| Código de retorno                                                                                  | Descrição                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**E \_ falha**</dt> </dl>       | Não foi possível definir o estado.<br/>                            |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | O controle de exibição de lista não estava pronto para a operação.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | A operação foi bem-sucedida.<br/>                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





