---
title: API WFP
description: A API da WFP (Windows Filtering Platform) é dividida nos componentes a seguir.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4230c82105f85c36e6fb112508a7128758b2ad60
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "105810376"
---
# <a name="wfp-api"></a><span data-ttu-id="94699-103">API WFP</span><span class="sxs-lookup"><span data-stu-id="94699-103">WFP API</span></span>

<span data-ttu-id="94699-104">A API da WFP (Windows Filtering Platform) é dividida nos componentes a seguir.</span><span class="sxs-lookup"><span data-stu-id="94699-104">The Windows Filtering Platform (WFP) API is divided into the following components.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="94699-105">Componente</span><span class="sxs-lookup"><span data-stu-id="94699-105">Component</span></span></th>
<th><span data-ttu-id="94699-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="94699-106">Description</span></span></th>
<th><span data-ttu-id="94699-107">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="94699-107">Header Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="94699-108"><a href="/windows-hardware/drivers/ddi/_netvista/">API de texto explicativo</a> (FWPS) $ {remove} $</span><span class="sxs-lookup"><span data-stu-id="94699-108"><a href="/windows-hardware/drivers/ddi/_netvista/">Callout API</a> (FWPS)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="94699-109"><a href="/windows-hardware/drivers/ddi/_netvista/">Tipos de dados</a> usados por textos explicativos. <strong>Observação</strong>  Esses tipos de dados estão documentados no Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="94699-109"><a href="/windows-hardware/drivers/ddi/_netvista/">Data types</a> used by callouts.<strong>Note</strong>  These data types are documented in the Microsoft Windows Driver Development Kit (DDK).</span></span><br/></td>
<td><dl> <span data-ttu-id="94699-110">fwpstypes. h</span><span class="sxs-lookup"><span data-stu-id="94699-110">fwpstypes.h</span></span><br />
<span data-ttu-id="94699-111">fwpstypes. idl</span><span class="sxs-lookup"><span data-stu-id="94699-111">fwpstypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94699-112"><a href="/windows-hardware/drivers/ddi/_netvista/">Funções</a> e <a href="/windows-hardware/drivers/ddi/_netvista/">tipos enumerados</a> usados para implementar textos explicativos. <strong>Observação</strong>  Essas funções e os tipos enumerados são documentados no DDK.</span><span class="sxs-lookup"><span data-stu-id="94699-112"><a href="/windows-hardware/drivers/ddi/_netvista/">Functions</a> and <a href="/windows-hardware/drivers/ddi/_netvista/">enumerated types</a> used to implement callouts.<strong>Note</strong>  These functions and enumerated types are documented in the DDK.</span></span><br/></td>
<td><dl> <span data-ttu-id="94699-113">fwpsu. h</span><span class="sxs-lookup"><span data-stu-id="94699-113">fwpsu.h</span></span><br />
<span data-ttu-id="94699-114">fwpsk. h</span><span class="sxs-lookup"><span data-stu-id="94699-114">fwpsk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="94699-115">API IKE/AuthIP (IKEEXT) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="94699-115">IKE/AuthIP API (IKEEXT)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="94699-116"><a href="fwp-enums.md">Tipos enumerados</a> e <a href="fwp-structs.md">estruturas</a> usadas para gerenciar a política e as associações de segurança do modo principal (mm) Ike e AuthIP.</span><span class="sxs-lookup"><span data-stu-id="94699-116"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IKE and AuthIP main mode (MM) policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="94699-117">iketypes. h</span><span class="sxs-lookup"><span data-stu-id="94699-117">iketypes.h</span></span><br />
<span data-ttu-id="94699-118">iketypes. idl</span><span class="sxs-lookup"><span data-stu-id="94699-118">iketypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94699-119"><a href="fwp-ike-functions.md">Funções</a> usadas para gerenciar a política e associações de segurança IKE e AuthIP mm.</span><span class="sxs-lookup"><span data-stu-id="94699-119"><a href="fwp-ike-functions.md">Functions</a> used for managing IKE and AuthIP MM policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="94699-120">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="94699-120">fwpmu.h</span></span><br />
<span data-ttu-id="94699-121">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="94699-121">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="94699-122">API IPsec (IPSEC) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="94699-122">IPsec API (IPSEC)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="94699-123"><a href="fwp-enums.md">Tipos enumerados</a> e <a href="fwp-structs.md">estruturas</a> usadas para gerenciar diretivas IPSec e associações de segurança.</span><span class="sxs-lookup"><span data-stu-id="94699-123"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="94699-124">ipsectypes. h</span><span class="sxs-lookup"><span data-stu-id="94699-124">ipsectypes.h</span></span><br />
<span data-ttu-id="94699-125">ipsectypes. idl</span><span class="sxs-lookup"><span data-stu-id="94699-125">ipsectypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94699-126"><a href="fwp-ipsec-functions.md">Funções</a> usadas para gerenciar diretivas IPSec e associações de segurança.</span><span class="sxs-lookup"><span data-stu-id="94699-126"><a href="fwp-ipsec-functions.md">Functions</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="94699-127">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="94699-127">fwpmu.h</span></span><br />
<span data-ttu-id="94699-128">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="94699-128">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="94699-129">API de gerenciamento (FWPM) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="94699-129">Management API (FWPM)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="94699-130"><a href="fwp-enums.md">Tipos enumerados</a> e <a href="fwp-structs.md">estruturas</a> usadas para gerenciar o mecanismo de filtro.</span><span class="sxs-lookup"><span data-stu-id="94699-130"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing the filter engine.</span></span></td>
<td><dl> <span data-ttu-id="94699-131">fwpmtypes. h</span><span class="sxs-lookup"><span data-stu-id="94699-131">fwpmtypes.h</span></span><br />
<span data-ttu-id="94699-132">fwpmtypes. idl</span><span class="sxs-lookup"><span data-stu-id="94699-132">fwpmtypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94699-133"><a href="fwp-mgmt-functions.md">Funções</a> usadas para gerenciar o mecanismo de filtro.</span><span class="sxs-lookup"><span data-stu-id="94699-133"><a href="fwp-mgmt-functions.md">Functions</a> used for managing the filter engine.</span></span> <span data-ttu-id="94699-134">Essas funções são usadas para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="94699-134">These functions are used to perform the following tasks:</span></span><br/>
<ul>
<li><span data-ttu-id="94699-135">Definir e consultar filtros, provedores e textos explicativos.</span><span class="sxs-lookup"><span data-stu-id="94699-135">Set and query filters, providers, and callouts.</span></span></li>
<li><span data-ttu-id="94699-136">Recuperar estatísticas de IPsec.</span><span class="sxs-lookup"><span data-stu-id="94699-136">Retrieve IPsec statistics.</span></span></li>
<li><span data-ttu-id="94699-137">Configure a plataforma de filtragem do Windows.</span><span class="sxs-lookup"><span data-stu-id="94699-137">Configure the Windows Filtering Platform.</span></span></li>
</ul></td>
<td><dl> <span data-ttu-id="94699-138">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="94699-138">fwpmu.h</span></span><br />
<span data-ttu-id="94699-139">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="94699-139">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="94699-140">API compartilhada (FWP)</span><span class="sxs-lookup"><span data-stu-id="94699-140">Shared API (FWP)</span></span></td>
<td><span data-ttu-id="94699-141"><a href="fwp-enums.md">Tipos enumerados</a> fundamentais e <a href="fwp-structs.md">estruturas</a> compartilhadas na plataforma de filtragem do Windows.</span><span class="sxs-lookup"><span data-stu-id="94699-141">Fundamental <a href="fwp-enums.md">enumerated types</a> and <a href="fwp-structs.md">structures</a> shared across the Windows Filtering Platform.</span></span></td>
<td><dl> <span data-ttu-id="94699-142">fwptypes. h</span><span class="sxs-lookup"><span data-stu-id="94699-142">fwptypes.h</span></span><br />
<span data-ttu-id="94699-143">fwptypes. idl</span><span class="sxs-lookup"><span data-stu-id="94699-143">fwptypes.idl</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="94699-144">Os nomes de tipos de dados são todos delimitados por letras maiúsculas e sublinhados.</span><span class="sxs-lookup"><span data-stu-id="94699-144">Data type names are all upper-case and underscore-delimited.</span></span> <span data-ttu-id="94699-145">O nome sempre começa com um prefixo que identifica seu grupo de componentes, como [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).</span><span class="sxs-lookup"><span data-stu-id="94699-145">The name always begins with a prefix that identifies its component group, such as [**FWPM\_PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).</span></span>

