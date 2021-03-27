---
description: Essencialmente, não há nenhuma restrição sobre como escrever um aplicativo de inicialização AutoRun.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Como implementar aplicativos de inicialização AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b553e102f574835103898b17558541000633412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921674"
---
# <a name="how-to-implement-autorun-startup-applications"></a><span data-ttu-id="be1f9-103">Como implementar aplicativos de inicialização AutoRun</span><span class="sxs-lookup"><span data-stu-id="be1f9-103">How to Implement AutoRun Startup Applications</span></span>

<span data-ttu-id="be1f9-104">Essencialmente, não há nenhuma restrição sobre como escrever um aplicativo de inicialização AutoRun.</span><span class="sxs-lookup"><span data-stu-id="be1f9-104">There are essentially no constraints on how to write an AutoRun startup application.</span></span> <span data-ttu-id="be1f9-105">Você pode implementar o aplicativo de inicialização para fazer aquilo que achar necessário para instalar, desinstalar, configurar ou executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="be1f9-105">You can implement the startup application to do whatever you find necessary to install, uninstall, configure, or run your application.</span></span> <span data-ttu-id="be1f9-106">No entanto, as dicas a seguir fornecem algumas diretrizes para implementar um aplicativo de inicialização de execução automática eficaz.</span><span class="sxs-lookup"><span data-stu-id="be1f9-106">However, the following tips provide some guidelines to implementing an effective AutoRun startup application.</span></span>

## <a name="instructions"></a><span data-ttu-id="be1f9-107">Instruções</span><span class="sxs-lookup"><span data-stu-id="be1f9-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="be1f9-108">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="be1f9-108">Step 1:</span></span>

<span data-ttu-id="be1f9-109">Certifique-se de que os usuários recebam comentários o mais rápido possível depois de inserir um disco de AutoRun na unidade.</span><span class="sxs-lookup"><span data-stu-id="be1f9-109">Make sure that users receive feedback as soon as possible after they insert an AutoRun disc into the drive.</span></span> <span data-ttu-id="be1f9-110">Os aplicativos de inicialização devem ser pequenos programas carregados rapidamente.</span><span class="sxs-lookup"><span data-stu-id="be1f9-110">Startup applications should be small programs that load quickly.</span></span> <span data-ttu-id="be1f9-111">Eles devem identificar claramente o aplicativo e fornecer uma maneira fácil de cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="be1f9-111">They should clearly identify the application and provide an easy way to cancel the operation.</span></span>

### <a name="step-2"></a><span data-ttu-id="be1f9-112">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="be1f9-112">Step 2:</span></span>

<span data-ttu-id="be1f9-113">Verifique se o programa já está instalado.</span><span class="sxs-lookup"><span data-stu-id="be1f9-113">Check to see if the program is already installed.</span></span> <span data-ttu-id="be1f9-114">Caso contrário, a próxima etapa provavelmente será o procedimento de instalação.</span><span class="sxs-lookup"><span data-stu-id="be1f9-114">If not, the next step will probably be the setup procedure.</span></span> <span data-ttu-id="be1f9-115">O aplicativo de inicialização pode aproveitar o tempo que o usuário gasta lendo a caixa de diálogo iniciando outro thread para começar a carregar o código de instalação.</span><span class="sxs-lookup"><span data-stu-id="be1f9-115">The startup application can take advantage of the time the user spends reading the dialog box by starting another thread to begin loading the setup code.</span></span> <span data-ttu-id="be1f9-116">Quando o usuário clicar em **OK**, seu programa de instalação já estará parcialmente se não estiver totalmente carregado.</span><span class="sxs-lookup"><span data-stu-id="be1f9-116">By the time the user clicks **OK**, your setup program will already be partly if not fully loaded.</span></span> <span data-ttu-id="be1f9-117">Essa abordagem reduz significativamente a percepção do usuário da quantidade de tempo que leva para carregar seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="be1f9-117">This approach significantly reduces the user's perception of the amount of time it takes to load your application.</span></span>

> [!Note]  
> <span data-ttu-id="be1f9-118">Normalmente, a parte inicial do aplicativo de inicialização apresenta aos usuários uma interface do usuário, como uma caixa de diálogo, perguntando como eles gostariam de continuar.</span><span class="sxs-lookup"><span data-stu-id="be1f9-118">Typically, the initial part of the startup application presents users with a user interface, such as a dialog box, asking them how they would like to proceed.</span></span>

 

