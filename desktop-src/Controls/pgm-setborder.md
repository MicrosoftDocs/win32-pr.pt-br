---
title: Mensagem de PGM_SETBORDER (commctrl. h)
description: Define o tamanho da borda atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetBorder do pager.
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- Controles de PGM_SETBORDER de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a987246a56da213098ba8632044af97ae51462df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009264"
---
# <a name="pgm_setborder-message"></a>\_Mensagem de SETborder do PGM

Define o tamanho da borda atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetBorder do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Novo tamanho da borda, em pixels. Esse valor não deve ser maior que o botão de pager ou menor que zero. Se *lParam* for muito grande, a borda será desenhada com o mesmo tamanho do botão. Se *lParam* for negativo, o tamanho da borda será definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor INT que contém o tamanho da borda anterior, em pixels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





