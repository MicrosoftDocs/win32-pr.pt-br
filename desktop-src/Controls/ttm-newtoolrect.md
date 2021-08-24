---
title: TTM_NEWTOOLRECT mensagem (Commctrl.h)
description: Define um novo retângulo delimitado para uma ferramenta.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- TTM_NEWTOOLRECT controles de Windows mensagem
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13889b0e9c0d80392b88130c33e5e9723ceb776a60a6b941d205d514d96ca22f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750976"
---
# <a name="ttm_newtoolrect-message"></a>Mensagem TTM \_ NEWTOOLRECT

Define um novo retângulo delimitado para uma ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TOOLINFO.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Os **membros hwnd** e **uId** identificam uma ferramenta e o **membro rect** especifica o novo retângulo delimitador. O **membro cbSize** dessa estrutura deve ser preenchido antes de enviar essa mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ NEWTOOLRECTW** (Unicode) e **TTM \_ NEWTOOLRECTA** (ANSI)<br/>           |



 

 





