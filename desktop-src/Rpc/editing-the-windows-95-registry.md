---
title: Editando o registro do Windows 95
description: Você pode usar o REGEDIT para editar o registro do Windows 95 para designar um NSP.
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c622ea44a5e365ca631d6d4db34af8e939ea6487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822946"
---
# <a name="editing-the-windows-95-registry"></a><span data-ttu-id="89ddb-103">Editando o registro do Windows 95</span><span class="sxs-lookup"><span data-stu-id="89ddb-103">Editing the Windows 95 Registry</span></span>

<span data-ttu-id="89ddb-104">Você pode usar o REGEDIT para editar o registro do Windows 95 para designar um NSP.</span><span class="sxs-lookup"><span data-stu-id="89ddb-104">You can use REGEDIT to edit the Windows 95 registry to designate an NSP.</span></span>

<span data-ttu-id="89ddb-105">**Para designar um provedor de serviços de Microsoft Locator Name para Windows 95**</span><span class="sxs-lookup"><span data-stu-id="89ddb-105">**To designate a Microsoft Locator name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="89ddb-106">Selecionar</span><span class="sxs-lookup"><span data-stu-id="89ddb-106">Select</span></span>

    <span data-ttu-id="89ddb-107">**HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **RPC**</span><span class="sxs-lookup"><span data-stu-id="89ddb-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="89ddb-108">Criar uma nova chave chamada</span><span class="sxs-lookup"><span data-stu-id="89ddb-108">Create a new key called</span></span>

    <span data-ttu-id="89ddb-109">**NameService**</span><span class="sxs-lookup"><span data-stu-id="89ddb-109">**NameService**</span></span>

3.  <span data-ttu-id="89ddb-110">Com a chave **NameService** selecionada, crie os novos nomes de **StringValue** e modifique-os para conter dados, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="89ddb-110">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="89ddb-111">Nome</span><span class="sxs-lookup"><span data-stu-id="89ddb-111">Name</span></span>                     | <span data-ttu-id="89ddb-112">Dados</span><span class="sxs-lookup"><span data-stu-id="89ddb-112">Data</span></span>                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | <span data-ttu-id="89ddb-113">**Defaultsyntax**</span><span class="sxs-lookup"><span data-stu-id="89ddb-113">**DefaultSyntax**</span></span>        | <span data-ttu-id="89ddb-114">3</span><span class="sxs-lookup"><span data-stu-id="89ddb-114">3</span></span><br/>                                                                |
    | <span data-ttu-id="89ddb-115">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="89ddb-115">**Protocol**</span></span>             | <span data-ttu-id="89ddb-116">ncacn \_ NP</span><span class="sxs-lookup"><span data-stu-id="89ddb-116">ncacn\_np</span></span><br/>                                                        |
    | <span data-ttu-id="89ddb-117">**Ponto de extremidade**</span><span class="sxs-lookup"><span data-stu-id="89ddb-117">**Endpoint**</span></span>             | <span data-ttu-id="89ddb-118">\\\\localizador de pipe</span><span class="sxs-lookup"><span data-stu-id="89ddb-118">\\pipe\\locator</span></span><br/>                                                  |
    | <span data-ttu-id="89ddb-119">**NetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="89ddb-119">**NetworkAddress**</span></span>       | <span data-ttu-id="89ddb-120">meuservidor (em que meuservidor é o nome do computador com Windows NT)</span><span class="sxs-lookup"><span data-stu-id="89ddb-120">myserver (where myserver is the name of the Windows NT computer)</span></span><br/> |
    | <span data-ttu-id="89ddb-121">**ServerNetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="89ddb-121">**ServerNetworkAddress**</span></span> | <span data-ttu-id="89ddb-122">meuservidor</span><span class="sxs-lookup"><span data-stu-id="89ddb-122">myserver</span></span><br/>                                                         |

    

     

