---
description: As funções de tempo incluídas no tempo de execução em C usam o \_ tipo de tempo t para representar o número de segundos decorridos desde a meia-noite, 1º de janeiro de 1970. O exemplo a seguir converte um \_ valor t de tempo em uma hora de arquivo, usando a função Int32x32To64.
ms.assetid: f626c0b2-a5a1-475d-9a24-64e7b0407278
title: Convertendo um valor de time_t em uma hora de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee866efaed716fb12d2501337236afdb7cf641b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749435"
---
# <a name="converting-a-time_t-value-to-a-file-time"></a>Convertendo um \_ valor t de tempo em uma hora de arquivo

As funções de tempo incluídas no tempo de execução em C usam o \_ tipo de tempo t para representar o número de segundos decorridos desde a meia-noite, 1º de janeiro de 1970. O exemplo a seguir converte um \_ valor t de tempo em uma hora de arquivo, usando a função [**Int32x32To64**](/windows/desktop/api/winnt/nf-winnt-int32x32to64) .


```C++
#include <windows.h>
#include <time.h>

void TimetToFileTime( time_t t, LPFILETIME pft )
{
    LONGLONG ll = Int32x32To64(t, 10000000) + 116444736000000000;
    pft->dwLowDateTime = (DWORD) ll;
    pft->dwHighDateTime = ll >>32;
}
```



Depois de obter uma hora do arquivo, você pode converter esse valor em hora do sistema usando a função [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) .

 

 
