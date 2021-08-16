---
title: Como processar a notificação de DTN_FORMAT
description: Este tópico demonstra como processar uma notificação de formato enviada pelo controle do seletor de data e hora (DTP).
ms.assetid: 7B559846-FE52-4181-B25D-888BE90EB038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070d1234dbd9d09159335539309deec86e2d3e1e05547d933cd18f16b9d7162d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829907"
---
# <a name="how-to-process-the-dtn_format-notification"></a>Como processar a notificação de \_ formato DTN

Este tópico demonstra como processar uma notificação de formato enviada pelo controle do seletor de data e hora (DTP).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções


Um controle DTP envia a notificação de [ \_ formato DTN](dtn-format.md) para solicitar texto que será exibido em um campo de retorno de chamada do controle. Seu aplicativo deve lidar com essa notificação para habilitar o controle DTP a fim de exibir informações de que ele não dá suporte nativo.

O exemplo de código C++ a seguir é uma função definida pelo aplicativo (**Doformat**) que processa códigos de notificação de [ \_ formato DTN](dtn-format.md) fornecendo uma cadeia de caracteres de texto para um campo de retorno de chamada. O aplicativo chama a função definida pelo aplicativo **GetDayNum** para solicitar o número do dia a ser usado na cadeia de caracteres de retorno de chamada.


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



**A função definida pelo aplicativo GetDayNum**

A função de exemplo definida pelo aplicativo **Doformat** chama a seguinte função definida pelo aplicativo **GetDayNum** para solicitar o número do dia com base na data atual. **GetDayNum** retorna um valor **int** que representa o dia atual do ano, de 0 a 366. Essa função chama outra função definida pelo aplicativo, **IsLeapYr**, durante o processamento.


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



**A função definida pelo aplicativo IsLeapYr**

A função definida pelo aplicativo **GetDayNum** chama a função **IsLeapYr** para determinar se o ano atual é um ano bissexto. **IsLeapYr** retornará um valor **bool** que será **true** se for um ano bissexto e **false** caso contrário.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de seletor de data e hora](using-date-and-time-picker.md)
</dt> <dt>

[Referência de controle do seletor de data e hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Seletor de data e hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




