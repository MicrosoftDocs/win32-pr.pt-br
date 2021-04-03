---
title: Modelo de Objeto
description: A tabela a seguir lista os tipos de objeto que podem ser manipulados por meio de vários conjuntos de API fornecidos pela WFP (Windows Filtering Platform).
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa90b4757a39617616c6f83b6b79fe322b2e64c8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104007156"
---
# <a name="object-model"></a><span data-ttu-id="3d974-103">Modelo de Objeto</span><span class="sxs-lookup"><span data-stu-id="3d974-103">Object Model</span></span>

<span data-ttu-id="3d974-104">A tabela a seguir lista os tipos de objeto que podem ser manipulados por meio de vários conjuntos de API fornecidos pela WFP (Windows Filtering Platform).</span><span class="sxs-lookup"><span data-stu-id="3d974-104">The following table lists the object types that can be manipulated through the various API sets supplied by the Windows Filtering Platform (WFP).</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d974-105">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="3d974-105">Object Type</span></span></th>
<th><span data-ttu-id="3d974-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d974-106">Description</span></span></th>
<th><span data-ttu-id="3d974-107">Propriedades de exemplo</span><span class="sxs-lookup"><span data-stu-id="3d974-107">Sample Properties</span></span></th>
<th><span data-ttu-id="3d974-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3d974-108">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d974-109">Filtrar</span><span class="sxs-lookup"><span data-stu-id="3d974-109">Filter</span></span></td>
<td><span data-ttu-id="3d974-110">Uma regra que governa a classificação.</span><span class="sxs-lookup"><span data-stu-id="3d974-110">A rule that governs classification.</span></span> <span data-ttu-id="3d974-111">Se as condições forem atendidas, a ação será invocada.</span><span class="sxs-lookup"><span data-stu-id="3d974-111">If the conditions are met, the action is invoked.</span></span> <br/> <span data-ttu-id="3d974-112">Esse é o objeto mais complexo exposto pela WFP, já que ele une todos os outros tipos de objeto.</span><span class="sxs-lookup"><span data-stu-id="3d974-112">This is the most complex object exposed by WFP since it ties together all the other object types.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="3d974-113">Matriz de condições</span><span class="sxs-lookup"><span data-stu-id="3d974-113">Array of conditions</span></span></li>
<li><span data-ttu-id="3d974-114">Ação (permitir, bloquear, texto explicativo)</span><span class="sxs-lookup"><span data-stu-id="3d974-114">Action (Permit, Block, Callout)</span></span></li>
<li><span data-ttu-id="3d974-115"><a href="filter-weight-assignment.md">Weight</a></span><span class="sxs-lookup"><span data-stu-id="3d974-115"><a href="filter-weight-assignment.md">Weight</a></span></span></li>
<li><span data-ttu-id="3d974-116">Contexto</span><span class="sxs-lookup"><span data-stu-id="3d974-116">Context</span></span></li>
</ul></td>
<td><span data-ttu-id="3d974-117">&quot;Bloquear o tráfego com uma porta TCP maior que 1024.&quot;</span><span class="sxs-lookup"><span data-stu-id="3d974-117">&quot;Block traffic with a TCP port greater than 1024.&quot;</span></span> <br/> <span data-ttu-id="3d974-118">&quot;Texto explicativo para IDS de todo o tráfego não protegido.&quot;</span><span class="sxs-lookup"><span data-stu-id="3d974-118">&quot;Callout to IDS for all traffic that is not secured.&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d974-119">Balão</span><span class="sxs-lookup"><span data-stu-id="3d974-119">Callout</span></span></td>
<td><span data-ttu-id="3d974-120">Um conjunto de funções que participam do processo de classificação.</span><span class="sxs-lookup"><span data-stu-id="3d974-120">A set of functions that participate in the classification process.</span></span><br/> <span data-ttu-id="3d974-121">Ele permite que o processamento de pacotes personalizado seja feito quando determinadas condições forem atendidas.</span><span class="sxs-lookup"><span data-stu-id="3d974-121">It allows for custom packet processing to be done when certain conditions are met.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="3d974-122">ID</span><span class="sxs-lookup"><span data-stu-id="3d974-122">ID</span></span></li>
<li><span data-ttu-id="3d974-123">Camada aplicável</span><span class="sxs-lookup"><span data-stu-id="3d974-123">Applicable layer</span></span></li>
</ul></td>
<td><span data-ttu-id="3d974-124">O driver NAT</span><span class="sxs-lookup"><span data-stu-id="3d974-124">The NAT driver</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d974-125">Camada</span><span class="sxs-lookup"><span data-stu-id="3d974-125">Layer</span></span></td>
<td><span data-ttu-id="3d974-126">Um contêiner de filtro no mecanismo de filtro.</span><span class="sxs-lookup"><span data-stu-id="3d974-126">A filter container in the filter engine.</span></span> <br/> <span data-ttu-id="3d974-127">Representa um ponto específico no processamento de tráfego de rede em que o mecanismo de filtro é invocado.</span><span class="sxs-lookup"><span data-stu-id="3d974-127">Represents a specific point in network traffic processing where the filter engine is invoked.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="3d974-128">Esquema para filtros que podem ser adicionados à camada</span><span class="sxs-lookup"><span data-stu-id="3d974-128">Schema for filters that can be added to the layer</span></span></li>
</ul></td>
<td><span data-ttu-id="3d974-129">A camada de transporte de entrada</span><span class="sxs-lookup"><span data-stu-id="3d974-129">The Inbound Transport Layer</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d974-130">Subcamada</span><span class="sxs-lookup"><span data-stu-id="3d974-130">Sub-layer</span></span></td>
<td><span data-ttu-id="3d974-131">Um subcomponente de uma camada, usado na <a href="filter-arbitration.md">arbitragem de filtro</a>.</span><span class="sxs-lookup"><span data-stu-id="3d974-131">A sub-component of a layer, used in <a href="filter-arbitration.md">filter arbitration</a>.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="3d974-132">Peso</span><span class="sxs-lookup"><span data-stu-id="3d974-132">Weight</span></span></li>
</ul></td>
<td><span data-ttu-id="3d974-133">A subcamada de túnel IPsec</span><span class="sxs-lookup"><span data-stu-id="3d974-133">The IPsec Tunnel sub-layer</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d974-134">Provedor</span><span class="sxs-lookup"><span data-stu-id="3d974-134">Provider</span></span></td>
<td><span data-ttu-id="3d974-135">Um provedor de política que criou uma solução em WFP.</span><span class="sxs-lookup"><span data-stu-id="3d974-135">A policy provider that has built a solution on WFP.</span></span><br/> <span data-ttu-id="3d974-136">Ele é usado unicamente para gerenciamento; Ele não afeta o processamento de pacotes em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="3d974-136">It is used solely for management; it does not affect run-time packet processing.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="3d974-137">ID</span><span class="sxs-lookup"><span data-stu-id="3d974-137">ID</span></span></li>
<li><span data-ttu-id="3d974-138">Nome do serviço</span><span class="sxs-lookup"><span data-stu-id="3d974-138">Service name</span></span></li>
</ul></td>
<td><span data-ttu-id="3d974-139">Firewall do Windows com Advanced Security</span><span class="sxs-lookup"><span data-stu-id="3d974-139">Windows Firewall with Advanced Security</span></span><br/> <span data-ttu-id="3d974-140">Um aplicativo de filtragem de URL de terceiros</span><span class="sxs-lookup"><span data-stu-id="3d974-140">A 3rd-party URL filtering application</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d974-141">Contexto do provedor</span><span class="sxs-lookup"><span data-stu-id="3d974-141">Provider Context</span></span></td>
<td><span data-ttu-id="3d974-142">Um blob de dados usado por um provedor de política para armazenar informações de contexto arbitrários.</span><span class="sxs-lookup"><span data-stu-id="3d974-142">A data blob used by a policy provider to store arbitrary context information.</span></span> <br/> <span data-ttu-id="3d974-143">Ele é usado para passar informações de configuração personalizadas para um texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="3d974-143">It is used to pass custom configuration information to a callout.</span></span><br/> <span data-ttu-id="3d974-144">A maneira mais comum de usar as informações de contexto é fazer com que os filtros façam referência a um contexto de provedor.</span><span class="sxs-lookup"><span data-stu-id="3d974-144">The most common way to use the context information is to have filters reference a provider context.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="3d974-145">ID</span><span class="sxs-lookup"><span data-stu-id="3d974-145">ID</span></span></li>
<li><span data-ttu-id="3d974-146">Blob de dados</span><span class="sxs-lookup"><span data-stu-id="3d974-146">Data blob</span></span></li>
</ul></td>
<td><span data-ttu-id="3d974-147">O IPsec armazena as configurações de autenticação no mecanismo de filtragem base (BFE).</span><span class="sxs-lookup"><span data-stu-id="3d974-147">IPsec stores authentication settings in the Base Filtering Engine ( BFE).</span></span> <span data-ttu-id="3d974-148">A &quot; &quot; Propriedade Context de um filtro indica as configurações de autenticação a serem usadas para o tráfego que o filtro descreve.</span><span class="sxs-lookup"><span data-stu-id="3d974-148">The &quot;Context&quot; property of a filter indicates the authentication settings to use for the traffic that the filter describes.</span></span><br/> <span data-ttu-id="3d974-149">O Shim de seleção de certificação SSL armazenará informações de certificação em um contexto de provedor.</span><span class="sxs-lookup"><span data-stu-id="3d974-149">The SSL certification selection shim will store certification information in a provider context.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3d974-150">Os tipos de objeto expostos pela API WFP têm semânticas consistentes.</span><span class="sxs-lookup"><span data-stu-id="3d974-150">The object types exposed by WFP API have consistent semantics.</span></span> <span data-ttu-id="3d974-151">As ações de adicionar, enumerar, assinar e assim por diante são semelhantes para todos os tipos de objeto.</span><span class="sxs-lookup"><span data-stu-id="3d974-151">The actions of add, enumerate, subscribe, and so on are similar for all object types.</span></span>

