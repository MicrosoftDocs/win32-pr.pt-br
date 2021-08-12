---
title: Mensagem de EM_SHOWBALLOONTIP (commctrl. h)
description: A \_ mensagem em SHOWBALLOONTIP exibe uma dica de balão associada a um controle de edição.
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- controles de Windows de mensagem de EM_SHOWBALLOONTIP
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ec2666d18c0f6ce43d5c7644eca0aa2a2cc1f3af72cea03ad34af5ca451cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672319"
---
# <a name="em_showballoontip-message"></a>\_Mensagem em SHOWBALLOONTIP

A mensagem em **\_ SHOWBALLOONTIP** exibe uma dica de balão associada a um controle de edição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) que contém informações sobre a dica de balão a ser exibida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem tiver sucesso, retornará **true**. Caso contrário, retornará **false**.

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

**Referência**
</dt> <dt>

[**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[**Editar \_ ShowBalloonTip**](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 





