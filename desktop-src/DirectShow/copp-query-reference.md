---
description: Referência de consulta COPP
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: Referência de consulta COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41de36f3cdcc37a38e2ebc53caa7b6b37c204d9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010065"
---
# <a name="copp-query-reference"></a><span data-ttu-id="56417-103">Referência de consulta COPP</span><span class="sxs-lookup"><span data-stu-id="56417-103">COPP Query Reference</span></span>

<span data-ttu-id="56417-104">Esta seção descreve as consultas de status com suporte pelo protocolo de proteção de saída certificado (COPP).</span><span class="sxs-lookup"><span data-stu-id="56417-104">This section describes the status queries that are supported by Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="56417-105">Para cada consulta, o GUID que define a consulta é listado, junto com os dados de entrada e retorna dados.</span><span class="sxs-lookup"><span data-stu-id="56417-105">For each query, the GUID that defines the query is listed, along with the input data and return data.</span></span>



| <span data-ttu-id="56417-106">Consulta</span><span class="sxs-lookup"><span data-stu-id="56417-106">Query</span></span>                   | <span data-ttu-id="56417-107">GUID</span><span class="sxs-lookup"><span data-stu-id="56417-107">GUID</span></span>                                     |
|-------------------------|------------------------------------------|
| <span data-ttu-id="56417-108">Dados de barramento</span><span class="sxs-lookup"><span data-stu-id="56417-108">Bus Data</span></span>                | <span data-ttu-id="56417-109">**COPPQueryBusData de DXVA \_**</span><span class="sxs-lookup"><span data-stu-id="56417-109">**DXVA\_COPPQueryBusData**</span></span>               |
| <span data-ttu-id="56417-110">Tipo de Conector</span><span class="sxs-lookup"><span data-stu-id="56417-110">Connector Type</span></span>          | <span data-ttu-id="56417-111">**COPPQueryConnectorType de DXVA \_**</span><span class="sxs-lookup"><span data-stu-id="56417-111">**DXVA\_COPPQueryConnectorType**</span></span>         |
| <span data-ttu-id="56417-112">Exibir dados</span><span class="sxs-lookup"><span data-stu-id="56417-112">Display Data</span></span>            | <span data-ttu-id="56417-113">**COPPQueryDisplayData de DXVA \_**</span><span class="sxs-lookup"><span data-stu-id="56417-113">**DXVA\_COPPQueryDisplayData**</span></span>           |
| <span data-ttu-id="56417-114">Dados de chave de HDCP</span><span class="sxs-lookup"><span data-stu-id="56417-114">HDCP Key Data</span></span>           | <span data-ttu-id="56417-115">**COPPQueryHDCPKeyData de DXVA \_**</span><span class="sxs-lookup"><span data-stu-id="56417-115">**DXVA\_COPPQueryHDCPKeyData**</span></span>           |
| <span data-ttu-id="56417-116">Nível de proteção global</span><span class="sxs-lookup"><span data-stu-id="56417-116">Global Protection Level</span></span> | <span data-ttu-id="56417-117">**COPPQueryGlobalProtectionLevel de DXVA \_**</span><span class="sxs-lookup"><span data-stu-id="56417-117">**DXVA\_COPPQueryGlobalProtectionLevel**</span></span> |
| <span data-ttu-id="56417-118">Nível de proteção local</span><span class="sxs-lookup"><span data-stu-id="56417-118">Local Protection Level</span></span>  | <span data-ttu-id="56417-119">**COPPQueryLocalProtectionLevel de DXVA \_**</span><span class="sxs-lookup"><span data-stu-id="56417-119">**DXVA\_COPPQueryLocalProtectionLevel**</span></span>  |
| <span data-ttu-id="56417-120">Tipo de proteção</span><span class="sxs-lookup"><span data-stu-id="56417-120">Protection Type</span></span>         | <span data-ttu-id="56417-121">**COPPQueryProtectionType de DXVA \_**</span><span class="sxs-lookup"><span data-stu-id="56417-121">**DXVA\_COPPQueryProtectionType**</span></span>        |
| <span data-ttu-id="56417-122">Sinalização</span><span class="sxs-lookup"><span data-stu-id="56417-122">Signaling</span></span>               | <span data-ttu-id="56417-123">**COPPQuerySignaling de DXVA \_**</span><span class="sxs-lookup"><span data-stu-id="56417-123">**DXVA\_COPPQuerySignaling**</span></span>             |



 

