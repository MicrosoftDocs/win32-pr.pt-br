---
title: LVM_SETITEMINDEXSTATE mensagem (Commctrl.h)
description: Define o estado de um item de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro ListView SetItemIndexState.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- LVM_SETITEMINDEXSTATE controles de Windows mensagem
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
ms.openlocfilehash: 18094986f5a57713e842b51b31c74ccfe4987d1c1fe62380ea8a986762e20c7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062206"
---
# <a name="lvm_setitemindexstate-message"></a>Mensagem LVM \_ SETITEMINDEXSTATE

Define o estado de um item de exibição de lista. Envie essa mensagem explicitamente ou usando a [**macro \_ ListView SetItemIndexState.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) para o item. O processo de chamada é responsável por alocar essa estrutura e definir os membros.

</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) O processo de chamada é responsável por alocar memória para a estrutura. De definir **o membro** de estado como um ou mais (como uma combinação bit a bit) dos sinalizadores Estados de [Item de](list-view-item-states.md) Exibição de Lista. De definir **o membro stateMask** da estrutura para indicar os bits válidos do **membro de** estado. Para obter mais informações, consulte **o membro stateMask** da **estrutura LVITEM.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes valores do tipo **HRESULT.**



| Código de retorno                                                                                  | Descrição                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Não foi possível definir o estado.<br/>                            |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | O controle de exibição de lista não estava pronto para a operação.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | A operação foi bem-sucedida.<br/>                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