### <a name="step-3"></a><span data-ttu-id="be1f9-119">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="be1f9-119">Step 3:</span></span>

<span data-ttu-id="be1f9-120">Inicie outro thread para começar a carregar o código do aplicativo para reduzir o tempo de espera do usuário.</span><span class="sxs-lookup"><span data-stu-id="be1f9-120">Start another thread to begin loading application code to shorten the waiting time for the user.</span></span> <span data-ttu-id="be1f9-121">Se o aplicativo já tiver sido instalado, o usuário provavelmente inseriu o disco para executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="be1f9-121">If the application has already been installed, the user probably inserted the disk to run the application.</span></span>

### <a name="step-4"></a><span data-ttu-id="be1f9-122">Etapa 4:</span><span class="sxs-lookup"><span data-stu-id="be1f9-122">Step 4:</span></span>

<span data-ttu-id="be1f9-123">Use as seguintes dicas para minimizar o uso do disco rígido:</span><span class="sxs-lookup"><span data-stu-id="be1f9-123">Use the following hints to minimize hard disk usage:</span></span>

-   <span data-ttu-id="be1f9-124">Mantenha o número de arquivos que devem estar no disco rígido para um mínimo.</span><span class="sxs-lookup"><span data-stu-id="be1f9-124">Keep the number of files that must be on the hard disk to a minimum.</span></span> <span data-ttu-id="be1f9-125">Eles devem ser restritos a arquivos que são essenciais para executar o programa ou que levaria um tempo muito grande para ler a partir da mídia.</span><span class="sxs-lookup"><span data-stu-id="be1f9-125">They should be restricted to files that are essential to running the program or that would take an unacceptably large amount of time to read from the media.</span></span>
-   <span data-ttu-id="be1f9-126">Em muitos casos, a instalação de arquivos não essenciais no disco rígido não é necessária, mas pode fornecer benefícios como o aumento do desempenho.</span><span class="sxs-lookup"><span data-stu-id="be1f9-126">In many cases, installing nonessential files on the hard disk is not necessary, but might provide benefits such as increased performance.</span></span> <span data-ttu-id="be1f9-127">Dê ao usuário a opção de decidir como fazer a compensação entre os custos e os benefícios do armazenamento de disco rígido.</span><span class="sxs-lookup"><span data-stu-id="be1f9-127">Give the user the option of deciding how to make the trade-off between the costs and benefits of hard disk storage.</span></span>
-   <span data-ttu-id="be1f9-128">Forneça uma maneira de desinstalar todos os componentes que foram colocados no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="be1f9-128">Provide a way to uninstall any components that were placed on the hard disk.</span></span>
-   <span data-ttu-id="be1f9-129">Se o seu aplicativo armazenar dados em cache, conceda a ele algum controle sobre ele.</span><span class="sxs-lookup"><span data-stu-id="be1f9-129">If your application caches data, give the user some control over it.</span></span> <span data-ttu-id="be1f9-130">Inclua opções no aplicativo de inicialização, como definir um limite na quantidade máxima de dados em cache que serão armazenados no disco rígido ou fazer com que o aplicativo descarte todos os dados armazenados em cache quando ele for encerrado.</span><span class="sxs-lookup"><span data-stu-id="be1f9-130">Include options in the startup application such as setting a limit on the maximum amount of cached data that will be stored on the hard disk, or having the application discard any cached data when it terminates.</span></span>

### <a name="step-5"></a><span data-ttu-id="be1f9-131">Etapa 5:</span><span class="sxs-lookup"><span data-stu-id="be1f9-131">Step 5:</span></span>

<span data-ttu-id="be1f9-132">Desabilite o autorun, se necessário.</span><span class="sxs-lookup"><span data-stu-id="be1f9-132">Disable Autorun if needed.</span></span> <span data-ttu-id="be1f9-133">O AutoRun pode ser suprimido programaticamente ou totalmente desabilitado com o registro, mesmo quando uma mídia tem um arquivo autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="be1f9-133">AutoRun can be suppressed programmatically or disabled entirely with the registry, even when a medium has an Autorun.inf file.</span></span> <span data-ttu-id="be1f9-134">Consulte [Habilitando e desabilitando o autorun](autoplay-reg.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="be1f9-134">See [Enabling and Disabling AutoRun](autoplay-reg.md) for more information.</span></span>

 

 



