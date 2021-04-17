---
description: Lista os tipos de ACE definidos atualmente.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (WinNT. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d06b3457e4df6aea38d3e35acf4f7aaa4e2f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751326"
---
# <a name="ace"></a><span data-ttu-id="4687d-103">PERFEITA</span><span class="sxs-lookup"><span data-stu-id="4687d-103">ACE</span></span>

<span data-ttu-id="4687d-104">Uma **Ace** é uma [*entrada de controle de acesso*](/windows/desktop/SecGloss/a-gly) em uma ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ).</span><span class="sxs-lookup"><span data-stu-id="4687d-104">An **ACE** is an [*access control entry*](/windows/desktop/SecGloss/a-gly) in an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL).</span></span>

<span data-ttu-id="4687d-105">A tabela a seguir lista os tipos de **Ace** definidos atualmente.</span><span class="sxs-lookup"><span data-stu-id="4687d-105">The following table lists the currently defined **ACE** types.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4687d-106">Tipo de ACE</span><span class="sxs-lookup"><span data-stu-id="4687d-106">ACE type</span></span></th>
<th><span data-ttu-id="4687d-107">Estrutura</span><span class="sxs-lookup"><span data-stu-id="4687d-107">Structure</span></span></th>
<th><span data-ttu-id="4687d-108">Tipo de ACL</span><span class="sxs-lookup"><span data-stu-id="4687d-108">ACL type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4687d-109">Acesso permitido</span><span class="sxs-lookup"><span data-stu-id="4687d-109">Access allowed</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-110"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-110"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-111">DACL</span><span class="sxs-lookup"><span data-stu-id="4687d-111">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="4687d-112">Acesso permitido</span><span class="sxs-lookup"><span data-stu-id="4687d-112">Access allowed</span></span></li>
<li><span data-ttu-id="4687d-113">Permite o retorno de chamada durante a verificação de acesso</span><span class="sxs-lookup"><span data-stu-id="4687d-113">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-114"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-114"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-115">DACL</span><span class="sxs-lookup"><span data-stu-id="4687d-115">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4687d-116">Acesso permitido</span><span class="sxs-lookup"><span data-stu-id="4687d-116">Access allowed</span></span></li>
<li><span data-ttu-id="4687d-117">Específico do objeto</span><span class="sxs-lookup"><span data-stu-id="4687d-117">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-118"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-118"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-119">DACL</span><span class="sxs-lookup"><span data-stu-id="4687d-119">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="4687d-120">Acesso permitido</span><span class="sxs-lookup"><span data-stu-id="4687d-120">Access allowed</span></span></li>
<li><span data-ttu-id="4687d-121">Específico do objeto</span><span class="sxs-lookup"><span data-stu-id="4687d-121">Object specific</span></span></li>
<li><span data-ttu-id="4687d-122">Permite o retorno de chamada durante a verificação de acesso</span><span class="sxs-lookup"><span data-stu-id="4687d-122">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-123"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-123"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-124">DACL</span><span class="sxs-lookup"><span data-stu-id="4687d-124">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4687d-125">Acesso negado</span><span class="sxs-lookup"><span data-stu-id="4687d-125">Access denied</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-126"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-126"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-127">DACL</span><span class="sxs-lookup"><span data-stu-id="4687d-127">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="4687d-128">Acesso negado</span><span class="sxs-lookup"><span data-stu-id="4687d-128">Access denied</span></span></li>
<li><span data-ttu-id="4687d-129">Permite o retorno de chamada durante a verificação de acesso</span><span class="sxs-lookup"><span data-stu-id="4687d-129">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-130"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-130"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-131">DACL</span><span class="sxs-lookup"><span data-stu-id="4687d-131">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4687d-132">Acesso negado</span><span class="sxs-lookup"><span data-stu-id="4687d-132">Access denied</span></span></li>
<li><span data-ttu-id="4687d-133">Específico do objeto</span><span class="sxs-lookup"><span data-stu-id="4687d-133">Object specific</span></span></li>
<li><span data-ttu-id="4687d-134">Permite o retorno de chamada durante a verificação de acesso</span><span class="sxs-lookup"><span data-stu-id="4687d-134">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-135"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-135"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-136">DACL</span><span class="sxs-lookup"><span data-stu-id="4687d-136">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="4687d-137">Acesso negado</span><span class="sxs-lookup"><span data-stu-id="4687d-137">Access denied</span></span></li>
<li><span data-ttu-id="4687d-138">Específico do objeto</span><span class="sxs-lookup"><span data-stu-id="4687d-138">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-139"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-139"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-140">DACL</span><span class="sxs-lookup"><span data-stu-id="4687d-140">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4687d-141">Alarme do sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-141">System alarm</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-142"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-142"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-143">Sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-143">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="4687d-144">Alarme do sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-144">System alarm</span></span></li>
<li><span data-ttu-id="4687d-145">Permite o retorno de chamada durante a verificação de acesso</span><span class="sxs-lookup"><span data-stu-id="4687d-145">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-146"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-146"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-147">Sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-147">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4687d-148">Alarme do sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-148">System alarm</span></span></li>
<li><span data-ttu-id="4687d-149">Específico do objeto</span><span class="sxs-lookup"><span data-stu-id="4687d-149">Object specific</span></span></li>
<li><span data-ttu-id="4687d-150">Permite o retorno de chamada durante a verificação de acesso</span><span class="sxs-lookup"><span data-stu-id="4687d-150">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-151"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-151"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-152">Sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-152">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="4687d-153">Alarme do sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-153">System alarm</span></span></li>
<li><span data-ttu-id="4687d-154">Específico do objeto</span><span class="sxs-lookup"><span data-stu-id="4687d-154">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-155"><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-155"><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-156">Sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-156">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4687d-157">Auditoria do sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-157">System audit</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-158"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-158"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-159">Sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-159">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="4687d-160">Auditoria do sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-160">System audit</span></span></li>
<li><span data-ttu-id="4687d-161">Permite o retorno de chamada durante a verificação de acesso</span><span class="sxs-lookup"><span data-stu-id="4687d-161">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-162"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-162"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-163">Sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-163">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4687d-164">Auditoria do sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-164">System audit</span></span></li>
<li><span data-ttu-id="4687d-165">Específico do objeto</span><span class="sxs-lookup"><span data-stu-id="4687d-165">Object specific</span></span></li>
<li><span data-ttu-id="4687d-166">Permite o retorno de chamada durante a verificação de acesso</span><span class="sxs-lookup"><span data-stu-id="4687d-166">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-167"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-167"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-168">Sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-168">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="4687d-169">Auditoria do sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-169">System audit</span></span></li>
<li><span data-ttu-id="4687d-170">Específico do objeto</span><span class="sxs-lookup"><span data-stu-id="4687d-170">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="4687d-171"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4687d-171"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="4687d-172">Sistema</span><span class="sxs-lookup"><span data-stu-id="4687d-172">System</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4687d-173">Não há suporte para as ACEs System-Alarm específicas do sistema e do objeto.</span><span class="sxs-lookup"><span data-stu-id="4687d-173">System-alarm and object-specific system-alarm ACEs are not currently supported.</span></span>

