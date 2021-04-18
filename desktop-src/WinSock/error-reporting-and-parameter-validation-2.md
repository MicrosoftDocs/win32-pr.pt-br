---
description: O esquema para o relatório de erros difere entre as interfaces SPI e API.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Relatório de erros e validação de parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291fa2ed950d916be39b1a696f5fe8ad6f07280c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789344"
---
# <a name="error-reporting-and-parameter-validation"></a><span data-ttu-id="3d28a-103">Relatório de erros e validação de parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d28a-103">Error Reporting and Parameter Validation</span></span>

<span data-ttu-id="3d28a-104">O esquema para o relatório de erros difere entre as interfaces SPI e API.</span><span class="sxs-lookup"><span data-stu-id="3d28a-104">The scheme for error reporting differs between the SPI and API interfaces.</span></span> <span data-ttu-id="3d28a-105">Os provedores de serviço do Windows Sockets relatam erros junto com a função retornando, em oposição à abordagem baseada em thread utilizada na API.</span><span class="sxs-lookup"><span data-stu-id="3d28a-105">Windows Sockets service providers report errors along with the function returning, as opposed to the per-thread based approach utilized in the API.</span></span> <span data-ttu-id="3d28a-106">O \_32.dll Ws2 usa o código de erro por função do provedor de serviços para atualizar o valor de erro por thread obtido por meio da função de API [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) .</span><span class="sxs-lookup"><span data-stu-id="3d28a-106">The Ws2\_32.dll uses the service provider's per-function error code to update the per-thread error value that is obtained through the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) API function.</span></span> <span data-ttu-id="3d28a-107">Os provedores de serviço ainda são necessários, no entanto, para manter o erro baseado em soquete que pode ser recuperado por meio da opção de soquete de erro de SO \_ .</span><span class="sxs-lookup"><span data-stu-id="3d28a-107">Service providers are still required, however, to maintain the per-socket based error which can be retrieved through the SO\_ERROR socket option.</span></span>

<span data-ttu-id="3d28a-108">O \_32.dll Ws2 executa a validação de parâmetro somente em chamadas de função que são implementadas inteiramente em si.</span><span class="sxs-lookup"><span data-stu-id="3d28a-108">The Ws2\_32.dll performs parameter validation only on function calls that are implemented entirely within itself.</span></span> <span data-ttu-id="3d28a-109">Os provedores de serviço são responsáveis por executar todas as suas próprias validações de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3d28a-109">Service providers are responsible for performing all of their own parameter validation.</span></span>

 

 



