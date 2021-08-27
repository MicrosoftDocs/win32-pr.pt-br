---
title: Mensagem de LVM_GETNUMBEROFWORKAREAS (commctrl. h)
description: Recupera o número de áreas de trabalho em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetNumberOfWorkAreas do ListView.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- controles de Windows de mensagem de LVM_GETNUMBEROFWORKAREAS
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 735dbb808755857df3dec4c5e8a021b9fe873e555607dc547bc77e67e123b948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088876"
---
# <a name="lvm_getnumberofworkareas-message"></a>\_Mensagem GETNUMBEROFWORKAREAS LVM

Recupera o número de áreas de trabalho em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetNumberOfWorkAreas do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um valor UINT que recebe o número de áreas de trabalho no controle de exibição de lista. Se zero for colocado nessa variável, nenhuma área de trabalho estará definida no momento. Esse valor não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor retornado para esta mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando controles de List-View](using-list-view-controls.md)
</dt> </dl>

 

 





