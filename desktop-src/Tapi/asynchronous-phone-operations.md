---
description: Há nove operações assíncronas relacionadas aos telefones.
ms.assetid: b255bdde-1677-401f-b02d-4850e0e98dc4
title: Operações de telefone assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4a70a1d980c4f0d42d5160ee020531b538f488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829129"
---
# <a name="asynchronous-phone-operations"></a>Operações de telefone assíncrono

Há nove operações assíncronas relacionadas aos telefones. Eles são iniciados pelas [**funções \_ TSPI phoneDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_phonedevspecific), [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo), [**TSPI \_ phoneSetData**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdata), [**TSPI \_ phoneSetDisplay**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdisplay), [**TSPI \_ phoneSetGain**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetgain), [**TSPI \_ phoneSetHookSwitch**](/windows/win32/api/tspi/nf-tspi-tspi_phonesethookswitch), [**TSPI \_ phoneSetLamp**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetlamp), [**TSPI \_ phoneSetRing**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetring)e [**TSPI \_ phoneSetVolume**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetvolume) . Se um aplicativo chamar a função TAPI [**phoneClose**](/windows/win32/api/tapi/nf-tapi-phoneclose) e tiver o único identificador para o telefone, a TAPI chamará a função [**\_ phoneClose do TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_phoneclose) para direcionar o provedor de serviços para encerrar as operações assíncronas e chamar a função de retorno de chamada [*\_ proc de conclusão*](/windows/win32/api/tspi/nc-tspi-async_completion) conforme apropriado. Se o aplicativo não tiver o único identificador para o telefone, o provedor de serviços não receberá nenhuma notificação da solicitação e todas as operações assíncronas pendentes permanecerão ativas.

 

 
