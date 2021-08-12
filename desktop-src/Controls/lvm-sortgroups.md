---
title: Mensagem de LVM_SORTGROUPS (commctrl. h)
description: Usa uma função de comparação definida pelo aplicativo para classificar grupos por ID dentro de um controle de exibição de lista.
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- controles de Windows de mensagem de LVM_SORTGROUPS
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ec17d46205746495cfe95a2af83690644dd8bfced26041906bdea4f809fb36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670780"
---
# <a name="lvm_sortgroups-message"></a>\_Mensagem SORTGROUPS LVM

Usa uma função de comparação definida pelo aplicativo para classificar grupos por ID dentro de um controle de exibição de lista.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Ponteiro para uma função de comparação definida pelo aplicativo, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</dd> <dt>

*lParam* 
</dt> <dd>Ponteiro void para as informações definidas pelo aplicativo.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará 1 se for bem-sucedido ou 0 caso contrário.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

