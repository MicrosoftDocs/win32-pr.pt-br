---
title: Mensagem de TTM_DELTOOL (commctrl. h)
description: Remove uma ferramenta de um controle ToolTip.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- Controles de TTM_DELTOOL de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943259c5496757c0f15ca4127d0a5e6a4237fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754801"
---
# <a name="ttm_deltool-message"></a>\_Mensagem TTM DELTOOL

Remove uma ferramenta de um controle ToolTip.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Os membros de **HWND** e **UID** identificam a ferramenta a ser removida e o membro **cbSize** deve especificar o tamanho da estrutura. Todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ DELTOOLW** (Unicode) e **TTM \_ DELTOOLA** (ANSI)<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**addferramenta TTM \_**](ttm-addtool.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Sobre os controles de dica de ferramenta](tooltip-controls.md)
</dt> </dl>

 

 





