---
title: Hierarquia de classe de objeto WinNT
description: A hierarquia da classe de objeto WinNT começa com o objeto namespace.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- ADSI do provedor de serviços WinNT, hierarquia de classe de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6facb31a41e3b03db8290dd6a11e56f9a56c06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498598"
---
# <a name="winnt-object-class-hierarchy"></a><span data-ttu-id="f642a-104">Hierarquia de classe de objeto WinNT</span><span class="sxs-lookup"><span data-stu-id="f642a-104">WinNT Object Class Hierarchy</span></span>

<span data-ttu-id="f642a-105">A hierarquia da classe de objeto WinNT começa com o objeto namespace.</span><span class="sxs-lookup"><span data-stu-id="f642a-105">The WinNT object class hierarchy starts from the Namespace object.</span></span>



| <span data-ttu-id="f642a-106">Classe Object</span><span class="sxs-lookup"><span data-stu-id="f642a-106">Object class</span></span>                   | <span data-ttu-id="f642a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f642a-107">Description</span></span>                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f642a-108">Namespace</span><span class="sxs-lookup"><span data-stu-id="f642a-108">Namespace</span></span><br/>           | <span data-ttu-id="f642a-109">Contêiner de objeto de nível superior.</span><span class="sxs-lookup"><span data-stu-id="f642a-109">Top-level object container.</span></span><br/>                                            |
| <span data-ttu-id="f642a-110">Domínio</span><span class="sxs-lookup"><span data-stu-id="f642a-110">Domain</span></span><br/>              | <span data-ttu-id="f642a-111">O domínio do Windows NT.</span><span class="sxs-lookup"><span data-stu-id="f642a-111">The Windows NT domain.</span></span><br/>                                                 |
| <span data-ttu-id="f642a-112">Usuário</span><span class="sxs-lookup"><span data-stu-id="f642a-112">User</span></span><br/>                | <span data-ttu-id="f642a-113">Conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="f642a-113">User account.</span></span><br/>                                                          |
| <span data-ttu-id="f642a-114">Agrupar</span><span class="sxs-lookup"><span data-stu-id="f642a-114">Group</span></span><br/>               | <span data-ttu-id="f642a-115">Conta de grupo para gerenciar direitos de acesso.</span><span class="sxs-lookup"><span data-stu-id="f642a-115">Group account for managing access rights.</span></span><br/>                              |
| <span data-ttu-id="f642a-116">Usergroupcollection</span><span class="sxs-lookup"><span data-stu-id="f642a-116">UserGroupCollection</span></span><br/> | <span data-ttu-id="f642a-117">Um conjunto de grupos de usuários implementando [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span><span class="sxs-lookup"><span data-stu-id="f642a-117">A set of user groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/>  |
| <span data-ttu-id="f642a-118">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="f642a-118">GroupCollection</span></span><br/>     | <span data-ttu-id="f642a-119">Um conjunto de outros grupos que implementam [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span><span class="sxs-lookup"><span data-stu-id="f642a-119">A set of other groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/> |
| <span data-ttu-id="f642a-120">Computador</span><span class="sxs-lookup"><span data-stu-id="f642a-120">Computer</span></span><br/>            | <span data-ttu-id="f642a-121">Servidor ou estação de trabalho do Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="f642a-121">Windows NT 4.0 server or workstation.</span></span><br/>                                  |
| <span data-ttu-id="f642a-122">PrintJob</span><span class="sxs-lookup"><span data-stu-id="f642a-122">PrintJob</span></span><br/>            | <span data-ttu-id="f642a-123">Trabalho de impressão na fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="f642a-123">Print job in the print queue.</span></span><br/>                                          |
| <span data-ttu-id="f642a-124">Trabalhos de trabalho</span><span class="sxs-lookup"><span data-stu-id="f642a-124">PrintJobsCollection</span></span><br/> | <span data-ttu-id="f642a-125">Um conjunto de trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="f642a-125">A set of print jobs.</span></span><br/>                                                   |
| <span data-ttu-id="f642a-126">PrintQueue</span><span class="sxs-lookup"><span data-stu-id="f642a-126">PrintQueue</span></span><br/>          | <span data-ttu-id="f642a-127">Fila de impressão em um spooler de impressora.</span><span class="sxs-lookup"><span data-stu-id="f642a-127">Print queue on a printer spooler.</span></span><br/>                                      |
| <span data-ttu-id="f642a-128">Serviço</span><span class="sxs-lookup"><span data-stu-id="f642a-128">Service</span></span><br/>             | <span data-ttu-id="f642a-129">Aplicativo em execução como um serviço.</span><span class="sxs-lookup"><span data-stu-id="f642a-129">Application running as a service.</span></span><br/>                                      |
| <span data-ttu-id="f642a-130">FileService</span><span class="sxs-lookup"><span data-stu-id="f642a-130">FileService</span></span><br/>         | <span data-ttu-id="f642a-131">Serviços acessando o sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f642a-131">Services accessing file system.</span></span><br/>                                        |
| <span data-ttu-id="f642a-132">FileShare</span><span class="sxs-lookup"><span data-stu-id="f642a-132">FileShare</span></span><br/>           | <span data-ttu-id="f642a-133">Ponto de compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f642a-133">File share point.</span></span><br/>                                                      |
| <span data-ttu-id="f642a-134">Recurso</span><span class="sxs-lookup"><span data-stu-id="f642a-134">Resource</span></span><br/>            | <span data-ttu-id="f642a-135">Um recurso no serviço.</span><span class="sxs-lookup"><span data-stu-id="f642a-135">A resource in the service.</span></span><br/>                                             |
| <span data-ttu-id="f642a-136">Session</span><span class="sxs-lookup"><span data-stu-id="f642a-136">Session</span></span><br/>             | <span data-ttu-id="f642a-137">Uma conexão de serviço de arquivo ativo.</span><span class="sxs-lookup"><span data-stu-id="f642a-137">An active file service connection.</span></span><br/>                                     |
| <span data-ttu-id="f642a-138">Usuário</span><span class="sxs-lookup"><span data-stu-id="f642a-138">User</span></span><br/>                | <span data-ttu-id="f642a-139">Conta de usuário local.</span><span class="sxs-lookup"><span data-stu-id="f642a-139">Local user account.</span></span><br/>                                                    |
| <span data-ttu-id="f642a-140">Agrupar</span><span class="sxs-lookup"><span data-stu-id="f642a-140">Group</span></span><br/>               | <span data-ttu-id="f642a-141">Grupo local.</span><span class="sxs-lookup"><span data-stu-id="f642a-141">Local group.</span></span><br/>                                                           |
| <span data-ttu-id="f642a-142">UserCollection</span><span class="sxs-lookup"><span data-stu-id="f642a-142">UserCollection</span></span><br/>      | <span data-ttu-id="f642a-143">Coleção de usuários locais.</span><span class="sxs-lookup"><span data-stu-id="f642a-143">Collection of local users.</span></span><br/>                                             |
| <span data-ttu-id="f642a-144">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="f642a-144">GroupCollection</span></span><br/>     | <span data-ttu-id="f642a-145">Coleção de grupos locais.</span><span class="sxs-lookup"><span data-stu-id="f642a-145">Collection of local groups.</span></span><br/>                                            |
| <span data-ttu-id="f642a-146">Esquema</span><span class="sxs-lookup"><span data-stu-id="f642a-146">Schema</span></span><br/>              | <span data-ttu-id="f642a-147">Contêiner de esquema WinNT.</span><span class="sxs-lookup"><span data-stu-id="f642a-147">WinNT Schema container.</span></span><br/>                                                |
| <span data-ttu-id="f642a-148">Classe</span><span class="sxs-lookup"><span data-stu-id="f642a-148">Class</span></span><br/>               | <span data-ttu-id="f642a-149">Definição de classe de esquema.</span><span class="sxs-lookup"><span data-stu-id="f642a-149">Schema class definition.</span></span><br/>                                               |
| <span data-ttu-id="f642a-150">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f642a-150">Property</span></span><br/>            | <span data-ttu-id="f642a-151">Definição de atributo de esquema.</span><span class="sxs-lookup"><span data-stu-id="f642a-151">Schema attribute definition.</span></span><br/>                                           |
| <span data-ttu-id="f642a-152">Syntax</span><span class="sxs-lookup"><span data-stu-id="f642a-152">Syntax</span></span><br/>              | <span data-ttu-id="f642a-153">Sintaxe de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="f642a-153">Syntax of a property.</span></span><br/>                                                  |



 

 

 





