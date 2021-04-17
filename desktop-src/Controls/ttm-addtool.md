---
title: Mensagem de TTM_ADDTOOL (commctrl. h)
description: Registra uma ferramenta com um controle ToolTip.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- Controles de TTM_ADDTOOL de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29dad3e297f8c3430f18286afa9a998eaf578a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755419"
---
# <a name="ttm_addtool-message"></a>\_Mensagem ADDFERRAMENTA TTM

Registra uma ferramenta com um controle ToolTip.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que contém informações que o controle ToolTip precisa para exibir o texto da ferramenta. O membro **cbSize** dessa estrutura deve ser preenchido antes de enviar esta mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ ADDTOOLW** (Unicode) e **TTM \_ addferramentaa** (ANSI)<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**TTM \_ DELTOOL**](ttm-deltool.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Sobre os controles de dica de ferramenta](tooltip-controls.md)
</dt> </dl>

 

 