<span data-ttu-id="56417-124">Consulta de dados de barramento</span><span class="sxs-lookup"><span data-stu-id="56417-124">Bus Data Query</span></span>

<span data-ttu-id="56417-125">Retorna o tipo de barramento de e/s usado pelo adaptador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="56417-125">Returns the type of I/O bus used by the graphics adapter.</span></span>

-   <span data-ttu-id="56417-126">**GUID**: DXVA \_ COPPQueryBusData</span><span class="sxs-lookup"><span data-stu-id="56417-126">**GUID**: DXVA\_COPPQueryBusData</span></span>
-   <span data-ttu-id="56417-127">**Dados de entrada**: nenhum.</span><span class="sxs-lookup"><span data-stu-id="56417-127">**Input data**: None.</span></span>
-   <span data-ttu-id="56417-128">**Retornar dados**: retorna uma estrutura de [**\_ COPPStatusData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="56417-128">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="56417-129">O tipo de barramento é retornado no membro **dwData** como um sinalizador da enumeração [**de \_ BusType Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) .</span><span class="sxs-lookup"><span data-stu-id="56417-129">The bus type is returned in the **dwData** member as a flag from the [**COPP\_BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) enumeration.</span></span>

<span data-ttu-id="56417-130">Consulta de tipo de conector</span><span class="sxs-lookup"><span data-stu-id="56417-130">Connector Type Query</span></span>

<span data-ttu-id="56417-131">Retorna o tipo de conector físico.</span><span class="sxs-lookup"><span data-stu-id="56417-131">Returns the physical connector type.</span></span>

-   <span data-ttu-id="56417-132">**GUID**: DXVA \_ COPPQueryConnectorType</span><span class="sxs-lookup"><span data-stu-id="56417-132">**GUID**: DXVA\_COPPQueryConnectorType</span></span>
-   <span data-ttu-id="56417-133">**Dados de entrada**: nenhum.</span><span class="sxs-lookup"><span data-stu-id="56417-133">**Input data**: None.</span></span>
-   <span data-ttu-id="56417-134">**Retornar dados**: retorna uma estrutura de [**\_ COPPStatusData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="56417-134">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="56417-135">O tipo de conector é retornado no membro **dwData** como um sinalizador da enumeração do tipo de [**\_ conector Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) .</span><span class="sxs-lookup"><span data-stu-id="56417-135">The connector type is returned in the **dwData** member as a flag from the [**COPP\_ConnectorType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) enumeration.</span></span>

<span data-ttu-id="56417-136">Consulta de exibição de dados</span><span class="sxs-lookup"><span data-stu-id="56417-136">Display Data Query</span></span>

<span data-ttu-id="56417-137">Retorna uma descrição do sinal de vídeo que está sendo transmitido pelo conector.</span><span class="sxs-lookup"><span data-stu-id="56417-137">Returns a description of the video signal that is being transmitted over the connector.</span></span>

<span data-ttu-id="56417-138">O sinal de vídeo transmitido pelo conector não necessariamente tem o mesmo formato que o modo de exibição da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="56417-138">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="56417-139">Por exemplo, o modo de exibição de área de trabalho pode ser de 1024x768 pixels a 85 Hz, enquanto o conector pode ser um conector de S-video que transmite um sinal de vídeo em 720x480 pixels, 60/1.01 Hz entrelaçados.</span><span class="sxs-lookup"><span data-stu-id="56417-139">For example, the desktop display mode might be 1024x768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720x480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="56417-140">Nesse caso, o driver retornaria a resolução do sinal S-Video, não a resolução da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="56417-140">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

-   <span data-ttu-id="56417-141">**GUID**: DXVA \_ COPPQueryDisplayData</span><span class="sxs-lookup"><span data-stu-id="56417-141">**GUID**: DXVA\_COPPQueryDisplayData</span></span>
-   <span data-ttu-id="56417-142">**Dados de entrada**: nenhum.</span><span class="sxs-lookup"><span data-stu-id="56417-142">**Input data**: None.</span></span>
-   <span data-ttu-id="56417-143">**Retornar dados**: retorna uma estrutura de [**\_ COPPStatusDisplayData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) .</span><span class="sxs-lookup"><span data-stu-id="56417-143">**Return data**: Returns a [**DXVA\_COPPStatusDisplayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) structure.</span></span>

<span data-ttu-id="56417-144">Consulta de dados de chave de HDCP</span><span class="sxs-lookup"><span data-stu-id="56417-144">HDCP Key Data Query</span></span>

<span data-ttu-id="56417-145">Retorna o vetor de seleção de chave de HDCP do dispositivo (B-KSV).</span><span class="sxs-lookup"><span data-stu-id="56417-145">Returns the device's HDCP key selection vector (B-KSV).</span></span>

<span data-ttu-id="56417-146">O KSV é um identificador fornecido para o fabricante do dispositivo e é usado no processo de autenticação e configuração de HDCP.</span><span class="sxs-lookup"><span data-stu-id="56417-146">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="56417-147">O aplicativo deve verificar esse valor em relação à lista de KSVs revogados.</span><span class="sxs-lookup"><span data-stu-id="56417-147">The application should check this value against the list of revoked KSVs.</span></span> <span data-ttu-id="56417-148">O mecanismo para obter a lista de revogação de KSV está fora do escopo do protocolo COPP.</span><span class="sxs-lookup"><span data-stu-id="56417-148">The mechanism for obtaining the KSV revocation list is outside the scope of the COPP protocol.</span></span> <span data-ttu-id="56417-149">Para obter mais informações, consulte a especificação de HDCP.</span><span class="sxs-lookup"><span data-stu-id="56417-149">For more information, consult the HDCP specification.</span></span>

<span data-ttu-id="56417-150">Essa consulta também determina se o dispositivo HDCP conectado é um monitor ou um repetidor HDCP.</span><span class="sxs-lookup"><span data-stu-id="56417-150">This query also determines whether the connected HDCP device is a monitor or an HDCP repeater.</span></span> <span data-ttu-id="56417-151">O aplicativo não deve reproduzir conteúdo protegido se o dispositivo HDCP for um repetidor HDCP, porque eles não têm suporte de COPP.</span><span class="sxs-lookup"><span data-stu-id="56417-151">The application should not play protected content if the HDCP device is an HDCP repeater, because these are not supported by COPP.</span></span>

-   <span data-ttu-id="56417-152">**GUID**: DXVA \_ COPPQueryHDCPKeyData</span><span class="sxs-lookup"><span data-stu-id="56417-152">**GUID**: DXVA\_COPPQueryHDCPKeyData</span></span>
-   <span data-ttu-id="56417-153">**Dados de entrada**: nenhum.</span><span class="sxs-lookup"><span data-stu-id="56417-153">**Input data**: None.</span></span>
-   <span data-ttu-id="56417-154">**Retornar dados**: retorna uma estrutura de [**\_ COPPStatusHDCPKeyData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) .</span><span class="sxs-lookup"><span data-stu-id="56417-154">**Return data**: Returns a [**DXVA\_COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) structure.</span></span>

<span data-ttu-id="56417-155">Consulta de nível de proteção global</span><span class="sxs-lookup"><span data-stu-id="56417-155">Global Protection Level Query</span></span>

<span data-ttu-id="56417-156">Retorna o nível de proteção global para um mecanismo de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="56417-156">Returns the global protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="56417-157">O nível de proteção global é o nível de proteção que está sendo aplicado no conector, independentemente de como o driver de gráficos foi instruído a aplicar a proteção.</span><span class="sxs-lookup"><span data-stu-id="56417-157">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="56417-158">Por exemplo, um aplicativo pode definir o nível de proteção de ACP chamando a função **ChangeDisplaySettingsEx** .</span><span class="sxs-lookup"><span data-stu-id="56417-158">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="56417-159">Nesse caso, o nível de proteção global refletiria essa configuração, embora não tenha sido solicitada por meio de COPP.</span><span class="sxs-lookup"><span data-stu-id="56417-159">In that case, the global protection level would reflect this setting, even though it was not requested through COPP.</span></span>

-   <span data-ttu-id="56417-160">**GUID**: DXVA \_ COPPQueryGlobalProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="56417-160">**GUID**: DXVA\_COPPQueryGlobalProtectionLevel</span></span>
-   <span data-ttu-id="56417-161">**Dados de entrada**: o mecanismo de proteção a ser consultado, especificado como um inteiro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="56417-161">**Input data**: The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="56417-162">Consulte [sinalizadores de tipo de proteção Copp](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="56417-162">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="56417-163">**Retornar dados**: retorna uma estrutura de [**\_ COPPStatusData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="56417-163">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="56417-164">O nível de proteção atual é retornado no membro **dwData** .</span><span class="sxs-lookup"><span data-stu-id="56417-164">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="56417-165">O significado desse valor depende do mecanismo de proteção que é consultado.</span><span class="sxs-lookup"><span data-stu-id="56417-165">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="56417-166">Para cada mecanismo de proteção, o valor do membro **dwData** é um sinalizador de uma enumeração diferente, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="56417-166">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="56417-167">Mecanismo de proteção</span><span class="sxs-lookup"><span data-stu-id="56417-167">Protection mechanism</span></span> | <span data-ttu-id="56417-168">Enumeração</span><span class="sxs-lookup"><span data-stu-id="56417-168">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="56417-169">ACP</span><span class="sxs-lookup"><span data-stu-id="56417-169">ACP</span></span>                  | [<span data-ttu-id="56417-170">**\_Nível de \_ proteção de ACP de Copp \_**</span><span class="sxs-lookup"><span data-stu-id="56417-170">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="56417-171">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="56417-171">CGMS-A</span></span>               | [<span data-ttu-id="56417-172">**\_Nível de \_ proteção Copp CGMSA \_**</span><span class="sxs-lookup"><span data-stu-id="56417-172">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="56417-173">HDCP</span><span class="sxs-lookup"><span data-stu-id="56417-173">HDCP</span></span>                 | [<span data-ttu-id="56417-174">**\_Nível de \_ proteção de HDCP de Copp \_**</span><span class="sxs-lookup"><span data-stu-id="56417-174">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="56417-175">Consulta de nível de proteção local</span><span class="sxs-lookup"><span data-stu-id="56417-175">Local Protection Level Query</span></span>

<span data-ttu-id="56417-176">Retorna o nível de proteção local para um mecanismo de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="56417-176">Returns the local protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="56417-177">O nível de proteção local é o nível de proteção que foi solicitado por meio da sessão COPP atual.</span><span class="sxs-lookup"><span data-stu-id="56417-177">The local protection level is the protection level that was requested through the current COPP session.</span></span> <span data-ttu-id="56417-178">O driver pode definir um nível de proteção mais alto.</span><span class="sxs-lookup"><span data-stu-id="56417-178">The driver might set a higher protection level.</span></span>

-   <span data-ttu-id="56417-179">**GUID**: DXVA \_ COPPQueryLocalProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="56417-179">**GUID**: DXVA\_COPPQueryLocalProtectionLevel</span></span>
-   <span data-ttu-id="56417-180">**Dados de entrada**: o mecanismo de proteção a ser consultado como um inteiro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="56417-180">**Input data**: The protection mechanism to query, as a 32-bit integer.</span></span> <span data-ttu-id="56417-181">Consulte [sinalizadores de tipo de proteção Copp](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="56417-181">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="56417-182">**Retornar dados**: retorna uma estrutura de [**\_ COPPStatusData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="56417-182">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="56417-183">O nível de proteção atual é retornado no membro **dwData** .</span><span class="sxs-lookup"><span data-stu-id="56417-183">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="56417-184">O significado desse valor depende do mecanismo de proteção que é consultado.</span><span class="sxs-lookup"><span data-stu-id="56417-184">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="56417-185">Para cada mecanismo de proteção, o valor do membro **dwData** é um sinalizador de uma enumeração diferente, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="56417-185">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="56417-186">Mecanismo de proteção</span><span class="sxs-lookup"><span data-stu-id="56417-186">Protection mechanism</span></span> | <span data-ttu-id="56417-187">Enumeração</span><span class="sxs-lookup"><span data-stu-id="56417-187">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="56417-188">ACP</span><span class="sxs-lookup"><span data-stu-id="56417-188">ACP</span></span>                  | [<span data-ttu-id="56417-189">**\_Nível de \_ proteção de ACP de Copp \_**</span><span class="sxs-lookup"><span data-stu-id="56417-189">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="56417-190">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="56417-190">CGMS-A</span></span>               | [<span data-ttu-id="56417-191">**\_Nível de \_ proteção Copp CGMSA \_**</span><span class="sxs-lookup"><span data-stu-id="56417-191">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="56417-192">HDCP</span><span class="sxs-lookup"><span data-stu-id="56417-192">HDCP</span></span>                 | [<span data-ttu-id="56417-193">**\_Nível de \_ proteção de HDCP de Copp \_**</span><span class="sxs-lookup"><span data-stu-id="56417-193">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="56417-194">Consulta de tipo de proteção</span><span class="sxs-lookup"><span data-stu-id="56417-194">Protection Type Query</span></span>

<span data-ttu-id="56417-195">Retorna os mecanismos de proteção disponíveis para o conector.</span><span class="sxs-lookup"><span data-stu-id="56417-195">Returns the protection mechanisms that are available for the connector.</span></span>

-   <span data-ttu-id="56417-196">**GUID**: DXVA \_ COPPQueryProtectionType</span><span class="sxs-lookup"><span data-stu-id="56417-196">**GUID**: DXVA\_COPPQueryProtectionType</span></span>
-   <span data-ttu-id="56417-197">**Dados de entrada**: nenhum.</span><span class="sxs-lookup"><span data-stu-id="56417-197">**Input data**: None.</span></span>
-   <span data-ttu-id="56417-198">**Retornar dados**: retorna uma estrutura de [**\_ COPPStatusData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="56417-198">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="56417-199">Os mecanismos de proteção são retornados no membro **dwData** como uma combinação de zero ou mais sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="56417-199">The protection mechanisms are returned in the **dwData** member as a combination of zero or more flags.</span></span> <span data-ttu-id="56417-200">Consulte [sinalizadores de tipo de proteção Copp](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="56417-200">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span> <span data-ttu-id="56417-201">Se mais de um mecanismo de proteção estiver disponível, os sinalizadores serão combinados com um **OR bit a** bit.</span><span class="sxs-lookup"><span data-stu-id="56417-201">If more than one protection mechanism is available, the flags are combined with a bitwise **OR**.</span></span>

<span data-ttu-id="56417-202">Consulta de sinalização</span><span class="sxs-lookup"><span data-stu-id="56417-202">Signaling Query</span></span>

<span data-ttu-id="56417-203">Retorna uma lista de todos os padrões de proteção compatíveis com o driver, o padrão atualmente ativo e a taxa de proporção atual ou outros dados de sinalização.</span><span class="sxs-lookup"><span data-stu-id="56417-203">Returns a list of all the protection standards that are supported by the driver, the standard that is currently active, and the current aspect ratio or other signaling data.</span></span>

-   <span data-ttu-id="56417-204">**GUID**: DXVA \_ COPPQuerySignaling</span><span class="sxs-lookup"><span data-stu-id="56417-204">**GUID**: DXVA\_COPPQuerySignaling</span></span>
-   <span data-ttu-id="56417-205">**Dados de entrada**: nenhum.</span><span class="sxs-lookup"><span data-stu-id="56417-205">**Input data**: None.</span></span>
-   <span data-ttu-id="56417-206">**Retornar dados**: retorna uma estrutura de [**\_ COPPStatusSignalingCmdData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) .</span><span class="sxs-lookup"><span data-stu-id="56417-206">**Return data**: Returns a [**DXVA\_COPPStatusSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56417-207">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="56417-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56417-208">Usando o protocolo COPP (certificado de proteção de saída)</span><span class="sxs-lookup"><span data-stu-id="56417-208">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



