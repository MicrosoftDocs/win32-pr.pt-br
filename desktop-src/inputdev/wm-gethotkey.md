---
title: Mensagem de WM_GETHOTKEY (WinUser. h)
description: Enviado para determinar a tecla de acesso associada a uma janela.
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- Entrada de mouse e teclado de mensagem WM_GETHOTKEY
topic_type:
- apiref
api_name:
- WM_GETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045ceefaf33c8d8edba0cb69e062ad589cfd833
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454960"
---
# <a name="wm_gethotkey-message"></a>Mensagem de autotecla do WM \_

Enviado para determinar a tecla de acesso associada a uma janela.


```C++
#define WM_GETHOTKEY                    0x0033
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o código de chave virtual e os modificadores para a tecla de acesso, ou **NULL** se nenhuma tecla de acesso estiver associada à janela. O código de chave virtual está no byte baixo do valor de retorno e os modificadores estão no byte alto. Os modificadores podem ser uma combinação dos seguintes sinalizadores de CommCtrl. h.



| Código/valor de retorno                                                                                                                                         | Descrição             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt> </dl>     | tecla ALT<br/>      |
| <dl> <dt>**HOTKEYF \_ CONTROLE**</dt> <dt>0x02</dt> </dl> | Tecla CTRL<br/>     |
| <dl> <dt>**HOTKEYF \_**</dt> <dt>0x08</dt> ext. </dl>     | Chave estendida<br/> |
| <dl> <dt>**HOTKEYF \_ SHIFT**</dt> <dt>0x01</dt> </dl>   | Tecla SHIFT<br/>    |



 

## <a name="remarks"></a>Comentários

Essas teclas de acesso não estão relacionadas às teclas de acesso definidas pela função [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_ SETtecla de atalho**](wm-sethotkey.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

