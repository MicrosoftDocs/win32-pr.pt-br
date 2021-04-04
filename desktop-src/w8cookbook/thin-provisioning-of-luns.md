---
title: Provisionamento dinâmico de unidades lógicas
description: Provisionamento dinâmico de unidades lógicas
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- LBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4abb6fa3cec112737b23e3cd658a48984cb0fcd1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104008503"
---
# <a name="thin-provisioning-of-logical-units"></a><span data-ttu-id="14397-105">Provisionamento dinâmico de unidades lógicas</span><span class="sxs-lookup"><span data-stu-id="14397-105">Thin provisioning of logical units</span></span>

## <a name="platforms"></a><span data-ttu-id="14397-106">Plataformas</span><span class="sxs-lookup"><span data-stu-id="14397-106">Platforms</span></span>

<span data-ttu-id="14397-107">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="14397-107">**Clients** – Windows 8</span></span>  
<span data-ttu-id="14397-108">**Servidores** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14397-108">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="14397-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="14397-109">Description</span></span>

<span data-ttu-id="14397-110">O provisionamento dinâmico do Windows é uma interface para a solução de provisionamento de armazenamento de ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="14397-110">Windows Thin Provisioning is an interface to the end-to-end storage provisioning solution.</span></span> <span data-ttu-id="14397-111">Para fornecer um serviço de provisionamento de armazenamento altamente disponível, escalonável e amigável requer implementações robustas do host do servidor para o dispositivo de destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="14397-111">To deliver a highly available, scalable and user-friendly storage provisioning service requires robust implementations from the server host to the storage target device.</span></span> <span data-ttu-id="14397-112">O recurso de provisionamento dinâmico do Windows fornece uma exibição síncrona dos dispositivos de armazenamento de provisionamento dinâmico para o administrador do sistema, o gerente de ti e o administrador de armazenamento por meio da identificação de LUN (unidade lógica), notificação de limite, tratamento de esgotamento de recursos e recuperação de estado LBA (Logical Block Addressing).</span><span class="sxs-lookup"><span data-stu-id="14397-112">The Windows thin provisioning feature provides a synchronous view of the thin provisioning storage devices to the system administrator, IT manager, and storage administrator through the thinly provisioned logical unit’s (LUN’s) identification, threshold notification, resource exhaustion handling, space reclamation, and logical block addressing (LBA) state retrieval.</span></span> <span data-ttu-id="14397-113">O recurso de provisionamento dinâmico do Windows apresenta um modelo de serviço de provisionamento de armazenamento robusto que pode ser aplicado a sistemas de armazenamento de cliente-servidor, armazenamento de virtualização e serviços de armazenamento em nuvem.</span><span class="sxs-lookup"><span data-stu-id="14397-113">The Windows thin provisioning feature presents a robust storage provisioning service model that can be applied to client-server storage systems, virtualization storage, and cloud storage services.</span></span> <span data-ttu-id="14397-114">A Microsoft garantirá a alta qualidade do recurso de provisionamento dinâmico ao impor os requisitos do kit de certificação de hardware do provisionamento dinâmico do Windows para produtos de matriz de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="14397-114">Microsoft will ensure the high quality of the thin provisioning feature by enforcing the Windows Thin Provisioning Hardware Certification Kit requirements for storage array products.</span></span>

<span data-ttu-id="14397-115">A solução de armazenamento de provisionamento dinâmico do Windows:</span><span class="sxs-lookup"><span data-stu-id="14397-115">The Windows Thin Provisioning storage solution:</span></span>

-   <span data-ttu-id="14397-116">Permite que os administradores de armazenamento criem um LUN maior com menos recursos de disco físico</span><span class="sxs-lookup"><span data-stu-id="14397-116">Allows storage administrators to create a larger LUN with fewer physical disk resources</span></span>
-   <span data-ttu-id="14397-117">Adiciona ou remove o recurso de disco físico sem interromper o serviço de provisionamento de armazenamento</span><span class="sxs-lookup"><span data-stu-id="14397-117">Adds or removes physical disk resource without interrupting the storage provisioning service</span></span>
-   <span data-ttu-id="14397-118">Alerta os usuários sobre o uso do volume de armazenamento por meio da configuração de limite</span><span class="sxs-lookup"><span data-stu-id="14397-118">Alerts users to the storage volume usage through the threshold setting</span></span>
-   <span data-ttu-id="14397-119">Dá suporte ao provisionamento de armazenamento por meio da configuração do pool de armazenamento compartilhado</span><span class="sxs-lookup"><span data-stu-id="14397-119">Supports storage provisioning through the shared storage pool configuration</span></span>
-   <span data-ttu-id="14397-120">Aumenta ou diminui o tamanho do pool de armazenamento de acordo com a demanda e o uso do espaço de armazenamento</span><span class="sxs-lookup"><span data-stu-id="14397-120">Increases or decreases the size of the storage pool according to the demand and usage of storage space</span></span>

<span data-ttu-id="14397-121">Resumo dos recursos de provisionamento fino do Windows:</span><span class="sxs-lookup"><span data-stu-id="14397-121">Summary of the Windows Thin Provisioning features:</span></span>

