---
description: As funções relacionadas ao tempo retornam o tempo em um dos vários formatos. Você pode usar as funções de tempo para converter entre alguns formatos de tempo para facilitar a comparação e a exibição. A tabela a seguir resume os formatos de hora.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: Sobre o tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a95571637bb480920f82e90011a72f6eba9e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011138"
---
# <a name="about-time"></a>Sobre o tempo

As funções relacionadas ao tempo retornam o tempo em um dos vários formatos. Você pode usar as funções de tempo para converter entre alguns formatos de tempo para facilitar a comparação e a exibição. A tabela a seguir resume os formatos de hora.



| Formatar          | Tipo                                                                     | Descrição                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Sistema          | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | Ano, mês, dia, hora, segundo e milissegundos, obtidos do relógio de hardware interno.                                            |
| Local           | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) ou [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) | Hora do sistema ou horário do arquivo convertido no fuso horário local do sistema.                                                               |
| Arquivo            | [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | O número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601.                                                                       |
| MS-DOS          | **WORD**                                                                 | Uma palavra compactada para a data, outra para a hora.                                                                                   |
| Windows         | **DWORD** ou **ULONGLONG**                                               | O número de milissegundos desde que o sistema foi iniciado pela última vez. Quando recuperada como um valor DWORD, o tempo do Windows é ciclos a cada 49,7 dias. |
| Contagem de interrupção | **ULONGLONG**                                                            | O número de intervalos de 100 a nanossegundos desde que o sistema foi iniciado pela última vez.                                                           |



 

Para mais informações, consulte os seguintes tópicos:

-   [Hora do sistema](system-time.md)
-   [Hora local](local-time.md)
-   [Horas de arquivo](file-times.md)
-   [Data e hora do MS-DOS](ms-dos-date-and-time.md)
-   [Tempo do Windows](windows-time.md)
-   [Tempo de interrupção](interrupt-time.md)

 

 
