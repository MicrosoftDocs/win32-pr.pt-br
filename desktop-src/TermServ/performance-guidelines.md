---
title: Diretrizes de desempenho
description: Diretrizes para o desenvolvimento de aplicativos que têm bom desempenho em um ambiente de Serviços de Área de Trabalho Remota.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea7ada6ee2b51943d47f39446d0b1bb3b7d6718
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364418"
---
# <a name="performance-guidelines"></a><span data-ttu-id="b77c6-103">Diretrizes de desempenho</span><span class="sxs-lookup"><span data-stu-id="b77c6-103">Performance guidelines</span></span>

<span data-ttu-id="b77c6-104">As seções a seguir fornecem diretrizes para o desenvolvimento de aplicativos que têm bom desempenho em um ambiente de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b77c6-104">The following sections provide guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b77c6-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b77c6-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b77c6-106">Efeitos gráficos</span><span class="sxs-lookup"><span data-stu-id="b77c6-106">Graphic effects</span></span>](graphic-effects.md)
</dt> <dd>

<span data-ttu-id="b77c6-107">Uma lista de recursos que devem ser desabilitados durante a execução como uma sessão remota em um ambiente de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b77c6-107">A list of features that should be disabled when running as a remote session in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="b77c6-108">Diretrizes para tarefas em segundo plano no Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="b77c6-108">Guidelines for background tasks in Remote Desktop Services</span></span>](background-tasks.md)
</dt> <dd>

<span data-ttu-id="b77c6-109">Para maximizar a disponibilidade da CPU para todos os usuários, desabilite as tarefas em segundo plano ao executar em um ambiente de Serviços de Área de Trabalho Remota ou crie tarefas em segundo plano eficientes que não usam muitos recursos.</span><span class="sxs-lookup"><span data-stu-id="b77c6-109">To maximize CPU availability for all users, either disable background tasks when running in a Remote Desktop Services environment or create efficient background tasks that are not resource-intensive.</span></span>

</dd> <dt>

[<span data-ttu-id="b77c6-110">Uso de thread</span><span class="sxs-lookup"><span data-stu-id="b77c6-110">Thread usage</span></span>](thread-usage.md)
</dt> <dd>

<span data-ttu-id="b77c6-111">Você deve ajustar e balancear o uso de threads de aplicativo para um ambiente multiusuário, multiprocessador Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b77c6-111">You should tune and balance application thread usage for a multiuser, multiprocessor Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="b77c6-112">Detectando o ambiente de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="b77c6-112">Detecting the Remote Desktop Services environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="b77c6-113">Para otimizar o desempenho, é uma boa prática para os aplicativos detectarem se eles estão sendo executados em uma sessão de cliente Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b77c6-113">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span>

</dd> </dl>

<span data-ttu-id="b77c6-114">Verifique se há vazamento de memória no aplicativo e resolva quaisquer problemas.</span><span class="sxs-lookup"><span data-stu-id="b77c6-114">Check your application for memory leaks and resolve any problems.</span></span> <span data-ttu-id="b77c6-115">É claro que esse é um bom conselho para qualquer aplicativo, mas em um ambiente de Serviços de Área de Trabalho Remota, um aplicativo pode ser executado várias vezes por vários usuários, aumentando rapidamente o efeito de um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="b77c6-115">Of course this is good advice for any application, but in a Remote Desktop Services environment, an application can be run multiple times by multiple users, thus rapidly magnifying the effect of a memory leak.</span></span>

<span data-ttu-id="b77c6-116">Animações, imagens grandes, áudio e outros serviços com uso intensivo de largura de banda devem ser configuráveis.</span><span class="sxs-lookup"><span data-stu-id="b77c6-116">Animations, large images, audio, and other bandwidth-intensive services must be configurable.</span></span> <span data-ttu-id="b77c6-117">Quando esses serviços não são a função principal, eles podem estar desativados por padrão para sessões remotas, mas habilitados quando uma sessão está em execução localmente ou em uma conexão de largura de banda alta.</span><span class="sxs-lookup"><span data-stu-id="b77c6-117">When these services are not the primary function, they can be off by default for remote sessions, but enabled when a session is running locally or over a high bandwidth connection.</span></span> <span data-ttu-id="b77c6-118">Se a finalidade de um aplicativo é fornecer serviços de alta largura de banda, como streaming de transmissão de vídeo, o serviço não precisa estar desativado por padrão.</span><span class="sxs-lookup"><span data-stu-id="b77c6-118">If the purpose of an application is to provide high bandwidth services, such as streaming video broadcasts, the service does not have to be off by default.</span></span>

 

 




