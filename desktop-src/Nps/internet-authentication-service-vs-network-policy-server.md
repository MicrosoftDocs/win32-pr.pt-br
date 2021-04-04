---
title: Serviço de autenticação da Internet & servidor de políticas de rede
description: O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca657da17e823caa51e8401905a8a0a3e307e975
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104008515"
---
# <a name="internet-authentication-service--network-policy-server"></a><span data-ttu-id="53981-103">Serviço de autenticação da Internet & servidor de políticas de rede</span><span class="sxs-lookup"><span data-stu-id="53981-103">Internet Authentication Service & Network Policy Server</span></span>

<span data-ttu-id="53981-104">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede).</span><span class="sxs-lookup"><span data-stu-id="53981-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span>

## <a name="internet-authentication-service"></a><span data-ttu-id="53981-105">Serviço de autenticação da Internet</span><span class="sxs-lookup"><span data-stu-id="53981-105">Internet Authentication Service</span></span>

<span data-ttu-id="53981-106">O serviço de autenticação da Internet é a implementação da Microsoft de um servidor RADIUS e proxy.</span><span class="sxs-lookup"><span data-stu-id="53981-106">Internet Authentication Service is the Microsoft implementation of a RADIUS server and proxy.</span></span>

<span data-ttu-id="53981-107">O serviço de autenticação da Internet dá suporte a dois conjuntos de API: API [das extensões do servidor de políticas de rede](ias-extensions.md) e [do Server Data Objects](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="53981-107">Internet Authentication Service supports two API sets: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="53981-108">Consulte [TechNet: serviço de autenticação da Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obter mais informações sobre o ias.</span><span class="sxs-lookup"><span data-stu-id="53981-108">See [TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on IAS.</span></span>

## <a name="network-policy-server"></a><span data-ttu-id="53981-109">Servidor de Políticas de Rede</span><span class="sxs-lookup"><span data-stu-id="53981-109">Network Policy Server</span></span>

<span data-ttu-id="53981-110">O servidor de políticas de rede é a implementação da Microsoft de um servidor RADIUS e proxy e está disponível em servidores Windows a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="53981-110">Network Policy Server is the Microsoft implementation of a RADIUS server and proxy and it is available on Windows servers starting with Windows Server 2008.</span></span>

<span data-ttu-id="53981-111">O NPS dá suporte aos mesmos dois conjuntos de API que o IAS: API de [extensões do servidor de políticas de rede](ias-extensions.md) e a diretiva de [objetos de dados do servidor](server-data-objects.md)</span><span class="sxs-lookup"><span data-stu-id="53981-111">NPS supports the same two API sets as IAS: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="53981-112">Além disso, o NPS contém um conjunto de novos recursos que expandem os recursos do IAS.</span><span class="sxs-lookup"><span data-stu-id="53981-112">In addition, NPS contains a set of new features that expand the IAS capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53981-113">Recurso</span><span class="sxs-lookup"><span data-stu-id="53981-113">Feature</span></span></th>
<th><span data-ttu-id="53981-114">O que há de novo para o NPS</span><span class="sxs-lookup"><span data-stu-id="53981-114">What's new for NPS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53981-115"><a href="/windows/desktop/NAP/network-access-protection-start-page">NAP (proteção de acesso à rede)</a></span><span class="sxs-lookup"><span data-stu-id="53981-115"><a href="/windows/desktop/NAP/network-access-protection-start-page">Network Access Protection (NAP)</a></span></span><br/></td>
<td><span data-ttu-id="53981-116">O NPS é o servidor central de proteção de acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="53981-116">NPS is the central server of Network Access Protection.</span></span><br/> <span data-ttu-id="53981-117">O NPS dá suporte à criação de política usando as seguintes condições adicionais:</span><span class="sxs-lookup"><span data-stu-id="53981-117">NPS supports policy authoring using the following additional conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="53981-118">Expiração da política.</span><span class="sxs-lookup"><span data-stu-id="53981-118">Policy expiration.</span></span></li>
<li><span data-ttu-id="53981-119">Versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="53981-119">Operating system version.</span></span></li>
<li><span data-ttu-id="53981-120">Acessar o endereço IP do cliente.</span><span class="sxs-lookup"><span data-stu-id="53981-120">Access client IP address.</span></span></li>
<li><span data-ttu-id="53981-121">Políticas de integridade.</span><span class="sxs-lookup"><span data-stu-id="53981-121">Health policies.</span></span></li>
<li><span data-ttu-id="53981-122">Tipos de EAP permitidos.</span><span class="sxs-lookup"><span data-stu-id="53981-122">Allowed EAP types.</span></span></li>
<li><span data-ttu-id="53981-123">HCAP.</span><span class="sxs-lookup"><span data-stu-id="53981-123">HCAP.</span></span></li>
</ul>
<span data-ttu-id="53981-124">O NPS dá suporte à criação de política usando as seguintes configurações adicionais:</span><span class="sxs-lookup"><span data-stu-id="53981-124">NPS supports policy authoring using the following additional settings:</span></span><br/>
<ul>
<li><span data-ttu-id="53981-125">Experiência.</span><span class="sxs-lookup"><span data-stu-id="53981-125">Probation.</span></span></li>
<li><span data-ttu-id="53981-126">Acesso limitado.</span><span class="sxs-lookup"><span data-stu-id="53981-126">Limited access.</span></span></li>
<li><span data-ttu-id="53981-127">Estado estendido para acesso limitado.</span><span class="sxs-lookup"><span data-stu-id="53981-127">Extended state for limited access.</span></span></li>
</ul>
<span data-ttu-id="53981-128">O NPS, por meio de NAP, interopera com o CISCO NAC.</span><span class="sxs-lookup"><span data-stu-id="53981-128">NPS, through NAP, interoperates with CISCO NAC.</span></span><br/> <span data-ttu-id="53981-129">O IAS não oferece suporte a NAP.</span><span class="sxs-lookup"><span data-stu-id="53981-129">IAS does not support NAP.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53981-130"><a href="/windows/win32/eap/eap-start-page">EAP</a> Suporte a políticas e <a href="/windows/win32/eaphost/portal">EAPHost</a></span><span class="sxs-lookup"><span data-stu-id="53981-130"><a href="/windows/win32/eap/eap-start-page">EAP</a> Policy and <a href="/windows/win32/eaphost/portal">EAPHost</a> Support</span></span><br/></td>
<td><span data-ttu-id="53981-131">O NPS usa o EAPHost para a extensibilidade do método EAP.</span><span class="sxs-lookup"><span data-stu-id="53981-131">NPS uses EAPHost for EAP method extensibility.</span></span> <span data-ttu-id="53981-132">Além disso, os administradores podem configurar a política de acesso à rede para o EAP.</span><span class="sxs-lookup"><span data-stu-id="53981-132">Additionally, administrators may configure network access policy for EAP.</span></span><br/> <span data-ttu-id="53981-133">O IAS não oferece suporte à integração do EAPHost ou condições de filtro de tipo EAP para políticas.</span><span class="sxs-lookup"><span data-stu-id="53981-133">IAS does not support EAPHost integration, or EAP type filter conditions for policies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53981-134">Suporte a IPv6</span><span class="sxs-lookup"><span data-stu-id="53981-134">IPv6 Support</span></span><br/></td>
<td><span data-ttu-id="53981-135">O NPS dá suporte à implantação em ambientes IPv6.</span><span class="sxs-lookup"><span data-stu-id="53981-135">NPS supports deployment in IPv6 environments.</span></span><br/> <span data-ttu-id="53981-136">O IAS não oferece suporte a endereços de rede IPv6.</span><span class="sxs-lookup"><span data-stu-id="53981-136">IAS does not support IPv6 network addresses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53981-137">Configuração de XML</span><span class="sxs-lookup"><span data-stu-id="53981-137">XML Configuration</span></span><br/></td>
<td><span data-ttu-id="53981-138">A configuração do NPS pode ser importada e exportada em formato XML.</span><span class="sxs-lookup"><span data-stu-id="53981-138">NPS configuration can be imported and exported in XML format.</span></span><br/> <span data-ttu-id="53981-139">O IAS está usando um banco de dados Jet para armazenar a configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="53981-139">IAS is using a Jet database for storing service configuration.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53981-140"><a href="https://www.niap-ccevs.org/cc-scheme/">Critérios comuns</a> Support</span><span class="sxs-lookup"><span data-stu-id="53981-140"><a href="https://www.niap-ccevs.org/cc-scheme/">Common Criteria</a> Support</span></span><br/></td>
<td><span data-ttu-id="53981-141">O NPS foi atualizado para dar suporte à sua implantação em ambientes que devem atender aos padrões de segurança de critérios comuns.</span><span class="sxs-lookup"><span data-stu-id="53981-141">NPS has been updated to support its deployment in environments that must meet the Common Criteria security standards.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53981-142"><a href="ias-extensions.md">API de extensões do NPS</a></span><span class="sxs-lookup"><span data-stu-id="53981-142"><a href="ias-extensions.md">NPS Extensions API</a></span></span><br/></td>
<td><span data-ttu-id="53981-143">As DLLs de extensão do NPS são executadas em um processo separado do serviço NPS.</span><span class="sxs-lookup"><span data-stu-id="53981-143">The NPS extension DLLs run in a separate process from the NPS service.</span></span> <span data-ttu-id="53981-144">Se uma DLL de extensão falhar, o NPS continuará em execução e as solicitações futuras serão rejeitadas.</span><span class="sxs-lookup"><span data-stu-id="53981-144">Should an extension DLL crash, NPS will keep running and future requests will be rejected.</span></span><br/> <span data-ttu-id="53981-145">As DLLs de extensão do IAS são executadas no mesmo processo que o serviço IAS e podem afetar negativamente o serviço.</span><span class="sxs-lookup"><span data-stu-id="53981-145">The IAS extension DLLs run in the same process as the IAS service and may adversely affect the service.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53981-146">Interface do usuário de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="53981-146">Management User Interface</span></span><br/></td>
<td><span data-ttu-id="53981-147">O console de gerenciamento do NPS (NPS. msc) tem uma nova aparência, melhor usabilidade e abrange toda a nova funcionalidade adicionada ao NPS.</span><span class="sxs-lookup"><span data-stu-id="53981-147">The NPS management console (nps.msc) has a new look, improved usability, and covers all the new functionality added to NPS.</span></span><br/> <span data-ttu-id="53981-148">O IAS usa o console de gerenciamento do IAS. msc.</span><span class="sxs-lookup"><span data-stu-id="53981-148">IAS uses the ias.msc management console.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53981-149">Ferramenta de gerenciamento de função e integração de Gerenciador do Servidor</span><span class="sxs-lookup"><span data-stu-id="53981-149">Role Management Tool and Server Manager Integration</span></span><br/></td>
<td><span data-ttu-id="53981-150">O NPS é integrado com o Gerenciador do Servidor e a ferramenta de gerenciamento de função.</span><span class="sxs-lookup"><span data-stu-id="53981-150">NPS is integrated with the Server Manager and the Role Management Tool.</span></span> <span data-ttu-id="53981-151">Essa integração facilita a configuração e o gerenciamento do NPS e dos cenários relacionados.</span><span class="sxs-lookup"><span data-stu-id="53981-151">This integration facilitates the configuration and management of NPS and related scenarios.</span></span><br/> <span data-ttu-id="53981-152">O Gerenciador do Servidor não está disponível em computadores que executam o IAS.</span><span class="sxs-lookup"><span data-stu-id="53981-152">Server Manager is not available on computers running IAS.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53981-153">Script de linha de comando atualizado com <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">netsh</a>.</span><span class="sxs-lookup"><span data-stu-id="53981-153">Updated Command Line Scripting with <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>.</span></span><br/></td>
<td><span data-ttu-id="53981-154">O NPS dá suporte à &quot; interface de linha de comando netsh nps &quot; .</span><span class="sxs-lookup"><span data-stu-id="53981-154">NPS supports the &quot;Netsh nps&quot; command line interface.</span></span> <span data-ttu-id="53981-155">&quot;O netsh nps &quot; contém novos comandos que permitem configurar completamente o NPS, incluindo recursos NAP.</span><span class="sxs-lookup"><span data-stu-id="53981-155">&quot;Netsh nps&quot; contains new commands that permit to fully configure NPS, including NAP features.</span></span><br/> <span data-ttu-id="53981-156">O IAS dá suporte à &quot; interface de linha de comando netsh aaaa &quot; .</span><span class="sxs-lookup"><span data-stu-id="53981-156">IAS supports the &quot;Netsh aaaa&quot; command line interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53981-157">Isolamento de política</span><span class="sxs-lookup"><span data-stu-id="53981-157">Policy Isolation</span></span><br/></td>
<td><span data-ttu-id="53981-158">O NPS permite a implementação do isolamento de política definindo a origem da política de rede.</span><span class="sxs-lookup"><span data-stu-id="53981-158">NPS enables the implementation of policy isolation by setting the Network Policy Source.</span></span> <span data-ttu-id="53981-159">As políticas podem ser configuradas que são aplicáveis apenas a um tipo de NAS predeterminado.</span><span class="sxs-lookup"><span data-stu-id="53981-159">Policies can be configured that are applicable only to a predetermined NAS type.</span></span><br/> <span data-ttu-id="53981-160">O IAS não dá suporte ao isolamento de política.</span><span class="sxs-lookup"><span data-stu-id="53981-160">IAS does not support policy isolation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="53981-161">Consulte [TechNet: servidor de políticas de rede](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obter mais informações sobre o NPS.</span><span class="sxs-lookup"><span data-stu-id="53981-161">See [TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on NPS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53981-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53981-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53981-163">Autenticação, autorização e contabilização RADIUS</span><span class="sxs-lookup"><span data-stu-id="53981-163">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="53981-164">Registrando em log com o servidor de políticas de rede</span><span class="sxs-lookup"><span data-stu-id="53981-164">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="53981-165">Trabalhando com um servidor de estado</span><span class="sxs-lookup"><span data-stu-id="53981-165">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

