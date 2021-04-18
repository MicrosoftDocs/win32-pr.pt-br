---
title: Mensagem de WM_PAINTCLIPBOARD (WinUser. h)
description: Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência quando a área de transferência contém dados no \_ formato OWNERDISPLAY do
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- Troca de dados de mensagem WM_PAINTCLIPBOARD
topic_type:
- apiref
api_name:
- WM_PAINTCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8148af6b513fd1fa956d48f22dc86e618544b073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757452"
---
# <a name="wm_paintclipboard-message"></a>Mensagem do WM \_ PAINTCLIPBOARD

Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência quando a área de transferência contém dados no formato [**\_ OWNERDISPLAY**](standard-clipboard-formats.md) do


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela do Visualizador da área de transferência.

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para um objeto de memória global que contém uma estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) . A estrutura define a parte da área do cliente a ser pintada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Para determinar se toda a área do cliente ou apenas uma parte dela precisa ser redesenhada, o proprietário da área de transferência deve comparar as dimensões das áreas de desenho fornecidas no membro **rcPaint** de [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) para as dimensões fornecidas na mensagem mais recente do [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md) .

O proprietário da área de transferência deve usar a função [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) para bloquear a memória que contém a estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) . Antes de retornar, o proprietário da área de transferência deve desbloquear essa memória usando a função [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .

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

[**SIZECLIPBOARD do WM \_**](wm-sizeclipboard.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> </dl>

 

