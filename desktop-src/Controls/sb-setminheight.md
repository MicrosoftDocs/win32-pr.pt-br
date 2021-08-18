---
title: SB_SETMINHEIGHT mensagem (Commctrl.h)
description: Define a altura mínima da área de desenho de uma janela de status.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- SB_SETMINHEIGHT controles de Windows mensagem
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
ms.openlocfilehash: 1b644067e48312b265d132f7d06d53343c4612b879c3a09b638ebd0a98a7c88a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293726"
---
# <a name="sb_setminheight-message"></a>Mensagem SB \_ SETMINHEIGHT

Define a altura mínima da área de desenho de uma janela de status.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Altura mínima, em pixels, da janela.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A altura mínima é a soma de *wParam* e duas vezes a largura, em pixels, da borda vertical da janela de status. Um aplicativo deve enviar a [**mensagem WM \_ SIZE**](/windows/desktop/winmsg/wm-size) para a janela de status para redesenhar a janela. Os *parâmetros wParam* *e lParam* da mensagem **WM \_ SIZE** devem ser definidos como zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

