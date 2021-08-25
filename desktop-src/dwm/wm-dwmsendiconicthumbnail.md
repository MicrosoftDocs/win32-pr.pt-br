---
title: WM_DWMSENDICONICTHUMBNAIL mensagem (Dwmapi.h)
description: Instrui uma janela a fornecer um bitmap estático a ser usado como uma representação em miniatura dessa janela.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- WM_DWMSENDICONICTHUMBNAIL mensagem Gerenciador de Janelas da Área de Trabalho
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
ms.openlocfilehash: 3263f34cd59ba68ee895e5d5c77e297144cbadd6c8d8bbaa49ca6272248c2024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842646"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a>Mensagem WM \_ DWMSENDICONICTHUMBNAIL

Instrui uma janela a fornecer um bitmap estático a ser usado como uma representação em miniatura dessa janela.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado.

</dd> <dt>

*lParam* 
</dt> <dd>

A [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) desse valor é a coordenada x máxima da miniatura. A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é a coordenada y máxima. Se uma miniatura tiver uma dimensão que exceda um ou ambos os valores, o DWM não aceitará a miniatura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="remarks"></a>Comentários

A DWM envia essa mensagem para uma janela se todas as seguintes situações são verdadeiras:

-   A DWM está exibindo uma representação de descrente da janela.
-   O [**atributo BITMAP DWMWA \_ HAS VOCÊ TEM O \_ \_ BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) é definido na janela.
-   A janela não definiu um bitmap armazenado em cache.
-   Há espaço no cache para outro bitmap.

A janela que recebe essa mensagem deve responder gerando um bitmap que não é maior que o tamanho solicitado nos parâmetros de mensagem. Em seguida, a janela chama [**a função DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) para substituir a miniatura padrão. Se a janela não fornecer um bitmap em um determinado período de tempo, a DWM usará sua própria representação padrão de desapresentação para a janela.

A janela deve pertencer ao processo de chamada.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como responder à mensagem **WM \_ DWMSENDICONICTHUMBNAIL.** O exemplo chama [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), com um handle para um bitmap personalizado e independente do dispositivo a ser usado como representação do Windows.


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



Para ver o exemplo completo, consulte o exemplo Personalizar uma miniatura de miniatura e [um bitmap](dwm-sample-customizethumbnail.md) de visualização ao vivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Dwmapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[**WM \_ DWMSENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