<span data-ttu-id="94699-146">Os nomes de função são de caso misto e delimitados por maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="94699-146">Function names are mixed-case and case-delimited.</span></span> <span data-ttu-id="94699-147">O nome sempre começa com um prefixo que identifica seu grupo de componentes, como [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).</span><span class="sxs-lookup"><span data-stu-id="94699-147">The name always begins with a prefix that identifies its component group, such as [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).</span></span>

<span data-ttu-id="94699-148">A maioria dos nomes de função e de dados termina com um número de versão.</span><span class="sxs-lookup"><span data-stu-id="94699-148">Most data and function names end with a version number.</span></span> <span data-ttu-id="94699-149">O arquivo de cabeçalho fwpvi. h mapeia os dados independentes de versão e os nomes de função para a versão apropriada para uso com um determinado sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="94699-149">The fwpvi.h header file maps version-independent data and function names to the version that is appropriate for use with a given operating system.</span></span> <span data-ttu-id="94699-150">Para obter mais informações, consulte [nomes de Version-Independent WFP e direcionamento de versões específicas do Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).</span><span class="sxs-lookup"><span data-stu-id="94699-150">For more information, see [WFP Version-Independent Names and Targeting Specific Versions of Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).</span></span>

<span data-ttu-id="94699-151">Cada componente não é autônomo.</span><span class="sxs-lookup"><span data-stu-id="94699-151">Each component does not stand alone.</span></span> <span data-ttu-id="94699-152">Por exemplo, as políticas de modo principal (MM) IKE são definidas no componente IKEEXT, mas são armazenadas em um contexto de provedor e são associadas a um filtro que são encontrados no componente de API FWPM.</span><span class="sxs-lookup"><span data-stu-id="94699-152">For example, IKE main mode (MM) policies are defined in the IKEEXT component, but are stored in a provider context and are associated with a filter both of which are found in the FWPM API component.</span></span>

