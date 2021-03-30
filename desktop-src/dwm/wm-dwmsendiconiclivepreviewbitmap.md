---
title: Mensagem de WM_DWMSENDICONICLIVEPREVIEWBITMAP (dwmapi. h)
description: Instrui uma janela para fornecer um bitmap estático a ser usado como uma visualização dinâmica (também conhecida como visualização de inspeção) dessa janela.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- Mensagem de WM_DWMSENDICONICLIVEPREVIEWBITMAP Gerenciador de Janelas da Área de Trabalho
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
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455241"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a>Mensagem do WM \_ DWMSENDICONICLIVEPREVIEWBITMAP

Instrui uma janela para fornecer um bitmap estático a ser usado como uma *Visualização dinâmica* (também conhecida como *visualização de inspeção*) dessa janela.

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

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Uma *Visualização dinâmica* (também conhecida como *visualização do Peek*) de uma janela é exibida quando um usuário move o ponteiro do mouse sobre a miniatura da janela na barra de tarefas ou dá o foco da miniatura na janela Alt + Tab. Essa exibição é uma visualização de tamanho completo da janela e pode ser um instantâneo ao vivo ou uma representação icônico.

Gerenciador de Janelas da Área de Trabalho (DWM) enviará essa mensagem para uma janela se todas as seguintes situações forem verdadeiras:

-   A visualização dinâmica foi invocada na janela.
-   O atributo [**DWMWA \_ tem \_ icônico \_ bitmap**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) está definido na janela.
-   Uma representação icônico é a única que existe para essa janela.

A janela que recebe essa mensagem deve responder gerando um bitmap de escala completa. Em seguida, a janela chama a função [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) para definir a visualização dinâmica. Se a janela não definir um bitmap em um determinado período de tempo, o DWM usará sua própria representação icônico padrão para a janela.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra uma resposta à **mensagem \_ DWMSENDICONICLIVEPREVIEWBITMAP do WM** . O exemplo chama a função [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) com um identificador para um bitmap personalizado independente de dispositivo a ser usado como a representação da janela.


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



Para obter o código completo, consulte a amostra [personalizar uma miniatura do icônico e um bitmap de visualização dinâmica](dwm-sample-customizethumbnail.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>Dwmapi. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**DWMSENDICONICTHUMBNAIL do WM \_**](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





