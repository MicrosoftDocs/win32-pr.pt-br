---
title: Segurança de estação de janela e direitos de acesso
description: A segurança permite que você controle o acesso a objetos de estação de janela. Para obter mais informações sobre segurança, consulte modelo de Access-Control.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105790255"
---
# <a name="window-station-security-and-access-rights"></a><span data-ttu-id="b8e0e-104">Segurança de estação de janela e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="b8e0e-104">Window Station Security and Access Rights</span></span>

<span data-ttu-id="b8e0e-105">A segurança permite que você controle o acesso a objetos de estação de janela.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-105">Security enables you to control access to window station objects.</span></span> <span data-ttu-id="b8e0e-106">Para obter mais informações sobre segurança, consulte [modelo de controle de acesso](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="b8e0e-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="b8e0e-107">Você pode especificar um [descritor de segurança](/windows/desktop/SecAuthZ/security-descriptors) para um objeto de estação de janela ao chamar a função [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) .</span><span class="sxs-lookup"><span data-stu-id="b8e0e-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a window station object when you call the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function.</span></span> <span data-ttu-id="b8e0e-108">Se você especificar NULL, a estação de janela obterá um descritor de segurança padrão.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-108">If you specify NULL, the window station gets a default security descriptor.</span></span> <span data-ttu-id="b8e0e-109">As ACLs no descritor de segurança padrão para uma estação de janela são provenientes do token principal ou de representação do criador.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-109">The ACLs in the default security descriptor for a window station come from the primary or impersonation token of the creator.</span></span>

