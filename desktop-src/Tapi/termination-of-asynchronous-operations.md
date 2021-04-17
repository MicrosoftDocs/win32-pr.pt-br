---
description: Quando um aplicativo chama a função lineClose com uma ou mais operações assíncronas pendentes, a TAPI pode instruir o provedor de serviços a encerrar operações assíncronas associadas a uma chamada.
ms.assetid: b26ce074-76dc-4a50-8c17-d3412c336d59
title: Término de operações assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ed2acb0f442e5f4f07427f0e224d7a288087d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754727"
---
# <a name="termination-of-asynchronous-operations"></a>Término de operações assíncronas

Quando um aplicativo chama a função [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) com uma ou mais operações assíncronas pendentes, a TAPI pode instruir o provedor de serviços a encerrar operações assíncronas associadas a uma chamada, dependendo se o aplicativo é o único proprietário da chamada e tem o único identificador para a chamada.

Se o aplicativo for o único proprietário de uma chamada, a TAPI chamará [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) ou [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) (dependendo do provedor) para cada chamada. O provedor de serviços deve verificar se há operações assíncronas pendentes associadas à chamada que está sendo descartada. Se houver uma operação pendente, o provedor de serviços deverá executar a ação apropriada, possivelmente encerrando a operação em andamento.

Se o aplicativo tiver o único identificador para uma chamada (ou seja, não houver outros proprietários ou monitores), a TAPI chamará a função [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) . O provedor de serviços deve considerar essa chamada para ser a indicação absoluta de que operações assíncronas pendentes devem ser abandonadas. O provedor de serviços deve garantir uma conclusão ordenada da chamada e deve chamar a função de retorno de chamada de [**\_ conclusão assíncrona**](/windows/win32/api/tspi/nc-tspi-async_completion) para todas as operações assíncronas pendentes, especificando o \_ valor de erro LINEERR OPERATIONFAILED. Se a TAPI chamou anteriormente a função [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) ou [**TSPI \_ LineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) , ela chamará **TSPI \_ lineCloseCall** imediatamente depois que o provedor de serviços retornar da outra chamada; ele não aguardará a operação assíncrona associada à função TSPI **\_ lineDrop** para ser concluída.

Se o aplicativo não for o único proprietário da chamada, a TAPI não chamará [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) ou [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop). Se o aplicativo não tiver o único identificador para a chamada, a TAPI não chamará a função [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) . Se o aplicativo não for o proprietário exclusivo nem o único possessor de um identificador para a chamada, a TAPI não enviará nenhuma notificação para o provedor de serviços e, portanto, quaisquer operações assíncronas pendentes permanecerão intactas. Isso significa que esses aplicativos não podem finalizar operações assíncronas que começaram usando a função [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) . No entanto, como cada operação assíncrona exige que o aplicativo de invocação seja um proprietário da chamada, a probabilidade de um aplicativo não ser capaz de encerrar as operações assíncronas é muito rara. Se isso ocorrer, os outros proprietários das chamadas deverão assumir a responsabilidade pela disposição da (s) chamada (ões).

Se a TAPI chamar [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) ou [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop), o provedor de serviços deverá, eventualmente, enviar uma \_ mensagem de LINECALLSTATE ociosa para a chamada associada (a menos que [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) seja chamado primeiro) para que os monitores na chamada possam ser limpos. Quando o último monitor chamou a função [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall) , a TAPI chama a **função \_ lineCloseCall TSPI** ; todas as operações pendentes devem ser concluídas ou terminadas e a [**\_ conclusão assíncrona**](/windows/win32/api/tspi/nc-tspi-async_completion) chamada, conforme descrito anteriormente.

 

 
