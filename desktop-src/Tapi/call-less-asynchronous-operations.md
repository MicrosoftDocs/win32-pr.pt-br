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
# <a name="call-less-asynchronous-operations"></a><span data-ttu-id="b60ff-103">Operações assíncronas menos chamadas</span><span class="sxs-lookup"><span data-stu-id="b60ff-103">Call-less Asynchronous Operations</span></span>

<span data-ttu-id="b60ff-104">Há cinco operações assíncronas que não estão relacionadas a nenhuma chamada específica.</span><span class="sxs-lookup"><span data-stu-id="b60ff-104">There are five asynchronous operations that are not related to any particular call.</span></span> <span data-ttu-id="b60ff-105">As funções TAPI 2. x [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward), [**lineSetTerminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal)e [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) iniciam essas operações.</span><span class="sxs-lookup"><span data-stu-id="b60ff-105">The TAPI 2.x [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward), [**lineSetTerminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal), and [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) functions initiate these operations.</span></span> <span data-ttu-id="b60ff-106">Se um aplicativo iniciar uma dessas operações assíncronas e chamar [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose), o provedor de serviços poderá não receber nenhuma indicação de que o aplicativo abandonou a função.</span><span class="sxs-lookup"><span data-stu-id="b60ff-106">If an application initiates one of these asynchronous operations and calls [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose), the service provider may receive no indication that the application has abandoned the function.</span></span> <span data-ttu-id="b60ff-107">Isso pode ocorrer se o aplicativo não fosse o único aplicativo para que a linha fosse aberta.</span><span class="sxs-lookup"><span data-stu-id="b60ff-107">This can occur if the application was not the only application to have the line open.</span></span> <span data-ttu-id="b60ff-108">Se o aplicativo chamar **lineClose** com uma dessas operações pendentes, e for o único aplicativo com um identificador para a linha, a TAPI chamará a função [**\_ lineClose TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) e o provedor de serviços deverá encerrar a operação assíncrona, chamando a função de retorno de chamada [*\_ proc de conclusão*](/windows/win32/api/tspi/nc-tspi-async_completion) para cada operação pendente com o \_ valor de erro LINEERR OPERATIONFAILED.</span><span class="sxs-lookup"><span data-stu-id="b60ff-108">If the application calls **lineClose** with one of these operations pending, and it is the only application with a handle to the line, TAPI calls the [**TSPI\_lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) function and the service provider should terminate the asynchronous operation, calling the [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) callback function for each such outstanding operation with the LINEERR\_OPERATIONFAILED error value.</span></span>

 

 
