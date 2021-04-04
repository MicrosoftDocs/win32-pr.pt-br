---
title: Gerenciador de reinicialização
description: Escreva instaladores personalizados para eliminar reinicializações do sistema que são necessárias para concluir a atualização de um arquivo em uso. Desligue e reinicie todos os serviços do sistema, exceto os críticos, dos programas.
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Gerenciador de reinicialização do reinício
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1244cff7bc22fd2e7b6d2540051bd0984596086
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007885"
---
# <a name="restart-manager"></a><span data-ttu-id="e18a5-105">Gerenciador de reinicialização</span><span class="sxs-lookup"><span data-stu-id="e18a5-105">Restart Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="e18a5-106">Finalidade</span><span class="sxs-lookup"><span data-stu-id="e18a5-106">Purpose</span></span>

<span data-ttu-id="e18a5-107">A API do Gerenciador de reinicialização pode eliminar ou reduzir o número de reinicializações do sistema que são necessárias para concluir uma instalação ou atualização.</span><span class="sxs-lookup"><span data-stu-id="e18a5-107">The Restart Manager API can eliminate or reduce the number of system restarts that are required to complete an installation or update.</span></span> <span data-ttu-id="e18a5-108">O principal motivo pelo qual as atualizações de software exigem uma reinicialização do sistema durante uma instalação ou atualização é que alguns dos arquivos que estão sendo atualizados estão sendo usados no momento por um aplicativo ou serviço em execução.</span><span class="sxs-lookup"><span data-stu-id="e18a5-108">The primary reason software updates require a system restart during an installation or update is that some of the files that are being updated are currently being used by a running application or service.</span></span> <span data-ttu-id="e18a5-109">O Gerenciador de reinicialização permite que todos, exceto os [serviços críticos do sistema](critical-system-services.md) sejam desligados e reiniciados.</span><span class="sxs-lookup"><span data-stu-id="e18a5-109">The Restart Manager enables all but the [critical system services](critical-system-services.md) to be shut down and restarted.</span></span> <span data-ttu-id="e18a5-110">Isso libera os arquivos que estão em uso e permite que as operações de instalação sejam concluídas.</span><span class="sxs-lookup"><span data-stu-id="e18a5-110">This frees files that are in use and allows installation operations to complete.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="e18a5-111">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="e18a5-111">Where applicable</span></span>

<span data-ttu-id="e18a5-112">O DLL do Gerenciador de reinicialização exporta uma interface C pública que pode ser carregada por instaladores padrão ou personalizados.</span><span class="sxs-lookup"><span data-stu-id="e18a5-112">The Restart Manager DLL exports a public C interface that can be loaded by standard or custom installers.</span></span> <span data-ttu-id="e18a5-113">O instalador pode usar o Gerenciador de reinicialização para registrar os arquivos que devem ser substituídos durante a instalação de um aplicativo ou atualização.</span><span class="sxs-lookup"><span data-stu-id="e18a5-113">The installer can use the Restart Manager to register files that should be replaced during the installation of an application or update.</span></span> <span data-ttu-id="e18a5-114">Em seguida, durante uma atualização ou instalação subsequente, o instalador pode usar o Gerenciador de reinicialização para determinar quais arquivos não podem ser atualizados porque estão em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="e18a5-114">Then during a subsequent update or installation, the installer can use the Restart Manager to determine which files cannot be updated because they are currently in use.</span></span> <span data-ttu-id="e18a5-115">O Gerenciador de reinicialização pode desligar e reiniciar os serviços não críticos ou os aplicativos que estão usando esses arquivos no momento.</span><span class="sxs-lookup"><span data-stu-id="e18a5-115">Restart Manager can shut down and restart the non-critical services or applications that are currently using those files.</span></span> <span data-ttu-id="e18a5-116">Os instaladores podem instruir o Gerenciador de reinicialização a desligar e reiniciar aplicativos ou serviços com base no arquivo em uso, na ID do processo (PID) ou no nome curto de um serviço do Windows.</span><span class="sxs-lookup"><span data-stu-id="e18a5-116">Installers can direct the Restart Manager to shut down and restart applications or services based on the file in use, the process ID (PID), or the short-name of a Windows service.</span></span>