## <a name="user-mode-and-kernel-mode-public-header-files"></a><span data-ttu-id="94699-153">User-Mode e Kernel-Mode arquivos de cabeçalho público</span><span class="sxs-lookup"><span data-stu-id="94699-153">User-Mode and Kernel-Mode Public Header Files</span></span>

<span data-ttu-id="94699-154">A maioria das funções de WFP pode ser chamada no modo de usuário ou no modo kernel.</span><span class="sxs-lookup"><span data-stu-id="94699-154">Most of the WFP functions can be called from either user mode or kernel mode.</span></span> <span data-ttu-id="94699-155">No entanto, as funções de modo de usuário retornam um valor **DWORD** que representa um código de erro Win32, enquanto as funções de modo kernel retornam um valor **NTSTATUS** que representa um código de status NT.</span><span class="sxs-lookup"><span data-stu-id="94699-155">However, user-mode functions return a **DWORD** value that represents a Win32 error code, whereas kernel-mode functions return an **NTSTATUS** value that represents an NT status code.</span></span> <span data-ttu-id="94699-156">Como resultado, os nomes de função e a semântica são idênticos entre o modo de usuário e o modo kernel, mas as assinaturas de função não são.</span><span class="sxs-lookup"><span data-stu-id="94699-156">As a result, function names and semantics are identical between user mode and kernel mode, but function signatures are not.</span></span> <span data-ttu-id="94699-157">Isso requer cabeçalhos específicos de modo de usuário e de modo kernel para os protótipos de função.</span><span class="sxs-lookup"><span data-stu-id="94699-157">This requires separate user-mode and kernel-mode specific headers for the function prototypes.</span></span> <span data-ttu-id="94699-158">Os nomes de arquivo de cabeçalho do modo de usuário terminam em "u" e os nomes de arquivo de cabeçalho do modo kernel terminam em "k".</span><span class="sxs-lookup"><span data-stu-id="94699-158">User-mode header file names end in "u" and kernel-mode header file names end in "k".</span></span>

<span data-ttu-id="94699-159">A tabela a seguir lista os arquivos de cabeçalho do Win32 que definem as funções de WFP.</span><span class="sxs-lookup"><span data-stu-id="94699-159">The following table lists the Win32 header files that define the WFP functions.</span></span>

