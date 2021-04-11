---
description: Tempo do Windows é o número de milissegundos decorridos desde a última vez que o sistema foi iniciado.
ms.assetid: 95c00204-bfdf-4376-9aae-8d8139ba6750
title: Tempo do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af776e2cc5a36993f6be0e0776d5b73fab6622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091438"
---
# <a name="windows-time"></a>Tempo do Windows

*Tempo do Windows* é o número de milissegundos decorridos desde a última vez que o sistema foi iniciado. Esse formato existe principalmente para compatibilidade com versões anteriores do Windows de 16 bits. Para garantir [**que os aplicativos**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) criados para o Windows de 16 bits continuem sendo executados com êxito, a função getor retorna a hora atual do Windows.

Normalmente, você usa a função [**ObterContagemMarcaEscala**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) ou [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) para comparar a hora atual do Windows com o tempo retornado pela função [**getmessagetime**](/windows/win32/api/winuser/nf-winuser-getmessagetime) . **Getmessagetime** retorna a hora do Windows em que a mensagem especificada foi criada. O **ObterContagemMarcaEscala** e o **GetTickCount64** são limitados à resolução do temporizador do sistema, que é de aproximadamente 10 milissegundos a 16 milissegundos. O tempo decorrido recuperado por **ObterContagemMarcaEscala** ou **GetTickCount64** inclui o tempo que o sistema gasta em suspensão ou hibernação.

Se você precisar de um temporizador de resolução mais alto, use a função [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) , um [temporizador de multimídia](/windows/desktop/Multimedia/multimedia-timers)ou um [temporizador de alta resolução](../winmsg/about-timers.md). O tempo decorrido recuperado pela função **QueryUnbiasedInterruptTime** inclui apenas o tempo que o sistema gasta no estado de funcionamento.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP/2000:** A função [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) está disponível a partir do Windows 7 e do windows Server 2008 R2.

Você pode usar o contador de desempenho tempo de funcionamento do sistema para obter o número de segundos decorridos desde que o computador foi iniciado. Esse contador de desempenho pode ser recuperado dos dados de desempenho na chave do registro **HKEY \_ performance \_ Data**. O valor retornado é um valor de 8 bytes. Para obter mais informações, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

 

 
