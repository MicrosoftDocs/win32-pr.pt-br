---
title: Compatibilidade de cliente e servidor-Windows 8
description: Compatibilidade de cliente e servidor com Windows 8 e Windows Server 2012
ms.assetid: 5067219A-EBA2-4FAF-8C17-7AB22C5EADD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5b685ae10b97a7b8197737944ea7231d226514
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2019
ms.locfileid: "104293669"
---
# <a name="windows-8-and-windows-server-2012-client-and-server-compatibility"></a><span data-ttu-id="b3e59-103">Compatibilidade de cliente e servidor com Windows 8 e Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b3e59-103">Windows 8 and Windows Server 2012 client and server compatibility</span></span>

<span data-ttu-id="b3e59-104">Esta seção descreve as alterações no sistema operacional que você deve prestar atenção especial devido aos possíveis impactos nos aplicativos existentes e como os novos aplicativos devem ser criados em clientes, em servidores ou em clientes e servidores.</span><span class="sxs-lookup"><span data-stu-id="b3e59-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="b3e59-105">A seguir está a lista de tópicos abordados nesta seção, agrupados por área de recurso:</span><span class="sxs-lookup"><span data-stu-id="b3e59-105">Following is the list of topics covered in this section, grouped by feature area:</span></span>

<span data-ttu-id="b3e59-106">**AppCompat**</span><span class="sxs-lookup"><span data-stu-id="b3e59-106">**AppCompat**</span></span>

-   <span data-ttu-id="b3e59-107">Atualização de regras de detecção de aplicativo de segurança</span><span class="sxs-lookup"><span data-stu-id="b3e59-107">Security app detection rules update</span></span>
-   <span data-ttu-id="b3e59-108">Determinando o status do Shim</span><span class="sxs-lookup"><span data-stu-id="b3e59-108">Determining shim status</span></span>
-   <span data-ttu-id="b3e59-109">Os aplicativos do servidor devem ser capazes de executar sem o shell gráfico do servidor</span><span class="sxs-lookup"><span data-stu-id="b3e59-109">Server apps must be able to run without the Server Graphical Shell</span></span>
-   <span data-ttu-id="b3e59-110">Os componentes do servidor RDS são removidos do Windows 8</span><span class="sxs-lookup"><span data-stu-id="b3e59-110">RDS server components are removed from Windows 8</span></span>
-   <span data-ttu-id="b3e59-111">Modelo de associações de protocolo e tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="b3e59-111">File type and protocol associations model</span></span>
-   <span data-ttu-id="b3e59-112">Moderador de atividade da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="b3e59-112">Desktop Activity Moderator</span></span>
-   <span data-ttu-id="b3e59-113">.NET Framework 4,5 é o padrão e .NET Framework 3,5 é opcional</span><span class="sxs-lookup"><span data-stu-id="b3e59-113">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>
-   <span data-ttu-id="b3e59-114">Os aplicativos da área de trabalho podem não estar visíveis depois de iniciar o navegador da Web padrão</span><span class="sxs-lookup"><span data-stu-id="b3e59-114">Desktop apps may not be visible after launching the default web browser</span></span>
-   <span data-ttu-id="b3e59-115">Modo de alto contraste</span><span class="sxs-lookup"><span data-stu-id="b3e59-115">High-contrast mode</span></span>
-   <span data-ttu-id="b3e59-116">Manifesto do aplicativo (executável)</span><span class="sxs-lookup"><span data-stu-id="b3e59-116">App (executable) manifest</span></span>
-   <span data-ttu-id="b3e59-117">O modelo presente na fila está sendo preterido</span><span class="sxs-lookup"><span data-stu-id="b3e59-117">Queued present model is being deprecated</span></span>
-   <span data-ttu-id="b3e59-118">Cenários do assistente de compatibilidade de programas para o Windows 8</span><span class="sxs-lookup"><span data-stu-id="b3e59-118">Program Compatibility Assistant scenarios for Windows 8</span></span>
-   <span data-ttu-id="b3e59-119">Gadgets de área de trabalho removidos</span><span class="sxs-lookup"><span data-stu-id="b3e59-119">Desktop gadgets removed</span></span>

<span data-ttu-id="b3e59-120">**Armazenamento e sistema de arquivos**</span><span class="sxs-lookup"><span data-stu-id="b3e59-120">**Storage and File System**</span></span>

-   <span data-ttu-id="b3e59-121">Atualização de compatibilidade de disco de formato avançado (4K)</span><span class="sxs-lookup"><span data-stu-id="b3e59-121">Advanced format (4K) disk compatibility update</span></span>
-   <span data-ttu-id="b3e59-122">Provisionamento dinâmico de unidades lógicas</span><span class="sxs-lookup"><span data-stu-id="b3e59-122">Thin provisioning of logical units</span></span>
-   <span data-ttu-id="b3e59-123">O armazenamento aprimorado agora é opcional para Ambiente de Pré-Instalação do Windows (WinPE) e SKU do servidor</span><span class="sxs-lookup"><span data-stu-id="b3e59-123">Enhanced storage is now optional for Windows Preinstallation Environment (WinPE) and server SKU</span></span>
-   <span data-ttu-id="b3e59-124">O serviço de disco virtual está em transição para a API de gerenciamento de armazenamento do Windows baseada em Instrumentação de Gerenciamento do Windows (WMI)</span><span class="sxs-lookup"><span data-stu-id="b3e59-124">Virtual Disk Service is transitioning to the Windows Management Instrumentation (WMI)-based Windows Storage Management API</span></span>
-   <span data-ttu-id="b3e59-125">Interface do usuário de versões anteriores removida para volumes locais</span><span class="sxs-lookup"><span data-stu-id="b3e59-125">Previous versions UI removed for local volumes</span></span>
-   <span data-ttu-id="b3e59-126">StorAHCI substitui MSAHCI</span><span class="sxs-lookup"><span data-stu-id="b3e59-126">StorAHCI replaces MSAHCI</span></span>
-   <span data-ttu-id="b3e59-127">Backup e restauração do Windows 7 preteridos</span><span class="sxs-lookup"><span data-stu-id="b3e59-127">Windows 7 backup and restore deprecated</span></span>
-   <span data-ttu-id="b3e59-128">Transferências de dados descarregadas</span><span class="sxs-lookup"><span data-stu-id="b3e59-128">Offloaded data transfers</span></span>

<span data-ttu-id="b3e59-129">**Outras**</span><span class="sxs-lookup"><span data-stu-id="b3e59-129">**Other**</span></span>

-   <span data-ttu-id="b3e59-130">Gerenciador de Janelas da Área de Trabalho está sempre ativada</span><span class="sxs-lookup"><span data-stu-id="b3e59-130">Desktop Window Manager is always on</span></span>
-   <span data-ttu-id="b3e59-131">Direct2D não dá suporte à renderização para metaarquivos "avançados" no Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="b3e59-131">Direct2D does not support rendering to "rich" metafiles in Internet Explorer 9</span></span>
-   <span data-ttu-id="b3e59-132">Alterações no suporte de hardware herdado DX9</span><span class="sxs-lookup"><span data-stu-id="b3e59-132">Changes in DX9 legacy hardware support</span></span>
-   <span data-ttu-id="b3e59-133">A MSAA não está disponível para aplicativos da Windows Store</span><span class="sxs-lookup"><span data-stu-id="b3e59-133">MSAA is not available to Windows Store apps</span></span>
-   <span data-ttu-id="b3e59-134">A porta 3 foi preterida para drivers NDIS 6,30</span><span class="sxs-lookup"><span data-stu-id="b3e59-134">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

 

 
