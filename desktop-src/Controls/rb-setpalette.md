---
title: Mensagem de RB_SETPALETTE (commctrl. h)
description: Define a paleta atual do controle rebar.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- Controles de RB_SETPALETTE de mensagens do Windows
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
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918778"
---
# <a name="rb_setpalette-message"></a>\_Mensagem de SETpalette de RB

Define a paleta atual do controle rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um **HPALETTE** que especifica a nova paleta que será usada pelo controle rebar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um **HPALETTE** que especifica a paleta anterior do controle rebar.

## <a name="remarks"></a>Comentários

É responsabilidade do aplicativo enviar essa mensagem para excluir o **HPALETTE** passado nesta mensagem (consulte [**DeleteId**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)). O controle rebar não excluirá um conjunto de **HPALETTE** com essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetPalette RB \_**](rb-getpalette.md)
</dt> </dl>

 

