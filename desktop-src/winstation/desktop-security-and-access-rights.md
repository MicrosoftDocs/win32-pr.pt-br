---
title: Segurança de desktop e direitos de acesso
description: A segurança permite que você controle o acesso a objetos da área de trabalho. Para obter mais informações sobre segurança, consulte modelo de Access-Control.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d18b48e0b80dc39ea1b3f65a77acb615c4cb8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366336"
---
# <a name="desktop-security-and-access-rights"></a><span data-ttu-id="cd21b-104">Segurança de desktop e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="cd21b-104">Desktop Security and Access Rights</span></span>

<span data-ttu-id="cd21b-105">A segurança permite que você controle o acesso a objetos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cd21b-105">Security enables you to control access to desktop objects.</span></span> <span data-ttu-id="cd21b-106">Para obter mais informações sobre segurança, consulte [modelo de controle de acesso](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="cd21b-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="cd21b-107">Você pode especificar um [descritor de segurança](/windows/desktop/SecAuthZ/security-descriptors) para um objeto de área de trabalho ao chamar a função [**createdesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) ou [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) .</span><span class="sxs-lookup"><span data-stu-id="cd21b-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a desktop object when you call the [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function.</span></span> <span data-ttu-id="cd21b-108">Se você especificar NULL, a área de trabalho obterá um descritor de segurança padrão.</span><span class="sxs-lookup"><span data-stu-id="cd21b-108">If you specify NULL, the desktop gets a default security descriptor.</span></span> <span data-ttu-id="cd21b-109">As ACLs no descritor de segurança padrão de uma área de trabalho são provenientes de sua estação de janela pai.</span><span class="sxs-lookup"><span data-stu-id="cd21b-109">The ACLs in the default security descriptor for a desktop come from its parent window station.</span></span>

