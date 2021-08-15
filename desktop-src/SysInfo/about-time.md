---
description: As funções relacionadas ao tempo retornam o tempo em um dos vários formatos. Você pode usar as funções de tempo para converter entre alguns formatos de tempo para facilitar a comparação e a exibição. A tabela a seguir resume os formatos de hora.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: Já não era sem tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cb2cd140ada7033ebe7bf672e654dbf7227385509c676176ee8e936ff590ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765027"
---
# <a name="about-time"></a>Já não era sem tempo

As funções relacionadas ao tempo retornam o tempo em um dos vários formatos. Você pode usar as funções de tempo para converter entre alguns formatos de tempo para facilitar a comparação e a exibição. A tabela a seguir resume os formatos de hora.



| Formatar          | Tipo                                                                     | Descrição                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Sistema          | [**Systemtime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | Ano, mês, dia, hora, segundo e milissegundo, retirados do relógio de hardware interno.                                            |
| Local           | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) ou [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) | Uma hora do sistema ou tempo de arquivo convertido no fuso horário local do sistema.                                                               |
| Arquivo            | [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | O número de intervalos de 100 nanossegundos desde 1º de janeiro de 1601.                                                                       |
| MS-DOS          | **WORD**                                                                 | Uma palavra empacotada para a data, outra para a hora.                                                                                   |
| Windows         | **DWORD** ou **ULONGLONG**                                               | O número de milissegundos desde que o sistema foi iniciado pela última vez. Quando recuperado como um valor DWORD, Windows de tempo a cada 49,7 dias. |
| Contagem de interrupções | **Ulonglong**                                                            | O número de intervalos de 100 nanossegundos desde que o sistema foi iniciado pela última vez.                                                           |



 

Para obter mais informações, consulte estes tópicos:

-   [Hora do sistema](system-time.md)
-   [Hora local](local-time.md)
-   [Tempos de arquivo](file-times.md)
-   [Data e hora do MS-DOS](ms-dos-date-and-time.md)
-   [Tempo do Windows](windows-time.md)
-   [Tempo de interrupção](interrupt-time.md)

 

 