<span data-ttu-id="89ddb-123">Você pode usar o REGEDIT para editar o registro do Windows 95 para designar um NSP de CDS do DCE.</span><span class="sxs-lookup"><span data-stu-id="89ddb-123">You can use REGEDIT to edit the Windows 95 registry to designate a DCE CDS NSP.</span></span>

<span data-ttu-id="89ddb-124">**Para designar um provedor de serviços de nome de CDS DCE para Windows 95**</span><span class="sxs-lookup"><span data-stu-id="89ddb-124">**To designate a DCE CDS name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="89ddb-125">Selecionar</span><span class="sxs-lookup"><span data-stu-id="89ddb-125">Select</span></span>

    <span data-ttu-id="89ddb-126">**HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **RPC**</span><span class="sxs-lookup"><span data-stu-id="89ddb-126">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="89ddb-127">Criar uma nova chave chamada</span><span class="sxs-lookup"><span data-stu-id="89ddb-127">Create a new key called</span></span>

    <span data-ttu-id="89ddb-128">**NameService**</span><span class="sxs-lookup"><span data-stu-id="89ddb-128">**NameService**</span></span>

3.  <span data-ttu-id="89ddb-129">Com a chave **NameService** selecionada, crie os novos nomes de **StringValue** e modifique-os para conter dados, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="89ddb-129">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="89ddb-130">Nome</span><span class="sxs-lookup"><span data-stu-id="89ddb-130">Name</span></span>                     | <span data-ttu-id="89ddb-131">Dados</span><span class="sxs-lookup"><span data-stu-id="89ddb-131">Data</span></span>                                                             |
    |--------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="89ddb-132">**Defaultsyntax**</span><span class="sxs-lookup"><span data-stu-id="89ddb-132">**DefaultSyntax**</span></span>        | <span data-ttu-id="89ddb-133">3</span><span class="sxs-lookup"><span data-stu-id="89ddb-133">3</span></span><br/>                                                     |
    | <span data-ttu-id="89ddb-134">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="89ddb-134">**Protocol**</span></span>             | <span data-ttu-id="89ddb-135">\_TCP IP \_ ncacn</span><span class="sxs-lookup"><span data-stu-id="89ddb-135">ncacn\_ip\_tcp</span></span><br/>                                        |
    | <span data-ttu-id="89ddb-136">**Ponto de extremidade**</span><span class="sxs-lookup"><span data-stu-id="89ddb-136">**Endpoint**</span></span>             | <span data-ttu-id="89ddb-137">"" (uma cadeia de caracteres vazia)</span><span class="sxs-lookup"><span data-stu-id="89ddb-137">"" (an empty string)</span></span><br/>                                  |
    | <span data-ttu-id="89ddb-138">**NetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="89ddb-138">**NetworkAddress**</span></span>       | <span data-ttu-id="89ddb-139">meuservidor (o nome do computador host que executa o nsid)</span><span class="sxs-lookup"><span data-stu-id="89ddb-139">myserver (the name of the host computer running nsid)</span></span><br/> |
    | <span data-ttu-id="89ddb-140">**ServerNetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="89ddb-140">**ServerNetworkAddress**</span></span> | <span data-ttu-id="89ddb-141">meuservidor (o nome do computador host que executa o nsid)</span><span class="sxs-lookup"><span data-stu-id="89ddb-141">myserver (the name of the host computer running nsid)</span></span><br/> |

    

     

    > [!Note]  
    > <span data-ttu-id="89ddb-142">Você deve ter o produto serviço de diretório de célula do DCE do Digital Equipment Corporation para configurar os CDS do DCE como seu provedor de serviços de nome.</span><span class="sxs-lookup"><span data-stu-id="89ddb-142">You must have the Digital Equipment Corporation DCE Cell Directory Service product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="89ddb-143">Consulte a documentação fornecida pela Digital Equipment Corporation para obter informações sobre os CDS da DCE.</span><span class="sxs-lookup"><span data-stu-id="89ddb-143">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

     

 

 





