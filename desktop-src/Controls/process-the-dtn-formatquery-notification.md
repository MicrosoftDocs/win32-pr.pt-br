---
title: Como processar a notificação DTN_FORMATQUERY dados
description: Este tópico demonstra como processar uma notificação formatar consulta enviada pelo controle DTP (selador de data e hora).
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c148332c36711e68b7c3b773fdb47acef202c5fd2a67f5620319f06c7fbc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696936"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a>Como processar a notificação DTN \_ FORMATQUERY

Este tópico demonstra como processar uma notificação formatar consulta enviada pelo controle DTP (selador de data e hora).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções


Um controle DTP envia um código de notificação [DTN \_ FORMATQUERY](dtn-formatquery.md) para solicitar informações sobre o tamanho máximo possível de um campo de retorno de chamada dentro do controle . Seu aplicativo deve lidar com essa mensagem para garantir que todos os campos sejam exibidos corretamente.

O exemplo de código C++ a seguir é uma função definida pelo aplicativo que processa o código de notificação [ \_ FORMATQUERY DTN](dtn-formatquery.md) calculando a largura da cadeia de caracteres mais ampla possível para um determinado campo de retorno de chamada.

**Aviso de segurança:** Usar **lstrcmp** incorretamente pode comprometer a segurança do seu aplicativo. Por exemplo, antes de chamar **lstrcmp** no exemplo de código a seguir, você deve garantir que as duas cadeias de caracteres sejam terminadas em nulo. Você deve revisar [considerações de segurança: Controles Windows Microsoft antes](sec-comctls.md) de continuar.



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

[Usando controles de selador de data e hora](using-date-and-time-picker.md)
</dt> <dt>

[Referência de controle do selador de data e hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selador de data e hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




