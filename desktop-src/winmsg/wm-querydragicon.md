---
description: Enviado para uma janela minimizada (icônico).
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: Mensagem de WM_QUERYDRAGICON (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20aac405a247f89a31c49f60a4e421fa171465d399dcb61a436936de5c646362
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055986"
---
# <a name="wm_querydragicon-message"></a>Mensagem do WM \_ QUERYDRAGICON

Enviado para uma janela minimizada (icônico). A janela está prestes a ser arrastada pelo usuário, mas não tem um ícone definido para sua classe. Um aplicativo pode retornar um identificador para um ícone ou cursor. O sistema exibe esse cursor ou ícone enquanto o usuário arrasta o ícone.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_QUERYDRAGICON                0x0037
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Um aplicativo deve retornar um identificador para um cursor ou um ícone que o sistema deverá exibir enquanto o usuário arrasta o ícone. O cursor ou o ícone deve ser compatível com a resolução do driver de vídeo. Se o aplicativo retornar **nulo**, o sistema exibirá o cursor padrão.

## <a name="remarks"></a>Comentários

Quando o usuário arrasta o ícone de uma janela sem um ícone de classe, o sistema substitui o ícone por um cursor padrão. Se o aplicativo exigir que um cursor diferente seja exibido durante a arrastar, ele deverá retornar um identificador para o cursor ou ícone compatível com a resolução do driver de vídeo. Se um aplicativo retornar um identificador para um cursor ou ícone de cor, o sistema converterá o cursor ou o ícone em preto e branco. O aplicativo pode chamar a função [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) ou [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) para carregar um cursor ou um ícone dos recursos em seu arquivo executável (.exe) e recuperar esse identificador.

Se um procedimento da caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado em um **bool** e retornar o valor diretamente. O valor de **\_ MSGRESULT DWL** definido pela função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