> [!Note]  
> <span data-ttu-id="4687d-174">Cada ACE começa com uma estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="4687d-174">Each ACE starts with an [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="4687d-175">O formato dos dados que seguem o cabeçalho varia de acordo com o tipo de ACE especificado no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="4687d-175">The format of the data following the header varies according to the ACE type specified in the header.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4687d-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4687d-176">Requirements</span></span>



| <span data-ttu-id="4687d-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="4687d-177">Requirement</span></span> | <span data-ttu-id="4687d-178">Valor</span><span class="sxs-lookup"><span data-stu-id="4687d-178">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4687d-179">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4687d-179">Minimum supported client</span></span><br/> | <span data-ttu-id="4687d-180">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4687d-180">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4687d-181">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4687d-181">Minimum supported server</span></span><br/> | <span data-ttu-id="4687d-182">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4687d-182">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="4687d-183">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4687d-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="4687d-184"><dt>Winnt. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4687d-184"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4687d-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="4687d-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4687d-186">**AddAce**</span><span class="sxs-lookup"><span data-stu-id="4687d-186">**AddAce**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[<span data-ttu-id="4687d-187">**Ace de acesso \_ permitido \_**</span><span class="sxs-lookup"><span data-stu-id="4687d-187">**ACCESS\_ALLOWED\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[<span data-ttu-id="4687d-188">**Ace de acesso \_ negado \_**</span><span class="sxs-lookup"><span data-stu-id="4687d-188">**ACCESS\_DENIED\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[<span data-ttu-id="4687d-189">**LCA**</span><span class="sxs-lookup"><span data-stu-id="4687d-189">**ACL**</span></span>](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[<span data-ttu-id="4687d-190">**\_Ace do alarme do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="4687d-190">**SYSTEM\_ALARM\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[<span data-ttu-id="4687d-191">**\_ACE de auditoria do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="4687d-191">**SYSTEM\_AUDIT\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

