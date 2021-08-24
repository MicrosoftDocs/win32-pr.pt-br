---
title: SB_SETBKCOLOR mensagem (Commctrl.h)
description: Define a cor da tela de fundo em uma barra de status.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- SB_SETBKCOLOR controles de Windows mensagem
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b97893d49d475789b07c28e17e88097aa4df4336154d6b4e0f9c4fa081e52635
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637076"
---
# <a name="sb_setbkcolor-message"></a>Mensagem SB \_ SETBKCOLOR

Define a cor da tela de fundo em uma barra de status.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

[**Valor COLORREF**](/windows/desktop/gdi/colorref) que especifica a nova cor da tela de fundo. Especifique o valor CLR \_ DEFAULT para fazer com que a barra de status use sua cor de plano de fundo padrão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a cor da tela de fundo anterior ou CLR \_ DEFAULT se a cor da tela de fundo for a cor padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

