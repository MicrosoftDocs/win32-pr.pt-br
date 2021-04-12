---
title: Mensagem de HDM_GETOVERFLOWRECT (commctrl. h)
description: Obtém o retângulo delimitador do botão de estouro quando o \_ estilo de estouro da HDS é definido no controle de cabeçalho e o botão de estouro está visível. Envie essa mensagem explicitamente ou usando a \_ macro GetOverflowRect do cabeçalho.
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- Controles de HDM_GETOVERFLOWRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f521bb6b188a10bb7af52ead46423e7ae0cf58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499488"
---
# <a name="hdm_getoverflowrect-message"></a>\_Mensagem HDM GETOVERFLOWRECT

Obtém o retângulo delimitador do botão de estouro quando o estilo de [**\_ estouro da HDS**](header-control-styles.md) é definido no controle de cabeçalho e o botão de estouro está visível. Envie essa mensagem explicitamente ou usando a macro [**\_ GetOverflowRect do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado. Deve ser zero.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para receber as informações do retângulo delimitador. O remetente da mensagem é responsável por alocar essa estrutura. As coordenadas retornadas na estrutura **Rect** são expressas como coordenadas da tela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se for bem-sucedido; caso contrário, **false**.

## <a name="remarks"></a>Comentários

O controle de cabeçalho deve ter o estilo **HDF \_ SPLITBUTTON**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sobre controles de cabeçalho](header-controls.md)
</dt> </dl>

 

