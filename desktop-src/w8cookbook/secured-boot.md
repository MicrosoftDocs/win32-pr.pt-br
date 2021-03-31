---
title: Antimalware de início antecipado
description: Antimalware de início antecipado
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c3e51d7fb009ffa0e85a59990b321fb38ad196
ms.sourcegitcommit: a93d3abaf4d6d45a6f0b87faed3f576b222b1745
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104011890"
---
# <a name="early-launch-antimalware"></a><span data-ttu-id="a8074-103">Antimalware de início antecipado</span><span class="sxs-lookup"><span data-stu-id="a8074-103">Early launch antimalware</span></span>

## <a name="platforms"></a><span data-ttu-id="a8074-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="a8074-104">Platforms</span></span>

 <span data-ttu-id="a8074-105">**Clientes** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="a8074-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="a8074-106">**Servidores** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a8074-106">**Servers** - Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="a8074-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8074-107">Description</span></span>

<span data-ttu-id="a8074-108">Como o software antimalware (AM) se tornou melhor e melhor na detecção de malware de tempo de execução, os invasores também estão se tornando melhores na criação de rootkits que podem se esconder da detecção.</span><span class="sxs-lookup"><span data-stu-id="a8074-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="a8074-109">Detectar malwares que iniciam no início do ciclo de inicialização é um desafio que a maioria dos fornecedores nos atendem de maneira programada.</span><span class="sxs-lookup"><span data-stu-id="a8074-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="a8074-110">Normalmente, eles criam hackers do sistema que não têm suporte no sistema operacional do host e podem realmente resultar na colocação do computador em um estado instável.</span><span class="sxs-lookup"><span data-stu-id="a8074-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="a8074-111">Até este ponto, o Windows não forneceu uma boa maneira para que eu detecte e resolva essas ameaças de inicialização antecipada.</span><span class="sxs-lookup"><span data-stu-id="a8074-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span>

<span data-ttu-id="a8074-112">O Windows 8 apresenta um novo recurso chamado inicialização segura, que protege a configuração e os componentes de inicialização do Windows e carrega um driver ELAM (AntiMalware de início antecipado).</span><span class="sxs-lookup"><span data-stu-id="a8074-112">Windows 8 introduces a new feature called Secure Boot, which protects the Windows boot configuration and components, and loads an Early Launch Anti-malware (ELAM) driver.</span></span> <span data-ttu-id="a8074-113">Esse driver começa antes de outros drivers de inicialização e habilita a avaliação desses drivers e ajuda o kernel do Windows a decidir se eles devem ser inicializados.</span><span class="sxs-lookup"><span data-stu-id="a8074-113">This driver starts before other boot-start drivers and enables the evaluation of those drivers and helps the Windows kernel decide whether they should be initialized.</span></span>

## <a name="manifestation"></a><span data-ttu-id="a8074-114">Manifestação</span><span class="sxs-lookup"><span data-stu-id="a8074-114">Manifestation</span></span>

<span data-ttu-id="a8074-115">Ao ser iniciado primeiro pelo kernel, o ELAM é garantido para ser iniciado antes de qualquer software de terceiros e, portanto, é capaz de detectar malware no processo de inicialização e impedir a inicialização.</span><span class="sxs-lookup"><span data-stu-id="a8074-115">By being launched first by the kernel, ELAM is ensured to be launched before any third-party software, and is therefore able to detect malware in the boot process and prevent it from initializing.</span></span>

## <a name="mitigation"></a><span data-ttu-id="a8074-116">Atenuação</span><span class="sxs-lookup"><span data-stu-id="a8074-116">Mitigation</span></span>

<span data-ttu-id="a8074-117">Os drivers de inicialização são inicializados com base na classificação retornada pelo driver ELAM de acordo com uma política de inicialização.</span><span class="sxs-lookup"><span data-stu-id="a8074-117">Boot drivers are initialized based on the classification that is returned from the ELAM driver according to an initialization policy.</span></span> <span data-ttu-id="a8074-118">Por padrão, a política Inicializa drivers bons e desconhecidos conhecidos, mas não inicializa drivers inválidos conhecidos.</span><span class="sxs-lookup"><span data-stu-id="a8074-118">By default, the policy initializes known good and unknown drivers, but will not initialize known bad drivers.</span></span> <span data-ttu-id="a8074-119">Um administrador do sistema pode especificar uma política personalizada por meio de Política de Grupo que pode impedir a inicialização de drivers desconhecidos ou a habilitação de drivers que são críticos para o processo de inicialização, mas foram adulterados, inicializados para inicialização.</span><span class="sxs-lookup"><span data-stu-id="a8074-119">A system administrator can specify a custom policy through Group Policy that can prevent unknown drivers from initializing or can enable drivers that are critical to the boot process, but have been tampered with, boot to be initialized.</span></span>

## <a name="solution"></a><span data-ttu-id="a8074-120">Solução</span><span class="sxs-lookup"><span data-stu-id="a8074-120">Solution</span></span>

