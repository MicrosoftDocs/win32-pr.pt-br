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
# <a name="how-to-process-the-dtn_formatquery-notification"></a><span data-ttu-id="a35d7-103">Como processar a notificação DTN \_ FORMATQUERY</span><span class="sxs-lookup"><span data-stu-id="a35d7-103">How to Process the DTN\_FORMATQUERY Notification</span></span>

<span data-ttu-id="a35d7-104">Este tópico demonstra como processar uma notificação de consulta de formato que é enviada pelo controle do seletor de data e hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="a35d7-104">This topic demonstrates how to process a Format Query notification that is sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a35d7-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="a35d7-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a35d7-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="a35d7-106">Technologies</span></span>

-   [<span data-ttu-id="a35d7-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="a35d7-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a35d7-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a35d7-108">Prerequisites</span></span>

-   <span data-ttu-id="a35d7-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="a35d7-109">C/C++</span></span>
-   <span data-ttu-id="a35d7-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="a35d7-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a35d7-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="a35d7-111">Instructions</span></span>


<span data-ttu-id="a35d7-112">Um controle DTP envia um código de notificação [DTN \_ FORMATQUERY](dtn-formatquery.md) para solicitar informações sobre o tamanho máximo possível de um campo de retorno de chamada dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="a35d7-112">A DTP control sends a [DTN\_FORMATQUERY](dtn-formatquery.md) notification code to request information about the maximum possible size of a callback field within the control.</span></span> <span data-ttu-id="a35d7-113">Seu aplicativo deve lidar com essa mensagem para garantir que todos os campos sejam exibidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="a35d7-113">Your application must handle this message to ensure that all fields are displayed properly.</span></span>

<span data-ttu-id="a35d7-114">O exemplo de código C++ a seguir é uma função definida pelo aplicativo que processa o código de notificação [DTN \_ FORMATQUERY](dtn-formatquery.md) calculando a largura da cadeia de caracteres mais larga possível para um determinado campo de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="a35d7-114">The following C++ code example is an application-defined function that processes the [DTN\_FORMATQUERY](dtn-formatquery.md) notification code by calculating the width of the widest possible string for a given callback field.</span></span>

<span data-ttu-id="a35d7-115">**Aviso de segurança:** O uso incorreto do **lstrcmp** pode comprometer a segurança do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a35d7-115">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="a35d7-116">Por exemplo, antes de chamar **lstrcmp** no exemplo de código a seguir, você deve verificar se as duas cadeias de caracteres são terminadas em nulo.</span><span class="sxs-lookup"><span data-stu-id="a35d7-116">For example, before calling **lstrcmp** in the following code example you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="a35d7-117">Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="a35d7-117">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="a35d7-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a35d7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a35d7-119">Usando controles de seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="a35d7-119">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="a35d7-120">Referência de controle do seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="a35d7-120">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a35d7-121">Seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="a35d7-121">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




