---
title: Mensagem de WM_DWMSENDICONICTHUMBNAIL (dwmapi. h)
description: Instrui uma janela para fornecer um bitmap estático a ser usado como uma representação em miniatura dessa janela.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- Mensagem de WM_DWMSENDICONICTHUMBNAIL Gerenciador de Janelas da Área de Trabalho
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded5b734278973afe35f5ed3d9fbb5b0aec9242b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455829"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a>Mensagem do WM \_ DWMSENDICONICTHUMBNAIL

Instrui uma janela para fornecer um bitmap estático a ser usado como uma representação em miniatura dessa janela.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) desse valor é a coordenada x máxima da miniatura. O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é a coordenada y máxima. Se uma miniatura tiver uma dimensão que exceda um ou ambos os valores, o DWM não aceitará a miniatura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

O DWM enviará essa mensagem para uma janela se todas as seguintes situações forem verdadeiras:

-   O DWM está exibindo uma representação icônico da janela.
-   O atributo [**DWMWA \_ tem \_ icônico \_ bitmap**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) está definido na janela.
-   A janela não definiu um bitmap armazenado em cache.
-   Há espaço no cache para outro bitmap.

A janela que recebe essa mensagem deve responder gerando um bitmap que não seja maior do que o tamanho solicitado nos parâmetros da mensagem. Em seguida, a janela chama a função [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) para substituir a miniatura padrão. Se a janela não fornecer um bitmap em um determinado período de tempo, o DWM usará sua própria representação icônico padrão para a janela.

A janela deve pertencer ao processo de chamada.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como responder à mensagem do **WM \_ DWMSENDICONICTHUMBNAIL** . O exemplo chama [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), com um identificador para um bitmap personalizado independente de dispositivo a ser usado como a representação do Windows.


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



Para obter o exemplo completo, consulte a amostra [personalizar uma miniatura do icônico e um bitmap de visualização dinâmica](dwm-sample-customizethumbnail.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>Dwmapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[**DWMSENDICONICLIVEPREVIEWBITMAP do WM \_**](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