<span data-ttu-id="3d974-152">Cada tipo de objeto é representado por uma estrutura de dados (por exemplo, [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)).</span><span class="sxs-lookup"><span data-stu-id="3d974-152">Each object type is represented by a data structure (for example, [**FWPM\_FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)).</span></span> <span data-ttu-id="3d974-153">Para minimizar o número de diferentes estruturas de dados expostas pela API WFP, a mesma estrutura de dados é usada para adicionar novos objetos e recuperar os existentes.</span><span class="sxs-lookup"><span data-stu-id="3d974-153">In order to minimize the number of different data structures exposed by the WFP API, the same data structure is used for both adding new objects and retrieving existing ones.</span></span> <span data-ttu-id="3d974-154">Portanto, pode haver campos em cada estrutura de dados que são ignorados ao adicionar um novo objeto, já que esses campos são preenchidos pelo BFE (mecanismo de filtragem base) e não pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="3d974-154">Thus, there may be fields in each data structure that are ignored when adding a new object since these fields are filled in by the Base Filtering Engine (BFE), and not by the caller.</span></span> <span data-ttu-id="3d974-155">Por exemplo, uma estrutura de dados **FWPM \_ FILTER0** tem um campo **filterid** que contém o **LUID** do **\_ FILTER0 FWPS** correspondente.</span><span class="sxs-lookup"><span data-stu-id="3d974-155">For example, an **FWPM\_FILTER0** data structure has a **filterId** field that contains the **LUID** of the corresponding **FWPS\_FILTER0**.</span></span> <span data-ttu-id="3d974-156">Esse **LUID** é atribuído por BFE e, portanto, esse campo é ignorado na chamada para [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).</span><span class="sxs-lookup"><span data-stu-id="3d974-156">This **LUID** is assigned by BFE, and thus, this field is ignored in the call to [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d974-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d974-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d974-158">Gerenciamento de objetos</span><span class="sxs-lookup"><span data-stu-id="3d974-158">Object Management</span></span>](object-management.md)
</dt> </dl>

 

 





