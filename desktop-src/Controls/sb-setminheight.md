---
title: Mensagem de SB_SETMINHEIGHT (commctrl. h)
description: Define a altura mínima da área de desenho de uma janela de status.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- Controles de SB_SETMINHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcad3bf0cb4d11567e82aae4ef46a95fefe3890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918866"
---
# <a name="sb_setminheight-message"></a>\_Mensagem de SETMINHEIGHT SB

Define a altura mínima da área de desenho de uma janela de status.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Altura mínima, em pixels, da janela.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A altura mínima é a soma de *wParam* e o dobro da largura, em pixels, da borda vertical da janela de status. Um aplicativo deve enviar a mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) para a janela de status para redesenhar a janela. Os parâmetros *wParam* e *lParam* da mensagem **de \_ tamanho do WM** devem ser definidos como zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

