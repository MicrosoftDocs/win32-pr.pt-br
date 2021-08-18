---
title: WM_DWMSENDICONICLIVEPREVIEWBITMAP mensagem (Dwmapi.h)
description: Instrui uma janela a fornecer um bitmap estático a ser usado como uma visualização ao vivo (também conhecida como uma visualização de Espiar) dessa janela.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP mensagem Gerenciador de Janelas da Área de Trabalho
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7742b70afad62a42378e50a06a6e40e503bee72309f5f233f9cf8bf62cf41d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985237"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a>Mensagem WM \_ DWMSENDICONICLIVEPREVIEWBITMAP

Instrui uma janela a fornecer um bitmap estático *a* ser usado como uma visualização ao vivo (também conhecida como uma *visualização de* Espiar ) dessa janela.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="remarks"></a>Comentários

Uma *visualização* ao vivo (também conhecida como visualização de Espiar *)* de uma janela é exibida quando um usuário move o ponteiro do mouse sobre a miniatura da janela na barra de tarefas ou fornece o foco da miniatura na janela ALT+TAB. Essa exibição é uma versão prévia de tamanho completo da janela e pode ser um instantâneo ao vivo ou uma representação de descarada.

Gerenciador de Janelas da Área de Trabalho (DWM) envia essa mensagem para uma janela se todas as seguintes situações são verdadeiras:

-   A versão prévia ao vivo foi invocada na janela.
-   O [**atributo BITMAP DWMWA \_ HAS VOCÊ TEM O \_ \_ BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) é definido na janela.
-   Uma representação de reação é a única que existe para essa janela.

A janela que recebe essa mensagem deve responder gerando um bitmap de escala completa. Em seguida, a janela chama a [**função DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) para definir a visualização ao vivo. Se a janela não definir um bitmap em um determinado período de tempo, a DWM usará sua própria representação padrão de desapresentação para a janela.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra uma resposta à mensagem **WM \_ DWMSENDICONICLIVEPREVIEWBITMAP.** O exemplo chama a [**função DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) com um handle para um bitmap personalizado e independente do dispositivo a ser usado como representação da janela.


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



Para ver o código completo, consulte o exemplo Personalizar [uma miniatura de miniatura e um bitmap](dwm-sample-customizethumbnail.md) de visualização ao vivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Dwmapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WM \_ DWMSENDICONICTHUMBNAIL**](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





