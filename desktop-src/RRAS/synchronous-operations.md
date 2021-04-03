---
title: Operações síncronas
description: Quando RasDial é invocado como uma operação síncrona, a função não retorna até que a conexão tenha sido estabelecida ou ocorra um erro.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2463e3112c3faac4d7601023ea73f0182e2d5b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006002"
---
# <a name="synchronous-operations"></a><span data-ttu-id="4e261-103">Operações síncronas</span><span class="sxs-lookup"><span data-stu-id="4e261-103">Synchronous Operations</span></span>

<span data-ttu-id="4e261-104">Quando [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) é invocado como uma operação síncrona, a função não retorna até que a conexão tenha sido estabelecida ou ocorra um erro.</span><span class="sxs-lookup"><span data-stu-id="4e261-104">When [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) is invoked as a synchronous operation, the function does not return until the connection has been established or an error occurs.</span></span> <span data-ttu-id="4e261-105">O modo síncrono fornece uma maneira simples para um cliente RAS estabelecer uma conexão.</span><span class="sxs-lookup"><span data-stu-id="4e261-105">Synchronous mode provides a simple way for a RAS client to establish a connection.</span></span> <span data-ttu-id="4e261-106">O cliente pode simplesmente chamar **RasDial**, aguardar a função retornar e, em seguida, chamar a função [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para determinar se a operação de conexão foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4e261-106">The client can simply call **RasDial**, wait for the function to return, and then call the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to determine whether the connection operation was successful.</span></span> <span data-ttu-id="4e261-107">Depois que a conexão tiver sido estabelecida, o aplicativo cliente poderá ser encerrado sem interromper a conexão.</span><span class="sxs-lookup"><span data-stu-id="4e261-107">Once the connection has been established, the client application can terminate without breaking the connection.</span></span> <span data-ttu-id="4e261-108">Se ocorrer um erro, o aplicativo cliente deverá [desligar a operação de conexão antes de](disconnecting.md) encerrar.</span><span class="sxs-lookup"><span data-stu-id="4e261-108">If an error occurs, the client application must [shut down the connection operation](disconnecting.md) before terminating.</span></span>

<span data-ttu-id="4e261-109">A desvantagem do modo síncrono é que o cliente não recebe notificações de progresso à medida que a operação de conexão continua.</span><span class="sxs-lookup"><span data-stu-id="4e261-109">The disadvantage of synchronous mode is that the client does not receive progress notifications as the connection operation proceeds.</span></span> <span data-ttu-id="4e261-110">Como solução alternativa para essa falta de notificações de progresso, um cliente de modo síncrono pode usar um thread separado que chama [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para sondar e exibir o estado atual.</span><span class="sxs-lookup"><span data-stu-id="4e261-110">As a workaround for this lack of progress notifications, a synchronous mode client can use a separate thread that calls [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) to poll for and display the current state.</span></span> <span data-ttu-id="4e261-111">No entanto, para clientes RAS que desejam receber informações de progresso, a técnica preferida é invocar [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="4e261-111">However, for RAS clients that want to receive progress information, the preferred technique is to invoke [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) asynchronously.</span></span>

 

 




