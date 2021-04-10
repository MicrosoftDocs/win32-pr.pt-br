---
description: Durante uma atualização do computador ou uma migração de computador a computador, os certificados em determinados repositórios de certificados serão migrados.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Migração do repositório de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31b42b83718aa1cab786ad79cc2df754b8fd9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011513"
---
# <a name="certificate-store-migration"></a><span data-ttu-id="3541b-103">Migração do repositório de certificados</span><span class="sxs-lookup"><span data-stu-id="3541b-103">Certificate Store Migration</span></span>

<span data-ttu-id="3541b-104">Durante uma atualização do computador ou uma migração de computador a computador, os certificados em determinados repositórios de certificados serão migrados.</span><span class="sxs-lookup"><span data-stu-id="3541b-104">During a computer upgrade or a computer-to-computer migration, the certificates in certain certificate stores will be migrated.</span></span> <span data-ttu-id="3541b-105">A tabela a seguir lista os repositórios de certificados que são migrados por padrão.</span><span class="sxs-lookup"><span data-stu-id="3541b-105">The following table lists the certificate stores that are migrated by default.</span></span> <span data-ttu-id="3541b-106">Para o repositório ACRS (configurações de solicitação de certificado) automática do sistema, somente as [*listas de certificados confiáveis*](../secgloss/c-gly.md) (CTLs) são migradas.</span><span class="sxs-lookup"><span data-stu-id="3541b-106">For the system Automatic Certificate Request Settings (ACRS) store, only the [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) are migrated.</span></span> <span data-ttu-id="3541b-107">Para todas as outras lojas listadas abaixo, somente os certificados são migrados.</span><span class="sxs-lookup"><span data-stu-id="3541b-107">For all other stores listed below, only the certificates are migrated.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3541b-108">Sistema/usuário</span><span class="sxs-lookup"><span data-stu-id="3541b-108">System/user</span></span></th>
<th><span data-ttu-id="3541b-109">Repositório</span><span class="sxs-lookup"><span data-stu-id="3541b-109">Store</span></span></th>
<th><span data-ttu-id="3541b-110">Local de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3541b-110">Storage location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3541b-111">$ {ROWSPAN8} $System $ {remover} $</span><span class="sxs-lookup"><span data-stu-id="3541b-111">${ROWSPAN8}$System${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="3541b-112">ROOT</span><span class="sxs-lookup"><span data-stu-id="3541b-112">ROOT</span></span></td>
<td><span data-ttu-id="3541b-113"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Raiz</strong> \ do <strong>Certificados</strong> do</span><span class="sxs-lookup"><span data-stu-id="3541b-113"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3541b-114">MY</span><span class="sxs-lookup"><span data-stu-id="3541b-114">MY</span></span></td>
<td><span data-ttu-id="3541b-115"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Meu</strong> \ <strong>Certificados</strong> do</span><span class="sxs-lookup"><span data-stu-id="3541b-115"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>My</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3541b-116">Quest</span><span class="sxs-lookup"><span data-stu-id="3541b-116">REQUEST</span></span></td>
<td><span data-ttu-id="3541b-117"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Solicitação</strong> \ do <strong>Certificados</strong> do</span><span class="sxs-lookup"><span data-stu-id="3541b-117"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Request</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3541b-118">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="3541b-118">TrustedPublisher</span></span></td>
<td><span data-ttu-id="3541b-119"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificados</strong> do</span><span class="sxs-lookup"><span data-stu-id="3541b-119"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3541b-120">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="3541b-120">TrustedPeople</span></span></td>
<td><span data-ttu-id="3541b-121"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificados</strong> do</span><span class="sxs-lookup"><span data-stu-id="3541b-121"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3541b-122">Não permitido</span><span class="sxs-lookup"><span data-stu-id="3541b-122">Disallowed</span></span></td>
<td><span data-ttu-id="3541b-123"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ Não <strong>permitido</strong> \ <strong>Certificados</strong> do</span><span class="sxs-lookup"><span data-stu-id="3541b-123"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3541b-124">AC</span><span class="sxs-lookup"><span data-stu-id="3541b-124">CA</span></span></td>
<td><span data-ttu-id="3541b-125"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>AC</strong> \ <strong>Certificados</strong> do</span><span class="sxs-lookup"><span data-stu-id="3541b-125"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3541b-126">ACRS</span><span class="sxs-lookup"><span data-stu-id="3541b-126">ACRS</span></span></td>
<td><span data-ttu-id="3541b-127"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>ACRS</strong> \ <strong>CTLs</strong></span><span class="sxs-lookup"><span data-stu-id="3541b-127"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>ACRS</strong>\<strong>CTLs</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td rowspan="7"><span data-ttu-id="3541b-128">Usuário $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="3541b-128">User${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="3541b-129">ROOT</span><span class="sxs-lookup"><span data-stu-id="3541b-129">ROOT</span></span></td>
<td><span data-ttu-id="3541b-130"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Raiz</strong> \ do <strong>Certificados</strong> do</span><span class="sxs-lookup"><span data-stu-id="3541b-130"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3541b-131">MY</span><span class="sxs-lookup"><span data-stu-id="3541b-131">MY</span></span></td>
<td><span data-ttu-id="3541b-132">arquivo: \\ %AppData%\Microsoft\SystemCertificates\My\Certificates</span><span class="sxs-lookup"><span data-stu-id="3541b-132">file:\\%APPDATA%\Microsoft\SystemCertificates\My\Certificates</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3541b-133">Quest</span><span class="sxs-lookup"><span data-stu-id="3541b-133">REQUEST</span></span></td>
<td><span data-ttu-id="3541b-134">arquivo: \\ %AppData%\Microsoft\SystemCertificates\Request\Certificates</span><span class="sxs-lookup"><span data-stu-id="3541b-134">file:\\%APPDATA%\Microsoft\SystemCertificates\Request\Certificates</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3541b-135">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="3541b-135">TrustedPublisher</span></span></td>
<td><span data-ttu-id="3541b-136"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificados</strong> do</span><span class="sxs-lookup"><span data-stu-id="3541b-136"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3541b-137">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="3541b-137">TrustedPeople</span></span></td>
<td><span data-ttu-id="3541b-138"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificados</strong> do</span><span class="sxs-lookup"><span data-stu-id="3541b-138"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3541b-139">Não permitido</span><span class="sxs-lookup"><span data-stu-id="3541b-139">Disallowed</span></span></td>
<td><span data-ttu-id="3541b-140"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ Não <strong>permitido</strong> \ <strong>Certificados</strong> do</span><span class="sxs-lookup"><span data-stu-id="3541b-140"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3541b-141">AC</span><span class="sxs-lookup"><span data-stu-id="3541b-141">CA</span></span></td>
<td><span data-ttu-id="3541b-142"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>AC</strong> \ <strong>Certificados</strong> do</span><span class="sxs-lookup"><span data-stu-id="3541b-142"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="3541b-143">Outros repositórios de certificados criados por aplicativos não são migrados por padrão.</span><span class="sxs-lookup"><span data-stu-id="3541b-143">Other certificate stores created by applications are not migrated by default.</span></span> <span data-ttu-id="3541b-144">Os aplicativos que criam suas próprias lojas são responsáveis pela migração das lojas que eles criam.</span><span class="sxs-lookup"><span data-stu-id="3541b-144">Applications that create their own stores are responsible for migration of the stores that they create.</span></span> <span data-ttu-id="3541b-145">Para criar lojas, recomendamos que você defina uma chave do registro nas configurações do aplicativo e crie um repositório dentro das configurações do registro usando o provedor de repositório de **certificados \_ \_ Prov \_ reg** Store.</span><span class="sxs-lookup"><span data-stu-id="3541b-145">To create stores, we recommend that you define a registry key in the application settings and create a store within the registry settings by using the **CERT\_STORE\_PROV\_REG** store provider.</span></span> <span data-ttu-id="3541b-146">Para obter mais informações sobre como migrar configurações de aplicativo, consulte o tópico *como criar um arquivo personalizado. xml* no guia *usando o USMT 3,0* em [ferramenta de migração do usuário 3,0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx).</span><span class="sxs-lookup"><span data-stu-id="3541b-146">For more information about migrating application settings, see the *How To Create a Custom .xml File* topic in the *Using USMT 3.0* guide at [User State Migration Tool 3.0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx).</span></span> <span data-ttu-id="3541b-147">(Esse recurso pode não estar disponível em alguns idiomas e países ou regiões.)</span><span class="sxs-lookup"><span data-stu-id="3541b-147">(This resource may not be available in some languages and countries or regions.)</span></span>

 

 
