---
title: LVM_REMOVEGROUP mensagem (Commctrl.h)
description: Remove um grupo de um controle de exibição de lista.
ms.assetid: c6f4f54c-4cf8-47d0-8e96-fa8a1df0501b
keywords:
- LVM_REMOVEGROUP controles Windows mensagem
topic_type:
- apiref
api_name:
- LVM_REMOVEGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c644a0367747ad63eb15a2b83a8df3078c1c89ca1c51875b178aa22d054de2b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062316"
---
# <a name="lvm_removegroup-message"></a>Mensagem REMOVEGROUP LVM \_

Remove um grupo de um controle de exibição de lista.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>ID que especifica o grupo a ser removido.</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará o índice do grupo se for bem-sucedido ou -1 caso contrário.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





