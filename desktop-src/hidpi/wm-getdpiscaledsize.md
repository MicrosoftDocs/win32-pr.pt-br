---
title: Mensagem de WM_GETDPISCALEDSIZE (WinUser. h)
description: Essa mensagem informa ao sistema operacional que a janela será dimensionada para dimensões que não sejam o padrão.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- DPI alta de mensagem de WM_GETDPISCALEDSIZE
topic_type:
- apiref
api_name:
- WM_GETDPISCALEDSIZE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95631e51247d7919307f36dd0af10c72621a612
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455193"
---
# <a name="wm_getdpiscaledsize-message"></a>Mensagem do WM \_ GETDPISCALEDSIZE

Essa mensagem informa ao sistema operacional que a janela será dimensionada para dimensões que não sejam o padrão.

Essa mensagem é enviada para janelas de nível superior com um [ \_ \_ contexto de reconhecimento de DPI](dpi-awareness-context.md) de por monitor v2 antes de uma mensagem de [**\_ DPICHANGED do WM**](wm-dpichanged.md) ser enviada e permite que a janela computasse seu tamanho desejado para a alteração de DPI pendente. Como o dimensionamento de DPI linear é o comportamento padrão, isso só é útil em cenários em que a janela deseja dimensionar de forma não linear. Se o aplicativo responder a essa mensagem, o tamanho resultante será o retângulo candidato enviar para o **WM \_ DPICHANGED**.

Use esta mensagem para alterar o tamanho do Rect fornecido com o [**WM \_ DPICHANGED**](wm-dpichanged.md).


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

WPARAM contém um valor de DPI. O tamanho da janela dimensionada que o aplicativo definiria precisa ser computado como se a janela fosse mudar para esse DPI.

</dd> <dt>

*lParam* 
</dt> <dd>

O LPARAM é um ponteiro de entrada/saída para uma estrutura de tamanho. O \_ \_ valor in no lParam é o tamanho pendente da janela após uma movimentação iniciada pelo usuário ou uma chamada para [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Se a janela estiver sendo redimensionada, esse tamanho não será necessariamente o mesmo que o tamanho atual da janela no momento em que essa mensagem for recebida.

O \_ \_ valor out no lParam deve ser gravado pelo aplicativo para especificar o tamanho de janela dimensionado desejado correspondente ao valor de DPI fornecido no wParam.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna um BOOL. Retornar TRUE indica que um novo tamanho foi computado. Retornar FALSE indica que a mensagem não será tratada e o dimensionamento de DPI linear padrão será aplicado à janela.

## <a name="remarks"></a>Comentários

Esta mensagem é enviada somente para janelas de nível superior que têm um contexto de reconhecimento de DPI de por monitor v2.

Esse evento é necessário para facilitar o dimensionamento não linear normal e garante que a posição do Windows permaneça constante em relação ao cursor e ao mover-se para frente e para trás entre monitores.

Não há nenhum tratamento padrão específico dessa mensagem em [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Como para todas as mensagens que ele não manipula explicitamente, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) retornará zero para esta mensagem. Conforme observado acima, esse retorno informa ao sistema para usar o comportamento linear padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



 