-   <span data-ttu-id="14397-122">Identificação de LUN de provisionamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="14397-122">Thin Provisioning LUN identification</span></span>
-   <span data-ttu-id="14397-123">Identificadores para notificação de limite, esgotamento de recursos temporários e esgotamento de recursos permanentes</span><span class="sxs-lookup"><span data-stu-id="14397-123">Handles for threshold notification, temporary resource exhaustion, and permanent resource exhaustion</span></span>
-   <span data-ttu-id="14397-124">Reclamação do espaço de armazenamento</span><span class="sxs-lookup"><span data-stu-id="14397-124">Storage space reclamation</span></span>
-   <span data-ttu-id="14397-125">Mapeamento de consultas de estado de blocos lógicos</span><span class="sxs-lookup"><span data-stu-id="14397-125">Mapping state queries of logical blocks</span></span>

## <a name="manifestation"></a><span data-ttu-id="14397-126">Manifestação</span><span class="sxs-lookup"><span data-stu-id="14397-126">Manifestation</span></span>

<span data-ttu-id="14397-127">Sem a compreensão correta dos identificadores do Windows para o LUN de provisionamento dinâmico, o aplicativo pode falhar com comportamento inesperado ou devido a uma causa desconhecida.</span><span class="sxs-lookup"><span data-stu-id="14397-127">Without the proper understanding of the Windows handles for thin provisioning LUN, the app could fail with unexpected behavior or for an unknown cause.</span></span>

## <a name="using-thin-provisioning-luns"></a><span data-ttu-id="14397-128">Usando LUNs de provisionamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="14397-128">Using thin provisioning LUNs</span></span>

<span data-ttu-id="14397-129">Para usar LUNs com provisionamento dinâmico no Windows 8 ou no Windows Server 2012, os administradores de sistema e armazenamento devem estar cientes dessas questões:</span><span class="sxs-lookup"><span data-stu-id="14397-129">To use thinly provisioned LUNs in Windows 8 or Windows Server 2012, system and storage administrators should be aware of these matters:</span></span>

-   <span data-ttu-id="14397-130">Identificação de LUN de provisionamento dinâmico; os administradores do sistema ou os usuários finais podem usar a desfragmentação e o utilitário de otimização de armazenamento para identificar o tipo de mídia do dispositivo de armazenamento</span><span class="sxs-lookup"><span data-stu-id="14397-130">Thin provisioning LUN identification; system administrators or end users can use Defrag and the Storage Optimizer utility to identify the media type of the storage device</span></span>
-   <span data-ttu-id="14397-131">Quando um evento de esgotamento de recursos permanente ou limite for atingido, o Windows registrará um evento do sistema para alertar o administrador do sistema</span><span class="sxs-lookup"><span data-stu-id="14397-131">When a threshold or a permanent resource exhaustion event is hit, Windows will log a system event to alert the system administrator</span></span>
-   <span data-ttu-id="14397-132">A reclamação do espaço de armazenamento pode ser realizada manual ou automaticamente pela notificação de exclusão de arquivo ou pelo Agendador do otimizador de armazenamento</span><span class="sxs-lookup"><span data-stu-id="14397-132">Storage space reclamation can be performed manually or automatically by file delete notification or the scheduler of the storage optimizer</span></span>
-   <span data-ttu-id="14397-133">O administrador de armazenamento deve implementar a notificação de limite para alertar o administrador do sistema ou o usuário final e evitar qualquer interrupção inesperada do serviço de armazenamento</span><span class="sxs-lookup"><span data-stu-id="14397-133">Storage administrator should implement the threshold notification to alert system administrator or end user and avoid any unexpected storage service interruption</span></span>

## <a name="tests"></a><span data-ttu-id="14397-134">Testes</span><span class="sxs-lookup"><span data-stu-id="14397-134">Tests</span></span>

-   <span data-ttu-id="14397-135">A matriz de armazenamento deve receber o certificado de provisionamento dinâmico do Windows 8 para dar suporte aos recursos de provisionamento fino do Windows</span><span class="sxs-lookup"><span data-stu-id="14397-135">Storage array must receive Windows 8 Thin Provisioning certificate to support Windows Thin Provisioning features</span></span>
-   <span data-ttu-id="14397-136">O kit de certificação de hardware de provisionamento dinâmico do Windows para matriz de armazenamento será uma ferramenta de teste útil para verificar a capacidade da matriz de armazenamento para o suporte ao recurso de provisionamento thin do Windows</span><span class="sxs-lookup"><span data-stu-id="14397-136">Windows Thin Provisioning Hardware Certification Kit for storage array will be a useful test tool to verify storage array’s capability for Windows Thin Provisioning feature support</span></span>
-   <span data-ttu-id="14397-137">O Windows espera que o LUN de provisionamento thin e o LUN de provisionamento completo funcionem no mesmo sistema sem qualquer problema</span><span class="sxs-lookup"><span data-stu-id="14397-137">Windows expects the Thin Provisioning LUN and Full Provisioning LUN to work in the same system without any issue</span></span>

## <a name="resources"></a><span data-ttu-id="14397-138">Recursos</span><span class="sxs-lookup"><span data-stu-id="14397-138">Resources</span></span>

-   [<span data-ttu-id="14397-139">Especificação de comando de bloco T10 SCSI (SBC3r27)</span><span class="sxs-lookup"><span data-stu-id="14397-139">T10 SCSI Block Command Spec (SBC3r27)</span></span>](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [<span data-ttu-id="14397-140">Serviços de painel de hardware</span><span class="sxs-lookup"><span data-stu-id="14397-140">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)

 

 