---
title: Práticas recomendadas de upload
description: Highloads pode causar várias condições de tempo limite do servidor, o que pode, por sua vez, aumentar a carga quando o cliente tentar novamente.
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95a229ff1e229c41fde8fd377e347f91cf43010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004965"
---
# <a name="upload-best-practices"></a><span data-ttu-id="8276c-103">Práticas recomendadas de upload</span><span class="sxs-lookup"><span data-stu-id="8276c-103">Upload Best Practices</span></span>

<span data-ttu-id="8276c-104">Highloads pode causar várias condições de tempo limite do servidor, o que pode, por sua vez, aumentar a carga quando o cliente tentar novamente.</span><span class="sxs-lookup"><span data-stu-id="8276c-104">Highloads may cause various server timeout conditions, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="8276c-105">Além disso, um grande número de conexões pendentes consumirá mais recursos do servidor e tornará a situação pior.</span><span class="sxs-lookup"><span data-stu-id="8276c-105">Also, a large number of outstanding connections will consume more server resources and make the situation worse.</span></span> <span data-ttu-id="8276c-106">Além disso, se o aplicativo de back-end não for gravado para lidar com condições de alta carga, ele poderá falhar ou se comportar.</span><span class="sxs-lookup"><span data-stu-id="8276c-106">On top of that, if backend app is not written to handle high load conditions, it may crash or mal-behave.</span></span> <span data-ttu-id="8276c-107">O aplicativo deve executar as etapas a seguir para limitar a carga no back-end.</span><span class="sxs-lookup"><span data-stu-id="8276c-107">The app shall perform the following steps to limit the load on the backend.</span></span>

<span data-ttu-id="8276c-108">Se o aplicativo do servidor não for gravado para lidar com grandes volumes, podem ocorrer condições de tempo limite, o que pode, por sua vez, aumentar a carga quando o cliente tentar novamente.</span><span class="sxs-lookup"><span data-stu-id="8276c-108">If the server application is not written to handle high volumes, timeout conditions may occur, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="8276c-109">Além disso, um grande número de conexões pendentes consumirá mais recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="8276c-109">Also, a large number of outstanding connections will consume more server resources.</span></span>

<span data-ttu-id="8276c-110">Ao testar o aplicativo de servidor, teste com a carga mais alta possível.</span><span class="sxs-lookup"><span data-stu-id="8276c-110">When testing your server application, test with highest load possible.</span></span> <span data-ttu-id="8276c-111">Você deve usar vários computadores cliente, cada um com vários trabalhos simultâneos do BITS de primeiro plano e medir a taxa de transferência máxima no back-end.</span><span class="sxs-lookup"><span data-stu-id="8276c-111">You should use multiple client machines, each with several concurrent, foreground BITS jobs, and measure the maximum throughput at the backend.</span></span> <span data-ttu-id="8276c-112">Se não for possível medir a taxa de transferência, você precisará estimar a taxa de transferência.</span><span class="sxs-lookup"><span data-stu-id="8276c-112">If you cannot measure the throughput, you will have to estimate the throughput.</span></span>

<span data-ttu-id="8276c-113">O aplicativo de servidor deve residir em uma URL diferente da URL de carregamento (consulte a propriedade do IIS do BITS, **BITSServerNotificationURL**).</span><span class="sxs-lookup"><span data-stu-id="8276c-113">The server application should reside on a different URL from the upload URL (see the BITS IIS property, **BITSServerNotificationURL**).</span></span>

<span data-ttu-id="8276c-114">É uma boa prática limitar a carga no servidor de aplicativos com base nos valores de taxa de transferência comprovados.</span><span class="sxs-lookup"><span data-stu-id="8276c-114">It is good practice to limit the load on the application server based on proven throughput values.</span></span> <span data-ttu-id="8276c-115">Você deve usar as propriedades do IIS, **MaxBandwidth** e **MaxConnections**, para limitar a carga no servidor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8276c-115">You should use the IIS properties, **MaxBandwidth** and **MaxConnections**, to limit the load on the application server.</span></span>

 

 




