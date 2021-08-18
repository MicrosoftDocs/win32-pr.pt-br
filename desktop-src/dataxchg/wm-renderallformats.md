---
title: WM_RENDERALLFORMATS mensagem (Winuser.h)
description: Enviado para o proprietário da área de transferência antes de ser destruído, se o proprietário da área de transferência tiver atrasado a renderização de um ou mais formatos de área de transferência.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- WM_RENDERALLFORMATS de dados de Exchange
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77dae9b44cb379ed62c99c601d308fdec500440a9ebad0ffeaffad16ec780dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636056"
---
# <a name="wm_renderallformats-message"></a>Mensagem WM \_ RENDERALLFORMATS

Enviado para o proprietário da área de transferência antes de ser destruído, se o proprietário da área de transferência tiver atrasado a renderização de um ou mais formatos de área de transferência. Para que o conteúdo da área de transferência permaneça disponível para outros aplicativos, o proprietário da área de transferência deve renderizar dados em todos os formatos que é capaz de gerar e colocar os dados na área de transferência chamando a [**função SetClipboardData.**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="remarks"></a>Comentários

Ao responder a uma mensagem **WM \_ RENDERALLFORMATS,** o aplicativo deve chamar a função [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) e verificar se ela ainda é o proprietário da área de transferência chamando a [**função GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) antes de chamar [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).

O aplicativo precisa verificar se ele ainda é o proprietário da área de transferência depois de abrir a área de transferência porque depois de receber a mensagem **WM \_ RENDERALLFORMATS,** mas antes de abrir a área de transferência, outro aplicativo pode ter aberto e assumido a propriedade da área de transferência e os dados do aplicativo não devem ser substituídos.

Na maioria dos casos, o aplicativo não deve chamar a função [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) antes de chamar [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), pois isso apagará os formatos da área de transferência que o aplicativo já renderizado.

Quando o aplicativo retorna, o sistema remove os formatos não remetentes da lista de formatos de área de transferência disponíveis. Para obter informações sobre renderização atrasada, consulte [Renderização atrasada.](clipboard-operations.md#delayed-rendering)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Emptyclipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[**Openclipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[**Setclipboarddata**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**WM \_ RENDERFORMAT**](wm-renderformat.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> </dl>

 

