---
title: Detectando e evitando a latência de replicação
description: A latência de replicação é um fato da vida em um sistema distribuído menos rígido.
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271b4d84689068824a6e46095a5ed93462f49e2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634975"
---
# <a name="detecting-and-avoiding-replication-latency"></a><span data-ttu-id="23638-103">Detectando e evitando a latência de replicação</span><span class="sxs-lookup"><span data-stu-id="23638-103">Detecting and Avoiding Replication Latency</span></span>

<span data-ttu-id="23638-104">A latência de replicação é um fato da vida em um sistema distribuído menos rígido.</span><span class="sxs-lookup"><span data-stu-id="23638-104">Replication latency is a fact of life in a loosely coupled distributed system.</span></span> <span data-ttu-id="23638-105">Os aplicativos devem acomodar isso.</span><span class="sxs-lookup"><span data-stu-id="23638-105">Applications must accommodate this.</span></span> <span data-ttu-id="23638-106">A melhor maneira de acomodar a latência de replicação é projetar aplicativos para minimizar os efeitos.</span><span class="sxs-lookup"><span data-stu-id="23638-106">The best way to accommodate replication latency is to design applications to minimize the effects.</span></span> <span data-ttu-id="23638-107">O aplicativo habilitado para diretório ideal:</span><span class="sxs-lookup"><span data-stu-id="23638-107">The ideal directory-enabled application:</span></span>

-   <span data-ttu-id="23638-108">Não é sensível à distorção de versão.</span><span class="sxs-lookup"><span data-stu-id="23638-108">Is insensitive to version skew.</span></span>
-   <span data-ttu-id="23638-109">Não depende de relações entre vários objetos.</span><span class="sxs-lookup"><span data-stu-id="23638-109">Does not depend on relationships among multiple objects.</span></span>
-   <span data-ttu-id="23638-110">Não tem requisitos de consistência dentro ou entre objetos.</span><span class="sxs-lookup"><span data-stu-id="23638-110">Has no intra- or inter-object consistency requirements.</span></span>

<span data-ttu-id="23638-111">Os aplicativos e serviços que se ajustam a esse perfil não precisam se preocupar com a latência de replicação.</span><span class="sxs-lookup"><span data-stu-id="23638-111">Applications and services that fit this profile need not be concerned with replication latency.</span></span> <span data-ttu-id="23638-112">Outros aplicativos devem ser projetados com a latência de replicação em mente.</span><span class="sxs-lookup"><span data-stu-id="23638-112">Other applications must be designed with replication latency in mind.</span></span> <span data-ttu-id="23638-113">A chave para o sucesso na criação de um aplicativo desse tipo é a percepção do processo de replicação.</span><span class="sxs-lookup"><span data-stu-id="23638-113">The key to success in designing such an application is awareness of the replication process.</span></span> <span data-ttu-id="23638-114">Etapas executadas em tempo de design para reduzir dependências entre objetos e minimizar as janelas de atualização parciais pagarão grandes dividendos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="23638-114">Steps taken at design time to reduce inter-object dependencies and minimize partial update windows will pay large dividends at run time.</span></span> <span data-ttu-id="23638-115">As abordagens para lidar com a latência de replicação são divididas em duas classes — evitam estratégias que reduzem o impacto da latência e das estratégias de detecção que permitem que um aplicativo detecte Estados induzidos por latência.</span><span class="sxs-lookup"><span data-stu-id="23638-115">Approaches to dealing with replication latency are divided into two classes—avoidance strategies that reduce the impact of latency and detection strategies that allow an application to detect latency-induced states.</span></span>

 

 




