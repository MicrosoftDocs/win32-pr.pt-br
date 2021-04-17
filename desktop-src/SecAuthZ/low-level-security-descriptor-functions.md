---
description: Funções para configurar e recuperar um descritor de segurança de objetos.
ms.assetid: 22bf0d6b-3ec6-4c28-ace4-49e48714f4bf
title: 'Funções de descritor de segurança de nível inferior '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72406dc2481e4671d8d535327f416a2d003c3a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755565"
---
# <a name="low-level-security-descriptor-functions"></a><span data-ttu-id="ff83f-103">Funções de descritor de segurança de nível inferior </span><span class="sxs-lookup"><span data-stu-id="ff83f-103">Low-level Security Descriptor Functions</span></span>

<span data-ttu-id="ff83f-104">Há vários pares de funções de nível baixo para configurar e recuperar o [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)de um objeto.</span><span class="sxs-lookup"><span data-stu-id="ff83f-104">There are several pairs of low-level functions for setting and retrieving an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="ff83f-105">Cada um desses pares funciona apenas com um conjunto limitado de objetos do Windows.</span><span class="sxs-lookup"><span data-stu-id="ff83f-105">Each of these pairs works only with a limited set of Windows objects.</span></span> <span data-ttu-id="ff83f-106">Por exemplo, um par funciona com objetos de arquivo e outro funciona com chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="ff83f-106">For example, one pair works with file objects and another works with registry keys.</span></span> <span data-ttu-id="ff83f-107">A tabela a seguir mostra as funções de nível baixo a serem usadas com os diferentes tipos de objetos protegíveis.</span><span class="sxs-lookup"><span data-stu-id="ff83f-107">The following table shows the low-level functions to use with the different types of securable objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff83f-108">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="ff83f-108">Object type</span></span></th>
<th><span data-ttu-id="ff83f-109">Funções de nível baixo</span><span class="sxs-lookup"><span data-stu-id="ff83f-109">Low-level functions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ff83f-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Arquivos</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Files</a></span></span></li>
<li><span data-ttu-id="ff83f-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Listas</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directories</a></span></span></li>
<li><span data-ttu-id="ff83f-112">Processadores</span><span class="sxs-lookup"><span data-stu-id="ff83f-112">Mailslots</span></span></li>
<li><span data-ttu-id="ff83f-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Pipes nomeados</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Named pipes</a></span></span></li>
</ul></td>
<td><span data-ttu-id="ff83f-114">Use as funções <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> e <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ff83f-114">Use the <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> and <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> functions.</span></span> <span data-ttu-id="ff83f-115">Essas funções usam cadeias de caracteres para identificar o objeto protegível, em vez de usar identificadores.</span><span class="sxs-lookup"><span data-stu-id="ff83f-115">These functions use character strings to identify the securable object, instead of using handles.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="ff83f-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Processos</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Processes</a></span></span></li>
<li><span data-ttu-id="ff83f-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Threads</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Threads</a></span></span></li>
<li><span data-ttu-id="ff83f-118"><a href="access-rights-for-access-token-objects.md">Tokens de acesso</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-118"><a href="access-rights-for-access-token-objects.md">Access tokens</a></span></span></li>
<li><span data-ttu-id="ff83f-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">Objetos de mapeamento de arquivos</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">File-mapping objects</a></span></span></li>
<li><span data-ttu-id="ff83f-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semáforos</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semaphores</a></span></span></li>
<li><span data-ttu-id="ff83f-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Eventos</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Events</a></span></span></li>
<li><span data-ttu-id="ff83f-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexes</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexes</a></span></span></li>
<li><span data-ttu-id="ff83f-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Temporizadores esperados</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Waitable timers</a></span></span></li>
</ul></td>
<td><span data-ttu-id="ff83f-124">Use as funções <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> e <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ff83f-124">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ff83f-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Estações de janela</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Window stations</a></span></span></li>
<li><span data-ttu-id="ff83f-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktops</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktops</a></span></span></li>
</ul></td>
<td><span data-ttu-id="ff83f-127">Use as funções <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> e <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ff83f-127">Use the <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="ff83f-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Chaves do Registro</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry keys</a></span></span></li>
</ul></td>
<td><span data-ttu-id="ff83f-129">Use as funções <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> e <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ff83f-129">Use the <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> and <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ff83f-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Objetos de serviço do Windows</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Windows service objects</a></span></span></li>
</ul></td>
<td><span data-ttu-id="ff83f-131">Use as funções <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> e <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ff83f-131">Use the <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="ff83f-132">Objetos de impressora</span><span class="sxs-lookup"><span data-stu-id="ff83f-132">Printer objects</span></span></li>
</ul></td>
<td><span data-ttu-id="ff83f-133">Use a estrutura de <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> com as funções <a href="/windows/desktop/printdocs/getprinter"><strong>getimpressor</strong></a> e <a href="/windows/desktop/printdocs/setprinter"><strong>setprinter</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ff83f-133">Use the <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> structure with the <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> and <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ff83f-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Compartilhamentos de rede</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Network shares</a></span></span></li>
</ul></td>
<td><span data-ttu-id="ff83f-135">Use o nível 502 com as funções <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> e <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ff83f-135">Use level 502 with the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> and <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="ff83f-136"><a href="acl-based-access-control.md">Objetos privados (objetos privados ao aplicativo de criação)</a></span><span class="sxs-lookup"><span data-stu-id="ff83f-136"><a href="acl-based-access-control.md">Private objects (objects private to the creating application)</a></span></span></li>
</ul></td>
<td><span data-ttu-id="ff83f-137">Use as funções <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> e <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ff83f-137">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> functions.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