| <span data-ttu-id="94699-160">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="94699-160">Header Files</span></span> | <span data-ttu-id="94699-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="94699-161">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94699-162">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="94699-162">fwpmk.h</span></span>      | <span data-ttu-id="94699-163">Protótipos de função em modo kernel para componentes FWPM, IPsec e IKEEXT.</span><span class="sxs-lookup"><span data-stu-id="94699-163">Kernel-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="94699-164">Disponível somente no DDK.</span><span class="sxs-lookup"><span data-stu-id="94699-164">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="94699-165">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="94699-165">fwpmu.h</span></span>      | <span data-ttu-id="94699-166">Protótipos de função de modo de usuário para componentes FWPM, IPsec e IKEEXT.</span><span class="sxs-lookup"><span data-stu-id="94699-166">User-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="94699-167">Disponível apenas no Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="94699-167">Available in the Microsoft Windows Software Development Kit (SDK) only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="94699-168">fwpsk. h</span><span class="sxs-lookup"><span data-stu-id="94699-168">fwpsk.h</span></span>      | <span data-ttu-id="94699-169">Protótipos de função no modo kernel e tipos enumerados para o componente FWPS.</span><span class="sxs-lookup"><span data-stu-id="94699-169">Kernel-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="94699-170">Disponível somente no DDK.</span><span class="sxs-lookup"><span data-stu-id="94699-170">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="94699-171">fwpsu. h</span><span class="sxs-lookup"><span data-stu-id="94699-171">fwpsu.h</span></span>      | <span data-ttu-id="94699-172">Protótipos de função de modo de usuário e tipos enumerados para o componente FWPS.</span><span class="sxs-lookup"><span data-stu-id="94699-172">User-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="94699-173">Disponível somente no SDK do Windows. **Observação**  Os tipos enumerados do modo de usuário FWPS são idênticos aos tipos enumerados do modo kernel FWPS.</span><span class="sxs-lookup"><span data-stu-id="94699-173">Available in the Windows SDK only.**Note**  The user-mode FWPS enumerated types are identical to the kernel-mode FWPS enumerated types.</span></span> <span data-ttu-id="94699-174">Em consequência, esses tipos são documentados apenas no DDK.</span><span class="sxs-lookup"><span data-stu-id="94699-174">In consequence, these types are documented in the DDK only.</span></span><br/> <span data-ttu-id="94699-175">**Observação**  Os protótipos de função FWPS de modo de usuário são idênticos aos protótipos de função FWPS de modo kernel com a exceção do código de retorno.</span><span class="sxs-lookup"><span data-stu-id="94699-175">**Note**  The user-mode FWPS function prototypes are identical to the kernel-mode FWPS function prototypes with the exception of the return code.</span></span> <span data-ttu-id="94699-176">As funções FWPS de modo de usuário retornam uma **DWORD**, enquanto as funções FWPS de modo kernel retornam um **NTSTATUS**.</span><span class="sxs-lookup"><span data-stu-id="94699-176">User-mode FWPS functions return a **DWORD**, whereas kernel-mode FWPS functions return an **NTSTATUS**.</span></span> <span data-ttu-id="94699-177">Em consequência, essas funções são documentadas somente no DDK.</span><span class="sxs-lookup"><span data-stu-id="94699-177">In consequence, these functions are documented in the DDK only.</span></span><br/> |



 

<span data-ttu-id="94699-178">Todas as funções de modo de usuário são exportadas de fwpuclnt.dll.</span><span class="sxs-lookup"><span data-stu-id="94699-178">All user-mode functions are exported from fwpuclnt.dll.</span></span> <span data-ttu-id="94699-179">Todas as funções de modo kernel são exportadas de fwpkclnt.sys.</span><span class="sxs-lookup"><span data-stu-id="94699-179">All kernel-mode functions are exported from fwpkclnt.sys.</span></span>

### <a name="management-fwpm-and-callout-fwps-data-types"></a><span data-ttu-id="94699-180">Tipos de dados de gerenciamento (FWPM) e texto explicativo (FWPS)</span><span class="sxs-lookup"><span data-stu-id="94699-180">Management (FWPM) and Callout (FWPS) Data Types</span></span>