<span data-ttu-id="b8e0e-110">Para obter ou definir o descritor de segurança de um objeto de estação de janela, chame as funções [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="b8e0e-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="b8e0e-111">Quando você chama a função [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) , o sistema verifica os direitos de acesso solicitados no descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-111">When you call the [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="b8e0e-112">Os direitos de acesso válidos para objetos de estação de janela incluem os [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights) e alguns direitos de acesso específicos ao objeto.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-112">The valid access rights for window station objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="b8e0e-113">A tabela a seguir lista os direitos de acesso padrão usados por todos os objetos.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="b8e0e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b8e0e-114">Value</span></span>                       | <span data-ttu-id="b8e0e-115">Significado</span><span class="sxs-lookup"><span data-stu-id="b8e0e-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e0e-116">EXCLUIR (0x00010000L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="b8e0e-117">Necessário para excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="b8e0e-118">\_Controle de leitura (0x00020000L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="b8e0e-119">Necessário para ler informações no descritor de segurança do objeto, não incluindo as informações na SACL.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="b8e0e-120">Para ler ou gravar a SACL, você deve solicitar o direito de acesso de segurança do sistema de acesso \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b8e0e-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="b8e0e-121">Para obter mais informações, consulte [direitos de acesso à SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="b8e0e-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="b8e0e-122">SINCRONIZAR (0x00100000L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="b8e0e-123">Sem suporte para objetos de estação de janela.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-123">Not supported for window station objects.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="b8e0e-124">GRAVAR \_ DAC (0x00040000L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="b8e0e-125">Necessário para modificar a DACL no descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="b8e0e-126">Proprietário da gravação \_ (0x00080000L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="b8e0e-127">Necessário para alterar o proprietário no descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="b8e0e-128">A tabela a seguir lista os direitos de acesso específicos ao objeto.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="b8e0e-129">Direito de acesso</span><span class="sxs-lookup"><span data-stu-id="b8e0e-129">Access right</span></span>                        | <span data-ttu-id="b8e0e-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8e0e-130">Description</span></span>                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e0e-131">WINSTA \_ todo o \_ acesso (0x37F)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-131">WINSTA\_ALL\_ACCESS (0x37F)</span></span>         | <span data-ttu-id="b8e0e-132">Todos os direitos de acesso possíveis para a estação de janela.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-132">All possible access rights for the window station.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="b8e0e-133">WINSTA \_ ACCESSCLIPBOARD (0x0004L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-133">WINSTA\_ACCESSCLIPBOARD (0x0004L)</span></span>   | <span data-ttu-id="b8e0e-134">Necessário para usar a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-134">Required to use the clipboard.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="b8e0e-135">WINSTA \_ ACCESSGLOBALATOMS (0x0020L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-135">WINSTA\_ACCESSGLOBALATOMS (0x0020L)</span></span> | <span data-ttu-id="b8e0e-136">Necessário para manipular Atoms globais.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-136">Required to manipulate global atoms.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="b8e0e-137">WINSTA \_ createdesktop (0x0008L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-137">WINSTA\_CREATEDESKTOP (0x0008L)</span></span>     | <span data-ttu-id="b8e0e-138">Necessário para criar novos objetos da área de trabalho na estação de janela.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-138">Required to create new desktop objects on the window station.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="b8e0e-139">WINSTA \_ ENUMDESKTOPS (0x0001L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-139">WINSTA\_ENUMDESKTOPS (0x0001L)</span></span>      | <span data-ttu-id="b8e0e-140">Necessário para enumerar objetos da área de trabalho existentes.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-140">Required to enumerate existing desktop objects.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="b8e0e-141">WINSTA \_ enumerar (0x0100L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-141">WINSTA\_ENUMERATE (0x0100L)</span></span>         | <span data-ttu-id="b8e0e-142">Necessário para que a estação de janela seja enumerada.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-142">Required for the window station to be enumerated.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="b8e0e-143">WINSTA \_ EXITWINDOWS (0x0040L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-143">WINSTA\_EXITWINDOWS (0x0040L)</span></span>       | <span data-ttu-id="b8e0e-144">Necessário para chamar com êxito a função [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) ou [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="b8e0e-144">Required to successfully call the [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span> <span data-ttu-id="b8e0e-145">As estações de janela podem ser compartilhadas por usuários e esse tipo de acesso pode impedir que outros usuários de uma estação de janela façam logoff do proprietário da estação de janela.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-145">Window stations can be shared by users and this access type can prevent other users of a window station from logging off the window station owner.</span></span> |
| <span data-ttu-id="b8e0e-146">WINSTA \_ ReadAttributes (0x0002L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-146">WINSTA\_READATTRIBUTES (0x0002L)</span></span>    | <span data-ttu-id="b8e0e-147">Necessário para ler os atributos de um objeto de estação de janela.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-147">Required to read the attributes of a window station object.</span></span> <span data-ttu-id="b8e0e-148">Esse atributo inclui configurações de cores e outras propriedades de estação de janela global.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-148">This attribute includes color settings and other global window station properties.</span></span>                                                                                                                                |
| <span data-ttu-id="b8e0e-149">WINSTA \_ READSCREEN (0x0200L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-149">WINSTA\_READSCREEN (0x0200L)</span></span>        | <span data-ttu-id="b8e0e-150">Necessário para acessar o conteúdo da tela.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-150">Required to access screen contents.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="b8e0e-151">WINSTA \_ WriteAttributes (0x0010L)</span><span class="sxs-lookup"><span data-stu-id="b8e0e-151">WINSTA\_WRITEATTRIBUTES (0x0010L)</span></span>   | <span data-ttu-id="b8e0e-152">Necessário para modificar os atributos de um objeto de estação de janela.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-152">Required to modify the attributes of a window station object.</span></span> <span data-ttu-id="b8e0e-153">Os atributos incluem configurações de cor e outras propriedades de estação de janela global.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-153">The attributes include color settings and other global window station properties.</span></span>                                                                                                                               |



 

<span data-ttu-id="b8e0e-154">A seguir estão os [direitos de acesso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para o objeto de estação de janela interativa, que é a estação de janela atribuída à sessão de logon do usuário interativo.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-154">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the interactive window station object, which is the window station assigned to the logon session of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b8e0e-155">Direito de acesso</span><span class="sxs-lookup"><span data-stu-id="b8e0e-155">Access right</span></span></th>
<th><span data-ttu-id="b8e0e-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8e0e-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b8e0e-157">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="b8e0e-157">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="b8e0e-158">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="b8e0e-158">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="b8e0e-159">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="b8e0e-159">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="b8e0e-160">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="b8e0e-160">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="b8e0e-161">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="b8e0e-161">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="b8e0e-162">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="b8e0e-162">WINSTA_READSCREEN</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8e0e-163">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="b8e0e-163">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="b8e0e-164">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="b8e0e-164">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="b8e0e-165">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="b8e0e-165">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="b8e0e-166">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="b8e0e-166">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="b8e0e-167">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="b8e0e-167">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b8e0e-168">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="b8e0e-168">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="b8e0e-169">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="b8e0e-169">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="b8e0e-170">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="b8e0e-170">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="b8e0e-171">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="b8e0e-171">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8e0e-172">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="b8e0e-172">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="b8e0e-173">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="b8e0e-173">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="b8e0e-174">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="b8e0e-174">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="b8e0e-175">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="b8e0e-175">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="b8e0e-176">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="b8e0e-176">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="b8e0e-177">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="b8e0e-177">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="b8e0e-178">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="b8e0e-178">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="b8e0e-179">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="b8e0e-179">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="b8e0e-180">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="b8e0e-180">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="b8e0e-181">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="b8e0e-181">WINSTA_READSCREEN</span></span><br />
<span data-ttu-id="b8e0e-182">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="b8e0e-182">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b8e0e-183">A seguir estão os [direitos de acesso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para um objeto de estação de janela não interativa.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-183">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a noninteractive window station object.</span></span> <span data-ttu-id="b8e0e-184">O sistema atribui estações de janela não interativas a todas as sessões de logon que não sejam do usuário interativo.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-184">The system assigns noninteractive window stations to all logon sessions other than that of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b8e0e-185">Direito de acesso</span><span class="sxs-lookup"><span data-stu-id="b8e0e-185">Access right</span></span></th>
<th><span data-ttu-id="b8e0e-186">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8e0e-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b8e0e-187">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="b8e0e-187">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="b8e0e-188">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="b8e0e-188">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="b8e0e-189">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="b8e0e-189">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="b8e0e-190">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="b8e0e-190">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="b8e0e-191">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="b8e0e-191">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8e0e-192">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="b8e0e-192">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="b8e0e-193">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="b8e0e-193">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="b8e0e-194">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="b8e0e-194">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="b8e0e-195">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="b8e0e-195">WINSTA_CREATEDESKTOP</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b8e0e-196">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="b8e0e-196">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="b8e0e-197">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="b8e0e-197">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="b8e0e-198">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="b8e0e-198">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="b8e0e-199">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="b8e0e-199">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8e0e-200">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="b8e0e-200">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="b8e0e-201">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="b8e0e-201">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="b8e0e-202">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="b8e0e-202">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="b8e0e-203">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="b8e0e-203">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="b8e0e-204">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="b8e0e-204">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="b8e0e-205">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="b8e0e-205">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="b8e0e-206">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="b8e0e-206">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="b8e0e-207">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="b8e0e-207">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="b8e0e-208">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="b8e0e-208">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b8e0e-209">Você pode solicitar o direito de acesso de segurança do sistema de acesso \_ \_ a um objeto de estação de janela se desejar ler ou gravar a SACL do objeto.</span><span class="sxs-lookup"><span data-stu-id="b8e0e-209">You can request the ACCESS\_SYSTEM\_SECURITY access right to a window station object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="b8e0e-210">Para obter mais informações, consulte [listas de controle de acesso (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) e [direito de acesso SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="b8e0e-210">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 