---
title: Como processar a notificação de DTN_FORMATQUERY
description: Este tópico demonstra como processar uma notificação de consulta de formato que é enviada pelo controle do seletor de data e hora (DTP).
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e8de1e1a80d04f9a7f9e9d0cfcda198118e67c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917815"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a>Como processar a notificação DTN \_ FORMATQUERY

Este tópico demonstra como processar uma notificação de consulta de formato que é enviada pelo controle do seletor de data e hora (DTP).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Um controle DTP envia um código de notificação [DTN \_ FORMATQUERY](dtn-formatquery.md) para solicitar informações sobre o tamanho máximo possível de um campo de retorno de chamada dentro do controle. Seu aplicativo deve lidar com essa mensagem para garantir que todos os campos sejam exibidos corretamente.

O exemplo de código C++ a seguir é uma função definida pelo aplicativo que processa o código de notificação [DTN \_ FORMATQUERY](dtn-formatquery.md) calculando a largura da cadeia de caracteres mais larga possível para um determinado campo de retorno de chamada.

**Aviso de segurança:** O uso incorreto do **lstrcmp** pode comprometer a segurança do seu aplicativo. Por exemplo, antes de chamar **lstrcmp** no exemplo de código a seguir, você deve verificar se as duas cadeias de caracteres são terminadas em nulo. Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.



```C++
//  DoFormatQuery processes DTN_FORMATQUERY messages to ensure that the
//  DTP control displays callback fields properly.
//

void WINAPI DoFormatQuery(
 HWND hwndDP, 
 LPNMDATETIMEFORMATQUERY lpDTFQuery)
{
    HDC hdc;
    HFONT hFont, hOrigFont;

    //  Prepare the device context for GetTextExtentPoint32 call.
    hdc = GetDC(hwndDP);

    hFont = (HFONT) SendMessage(hwndDP, WM_GETFONT, 0L, 0L); 

    if(!hFont)
        hFont = (HFONT)GetStockObject(DEFAULT_GUI_FONT);

    hOrigFont = (HFONT) SelectObject(hdc, hFont);

    // Check to see if this is the callback segment desired. If so,
    // use the longest text segment to determine the maximum 
    // width of the callback field, and then place the information into 
    // the NMDATETIMEFORMATQUERY structure.
    if(!lstrcmp(L"XX",lpDTFQuery->pszFormat))
        GetTextExtentPoint32 (hdc,
                          L"366",  // widest date string
                          3,
                          &lpDTFQuery->szMax);

    // Reset the font in the device context; then release the context.
    SelectObject(hdc,hOrigFont);
    ReleaseDC(hwndDP, hdc);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de seletor de data e hora](using-date-and-time-picker.md)
</dt> <dt>

[Referência de controle do seletor de data e hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Seletor de data e hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




