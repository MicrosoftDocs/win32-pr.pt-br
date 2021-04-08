---
description: Uma das responsabilidades mais importantes de um provedor de serviços de transporte de dados é o fornecimento de indicações ao cliente quando determinados eventos de rede ocorreram.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Notificação de eventos de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090d3adda7d34c0fe49eb14936bc01bf20878b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827104"
---
# <a name="notification-of-network-events"></a><span data-ttu-id="bb17d-103">Notificação de eventos de rede</span><span class="sxs-lookup"><span data-stu-id="bb17d-103">Notification of Network Events</span></span>

<span data-ttu-id="bb17d-104">Uma das responsabilidades mais importantes de um provedor de serviços de transporte de dados é o fornecimento de indicações ao cliente quando determinados eventos de rede ocorreram.</span><span class="sxs-lookup"><span data-stu-id="bb17d-104">One of the most important responsibilities of a data transport service provider is that of providing indications to the client when certain network events have occurred.</span></span> <span data-ttu-id="bb17d-105">A lista de eventos de rede definidos consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="bb17d-105">The list of defined network events consists of the following:</span></span>

-   <span data-ttu-id="bb17d-106">**FD \_ CONECTAR**– uma conexão a um host remoto ou a uma sessão de multicast foi concluída.</span><span class="sxs-lookup"><span data-stu-id="bb17d-106">**FD\_CONNECT**— A connection to a remote host or to a multicast session has been completed.</span></span>
-   <span data-ttu-id="bb17d-107">**FD \_ ACEITAR**— um host remoto está fazendo uma solicitação de conexão.</span><span class="sxs-lookup"><span data-stu-id="bb17d-107">**FD\_ACCEPT**— A remote host is making a connection request.</span></span>
-   <span data-ttu-id="bb17d-108">**FD \_ LEITURA**— dados de rede recebidos que estão disponíveis para serem lidos.</span><span class="sxs-lookup"><span data-stu-id="bb17d-108">**FD\_READ**— Network data has arrived which is available to be read.</span></span>
-   <span data-ttu-id="bb17d-109">**FD \_ GRAVAÇÃO**— o espaço se tornou disponível nos buffers do provedor de serviços para que os dados adicionais possam ser enviados agora.</span><span class="sxs-lookup"><span data-stu-id="bb17d-109">**FD\_WRITE**— Space has become available in the service provider's buffers so that additional data may now be sent.</span></span>
-   <span data-ttu-id="bb17d-110">**FD \_ OOB**– os dados fora da banda estão disponíveis para leitura.</span><span class="sxs-lookup"><span data-stu-id="bb17d-110">**FD\_OOB**— Out of band data is available to be read.</span></span>
-   <span data-ttu-id="bb17d-111">**FD \_ FECHAR**– o host remoto fechou a conexão.</span><span class="sxs-lookup"><span data-stu-id="bb17d-111">**FD\_CLOSE**— The remote host has closed down the connection.</span></span>
-   <span data-ttu-id="bb17d-112">**FD \_ QOS**— ocorreu uma alteração em níveis de QoS negociados.</span><span class="sxs-lookup"><span data-stu-id="bb17d-112">**FD\_QOS**— A change has occurred in negotiated QoS levels.</span></span>
-   <span data-ttu-id="bb17d-113">**FD \_ \_QoS de grupo**– reservado.</span><span class="sxs-lookup"><span data-stu-id="bb17d-113">**FD\_GROUP\_QOS**— Reserved.</span></span>
-   <span data-ttu-id="bb17d-114">**FD \_ \_ \_ Alteração de interface de roteamento**— uma interface local que deve ser usada para alcançar o destino especificado em sio de **\_ \_ \_ alteração de interface de roteamento de entrada** foi alterada.</span><span class="sxs-lookup"><span data-stu-id="bb17d-114">**FD\_ROUTING\_INTERFACE\_CHANGE**— A local interface that should be used to reach the destination specified in **SIO\_ROUTING\_INTERFACE\_CHANGE IOCTL** has changed.</span></span>
-   <span data-ttu-id="bb17d-115">**FD \_ \_ \_ Alteração da lista de endereços**— a lista de endereços locais aos quais o aplicativo pode ser associado foi alterada.</span><span class="sxs-lookup"><span data-stu-id="bb17d-115">**FD\_ADDRESS\_LIST\_CHANGE**— The list of local addresses to which application can bind has changed.</span></span>

<span data-ttu-id="bb17d-116">O conjunto de eventos de rede enumerado acima é, às vezes, chamado de eventos **FD \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="bb17d-116">The set of network events enumerated above is sometimes referred to as the **FD\_XXX** events.</span></span> <span data-ttu-id="bb17d-117">A indicação da ocorrência de um ou mais desses eventos de rede pode ser fornecida de várias maneiras, dependendo de como o cliente solicita a notificação.</span><span class="sxs-lookup"><span data-stu-id="bb17d-117">Indication of the occurrence of one or more of such network events may be given in a number of ways depending on how the client requests notification.</span></span>

 

 



