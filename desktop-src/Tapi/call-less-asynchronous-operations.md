---
description: Há cinco operações assíncronas que não estão relacionadas a nenhuma chamada específica.
ms.assetid: d7107834-07e4-40ed-91ea-2e6127597c13
title: Operações assíncronas menos chamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f4a246ab4a9022ce01d9707a7c5dc5cdc6e9e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296788"
---
# <a name="call-less-asynchronous-operations"></a>Operações assíncronas menos chamadas

Há cinco operações assíncronas que não estão relacionadas a nenhuma chamada específica. As funções TAPI 2. x [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward), [**lineSetTerminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal)e [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) iniciam essas operações. Se um aplicativo iniciar uma dessas operações assíncronas e chamar [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose), o provedor de serviços poderá não receber nenhuma indicação de que o aplicativo abandonou a função. Isso pode ocorrer se o aplicativo não fosse o único aplicativo para que a linha fosse aberta. Se o aplicativo chamar **lineClose** com uma dessas operações pendentes, e for o único aplicativo com um identificador para a linha, a TAPI chamará a função [**\_ lineClose TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) e o provedor de serviços deverá encerrar a operação assíncrona, chamando a função de retorno de chamada [*\_ proc de conclusão*](/windows/win32/api/tspi/nc-tspi-async_completion) para cada operação pendente com o \_ valor de erro LINEERR OPERATIONFAILED.

 

 
