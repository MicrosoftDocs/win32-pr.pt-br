---
title: Mensagem de WM_SIZECLIPBOARD (WinUser. h)
description: Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência quando a área de transferência contém dados no formato de OWNERDISPLAY do CF \_ e o tamanho do cliente do Visualizador de áreas de transferência é alterado.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- Troca de dados de mensagem WM_SIZECLIPBOARD
topic_type:
- apiref
api_name:
- WM_SIZECLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235de630b20757a571b1917a975d1425bee06cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644740"
---
# <a name="wm_sizeclipboard-message"></a>Mensagem do WM \_ SIZECLIPBOARD

Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência quando a área de transferência contém dados no formato de [**\_ OWNERDISPLAY do CF**](standard-clipboard-formats.md) e o tamanho do cliente do Visualizador de áreas de transferência é alterado.


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela do Visualizador da área de transferência.

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para um objeto de memória global que contém uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) . A estrutura especifica as novas dimensões da área do cliente do Visualizador da área de transferência.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Quando a janela do Visualizador da área de transferência está prestes a ser destruída ou redimensionada, uma mensagem do **WM \_ SIZECLIPBOARD** é enviada com um retângulo nulo (0, 0, 0, 0) como o novo tamanho. Isso permite que o proprietário da área de transferência libere seus recursos de exibição.

O proprietário da área de transferência deve usar a função [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) para bloquear o objeto de memória que contém [**Rect**](/previous-versions//dd162897(v=vs.85)). Antes de retornar, o proprietário da área de transferência deve desbloquear o objeto usando a função [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Conceitua**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> </dl>

 

