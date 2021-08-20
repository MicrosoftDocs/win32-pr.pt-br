---
description: Enviado quando o usuário descarta um arquivo na janela de um aplicativo que se registrou como um destinatário de arquivos descartados.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: WM_DROPFILES mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c36043997b4d462b5d453952f690cc8569218c398796b6a42b10709053b0d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118046477"
---
# <a name="wm_dropfiles-message"></a>Mensagem WM \_ DROPFILES

Enviado quando o usuário descarta um arquivo na janela de um aplicativo que se registrou como um destinatário de arquivos descartados.


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

Um handle para uma estrutura interna que descreve os arquivos descartados. Passe esse handle [**DragFinish,**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish) [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)ou [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) para recuperar informações sobre os arquivos descartados.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deverá retornar zero se ele processa essa mensagem.

## <a name="remarks"></a>Comentários

O alça HDROP é declarado em Shellapi.h. Você deve incluir esse header em seu build para usar **WM \_ DROPFILES**. Para mais discussão sobre como usar o tipo "arrastar e soltar" para transferir dados do Shell, consulte Transferindo dados do Shell usando o tipo "arrastar e soltar" ou ["Área de Transferência".](dragdrop.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**Dragacceptfiles**](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