<span data-ttu-id="94699-181">A maioria dos tipos de dados FWPM, que são usados para tarefas de gerenciamento, como adicionar filtros ou textos explicativos de um aplicativo ou driver, têm contrapartes FWPS.</span><span class="sxs-lookup"><span data-stu-id="94699-181">Most FWPM data types, which are used for management tasks such as adding filters or callouts from an application or driver, have FWPS counterparts.</span></span> <span data-ttu-id="94699-182">Os tipos de dados FWPS são usados durante a filtragem real do tráfego de rede, no contexto de uma rotina de texto explicativo para classificação.</span><span class="sxs-lookup"><span data-stu-id="94699-182">The FWPS data types are used during the actual filtering of network traffic, in the context of a callout routine for classification.</span></span>

<span data-ttu-id="94699-183">Por exemplo, para adicionar um filtro a uma determinada camada de mecanismo de filtragem, o programador deve usar um tipo FWPM, como: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` .</span><span class="sxs-lookup"><span data-stu-id="94699-183">For example, in order to add a filter to a certain filtering engine layer, the programmer should use an FWPM type, like: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET`.</span></span> <span data-ttu-id="94699-184">Para verificar a qual camada um texto explicativo está sendo chamado, o programador deve usar o tipo de FWPS correspondente: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .</span><span class="sxs-lookup"><span data-stu-id="94699-184">To check which layer a callout is being called from, the programmer should use the corresponding FWPS type: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)`.</span></span>

<span data-ttu-id="94699-185">Algumas contrapartes FWPS para tipos de dados FWPM estão expandindo os tipos de dados FWPM originais.</span><span class="sxs-lookup"><span data-stu-id="94699-185">Some FWPS counterparts to FWPM data types are expanding the original FWPM data types.</span></span> <span data-ttu-id="94699-186">Por exemplo, para adicionar uma condição de filtro em muitas camadas de mecanismo de filtragem, o programador especifica o mesmo que a `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` camada do mecanismo de filtragem.</span><span class="sxs-lookup"><span data-stu-id="94699-186">For example, to add a filter condition at many filtering engine layers, the programmer specifies the `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` regardless of the filtering engine layer.</span></span> <span data-ttu-id="94699-187">Para localizar um valor de condição de filtro, o programador especifica um tipo de FWPS específico de camada, como: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` .</span><span class="sxs-lookup"><span data-stu-id="94699-187">To find a filter condition value, the programmer specifies a layer specific FWPS type, like: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]`.</span></span>

<span data-ttu-id="94699-188">Os tipos de dados FWPS são geralmente menores do que suas contrapartes FWPM.</span><span class="sxs-lookup"><span data-stu-id="94699-188">The FWPS data types are generally smaller than their FWPM counterparts.</span></span> <span data-ttu-id="94699-189">Por exemplo, os [**identificadores da camada de filtragem FWPM**](management-filtering-layer-identifiers-.md) são **GUIDs**(16 bytes) enquanto os [identificadores da camada de filtragem FWPS](/windows-hardware/drivers/network/management-filtering-layer-identifiers) são **UINT16** (16 bits).</span><span class="sxs-lookup"><span data-stu-id="94699-189">For example, the [**FWPM filtering layer identifiers**](management-filtering-layer-identifiers-.md) are **GUID** s (16-bytes) whereas the [FWPS filtering layer identifiers](/windows-hardware/drivers/network/management-filtering-layer-identifiers) are **UINT16** (16-bits).</span></span> <span data-ttu-id="94699-190">O tamanho menor para os tipos de dados FWPS melhora o desempenho do sistema, pois comparações de inteiros compensam as comparações de **GUID** para tráfego em tempo real.</span><span class="sxs-lookup"><span data-stu-id="94699-190">The smaller size for FWPS data types improves system performance since integer comparisons outweigh **GUID** comparisons for real-time traffic.</span></span> <span data-ttu-id="94699-191">Além disso, a memória do kernel é usada com eficiência, pois os tipos FWPS são todos usados no kernel para gerenciar os filtros, enquanto os tipos FWPM são armazenados no modo de usuário para gerenciar as diferentes camadas.</span><span class="sxs-lookup"><span data-stu-id="94699-191">Also, the kernel memory is used efficiently since the FWPS types are all used in the kernel for managing the filters, whereas the FWPM types are stored in user-mode to manage the different layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94699-192">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94699-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94699-193">Modelo de objeto da API WFP</span><span class="sxs-lookup"><span data-stu-id="94699-193">WFP API Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="94699-194">Gerenciamento de objetos de API WFP</span><span class="sxs-lookup"><span data-stu-id="94699-194">WFP API Object Management</span></span>](object-management.md)
</dt> </dl>

