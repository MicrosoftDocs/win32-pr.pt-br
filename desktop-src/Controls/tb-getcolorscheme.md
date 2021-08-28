---
title: TB_GETCOLORSCHEME mensagem (Commctrl.h)
description: Recupera as informações do esquema de cores do controle da barra de ferramentas.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- TB_GETCOLORSCHEME controles Windows mensagem
topic_type:
- apiref
api_name:
- TB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fca3a7a88fd108454c3838d646db311c9be19bf04163b4c8987db67f6c09c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918866"
---
# <a name="tb_getcolorscheme-message"></a>Mensagem \_ GETCOLORSCHEME de TB

Recupera as informações do esquema de cores do controle da barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que receberá as informações do esquema de cores. Você deve definir o **membro cbSize** dessa estrutura como **sizeof**(COLORSCHEME) antes de enviar essa mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TB \_ SETCOLORSCHEME**](tb-setcolorscheme.md)
</dt> </dl>

 

 





