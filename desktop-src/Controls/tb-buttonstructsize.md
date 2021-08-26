---
title: TB_BUTTONSTRUCTSIZE mensagem (Commctrl.h)
description: Especifica o tamanho da estrutura TBBUTTON.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- TB_BUTTONSTRUCTSIZE controles Windows mensagem
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
ms.openlocfilehash: ceed10eec9038b338d060f28acdab8a10aa88aecef6b264b6d6d0682168f4937
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919136"
---
# <a name="tb_buttonstructsize-message"></a>Mensagem TB \_ BUTTONSTRUCTSIZE

Especifica o tamanho da estrutura [**TBBUTTON.**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamanho, em bytes, da [**estrutura TBBUTTON.**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O sistema usa o tamanho para determinar qual versão da DLL (biblioteca de vínculo dinâmico) de controle comum está sendo usada.

Se um aplicativo usar a [**função CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar a barra de ferramentas, o aplicativo deverá enviar essa mensagem para a barra de ferramentas antes de enviar a mensagem [**\_ ADDBITMAP**](tb-addbitmap.md) ou [**\_ ADDBUTTONS**](tb-addbuttons.md) de TB. A [**função CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) envia **automaticamente TB \_ BUTTONSTRUCTSIZE** e o tamanho da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) é um parâmetro da função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

