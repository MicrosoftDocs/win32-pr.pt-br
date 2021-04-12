---
title: Gadgets de área de trabalho removidos
description: Gadgets de área de trabalho removidos
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- miniaplicativo
- gadgets de área de trabalho
- Barra lateral do Windows
- Barra lateral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c37c058a75aca82d7727566041af4c30f3bb474
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104366802"
---
# <a name="desktop-gadgets-removed"></a><span data-ttu-id="655dc-107">Gadgets de área de trabalho removidos</span><span class="sxs-lookup"><span data-stu-id="655dc-107">Desktop gadgets removed</span></span>

## <a name="platforms"></a><span data-ttu-id="655dc-108">Plataformas</span><span class="sxs-lookup"><span data-stu-id="655dc-108">Platforms</span></span>

 <span data-ttu-id="655dc-109">**Clientes** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="655dc-109">**Clients** - Windows 8</span></span>  
<span data-ttu-id="655dc-110">**Servidores** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="655dc-110">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="655dc-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="655dc-111">Description</span></span>

<span data-ttu-id="655dc-112">Do ponto de vista da funcionalidade, os gadgets já foram preteridos e são descritos por novos blocos dinâmicos e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="655dc-112">From a functionality standpoint, Gadgets have already been deprecated and are outclassed by new live tiles and apps.</span></span> <span data-ttu-id="655dc-113">Os gadgets também apresentam um risco de segurança aos usuários.</span><span class="sxs-lookup"><span data-stu-id="655dc-113">Gadgets also present a security risk to users.</span></span> <span data-ttu-id="655dc-114">Como plataforma, existem vulnerabilidades, de modo que até mesmo os gadgets benignos pudessem ser explorados.</span><span class="sxs-lookup"><span data-stu-id="655dc-114">As a platform, vulnerabilities exist such that even benign Gadgets could be exploited.</span></span> <span data-ttu-id="655dc-115">Portanto, para defender o Windows 8 como nosso sistema operacional mais moderno e seguro, optamos por remover os gadgets do sistema operacional inteiramente.</span><span class="sxs-lookup"><span data-stu-id="655dc-115">Therefore, in order to uphold Windows 8 as our most modern and secure operating system, we have chosen to remove Gadgets from the operating system entirely.</span></span> <span data-ttu-id="655dc-116">Os usuários do Windows 7 com gadgets em sua área de trabalho serão notificados e os gadgets serão desinstalados.</span><span class="sxs-lookup"><span data-stu-id="655dc-116">Windows 7 users with Gadgets on their Desktop will be notified and Gadgets will be uninstalled.</span></span>

## <a name="manifestation"></a><span data-ttu-id="655dc-117">Manifestação</span><span class="sxs-lookup"><span data-stu-id="655dc-117">Manifestation</span></span>

<span data-ttu-id="655dc-118">Os gadgets de área de trabalho não estarão disponíveis na área de trabalho do Windows.</span><span class="sxs-lookup"><span data-stu-id="655dc-118">Desktop Gadgets will not be available on the Windows Desktop.</span></span>

## <a name="mitigation"></a><span data-ttu-id="655dc-119">Atenuação</span><span class="sxs-lookup"><span data-stu-id="655dc-119">Mitigation</span></span>

<span data-ttu-id="655dc-120">A estrutura de pastas e a API dos gadgets de área de trabalho permanecerão em vigor para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="655dc-120">The Desktop Gadgets API and folder structure will remain in place for Windows 8.</span></span> <span data-ttu-id="655dc-121">Os aplicativos que instalam e executam gadgets de forma programática usando essa API continuarão a ser executados sem falha (embora os próprios gadgets não sejam).</span><span class="sxs-lookup"><span data-stu-id="655dc-121">Applications which programmatically install and run Gadgets using this API will continue to run without fail (although the Gadgets themselves will not).</span></span>

## <a name="solution"></a><span data-ttu-id="655dc-122">Solução</span><span class="sxs-lookup"><span data-stu-id="655dc-122">Solution</span></span>

<span data-ttu-id="655dc-123">Os desenvolvedores de aplicativos de área de trabalho não devem empacotar gadgets em seus instaladores.</span><span class="sxs-lookup"><span data-stu-id="655dc-123">Desktop app developers should not package Gadgets in their installers.</span></span> <span data-ttu-id="655dc-124">Esses gadgets ocuparão espaço para o usuário e não poderão ser executados no sistema.</span><span class="sxs-lookup"><span data-stu-id="655dc-124">These Gadgets will just take up space for the user and will not be able to be run in the system.</span></span>

## <a name="tests"></a><span data-ttu-id="655dc-125">Testes</span><span class="sxs-lookup"><span data-stu-id="655dc-125">Tests</span></span>

<span data-ttu-id="655dc-126">Os desenvolvedores podem testar a compatibilidade dessa alteração desabilitando o componente opcional para gadgets de área de trabalho no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="655dc-126">Developers are able to test compatibility of this change by disabling the optional component for Desktop Gadgets in Windows 7.</span></span> <span data-ttu-id="655dc-127">Para desabilitar gadgets em um PC com Windows 7, siga as etapas abaixo:</span><span class="sxs-lookup"><span data-stu-id="655dc-127">To disable Gadgets on a Windows 7 PC, follow the steps below:</span></span>

1.  <span data-ttu-id="655dc-128">Navegue para ativar ou desativar recursos do Windows no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="655dc-128">Navigate to Turn Windows Features on or off from the Control Panel.</span></span>
2.  <span data-ttu-id="655dc-129">Desmarque a caixa ao lado de "plataforma de gadget do Windows".</span><span class="sxs-lookup"><span data-stu-id="655dc-129">Uncheck the box next to “Windows Gadget Platform”.</span></span>
3.  <span data-ttu-id="655dc-130">Clique em OK e siga as instruções adicionais na tela.</span><span class="sxs-lookup"><span data-stu-id="655dc-130">Click OK and follow any additional on-screen instructions.</span></span>

## <a name="resources"></a><span data-ttu-id="655dc-131">Recursos</span><span class="sxs-lookup"><span data-stu-id="655dc-131">Resources</span></span>

[<span data-ttu-id="655dc-132">Vulnerabilidades em gadgets podem permitir a execução remota de código</span><span class="sxs-lookup"><span data-stu-id="655dc-132">Vulnerabilities in Gadgets Could Allow Remote Code Execution</span></span>](https://support.microsoft.com/kb/2719662)

 

 




