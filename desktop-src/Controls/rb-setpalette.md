---
title: RB_SETPALETTE mensagem (Commctrl.h)
description: Define a paleta atual do controle de barra de rebar.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- RB_SETPALETTE controles de Windows mensagem
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85cd2968fa5fa74915e37f40f30dd47751e2316e8d91d0f51f9d3c7145b893fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434936"
---
# <a name="rb_setpalette-message"></a>Mensagem RB \_ SETPALETTE

Define a paleta atual do controle de barra de rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um **HPALETTE** que especifica a nova paleta que o controle de barra de rebar usará.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **HPALETTE** que especifica a paleta anterior do controle de barras.

## <a name="remarks"></a>Comentários

É responsabilidade do aplicativo enviar essa mensagem para excluir o **HPALETTE** passado nesta mensagem (consulte [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)). O controle de barra de rebar não excluirá um **conjunto HPALETTE** com esta mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RB \_ GETPALETTE**](rb-getpalette.md)
</dt> </dl>

 

