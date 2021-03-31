---
description: O sistema operacional Microsoft Windows oferece suporte a uma variedade de dispositivos de hardware e protocolos de tempo de rede usando a arquitetura de provedor de tempo.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Provedor de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c844e2c4d0d49e87e978a47621338b167c4f5a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829520"
---
# <a name="time-provider"></a><span data-ttu-id="d2d39-103">Provedor de tempo</span><span class="sxs-lookup"><span data-stu-id="d2d39-103">Time Provider</span></span>

<span data-ttu-id="d2d39-104">O sistema operacional Microsoft Windows oferece suporte a uma variedade de dispositivos de hardware e protocolos de tempo de rede usando a arquitetura de *provedor de tempo* .</span><span class="sxs-lookup"><span data-stu-id="d2d39-104">The Microsoft Windows operating system provides support for a variety of hardware devices and network time protocols using the *time provider* architecture.</span></span> <span data-ttu-id="d2d39-105">Provedores de tempo de entrada recuperam carimbos de data/hora precisos do hardware ou da rede, e provedores de tempo de saída fornecem carimbos de data/hora para outros clientes na rede.</span><span class="sxs-lookup"><span data-stu-id="d2d39-105">Input time providers retrieve accurate time stamps from hardware or the network, and output time providers provide time stamps to other clients on the network.</span></span>

<span data-ttu-id="d2d39-106">Os provedores de tempo são gerenciados pelo *Gerenciador de provedores de tempo*.</span><span class="sxs-lookup"><span data-stu-id="d2d39-106">Time providers are managed by the *time provider manager*.</span></span> <span data-ttu-id="d2d39-107">Ele é responsável por carregar, iniciar e parar provedores de tempo conforme orientado pelo Gerenciador de controle de serviços.</span><span class="sxs-lookup"><span data-stu-id="d2d39-107">It is responsible for loading, starting, and stopping time providers as directed by the service control manager.</span></span> <span data-ttu-id="d2d39-108">Essa interface torna mais fácil escrever um provedor de tempo do que escrever um serviço completo.</span><span class="sxs-lookup"><span data-stu-id="d2d39-108">This interface makes writing a time provider easier than writing a full service.</span></span>

-   [<span data-ttu-id="d2d39-109">Criando um provedor de tempo</span><span class="sxs-lookup"><span data-stu-id="d2d39-109">Creating a Time Provider</span></span>](creating-a-time-provider.md)
-   [<span data-ttu-id="d2d39-110">Registrando um provedor de tempo</span><span class="sxs-lookup"><span data-stu-id="d2d39-110">Registering a Time Provider</span></span>](registering-a-time-provider.md)
-   [<span data-ttu-id="d2d39-111">Provedor de tempo de exemplo</span><span class="sxs-lookup"><span data-stu-id="d2d39-111">Sample Time Provider</span></span>](sample-time-provider.md)

## <a name="related-topics"></a><span data-ttu-id="d2d39-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d2d39-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2d39-113">Serviço de Tempo do Windows</span><span class="sxs-lookup"><span data-stu-id="d2d39-113">Windows Time Service</span></span>](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