<span data-ttu-id="e18a5-117">O Gerenciador de reinicialização destina-se ao desenvolvimento de aplicativos de estilo de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e18a5-117">Restart Manager is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e18a5-118">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="e18a5-118">Developer audience</span></span>

<span data-ttu-id="e18a5-119">Esta documentação destina-se a desenvolvedores de aplicativos de instalação que desejam aproveitar os recursos do instalador no Windows Vista ou no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e18a5-119">This documentation is intended for developers of installation applications who want to take advantage of the installer capabilities in Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="e18a5-120">Os aplicativos que usam o [Windows Installer](/windows/desktop/Msi/windows-installer-portal) versão 4,0 para instalação e manutenção automaticamente usam o Gerenciador de reinicialização para reduzir as reinicializações do sistema.</span><span class="sxs-lookup"><span data-stu-id="e18a5-120">Applications that use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) version 4.0 for installation and servicing automatically use the Restart Manager to reduce system restarts.</span></span> <span data-ttu-id="e18a5-121">Instaladores personalizados também podem ser criados para chamar a API do Gerenciador de reinicialização para desligar e reiniciar aplicativos e serviços.</span><span class="sxs-lookup"><span data-stu-id="e18a5-121">Custom installers can also be designed to call the Restart Manager API to shut down and restart applications and services.</span></span> <span data-ttu-id="e18a5-122">Nos casos em que uma reinicialização do sistema é inevitável, os instaladores podem usar a API do Gerenciador de reinicialização para agendar reinicializações de forma a minimizar a interrupção do fluxo de trabalho do usuário.</span><span class="sxs-lookup"><span data-stu-id="e18a5-122">In cases where a system restart is unavoidable, installers can use the Restart Manager API to schedule restarts in such a way that it minimizes the disruption of the user's work flow.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e18a5-123">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="e18a5-123">Run-time requirements</span></span>

<span data-ttu-id="e18a5-124">A API do Gerenciador de reinicialização está disponível a partir do Windows Vista e do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e18a5-124">The Restart Manager API is available beginning with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="e18a5-125">O Gerenciador de reinicialização consiste em uma única DLL que os aplicativos podem carregar para acessar a API do Gerenciador de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="e18a5-125">Restart Manager consists of a single DLL that applications can load to access the Restart Manager API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e18a5-126">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e18a5-126">In this section</span></span>



| <span data-ttu-id="e18a5-127">Tópico</span><span class="sxs-lookup"><span data-stu-id="e18a5-127">Topic</span></span>                                                                 | <span data-ttu-id="e18a5-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="e18a5-128">Description</span></span>                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="e18a5-129">Sobre o Gerenciador de reinicialização</span><span class="sxs-lookup"><span data-stu-id="e18a5-129">About Restart Manager</span></span>](about-restart-manager.md)<br/>         | <span data-ttu-id="e18a5-130">Tópicos de visão geral que descrevem o Gerenciador de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="e18a5-130">Overview topics that describe the Restart Manager.</span></span><br/>   |
| [<span data-ttu-id="e18a5-131">Usando o Gerenciador de reinicialização</span><span class="sxs-lookup"><span data-stu-id="e18a5-131">Using Restart Manager</span></span>](using-restart-manager.md)<br/>         | <span data-ttu-id="e18a5-132">Tópicos de visão geral sobre como usar a API do Gerenciador de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="e18a5-132">Overview topics about using the Restart Manager API.</span></span><br/> |
| [<span data-ttu-id="e18a5-133">Referência do Gerenciador de reinicialização</span><span class="sxs-lookup"><span data-stu-id="e18a5-133">Restart Manager Reference</span></span>](restart-manager-reference.md)<br/> | <span data-ttu-id="e18a5-134">Tópicos de referência para a API do Gerenciador de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="e18a5-134">Reference topics for the Restart Manager API.</span></span><br/>        |



 

 

