---
title: Mensagem de TB_BUTTONSTRUCTSIZE (commctrl. h)
description: Especifica o tamanho da estrutura TBBUTTON.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- Controles de TB_BUTTONSTRUCTSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7187c1f4cb45306fd293c7eb74ef8807f395ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009775"
---
# <a name="tb_buttonstructsize-message"></a>TB de \_ mensagem BUTTONSTRUCTSIZE

Especifica o tamanho da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamanho, em bytes, da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O sistema usa o tamanho para determinar qual versão da DLL (biblioteca de vínculo dinâmico) de controle comum está sendo usada.

Se um aplicativo usar a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar a barra de ferramentas, o aplicativo deverá enviar essa mensagem para a barra de ferramentas antes de enviar a mensagem de * [**TB \_ AddBitmap**](tb-addbitmap.md) ou [**TB \_**](tb-addbuttons.md) . A função [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) envia automaticamente **TB \_ BUTTONSTRUCTSIZE** e o tamanho da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) é um parâmetro da função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

