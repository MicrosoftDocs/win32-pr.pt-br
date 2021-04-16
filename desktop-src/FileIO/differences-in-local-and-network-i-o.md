---
description: Diferenças entre e/s local e e/s de rede no Windows.
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: Diferenças em e/s de rede e local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30c4faf6b7358a1c7c134dccdeb12298309c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757561"
---
# <a name="differences-in-local-and-network-io"></a><span data-ttu-id="2f79b-103">Diferenças em e/s de rede e local</span><span class="sxs-lookup"><span data-stu-id="2f79b-103">Differences in Local and Network I/O</span></span>

<span data-ttu-id="2f79b-104">Há algumas diferenças notáveis entre a e/s local e a I/O de rede no Windows:</span><span class="sxs-lookup"><span data-stu-id="2f79b-104">There are some notable differences between local I/O and network I/O on Windows:</span></span>

-   <span data-ttu-id="2f79b-105">O suporte de e/s de rede depende do redirecionador e do protocolo de rede.</span><span class="sxs-lookup"><span data-stu-id="2f79b-105">Network I/O support depends on the redirector and the network protocol.</span></span>
-   <span data-ttu-id="2f79b-106">O desempenho de e/s de rede depende de quantas operações de e/s de rede estão ocorrendo e da velocidade da conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="2f79b-106">Network I/O performance depends on how many network I/O operations are taking place and the speed of the network connection.</span></span> <span data-ttu-id="2f79b-107">Seu aplicativo deve ser capaz de lidar com operações de e/s de rede com servidores que podem ser muito mais rápidos ou mais lentos do que o computador local, bem como alterações transitórias na capacidade da rede.</span><span class="sxs-lookup"><span data-stu-id="2f79b-107">Your application must be able to handle network I/O operations with servers that may be much faster or slower than your local machine, as well as transient changes in network capacity.</span></span> <span data-ttu-id="2f79b-108">Nesses casos, seu aplicativo pode precisar permitir mais tempo para a operação ser concluída.</span><span class="sxs-lookup"><span data-stu-id="2f79b-108">In these cases, your application may need to allow more time for the operation to complete.</span></span>
-   <span data-ttu-id="2f79b-109">As funções usadas para executar a e/s de arquivo local podem se comportar de maneira diferente pela rede.</span><span class="sxs-lookup"><span data-stu-id="2f79b-109">The functions you use to perform local file I/O may behave differently over the network.</span></span> <span data-ttu-id="2f79b-110">Por exemplo, uma operação de e/s de rede que leva muito tempo para ser concluída pode atingir o tempo limite. Em algumas situações, os identificadores de arquivo podem ser deixados abertos indefinidamente por causa disso.</span><span class="sxs-lookup"><span data-stu-id="2f79b-110">For example, a network I/O operation that takes a long time to complete may time out. In some situations, file handles may be left open indefinitely because of this.</span></span> <span data-ttu-id="2f79b-111">Outro exemplo é que as funções podem retornar códigos de erro para que seu aplicativo processe que seja específico para e/s de rede.</span><span class="sxs-lookup"><span data-stu-id="2f79b-111">Another example is that functions may return error codes for your application to process that are specific to network I/O.</span></span>

 

 



