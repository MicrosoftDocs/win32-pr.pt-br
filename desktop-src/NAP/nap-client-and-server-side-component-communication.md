---
title: Comunicação do cliente NAP e do componente do lado do servidor
description: Comunicação do cliente NAP e do componente do lado do servidor
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07597ac80a1e02c4f8528b3c99050aefb5963988
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364348"
---
# <a name="nap-client-and-server-side-component-communication"></a><span data-ttu-id="9c7d2-103">Comunicação do cliente NAP e do componente do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="9c7d2-103">NAP Client and Server-side Component Communication</span></span>

> [!Note]  
> <span data-ttu-id="9c7d2-104">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="9c7d2-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9c7d2-105">O componente agente NAP pode se comunicar com o componente de servidor de administração NAP por meio do seguinte processo:</span><span class="sxs-lookup"><span data-stu-id="9c7d2-105">The NAP Agent component can communicate with the NAP Administration Server component through the following process:</span></span>

1.  <span data-ttu-id="9c7d2-106">O agente NAP passa o SSoH para o NAP EC.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-106">The NAP Agent passes the SSoH to the NAP EC.</span></span>
2.  <span data-ttu-id="9c7d2-107">O NAP EC passa o SSoH para o NAP ES.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-107">The NAP EC passes the SSoH to the NAP ES.</span></span>
3.  <span data-ttu-id="9c7d2-108">O NAP ES passa o SSoH para o serviço de servidor de diretivas de rede (NPS).</span><span class="sxs-lookup"><span data-stu-id="9c7d2-108">The NAP ES passes the SSoH to the Network Policy Server (NPS) service.</span></span>
4.  <span data-ttu-id="9c7d2-109">O serviço NPS passa o SSoH para o servidor de administração NAP.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-109">The NPS service passes the SSoH to the NAP Administration Server.</span></span>

<span data-ttu-id="9c7d2-110">Um SHA pode se comunicar com seu SHV correspondente por meio do seguinte processo:</span><span class="sxs-lookup"><span data-stu-id="9c7d2-110">An SHA can communicate with its corresponding SHV through the following process:</span></span>

1.  <span data-ttu-id="9c7d2-111">O SHA passa seu SoH para o agente NAP.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-111">The SHA passes its SoH to the NAP Agent.</span></span>
2.  <span data-ttu-id="9c7d2-112">O agente NAP passa a SoH, contida no SSoH, para a NAP EC.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-112">The NAP Agent passes the SoH, contained within the SSoH, to the NAP EC.</span></span>
3.  <span data-ttu-id="9c7d2-113">O NAP EC passa a SoH para a NAP ES.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-113">The NAP EC passes the SoH to the NAP ES.</span></span>
4.  <span data-ttu-id="9c7d2-114">O NAP ES passa a SoH para o servidor de administração de NAP.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-114">The NAP ES passes the SoH to the NAP Administration Server.</span></span>
5.  <span data-ttu-id="9c7d2-115">O servidor de administração NAP passa a SoH para o SHV.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-115">The NAP Administration Server passes the SoH to the SHV.</span></span>

<span data-ttu-id="9c7d2-116">A figura a seguir mostra o processo de comunicação de componentes de cliente NAP para componentes do lado do servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-116">The figure below shows the communication process from NAP client components to NAP server-side components.</span></span>

![arquitetura de cliente para comunicação de servidor na plataforma NAP](images/nap-client-to-server-comm.png)

<span data-ttu-id="9c7d2-118">O servidor de administração NAP pode se comunicar com o agente NAP por meio do seguinte processo:</span><span class="sxs-lookup"><span data-stu-id="9c7d2-118">The NAP Administration Server can communicate with the NAP Agent through the following process:</span></span>

1.  <span data-ttu-id="9c7d2-119">O servidor de administração NAP passa o SoHRs para o serviço NPS.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-119">The NAP Administration Server passes the SoHRs to the NPS service.</span></span>
2.  <span data-ttu-id="9c7d2-120">O serviço NPS passa o SSoHR para o NAP ES.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-120">The NPS service passes the SSoHR to the NAP ES.</span></span>
3.  <span data-ttu-id="9c7d2-121">O NAP ES passa o SSoHR para o NAP EC.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-121">The NAP ES passes the SSoHR to the NAP EC.</span></span>
4.  <span data-ttu-id="9c7d2-122">O NAP EC passa o SSoHR para o agente NAP.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-122">The NAP EC passes the SSoHR to the NAP Agent.</span></span>

<span data-ttu-id="9c7d2-123">O SHV pode se comunicar com seu SHA correspondente por meio do seguinte processo:</span><span class="sxs-lookup"><span data-stu-id="9c7d2-123">The SHV can communicate with its corresponding SHA through the following process:</span></span>

1.  <span data-ttu-id="9c7d2-124">O SHV passa seu SoHR para o servidor de administração de NAP.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-124">The SHV passes its SoHR to the NAP Administration Server.</span></span>
2.  <span data-ttu-id="9c7d2-125">O servidor de administração NAP passa o SoHR para o serviço NPS.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-125">The NAP Administration Server passes the SoHR to the NPS service.</span></span>
3.  <span data-ttu-id="9c7d2-126">O serviço NPS passa o SoHR, contido dentro do SSoHR, para a NAP ES.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-126">The NPS service passes the SoHR, contained within the SSoHR, to the NAP ES.</span></span>
4.  <span data-ttu-id="9c7d2-127">O NAP ES passa o SoHR para o NAP EC.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-127">The NAP ES passes the SoHR to the NAP EC.</span></span>
5.  <span data-ttu-id="9c7d2-128">O NAP EC passa o SoHR para o agente NAP.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-128">The NAP EC passes the SoHR to the NAP Agent.</span></span>
6.  <span data-ttu-id="9c7d2-129">O agente NAP passa o SoHR para o SHA.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-129">The NAP Agent passes the SoHR to the SHA.</span></span>

<span data-ttu-id="9c7d2-130">A figura a seguir mostra o processo de comunicação de componentes do lado do servidor NAP para componentes de cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="9c7d2-130">The figure below shows the communication process from NAP server-side components to NAP client components.</span></span>

![arquitetura de servidor para comunicação de cliente na plataforma NAP](images/nap-server-to-client-comm.png)

 

 




