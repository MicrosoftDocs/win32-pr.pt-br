---
title: Mensagem de LVM_CANCELEDITLABEL (commctrl. h)
description: Cancela uma operação de edição de texto de item.
ms.assetid: 73e9c922-3223-4c49-a33c-df7c09443ccc
keywords:
- controles de Windows de mensagem de LVM_CANCELEDITLABEL
topic_type:
- apiref
api_name:
- LVM_CANCELEDITLABEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0b105c1082457c2cafd14e7a36361100f8e82197db7e5d76ae51447f945897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698796"
---
# <a name="lvm_canceleditlabel-message"></a>\_Mensagem CANCELEDITLABEL LVM

Cancela uma operação de edição de texto de item.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

Essa mensagem faz com que uma notificação [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) seja enviada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





