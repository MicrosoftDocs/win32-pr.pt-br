---
title: Mensagem de HDM_GETITEMRECT (commctrl. h)
description: Obtém o retângulo delimitador para um determinado item em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetItemRect do cabeçalho.
ms.assetid: b483ef97-3700-425b-8160-81c673850f68
keywords:
- Controles de HDM_GETITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4baec72bd914a9d2dad72556a5444c0059452cf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455435"
---
# <a name="hdm_getitemrect-message"></a>\_Mensagem HDM GETITEMRECT

Obtém o retângulo delimitador para um determinado item em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetItemRect do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

O índice de base zero do item de controle de cabeçalho para o qual recuperar o retângulo delimitador.

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/windows/win32/api/windef/ns-windef-rect) que recebe as informações do retângulo delimitador. O remetente da mensagem é responsável por alocar essa estrutura. As coordenadas retornadas na estrutura RECT são expressas em relação ao pai do controle de cabeçalho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





