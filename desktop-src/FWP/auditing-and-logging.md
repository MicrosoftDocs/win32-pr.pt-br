---
title: Auditoria
description: A WFP (plataforma de filtragem do Windows) fornece auditoria de eventos relacionados a firewall e IPsec.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cef1d4fee81afc366a987575935c1de8880092c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "103917852"
---
# <a name="auditing"></a><span data-ttu-id="d37dd-103">Auditoria</span><span class="sxs-lookup"><span data-stu-id="d37dd-103">Auditing</span></span>

<span data-ttu-id="d37dd-104">A WFP (plataforma de filtragem do Windows) fornece auditoria de eventos relacionados a firewall e IPsec.</span><span class="sxs-lookup"><span data-stu-id="d37dd-104">The Windows Filtering Platform (WFP) provides auditing of firewall and IPsec related events.</span></span> <span data-ttu-id="d37dd-105">Esses eventos são armazenados no log de segurança do sistema.</span><span class="sxs-lookup"><span data-stu-id="d37dd-105">These events are stored in the system security log.</span></span>

<span data-ttu-id="d37dd-106">Os eventos auditados são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="d37dd-106">The audited events are as follows.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d37dd-107">Categoria de auditoria</span><span class="sxs-lookup"><span data-stu-id="d37dd-107">Auditing category</span></span></th>
<th><span data-ttu-id="d37dd-108">Subcategoria de auditoria</span><span class="sxs-lookup"><span data-stu-id="d37dd-108">Auditing subcategory</span></span></th>
<th><span data-ttu-id="d37dd-109">Eventos auditados</span><span class="sxs-lookup"><span data-stu-id="d37dd-109">Audited events</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d37dd-110">Alteração de política</span><span class="sxs-lookup"><span data-stu-id="d37dd-110">Policy Change</span></span><br/> <span data-ttu-id="d37dd-111">{6997984D-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="d37dd-111">{6997984D-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="d37dd-112">Filtrando alteração de política da plataforma</span><span class="sxs-lookup"><span data-stu-id="d37dd-112">Filtering Platform Policy Change</span></span><br/> <span data-ttu-id="d37dd-113">{0CCE9233-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="d37dd-113">{0CCE9233-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="d37dd-114">Os números representam as IDs de evento, conforme exibido pelo Visualizador de Eventos (eventvwr.exe).</span><span class="sxs-lookup"><span data-stu-id="d37dd-114">The numbers represent the Event IDs as displayed by Event Viewer (eventvwr.exe).</span></span>
</blockquote>
<br/> <span data-ttu-id="d37dd-115">Adição e remoção de objetos WFP:</span><span class="sxs-lookup"><span data-stu-id="d37dd-115">WFP object addition and removal:</span></span><br/>
<ul>
<li><span data-ttu-id="d37dd-116">5440 balão persistente adicionado</span><span class="sxs-lookup"><span data-stu-id="d37dd-116">5440 Persistent callout added</span></span></li>
<li><span data-ttu-id="d37dd-117">5441 tempo de inicialização ou filtro persistente adicionado</span><span class="sxs-lookup"><span data-stu-id="d37dd-117">5441 Boot-time or persistent filter added</span></span></li>
<li><span data-ttu-id="d37dd-118">5442 provedor persistente adicionado</span><span class="sxs-lookup"><span data-stu-id="d37dd-118">5442 Persistent provider added</span></span></li>
<li><span data-ttu-id="d37dd-119">5443 contexto de provedor persistente adicionado</span><span class="sxs-lookup"><span data-stu-id="d37dd-119">5443 Persistent provider context added</span></span></li>
<li><span data-ttu-id="d37dd-120">5444 subcamada persistente adicionada</span><span class="sxs-lookup"><span data-stu-id="d37dd-120">5444 Persistent sub-layer added</span></span></li>
<li><span data-ttu-id="d37dd-121">texto explicativo de tempo de execução 5446 adicionado ou removido</span><span class="sxs-lookup"><span data-stu-id="d37dd-121">5446 Run-time callout added or removed</span></span></li>
<li><span data-ttu-id="d37dd-122">filtro de tempo de execução adicionado ou removido do 5447</span><span class="sxs-lookup"><span data-stu-id="d37dd-122">5447 Run-time filter added or removed</span></span></li>
<li><span data-ttu-id="d37dd-123">5448 provedor de tempo de execução adicionado ou removido</span><span class="sxs-lookup"><span data-stu-id="d37dd-123">5448 Run-time provider added or removed</span></span></li>
<li><span data-ttu-id="d37dd-124">o contexto do provedor de tempo de execução 5449 foi adicionado ou removido</span><span class="sxs-lookup"><span data-stu-id="d37dd-124">5449 Run-time provider context added or removed</span></span></li>
<li><span data-ttu-id="d37dd-125">5450 subcamada em tempo de execução adicionada ou removida</span><span class="sxs-lookup"><span data-stu-id="d37dd-125">5450 Run-time sub-layer added or removed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d37dd-126">Acesso a objetos</span><span class="sxs-lookup"><span data-stu-id="d37dd-126">Object Access</span></span><br/> <span data-ttu-id="d37dd-127">{6997984A-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="d37dd-127">{6997984A-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="d37dd-128">Remoção de pacote de plataforma de filtragem</span><span class="sxs-lookup"><span data-stu-id="d37dd-128">Filtering Platform Packet Drop</span></span> <br/> <span data-ttu-id="d37dd-129">{0CCE9225-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="d37dd-129">{0CCE9225-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="d37dd-130">Pacotes removidos por WFP:</span><span class="sxs-lookup"><span data-stu-id="d37dd-130">Packets dropped by WFP:</span></span><br/>
<ul>
<li><span data-ttu-id="d37dd-131">pacote 5152 Descartado</span><span class="sxs-lookup"><span data-stu-id="d37dd-131">5152 Packet dropped</span></span></li>
<li><span data-ttu-id="d37dd-132">pacote de 5153 vetado</span><span class="sxs-lookup"><span data-stu-id="d37dd-132">5153 Packet vetoed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d37dd-133">Acesso a objetos</span><span class="sxs-lookup"><span data-stu-id="d37dd-133">Object Access</span></span><br/></td>
<td><span data-ttu-id="d37dd-134">Conexão da plataforma de filtragem</span><span class="sxs-lookup"><span data-stu-id="d37dd-134">Filtering Platform Connection</span></span> <br/> <span data-ttu-id="d37dd-135">{0CCE9226-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="d37dd-135">{0CCE9226-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="d37dd-136">Conexões permitidas e bloqueadas:</span><span class="sxs-lookup"><span data-stu-id="d37dd-136">Allowed and blocked connections:</span></span><br/>
<ul>
<li><span data-ttu-id="d37dd-137">5154 escuta permitida</span><span class="sxs-lookup"><span data-stu-id="d37dd-137">5154 Listen permitted</span></span></li>
<li><span data-ttu-id="d37dd-138">5155 escuta bloqueada</span><span class="sxs-lookup"><span data-stu-id="d37dd-138">5155 Listen blocked</span></span></li>
<li><span data-ttu-id="d37dd-139">5156 conexão permitida</span><span class="sxs-lookup"><span data-stu-id="d37dd-139">5156 Connection permitted</span></span></li>
<li><span data-ttu-id="d37dd-140">5157 conexão bloqueada</span><span class="sxs-lookup"><span data-stu-id="d37dd-140">5157 Connection blocked</span></span></li>
<li><span data-ttu-id="d37dd-141">5158 Associação permitida</span><span class="sxs-lookup"><span data-stu-id="d37dd-141">5158 Bind permitted</span></span></li>
<li><span data-ttu-id="d37dd-142">5159 Associação bloqueada</span><span class="sxs-lookup"><span data-stu-id="d37dd-142">5159 Bind blocked</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="d37dd-143">As conexões permitidas nem sempre auditam a ID do filtro associado.</span><span class="sxs-lookup"><span data-stu-id="d37dd-143">Permitted connections do not always audit the ID of the associated filter.</span></span> <span data-ttu-id="d37dd-144">O Filterid para TCP será 0, a menos que um subconjunto dessas condições de filtragem seja usado: UserID, AppID, protocolo, porta remota.</span><span class="sxs-lookup"><span data-stu-id="d37dd-144">The FilterID for TCP will be 0 unless a subset of these filtering conditions are used: UserID, AppID, Protocol, Remote Port.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d37dd-145">Acesso a objetos</span><span class="sxs-lookup"><span data-stu-id="d37dd-145">Object Access</span></span><br/></td>
<td><span data-ttu-id="d37dd-146">Outros eventos de acesso de objeto</span><span class="sxs-lookup"><span data-stu-id="d37dd-146">Other Object Access Events</span></span><br/> <span data-ttu-id="d37dd-147">{0CCE9227-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="d37dd-147">{0CCE9227-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="d37dd-148">Essa subcategoria permite muitas auditorias.</span><span class="sxs-lookup"><span data-stu-id="d37dd-148">This subcategory enables many audits.</span></span> <span data-ttu-id="d37dd-149">As auditorias específicas de WFP são listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="d37dd-149">WFP specific audits are listed below.</span></span>
</blockquote>
<br/> <span data-ttu-id="d37dd-150">Status de prevenção de negação de serviço:</span><span class="sxs-lookup"><span data-stu-id="d37dd-150">Denial of Service prevention status:</span></span><br/>
<ul>
<li><span data-ttu-id="d37dd-151">modo de prevenção de DoS 5148 de WFP iniciado</span><span class="sxs-lookup"><span data-stu-id="d37dd-151">5148 WFP DoS prevention mode started</span></span></li>
<li><span data-ttu-id="d37dd-152">modo de prevenção de DoS 5149 de WFP interrompido</span><span class="sxs-lookup"><span data-stu-id="d37dd-152">5149 WFP DoS prevention mode stopped</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d37dd-153">Logon/logoff</span><span class="sxs-lookup"><span data-stu-id="d37dd-153">Logon/Logoff</span></span><br/> <span data-ttu-id="d37dd-154">{69979849-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="d37dd-154">{69979849-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="d37dd-155">Modo principal do IPsec</span><span class="sxs-lookup"><span data-stu-id="d37dd-155">IPsec Main Mode</span></span><br/> <span data-ttu-id="d37dd-156">{0CCE9218-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="d37dd-156">{0CCE9218-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="d37dd-157">Negociação de modo principal IKE e AuthIP:</span><span class="sxs-lookup"><span data-stu-id="d37dd-157">IKE and AuthIP Main Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="d37dd-158">4650, associação de segurança 4651 estabelecida</span><span class="sxs-lookup"><span data-stu-id="d37dd-158">4650, 4651 Security association established</span></span></li>
<li><span data-ttu-id="d37dd-159">4652, falha na negociação de 4653</span><span class="sxs-lookup"><span data-stu-id="d37dd-159">4652, 4653 Negotiation failed</span></span></li>
<li><span data-ttu-id="d37dd-160">4655 Associação de segurança encerrada</span><span class="sxs-lookup"><span data-stu-id="d37dd-160">4655 Security association ended</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d37dd-161">Logon/logoff</span><span class="sxs-lookup"><span data-stu-id="d37dd-161">Logon/Logoff</span></span><br/></td>
<td><span data-ttu-id="d37dd-162">Modo rápido do IPsec</span><span class="sxs-lookup"><span data-stu-id="d37dd-162">IPsec Quick Mode</span></span> <br/> <span data-ttu-id="d37dd-163">{0CCE9219-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="d37dd-163">{0CCE9219-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="d37dd-164">Negociação de modo rápido IKE e AuthIP:</span><span class="sxs-lookup"><span data-stu-id="d37dd-164">IKE and AuthIP Quick Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="d37dd-165">Associação de segurança 5451 estabelecida</span><span class="sxs-lookup"><span data-stu-id="d37dd-165">5451 Security association established</span></span></li>
<li><span data-ttu-id="d37dd-166">5452 Associação de segurança encerrada</span><span class="sxs-lookup"><span data-stu-id="d37dd-166">5452 Security association ended</span></span></li>
<li><span data-ttu-id="d37dd-167">4654 a negociação falhou</span><span class="sxs-lookup"><span data-stu-id="d37dd-167">4654 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d37dd-168">Logon/logoff</span><span class="sxs-lookup"><span data-stu-id="d37dd-168">Logon/Logoff</span></span> <br/></td>
<td><span data-ttu-id="d37dd-169">Modo estendido do IPsec</span><span class="sxs-lookup"><span data-stu-id="d37dd-169">IPsec Extended Mode</span></span><br/> <span data-ttu-id="d37dd-170">{0CCE921A-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="d37dd-170">{0CCE921A-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="d37dd-171">Negociação de modo estendido AuthIP:</span><span class="sxs-lookup"><span data-stu-id="d37dd-171">AuthIP Extended Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="d37dd-172">4978 pacote de negociação inválido</span><span class="sxs-lookup"><span data-stu-id="d37dd-172">4978 Invalid negotiation packet</span></span></li>
<li><span data-ttu-id="d37dd-173">4979, 4980, 4981, 4982 Associação de segurança estabelecida</span><span class="sxs-lookup"><span data-stu-id="d37dd-173">4979, 4980, 4981, 4982 Security association established</span></span></li>
<li><span data-ttu-id="d37dd-174">4983, falha na negociação de 4984</span><span class="sxs-lookup"><span data-stu-id="d37dd-174">4983, 4984 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d37dd-175">Sistema</span><span class="sxs-lookup"><span data-stu-id="d37dd-175">System</span></span><br/> <span data-ttu-id="d37dd-176">{69979848-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="d37dd-176">{69979848-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="d37dd-177">Driver IPsec</span><span class="sxs-lookup"><span data-stu-id="d37dd-177">IPsec Driver</span></span><br/> <span data-ttu-id="d37dd-178">{0CCE9213-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="d37dd-178">{0CCE9213-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="d37dd-179">Pacotes removidos pelo driver IPsec:</span><span class="sxs-lookup"><span data-stu-id="d37dd-179">Packets dropped by the IPsec driver:</span></span><br/>
<ul>
<li><span data-ttu-id="d37dd-180">4963 pacote de texto não criptografado de entrada Descartado</span><span class="sxs-lookup"><span data-stu-id="d37dd-180">4963 Inbound clear text packet dropped</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d37dd-181">Por padrão, a auditoria para WFP está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="d37dd-181">By default, auditing for WFP is disabled.</span></span>

<span data-ttu-id="d37dd-182">A auditoria pode ser habilitada por categoria através do snap-in do Editor de Objeto de Política de Grupo MMC, do snap-in do MMC de diretiva de segurança local ou do comando auditpol.exe.</span><span class="sxs-lookup"><span data-stu-id="d37dd-182">Auditing can be enabled on a per-category basis through either the Group Policy Object Editor MMC snap-in, the Local Security Policy MMC snap-in, or the auditpol.exe command.</span></span>

<span data-ttu-id="d37dd-183">Por exemplo, para habilitar a auditoria de eventos de alteração de diretiva, você pode:</span><span class="sxs-lookup"><span data-stu-id="d37dd-183">For example, to enable the auditing of Policy Change events you may:</span></span>

-   <span data-ttu-id="d37dd-184">Usar o Editor de Objeto de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="d37dd-184">Use the Group Policy Object Editor</span></span>

    1.  <span data-ttu-id="d37dd-185">Execute **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="d37dd-185">Run **gpedit.msc**.</span></span>
    2.  <span data-ttu-id="d37dd-186">Expanda política de computador local.</span><span class="sxs-lookup"><span data-stu-id="d37dd-186">Expand Local Computer Policy.</span></span>
    3.  <span data-ttu-id="d37dd-187">Expanda Configuração do computador.</span><span class="sxs-lookup"><span data-stu-id="d37dd-187">Expand Computer Configuration.</span></span>
    4.  <span data-ttu-id="d37dd-188">Expanda Configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="d37dd-188">Expand Windows Settings.</span></span>
    5.  <span data-ttu-id="d37dd-189">Expanda Configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="d37dd-189">Expand Security Settings.</span></span>
    6.  <span data-ttu-id="d37dd-190">Expanda políticas locais.</span><span class="sxs-lookup"><span data-stu-id="d37dd-190">Expand Local Policies.</span></span>
    7.  <span data-ttu-id="d37dd-191">Clique em política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="d37dd-191">Click Audit Policy.</span></span>
    8.  <span data-ttu-id="d37dd-192">Clique duas vezes em diretiva de auditoria alterar para iniciar a caixa de diálogo Propriedades.</span><span class="sxs-lookup"><span data-stu-id="d37dd-192">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    9.  <span data-ttu-id="d37dd-193">Verifique as caixas de seleção êxito e falha.</span><span class="sxs-lookup"><span data-stu-id="d37dd-193">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="d37dd-194">Usar a política de segurança local</span><span class="sxs-lookup"><span data-stu-id="d37dd-194">Use the Local Security Policy</span></span>

    1.  <span data-ttu-id="d37dd-195">Execute **secpol. msc**.</span><span class="sxs-lookup"><span data-stu-id="d37dd-195">Run **secpol.msc**.</span></span>
    2.  <span data-ttu-id="d37dd-196">Expanda políticas locais.</span><span class="sxs-lookup"><span data-stu-id="d37dd-196">Expand Local Policies.</span></span>
    3.  <span data-ttu-id="d37dd-197">Clique em política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="d37dd-197">Click Audit Policy.</span></span>
    4.  <span data-ttu-id="d37dd-198">Clique duas vezes em diretiva de auditoria alterar para iniciar a caixa de diálogo Propriedades.</span><span class="sxs-lookup"><span data-stu-id="d37dd-198">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    5.  <span data-ttu-id="d37dd-199">Verifique as caixas de seleção êxito e falha.</span><span class="sxs-lookup"><span data-stu-id="d37dd-199">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="d37dd-200">Usar o comando auditpol.exe</span><span class="sxs-lookup"><span data-stu-id="d37dd-200">Use the auditpol.exe command</span></span>

    -   <span data-ttu-id="d37dd-201">**Auditpol/set/Category: "alteração de política"/success: habilitar/Failure: habilitar**</span><span class="sxs-lookup"><span data-stu-id="d37dd-201">**auditpol /set /category:"Policy Change" /success:enable /failure:enable**</span></span>

<span data-ttu-id="d37dd-202">A auditoria pode ser habilitada em uma base por subcategoria somente por meio do comando auditpol.exe.</span><span class="sxs-lookup"><span data-stu-id="d37dd-202">Auditing can be enabled on a per-subcategory basis only through the auditpol.exe command.</span></span>

<span data-ttu-id="d37dd-203">Os nomes de categoria e subcategoria de auditoria são localizados.</span><span class="sxs-lookup"><span data-stu-id="d37dd-203">The auditing category and subcategory names are localized.</span></span> <span data-ttu-id="d37dd-204">Para evitar a localização de scripts de auditoria, os GUIDs correspondentes podem ser usados no lugar dos nomes.</span><span class="sxs-lookup"><span data-stu-id="d37dd-204">To avoid localization for auditing scripts, the corresponding GUIDs may be used in place of the names.</span></span>

<span data-ttu-id="d37dd-205">Por exemplo, para habilitar a auditoria de filtragem de eventos de alteração de política de plataforma, você pode usar um dos seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="d37dd-205">For example, to enable the auditing of Filtering Platform Policy Change events you may use either one of the following commands:</span></span>

-   <span data-ttu-id="d37dd-206">**Auditpol/set/SubCategory: "filtro de alteração de política da plataforma de filtragem"/success: habilitar/Failure: habilitar**</span><span class="sxs-lookup"><span data-stu-id="d37dd-206">**auditpol /set /subcategory:"Filtering Platform Policy Change" /success:enable /failure:enable**</span></span>
-   <span data-ttu-id="d37dd-207">**Auditpol/set/SubCategory: "{0CCE9233-69AE-11D9-BED3-505054503030}"/success: habilitar/Failure: Enable**</span><span class="sxs-lookup"><span data-stu-id="d37dd-207">**auditpol /set /subcategory:"{0CCE9233-69AE-11D9-BED3-505054503030}" /success:enable /failure:enable**</span></span>

## <a name="related-topics"></a><span data-ttu-id="d37dd-208">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d37dd-208">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d37dd-209">[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="d37dd-209">[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="d37dd-210">[Log de Eventos](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="d37dd-210">[Event Log](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="d37dd-211">Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="d37dd-211">Group Policy</span></span>](/windows/deployment/deploy-whats-new)
</dt> </dl>

