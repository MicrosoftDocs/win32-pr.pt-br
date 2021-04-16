---
description: Usando NSPStartup e NSPCleanup para inicialização e limpeza do provedor de namespace no SPI do Windows Sockets (Winsock).
ms.assetid: c9f55845-190d-440f-8b27-1be9585137e2
title: Inicialização e limpeza do provedor de namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fedd7b40d79e755262df581c92e1fe3bdbfb06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501684"
---
# <a name="namespace-provider-initialization-and-cleanup"></a><span data-ttu-id="050a9-103">Inicialização e limpeza do provedor de namespace</span><span class="sxs-lookup"><span data-stu-id="050a9-103">Namespace Provider Initialization and Cleanup</span></span>

-   [<span data-ttu-id="050a9-104">**NSPStartup**</span><span class="sxs-lookup"><span data-stu-id="050a9-104">**NSPStartup**</span></span>](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)
-   [<span data-ttu-id="050a9-105">**NSPCleanup**</span><span class="sxs-lookup"><span data-stu-id="050a9-105">**NSPCleanup**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)

<span data-ttu-id="050a9-106">Como é o caso do SPI de transporte, um provedor de namespace é inicializado com uma chamada para [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) e termina com uma chamada final para [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup).</span><span class="sxs-lookup"><span data-stu-id="050a9-106">As is the case for the transport SPI, a namespace provider is initialized with a call to [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) and is terminated with a final call to [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup).</span></span> <span data-ttu-id="050a9-107">As chamadas para a função de inicialização podem ser aninhadas, mas serão correspondidas pelas chamadas correspondentes à função de limpeza.</span><span class="sxs-lookup"><span data-stu-id="050a9-107">Calls to the startup function may be nested, but will be matched by corresponding calls to the cleanup function.</span></span> <span data-ttu-id="050a9-108">Um provedor deve empregar a contagem de referência para determinar quando ocorreu a chamada final para **NSPCleanup** .</span><span class="sxs-lookup"><span data-stu-id="050a9-108">A provider should employ reference counting to determine when the final call to **NSPCleanup** has occurred.</span></span>

 

 



