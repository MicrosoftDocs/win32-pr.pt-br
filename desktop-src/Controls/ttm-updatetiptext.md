---
title: Mensagem de TTM_UPDATETIPTEXT (commctrl. h)
description: Define o texto de ToolTip para uma ferramenta.
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- Controles de TTM_UPDATETIPTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_UPDATETIPTEXT
- TTM_UPDATETIPTEXTA
- TTM_UPDATETIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c94b14ec83c190ce019ecba1413d2fa05f0103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085807"
---
# <a name="ttm_updatetiptext-message"></a>\_Mensagem TTM UPDATETIPTEXT

Define o texto de ToolTip para uma ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Os membros **hinst** e **lpszText** devem especificar o identificador de instância e o endereço do texto. Os membros de **HWND** e **UID** identificam a ferramenta a ser atualizada. O membro **cbSize** dessa estrutura deve ser preenchido antes de enviar esta mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ UPDATETIPTEXTW** (Unicode) e **TTM \_ UPDATETIPTEXTA** (ANSI)<br/>       |



 

 