<span data-ttu-id="a8074-121">Um driver ELAM deve se registrar para retornos de chamada de kernel para obter informações sobre cada driver de inicialização inicial à medida que ele está sendo inicializado.</span><span class="sxs-lookup"><span data-stu-id="a8074-121">An ELAM driver must register for kernel callbacks to get info about each boot-start driver as it is initializing.</span></span> <span data-ttu-id="a8074-122">O driver ELAM pode retornar uma classificação para cada driver.</span><span class="sxs-lookup"><span data-stu-id="a8074-122">The ELAM driver can then return a classification for each driver.</span></span> <span data-ttu-id="a8074-123">Essas funções são necessárias:</span><span class="sxs-lookup"><span data-stu-id="a8074-123">These functions are required:</span></span>

-   [<span data-ttu-id="a8074-124">IoRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="a8074-124">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="a8074-125">IoUnRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="a8074-125">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

<span data-ttu-id="a8074-126">Um driver ELAM também pode se registrar para retornos de chamada do registro.</span><span class="sxs-lookup"><span data-stu-id="a8074-126">An ELAM driver can also register for registry callbacks.</span></span> <span data-ttu-id="a8074-127">Isso permite que o driver ELAM Inspecione os dados de configuração que são usados por cada driver de inicialização inicial.</span><span class="sxs-lookup"><span data-stu-id="a8074-127">Doing so enables the ELAM driver to inspect the configuration data that is used by each boot-start driver.</span></span> <span data-ttu-id="a8074-128">O driver ELAM pode, então, bloquear ou modificar os dados antes que eles sejam usados pelos drivers de inicialização inicial, se necessário.</span><span class="sxs-lookup"><span data-stu-id="a8074-128">The ELAM driver can then block or modify the data before it is used by the boot-start drivers, if necessary.</span></span> <span data-ttu-id="a8074-129">Essas funções são necessárias:</span><span class="sxs-lookup"><span data-stu-id="a8074-129">These functions are required:</span></span>

-   [<span data-ttu-id="a8074-130">CmRegisterCallbackEx</span><span class="sxs-lookup"><span data-stu-id="a8074-130">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="a8074-131">CmUnRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="a8074-131">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

<span data-ttu-id="a8074-132">Para obter mais detalhes sobre os requisitos do driver ELAM e o uso da API, consulte [pré-malware de início antecipado](/windows-hardware/drivers/install/early-launch-antimalware).</span><span class="sxs-lookup"><span data-stu-id="a8074-132">For more details about ELAM driver requirements and API usage, see [Early Launch Antimalware](/windows-hardware/drivers/install/early-launch-antimalware).</span></span>

## <a name="tests"></a><span data-ttu-id="a8074-133">Testes</span><span class="sxs-lookup"><span data-stu-id="a8074-133">Tests</span></span>

<span data-ttu-id="a8074-134">Os drivers ELAM devem ser assinados especialmente pela Microsoft para garantir que eles sejam iniciados pelo kernel do Windows no início do processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="a8074-134">ELAM drivers must be specially signed by Microsoft to ensure they are started by the Windows kernel early in the boot process.</span></span> <span data-ttu-id="a8074-135">Para obter a assinatura, os drivers ELAM devem passar um conjunto de testes de certificação para verificar o desempenho e outros comportamentos.</span><span class="sxs-lookup"><span data-stu-id="a8074-135">To get the signature, ELAM drivers must pass a set of certification tests to verify performance and other behavior.</span></span> <span data-ttu-id="a8074-136">Esses testes estão incluídos no kit de certificação de hardware do Windows.</span><span class="sxs-lookup"><span data-stu-id="a8074-136">These tests are included in the Windows Hardware Certification Kit.</span></span>

## <a name="resources"></a><span data-ttu-id="a8074-137">Recursos</span><span class="sxs-lookup"><span data-stu-id="a8074-137">Resources</span></span>

-   [<span data-ttu-id="a8074-138">AntiMalware de início antecipado</span><span class="sxs-lookup"><span data-stu-id="a8074-138">Early Launch Antimalware</span></span>](/windows-hardware/drivers/install/early-launch-antimalware)
-   [<span data-ttu-id="a8074-139">CmRegisterCallbackEx</span><span class="sxs-lookup"><span data-stu-id="a8074-139">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="a8074-140">CmUnRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="a8074-140">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [<span data-ttu-id="a8074-141">IoRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="a8074-141">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="a8074-142">IoUnRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="a8074-142">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [<span data-ttu-id="a8074-143">Certificando o hardware com a apresentação de conferência de Build do kit de certificação de hardware do Windows</span><span class="sxs-lookup"><span data-stu-id="a8074-143">Certifying hardware with the Windows Hardware Certification Kit Build Conference presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [<span data-ttu-id="a8074-144">Baixar kits e ferramentas</span><span class="sxs-lookup"><span data-stu-id="a8074-144">Download Kits and Tools</span></span>](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