<span data-ttu-id="cd21b-110">Para obter ou definir o descritor de segurança de um objeto de estação de janela, chame as funções [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="cd21b-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="cd21b-111">Quando você chama a função [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) ou [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) , o sistema verifica os direitos de acesso solicitados no descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="cd21b-111">When you call the [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) or [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="cd21b-112">Os direitos de acesso válidos para objetos da área de trabalho incluem os [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights) e alguns direitos de acesso específicos ao objeto.</span><span class="sxs-lookup"><span data-stu-id="cd21b-112">The valid access rights for desktop objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="cd21b-113">A tabela a seguir lista os direitos de acesso padrão usados por todos os objetos.</span><span class="sxs-lookup"><span data-stu-id="cd21b-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="cd21b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="cd21b-114">Value</span></span>                       | <span data-ttu-id="cd21b-115">Significado</span><span class="sxs-lookup"><span data-stu-id="cd21b-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd21b-116">EXCLUIR (0x00010000L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="cd21b-117">Necessário para excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="cd21b-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="cd21b-118">\_Controle de leitura (0x00020000L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="cd21b-119">Necessário para ler informações no descritor de segurança do objeto, não incluindo as informações na SACL.</span><span class="sxs-lookup"><span data-stu-id="cd21b-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="cd21b-120">Para ler ou gravar a SACL, você deve solicitar o direito de acesso de segurança do sistema de acesso \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cd21b-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="cd21b-121">Para obter mais informações, consulte [direitos de acesso à SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="cd21b-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="cd21b-122">SINCRONIZAR (0x00100000L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="cd21b-123">Sem suporte para objetos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cd21b-123">Not supported for desktop objects.</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cd21b-124">GRAVAR \_ DAC (0x00040000L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="cd21b-125">Necessário para modificar a DACL no descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="cd21b-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="cd21b-126">Proprietário da gravação \_ (0x00080000L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="cd21b-127">Necessário para alterar o proprietário no descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="cd21b-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="cd21b-128">A tabela a seguir lista os direitos de acesso específicos ao objeto.</span><span class="sxs-lookup"><span data-stu-id="cd21b-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="cd21b-129">Direito de acesso</span><span class="sxs-lookup"><span data-stu-id="cd21b-129">Access right</span></span>                       | <span data-ttu-id="cd21b-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd21b-130">Description</span></span>                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd21b-131">CreateMenu da área \_ de trabalho (0x0004L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-131">DESKTOP\_CREATEMENU (0x0004L)</span></span>      | <span data-ttu-id="cd21b-132">Necessário para criar um menu na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cd21b-132">Required to create a menu on the desktop.</span></span>                                                   |
| <span data-ttu-id="cd21b-133">DESKTOP \_ CREATEWINDOW (0x0002L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-133">DESKTOP\_CREATEWINDOW (0x0002L)</span></span>    | <span data-ttu-id="cd21b-134">Necessário para criar uma janela na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cd21b-134">Required to create a window on the desktop.</span></span>                                                 |
| <span data-ttu-id="cd21b-135">\_Enumerar desktops (0x0040L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-135">DESKTOP\_ENUMERATE (0x0040L)</span></span>       | <span data-ttu-id="cd21b-136">Necessário para que a área de trabalho seja enumerada.</span><span class="sxs-lookup"><span data-stu-id="cd21b-136">Required for the desktop to be enumerated.</span></span>                                                  |
| <span data-ttu-id="cd21b-137">HOOKCONTROL da área \_ de trabalho (0x0008L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-137">DESKTOP\_HOOKCONTROL (0x0008L)</span></span>     | <span data-ttu-id="cd21b-138">Necessário para estabelecer qualquer um dos ganchos de janela.</span><span class="sxs-lookup"><span data-stu-id="cd21b-138">Required to establish any of the window hooks.</span></span>                                              |
| <span data-ttu-id="cd21b-139">JOURNALPLAYBACK da área \_ de trabalho (0x0020L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-139">DESKTOP\_JOURNALPLAYBACK (0x0020L)</span></span> | <span data-ttu-id="cd21b-140">Necessário para executar a reprodução do diário em uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cd21b-140">Required to perform journal playback on a desktop.</span></span>                                          |
| <span data-ttu-id="cd21b-141">JOURNALRECORD da área \_ de trabalho (0x0010L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-141">DESKTOP\_JOURNALRECORD (0x0010L)</span></span>   | <span data-ttu-id="cd21b-142">Necessário para executar a gravação do diário em uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cd21b-142">Required to perform journal recording on a desktop.</span></span>                                         |
| <span data-ttu-id="cd21b-143">READOBJECTS da área \_ de trabalho (0x0001L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-143">DESKTOP\_READOBJECTS (0x0001L)</span></span>     | <span data-ttu-id="cd21b-144">Necessário para ler objetos na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cd21b-144">Required to read objects on the desktop.</span></span>                                                    |
| <span data-ttu-id="cd21b-145">SWITCHDESKTOP da área \_ de trabalho (0x0100L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-145">DESKTOP\_SWITCHDESKTOP (0x0100L)</span></span>   | <span data-ttu-id="cd21b-146">Necessário para ativar a área de trabalho usando a função [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) .</span><span class="sxs-lookup"><span data-stu-id="cd21b-146">Required to activate the desktop using the [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) function.</span></span> |
| <span data-ttu-id="cd21b-147">WRITEOBJECTS da área \_ de trabalho (0x0080L)</span><span class="sxs-lookup"><span data-stu-id="cd21b-147">DESKTOP\_WRITEOBJECTS (0x0080L)</span></span>    | <span data-ttu-id="cd21b-148">Necessário para gravar objetos na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cd21b-148">Required to write objects on the desktop.</span></span>                                                   |



 

<span data-ttu-id="cd21b-149">A seguir estão os [direitos de acesso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para um objeto de área de trabalho contido na estação de janela interativa da sessão de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="cd21b-149">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a desktop object contained in the interactive window station of the user's logon session.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cd21b-150">Direito de acesso</span><span class="sxs-lookup"><span data-stu-id="cd21b-150">Access right</span></span></th>
<th><span data-ttu-id="cd21b-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd21b-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd21b-152">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="cd21b-152">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="cd21b-153">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="cd21b-153">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="cd21b-154">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="cd21b-154">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="cd21b-155">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="cd21b-155">STANDARD_RIGHTS_READ</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd21b-156">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="cd21b-156">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="cd21b-157">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="cd21b-157">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="cd21b-158">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="cd21b-158">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="cd21b-159">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="cd21b-159">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="cd21b-160">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="cd21b-160">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="cd21b-161">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="cd21b-161">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="cd21b-162">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="cd21b-162">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="cd21b-163">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="cd21b-163">STANDARD_RIGHTS_WRITE</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd21b-164">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="cd21b-164">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="cd21b-165">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="cd21b-165">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="cd21b-166">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="cd21b-166">STANDARD_RIGHTS_EXECUTE</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd21b-167">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="cd21b-167">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="cd21b-168">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="cd21b-168">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="cd21b-169">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="cd21b-169">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="cd21b-170">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="cd21b-170">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="cd21b-171">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="cd21b-171">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="cd21b-172">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="cd21b-172">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="cd21b-173">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="cd21b-173">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="cd21b-174">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="cd21b-174">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="cd21b-175">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="cd21b-175">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="cd21b-176">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="cd21b-176">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="cd21b-177">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="cd21b-177">STANDARD_RIGHTS_REQUIRED</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cd21b-178">Você pode solicitar o direito de acesso de segurança do sistema de acesso \_ \_ a um objeto de área de trabalho se quiser ler ou gravar a SACL do objeto.</span><span class="sxs-lookup"><span data-stu-id="cd21b-178">You can request the ACCESS\_SYSTEM\_SECURITY access right to a desktop object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="cd21b-179">Para obter mais informações, consulte [listas de controle de acesso (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) e [direito de acesso SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="cd21b-179">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 