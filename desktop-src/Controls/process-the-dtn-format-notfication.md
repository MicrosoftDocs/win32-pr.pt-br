---
title: Como processar a notificação de DTN_FORMAT
description: Este tópico demonstra como processar uma notificação de formato enviada pelo controle do seletor de data e hora (DTP).
ms.assetid: 7B559846-FE52-4181-B25D-888BE90EB038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25271ff33ee6978ebcb0bc474492f884ed7faaa2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103824068"
---
# <a name="how-to-process-the-dtn_format-notification"></a><span data-ttu-id="d09b4-103">Como processar a notificação de \_ formato DTN</span><span class="sxs-lookup"><span data-stu-id="d09b4-103">How to Process the DTN\_FORMAT Notification</span></span>

<span data-ttu-id="d09b4-104">Este tópico demonstra como processar uma notificação de formato enviada pelo controle do seletor de data e hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="d09b4-104">This topic demonstrates how to process a format notification sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d09b4-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="d09b4-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d09b4-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="d09b4-106">Technologies</span></span>

-   [<span data-ttu-id="d09b4-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="d09b4-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d09b4-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="d09b4-108">Prerequisites</span></span>

-   <span data-ttu-id="d09b4-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="d09b4-109">C/C++</span></span>
-   <span data-ttu-id="d09b4-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="d09b4-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d09b4-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="d09b4-111">Instructions</span></span>


<span data-ttu-id="d09b4-112">Um controle DTP envia a notificação de [ \_ formato DTN](dtn-format.md) para solicitar texto que será exibido em um campo de retorno de chamada do controle.</span><span class="sxs-lookup"><span data-stu-id="d09b4-112">A DTP control sends the [DTN\_FORMAT](dtn-format.md) notification to request text that will be displayed in a callback field of the control.</span></span> <span data-ttu-id="d09b4-113">Seu aplicativo deve lidar com essa notificação para habilitar o controle DTP a fim de exibir informações de que ele não dá suporte nativo.</span><span class="sxs-lookup"><span data-stu-id="d09b4-113">Your application must handle this notification to enable the DTP control to display information that it does not natively support.</span></span>

<span data-ttu-id="d09b4-114">O exemplo de código C++ a seguir é uma função definida pelo aplicativo (**Doformat**) que processa códigos de notificação de [ \_ formato DTN](dtn-format.md) fornecendo uma cadeia de caracteres de texto para um campo de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="d09b4-114">The following C++ code example is an application-defined function (**DoFormat**) that processes [DTN\_FORMAT](dtn-format.md) notification codes by providing a text string for a callback field.</span></span> <span data-ttu-id="d09b4-115">O aplicativo chama a função definida pelo aplicativo **GetDayNum** para solicitar o número do dia a ser usado na cadeia de caracteres de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="d09b4-115">The application calls the **GetDayNum** application-defined function to request the day number to be used in the callback string.</span></span>


```C++
//  DoFormat processes DTN_FORMAT to provide the text for a callback
//  field in a DTP control. In this example, the callback field
//  contains a value for the day of year. The function calls the 
//  application-defined function GetDayNum (below) to retrieve
//  the correct value. StringCchPrintf truncates the formatted string if
//  the entire string will not fit into the destination buffer. 

void WINAPI DoFormat(HWND hwndDP, LPNMDATETIMEFORMAT lpDTFormat)
{
HRESULT hr = StringCchPrintf(lpDTFormat->szDisplay,
                sizeof(lpDTFormat->szDisplay)/sizeof(lpDTFormat->szDisplay[0]),
                L"%d",GetDayNum(&lpDTFormat->st));
if(SUCCEEDED(hr))
 {
   // Insert code here to handle the case when the function succeeds.      
 }
else
 {
   // Insert code here to handle the case when the function fails or the string 
   // is truncated.
 }
}
```



<span data-ttu-id="d09b4-116">**A função definida pelo aplicativo GetDayNum**</span><span class="sxs-lookup"><span data-stu-id="d09b4-116">**The GetDayNum application-defined function**</span></span>

<span data-ttu-id="d09b4-117">A função de exemplo definida pelo aplicativo **Doformat** chama a seguinte função definida pelo aplicativo **GetDayNum** para solicitar o número do dia com base na data atual.</span><span class="sxs-lookup"><span data-stu-id="d09b4-117">The application-defined sample function **DoFormat** calls the following **GetDayNum** application-defined function to request the day number based on the current date.</span></span> <span data-ttu-id="d09b4-118">**GetDayNum** retorna um valor **int** que representa o dia atual do ano, de 0 a 366.</span><span class="sxs-lookup"><span data-stu-id="d09b4-118">**GetDayNum** returns an **INT** value that represents the current day of the year, from 0 to 366.</span></span> <span data-ttu-id="d09b4-119">Essa função chama outra função definida pelo aplicativo, **IsLeapYr**, durante o processamento.</span><span class="sxs-lookup"><span data-stu-id="d09b4-119">This function calls another application-defined function, **IsLeapYr**, during processing.</span></span>


```C++
//  GetDayNum is an application-defined function that retrieves the 
//  correct day of year value based on the contents of a given 
//  SYSTEMTIME structure. This function calls the IsLeapYr function to 
//  check if the current year is a leap year. The function returns an 
//  integer value that represents the day of year.

int WINAPI GetDayNum(SYSTEMTIME *st)
{
    int iNormYearAccum[ ] = {31,59,90,120,151,181,
                            212,243,273,304,334,365};
    int iLeapYearAccum[ ] = {31,60,91,121,152,182,
                            213,244,274,305,335,366};
    int iDayNum;

    if(IsLeapYr(st->wYear))
        iDayNum=iLeapYearAccum[st->wMonth-2]+st->wDay;
    else
        iDayNum=iNormYearAccum[st->wMonth-2]+st->wDay;

    return (iDayNum);
}        
```



<span data-ttu-id="d09b4-120">**A função definida pelo aplicativo IsLeapYr**</span><span class="sxs-lookup"><span data-stu-id="d09b4-120">**The IsLeapYr application-defined function**</span></span>

<span data-ttu-id="d09b4-121">A função definida pelo aplicativo **GetDayNum** chama a função **IsLeapYr** para determinar se o ano atual é um ano bissexto.</span><span class="sxs-lookup"><span data-stu-id="d09b4-121">The application-defined function **GetDayNum** calls the **IsLeapYr** function to determine whether the current year is a leap year.</span></span> <span data-ttu-id="d09b4-122">**IsLeapYr** retornará um valor **bool** que será **true** se for um ano bissexto e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="d09b4-122">**IsLeapYr** returns a **BOOL** value that is **TRUE** if it is a leap year and **FALSE** otherwise.</span></span>


```C++
//  IsLeapYr determines if a given year value is a leap year. The
//  function returns TRUE if the current year is a leap year, and 
//  FALSE otherwise.

BOOL WINAPI IsLeapYr(int iYear)
{
    BOOL fLeapYr = FALSE;

    // If the year is evenly divisible by 4 and not by 100, but is 
    // divisible by 400, it is a leap year.
    if ((!(iYear % 4))             // each even fourth year
            && ((iYear % 100)      // not each even 100 year
            || (!(iYear % 400))))  // but each even 400 year
        fLeapYr = TRUE;

    return (fLeapYr);
}        
```



## <a name="related-topics"></a><span data-ttu-id="d09b4-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d09b4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d09b4-124">Usando controles de seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="d09b4-124">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="d09b4-125">Referência de controle do seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="d09b4-125">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d09b4-126">Seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="d09b4-126">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




