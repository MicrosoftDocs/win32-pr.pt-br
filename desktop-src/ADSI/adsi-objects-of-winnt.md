---
title: Objetos ADSI do WinNT
description: O provedor do ADSI WinNT implementa os seguintes objetos COM para dar suporte a recursos e serviços de várias interfaces ADSI.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- ADSI do provedor de serviços do WinNT, objetos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d0c9e5c486d07e1e392a9f307ecd9af4509ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084013"
---
# <a name="adsi-objects-of-winnt"></a><span data-ttu-id="3eac6-104">Objetos ADSI do WinNT</span><span class="sxs-lookup"><span data-stu-id="3eac6-104">ADSI Objects of WinNT</span></span>

<span data-ttu-id="3eac6-105">O provedor do ADSI WinNT implementa os seguintes objetos COM para dar suporte a recursos e serviços de várias interfaces ADSI.</span><span class="sxs-lookup"><span data-stu-id="3eac6-105">The ADSI WinNT provider implement the following COM objects to support features and services of various ADSI interfaces.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3eac6-106">Objeto ADSI</span><span class="sxs-lookup"><span data-stu-id="3eac6-106">ADSI Object</span></span></th>
<th><span data-ttu-id="3eac6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3eac6-107">Description</span></span></th>
<th><span data-ttu-id="3eac6-108">Interfaces com suporte</span><span class="sxs-lookup"><span data-stu-id="3eac6-108">Supported Interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eac6-109"><strong>Classe</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-109"><strong>Class</strong></span></span></td>
<td><span data-ttu-id="3eac6-110">Um objeto ADSI que representa uma definição de classe.</span><span class="sxs-lookup"><span data-stu-id="3eac6-110">An ADSI object that represents a class definition.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"> <strong>IADsClass</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>IADsClass</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-112"><strong>Computador</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-112"><strong>Computer</strong></span></span></td>
<td><span data-ttu-id="3eac6-113">Um objeto ADSI que representa um computador.</span><span class="sxs-lookup"><span data-stu-id="3eac6-113">An ADSI object that represents a computer.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-115"><strong>Domínio</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-115"><strong>Domain</strong></span></span></td>
<td><span data-ttu-id="3eac6-116">Um objeto ADSI que representa um domínio pela rede.</span><span class="sxs-lookup"><span data-stu-id="3eac6-116">An ADSI object that represents a domain over the network.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-118"><strong>FileService</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-118"><strong>FileService</strong></span></span></td>
<td><span data-ttu-id="3eac6-119">Um objeto ADSI que representa um serviço de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3eac6-119">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-121"><strong>FileShare</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-121"><strong>FileShare</strong></span></span></td>
<td><span data-ttu-id="3eac6-122">Um objeto ADSI que representa um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3eac6-122">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-124"><strong>FPNWFileService</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-124"><strong>FPNWFileService</strong></span></span></td>
<td><span data-ttu-id="3eac6-125">Um objeto ADSI que representa um serviço de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3eac6-125">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-127"><strong>FPNWFileShare</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-127"><strong>FPNWFileShare</strong></span></span></td>
<td><span data-ttu-id="3eac6-128">Um objeto ADSI que representa um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3eac6-128">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-130"><strong>FPNWResource</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-130"><strong>FPNWResource</strong></span></span></td>
<td><span data-ttu-id="3eac6-131">Um objeto ADSI que representa um recurso.</span><span class="sxs-lookup"><span data-stu-id="3eac6-131">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-133"><strong>FPNWResourcesCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-133"><strong>FPNWResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="3eac6-134">Um objeto ADSI que representa uma coleção de recursos.</span><span class="sxs-lookup"><span data-stu-id="3eac6-134">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="3eac6-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADscollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3eac6-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-136"><strong>FPNWSession</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-136"><strong>FPNWSession</strong></span></span></td>
<td><span data-ttu-id="3eac6-137">Um objeto ADSI que representa uma sessão.</span><span class="sxs-lookup"><span data-stu-id="3eac6-137">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-139"><strong>FPNWSessionsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-139"><strong>FPNWSessionsCollection</strong></span></span></td>
<td><span data-ttu-id="3eac6-140">Um objeto ADSI que representa uma coleção de sessões.</span><span class="sxs-lookup"><span data-stu-id="3eac6-140">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="3eac6-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADscollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3eac6-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-142"><strong>Grupo</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-142"><strong>Group</strong></span></span></td>
<td><span data-ttu-id="3eac6-143">Um objeto ADSI que representa um grupo.</span><span class="sxs-lookup"><span data-stu-id="3eac6-143">An ADSI object that represents a group.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl>
<blockquote>
[!Note]<br />
<span data-ttu-id="3eac6-145">GetInfo não pode ser usada para grupos que contêm membros que são entidades de segurança wellKnown no escopo WinNT.</span><span class="sxs-lookup"><span data-stu-id="3eac6-145">GetInfo cannot be used for groups that contain members that are wellKnown security principals in the WinNT scope.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-146"><strong>GroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-146"><strong>GroupCollection</strong></span></span></td>
<td><span data-ttu-id="3eac6-147">Um objeto ADSI que representa uma coleção de grupos.</span><span class="sxs-lookup"><span data-stu-id="3eac6-147">An ADSI object that represents a collection of groups.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-149"><strong>Localgroup</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-149"><strong>LocalGroup</strong></span></span></td>
<td><span data-ttu-id="3eac6-150">Um objeto ADSI que representa um grupo local.</span><span class="sxs-lookup"><span data-stu-id="3eac6-150">An ADSI object that represents a local group.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-152"><strong>LocalgroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-152"><strong>LocalgroupCollection</strong></span></span></td>
<td><span data-ttu-id="3eac6-153">Um objeto ADSI que representa uma coleção de grupos locais.</span><span class="sxs-lookup"><span data-stu-id="3eac6-153">An ADSI object that represents a collection of local groups.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-155"><strong>Namespace</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-155"><strong>Namespace</strong></span></span></td>
<td><span data-ttu-id="3eac6-156">Um objeto ADSI que representa o namespace WinNT.</span><span class="sxs-lookup"><span data-stu-id="3eac6-156">An ADSI object that represents the WinNT namespace.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-158"><strong>PrintJob</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-158"><strong>PrintJob</strong></span></span></td>
<td><span data-ttu-id="3eac6-159">Um objeto ADSI que representa um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="3eac6-159">An ADSI object that represents a print job.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-161"><strong>Trabalhos de trabalho</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-161"><strong>PrintJobsCollection</strong></span></span></td>
<td><span data-ttu-id="3eac6-162">Um objeto ADSI que representa uma coleção de trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="3eac6-162">An ADSI object that represents a collection of print jobs.</span></span></td>
<td><span data-ttu-id="3eac6-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADscollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3eac6-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-164"><strong>PrintQueue</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-164"><strong>PrintQueue</strong></span></span></td>
<td><span data-ttu-id="3eac6-165">Um objeto ADSI que representa uma fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="3eac6-165">An ADSI object that represents a print queue.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-167"><strong>Propriedade</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-167"><strong>Property</strong></span></span></td>
<td><span data-ttu-id="3eac6-168">Um objeto ADSI que representa uma definição de atributo.</span><span class="sxs-lookup"><span data-stu-id="3eac6-168">An ADSI object that represents an attribute definition.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong>iadsproperty</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"><strong>IADsProperty</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-170"><strong>Recurso</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-170"><strong>Resource</strong></span></span></td>
<td><span data-ttu-id="3eac6-171">Um objeto ADSI que representa um recurso.</span><span class="sxs-lookup"><span data-stu-id="3eac6-171">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-173"><strong>Recursos</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-173"><strong>ResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="3eac6-174">Um objeto ADSI que representa uma coleção de recursos.</span><span class="sxs-lookup"><span data-stu-id="3eac6-174">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="3eac6-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADscollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3eac6-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-176"><strong>Esquema</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-176"><strong>Schema</strong></span></span></td>
<td><span data-ttu-id="3eac6-177">Um objeto ADSI que representa o contêiner de esquema.</span><span class="sxs-lookup"><span data-stu-id="3eac6-177">An ADSI object that represents the schema container.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>IADsContainer</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-179"><strong>Serviço</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-179"><strong>Service</strong></span></span></td>
<td><span data-ttu-id="3eac6-180">Um objeto ADSI que representa um serviço.</span><span class="sxs-lookup"><span data-stu-id="3eac6-180">An ADSI object that represents a service.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-182"><strong>Sessão</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-182"><strong>Session</strong></span></span></td>
<td><span data-ttu-id="3eac6-183">Um objeto ADSI que representa uma sessão.</span><span class="sxs-lookup"><span data-stu-id="3eac6-183">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-185"><strong>Sessõescollection</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-185"><strong>SessionsCollection</strong></span></span></td>
<td><span data-ttu-id="3eac6-186">Um objeto ADSI que representa uma coleção de sessões.</span><span class="sxs-lookup"><span data-stu-id="3eac6-186">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="3eac6-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADscollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3eac6-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-188"><strong>Sintaxe</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-188"><strong>Syntax</strong></span></span></td>
<td><span data-ttu-id="3eac6-189">Um objeto ADSI que representa a sintaxe de um atributo.</span><span class="sxs-lookup"><span data-stu-id="3eac6-189">An ADSI object that represents the syntax of an attribute.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"> <strong>IADsSyntax</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"><strong>IADsSyntax</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac6-191"><strong>Usuário</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-191"><strong>User</strong></span></span></td>
<td><span data-ttu-id="3eac6-192">Um objeto ADSI que representa uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="3eac6-192">An ADSI object that represents a user account.</span></span></td>
<td><dl> <span data-ttu-id="3eac6-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3eac6-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eac6-194"><strong>Usergroupcollection</strong></span><span class="sxs-lookup"><span data-stu-id="3eac6-194"><strong>UserGroupCollection</strong></span></span></td>
<td><span data-ttu-id="3eac6-195">Um objeto ADSI que representa uma coleção de grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="3eac6-195">An ADSI object that represents a collection of user groups.</span></span></td>
<td><span data-ttu-id="3eac6-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></span><span class="sxs-lookup"><span data-stu-id="3eac6-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





