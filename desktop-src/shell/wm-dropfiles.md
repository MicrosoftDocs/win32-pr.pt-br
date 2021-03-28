---
description: Enviado quando o usuário remove um arquivo na janela de um aplicativo que se registrou como um destinatário dos arquivos soltos.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: Mensagem de WM_DROPFILES (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967879"
---
# <a name="wm_dropfiles-message"></a>Mensagem do WM \_ DropFiles

Enviado quando o usuário remove um arquivo na janela de um aplicativo que se registrou como um destinatário dos arquivos soltos.


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDrop* 
</dt> <dd>

Um identificador para uma estrutura interna que descreve os arquivos descartados. Passe esse identificador [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)ou [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) para recuperar informações sobre os arquivos ignorados.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

O identificador HDROP é declarado em shellapi. h. Você deve incluir esse cabeçalho em sua compilação para usar o **WM \_ DropFiles**. Para obter mais informações sobre como usar o recurso de arrastar e soltar para transferir dados do Shell, consulte [transferindo dados do shell usando o recurso de arrastar e soltar ou a área de transferência](dragdrop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**DragAcceptFiles**](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
