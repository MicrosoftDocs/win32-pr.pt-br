---
description: Este tópico define os identificadores de calendário (tipo de dados CALID) que são usados para especificar calendários diferentes.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Identificadores de calendário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5f9f21aeff1143c4f981e3bfae20214f1b86e86307f7f32b103a19ef99b9803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083026"
---
# <a name="calendar-identifiers"></a>Identificadores de calendário

Este tópico define os identificadores de calendário (tipo de dados CALID) que são usados para especificar calendários diferentes. Seus aplicativos podem usar esses identificadores ao usar as seguintes funções NLS e funções de retorno de chamada, que têm parâmetros que usam o tipo de dados CALID:

-   [**ConvertSystemTimeToCalDateTime**](convertsystemtimetocaldatetime.md)
-   [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   [**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))
-   [**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))
-   [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [**GetCalendarSupportedDateRange**](getcalendarsupporteddaterange.md)
-   [**IsCalendarLeapYear**](iscalendarleapyear.md)
-   [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

Os valores a seguir são definidos. Todos os outros valores são reservados. Esses valores não podem ser combinados entre si.



Identificador de calendário

Significado

1

CAL \_ gregoriano

Gregoriano (localizado)

2

CAL \_ gregoriano \_ dos EUA

Gregoriano (sempre, cadeias de caracteres em inglês)

3

CAL do \_ Japão

Era do imperador japonês

4

CAL \_ Taiwan

Calendário de Taiwan

5

Coreia do CAL \_

Era coreano Tangun

6

HIJRI do CAL \_

Hijri (lunar árabe)

7

CAL \_ tailandês

Tailandês

8

Hebraico da CAL \_

Hebraico (lunar)

9

CAL \_ gregoriano \_ me \_ francês

Gregorian Middle East French

10

CAL \_ gregoriano \_ árabe

Gregorian Arabic

11

CAL \_ gregoriano \_ XLIT \_ Inglês

Gregoriano de transliteração em inglês

12

CAL \_ gregoriano \_ XLIT \_ francês

Gregoriano de transliteração francesa

23

\_UMALQURA Cal

**Windows Vista e posterior:** Calendário do um Al Qura (lunar árabe)



 

> [!Note]  
> A lacuna na numeração entre os identificadores CAL \_ gregoriano \_ XLIT \_ francês e Cal \_ UMALQURA é intencional. O designador para CAL \_ UMALQURA é 23, e não 13.

 

Além disso, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) e [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) permitem o uso do valor enumerar \_ todos os \_ calendários para solicitar uma enumeração de todos os calendários aplicáveis.

Valor

Significado

0xffffffff

ENUMERAr \_ todos os \_ calendários

Todos os calendários aplicáveis para a localidade especificada



 

 

 
