---
title: Estrutura de IP_SPECIFIC_DATA (RTM. h)
description: A \_ estrutura de dados específica de IP contém dados específicos de IP.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- RAS da estrutura de IP_SPECIFIC_DATA
- RAS de ponteiro de estrutura de PIP_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- IP_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a3ed319f7cf42295bf918ed3ec67f5d59fe5d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085888"
---
# <a name="ip_specific_data-structure"></a><span data-ttu-id="1e773-105">\_Estrutura de dados específica de IP \_</span><span class="sxs-lookup"><span data-stu-id="1e773-105">IP\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="1e773-106">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1e773-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="1e773-107">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="1e773-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="1e773-108">A estrutura de **\_ dados específica de IP** contém dados específicos de IP.</span><span class="sxs-lookup"><span data-stu-id="1e773-108">The **IP\_SPECIFIC DATA** structure contains IP-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e773-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e773-109">Syntax</span></span>


```C++
typedef struct _IP_SPECIFIC_DATA {
  DWORD FSD_Type;
  DWORD FSD_Policy;
  DWORD FSD_NextHopAS;
  DWORD FSD_Priority;
  DWORD FSD_Metric;
  DWORD FSD_Metric1;
  DWORD FSD_Metric2;
  DWORD FSD_Metric3;
  DWORD FSD_Metric4;
  DWORD FSD_Metric5;
  DWORD FSD_Flags;
} IP_SPECIFIC_DATA, *PIP_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="1e773-110">Membros</span><span class="sxs-lookup"><span data-stu-id="1e773-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="1e773-111">**Tipo de FSD \_**</span><span class="sxs-lookup"><span data-stu-id="1e773-111">**FSD\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="1e773-112">Especifica o tipo de rota conforme definido no [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="1e773-112">Specifies the route type as defined in [RFC 1354](routing-protocols-request-for-comments.md).</span></span> <span data-ttu-id="1e773-113">A tabela a seguir mostra os valores possíveis para esse membro.</span><span class="sxs-lookup"><span data-stu-id="1e773-113">The following table shows the possible values for this member.</span></span>



| <span data-ttu-id="1e773-114">Membro</span><span class="sxs-lookup"><span data-stu-id="1e773-114">Member</span></span>                                                                                               | <span data-ttu-id="1e773-115">Significado</span><span class="sxs-lookup"><span data-stu-id="1e773-115">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="1e773-116"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1e773-116"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="1e773-117">O tipo de rota não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="1e773-117">The route type is not specified.</span></span> <span data-ttu-id="1e773-118">O tipo é diferente daqueles listados aqui.</span><span class="sxs-lookup"><span data-stu-id="1e773-118">The type is different from those listed here.</span></span><br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <span data-ttu-id="1e773-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1e773-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="1e773-120">A rota é inválida.</span><span class="sxs-lookup"><span data-stu-id="1e773-120">The route is invalid.</span></span> <span data-ttu-id="1e773-121">Normalmente, esse valor é usado para invalidar uma rota.</span><span class="sxs-lookup"><span data-stu-id="1e773-121">Normally, this value is used to invalidate a route.</span></span> <span data-ttu-id="1e773-122">No entanto, como a invalidação não é suportada pelo Gerenciador de tabelas de roteamento, a rota ainda é considerada em cálculos de melhor rota.</span><span class="sxs-lookup"><span data-stu-id="1e773-122">However, since invalidation is not supported by the routing table manager, the route is still considered in best-route computations.</span></span> <span data-ttu-id="1e773-123">Portanto, os protocolos de roteamento não devem usar esse valor.</span><span class="sxs-lookup"><span data-stu-id="1e773-123">Therefore, routing protocols should not use this value.</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="1e773-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="1e773-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="1e773-125">A rota é uma rota local, ou seja, o próximo salto é o destino final.</span><span class="sxs-lookup"><span data-stu-id="1e773-125">The route is a local route, that is, the next hop is the final destination.</span></span><br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <span data-ttu-id="1e773-126"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="1e773-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="1e773-127">A rota é uma rota remota, ou seja, o próximo salto não é o destino final.</span><span class="sxs-lookup"><span data-stu-id="1e773-127">The route is a remote route, that is, the next hop is not the final destination.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="1e773-128">**Política de FSD \_**</span><span class="sxs-lookup"><span data-stu-id="1e773-128">**FSD\_Policy**</span></span>
</dt> <dd>

<span data-ttu-id="1e773-129">Especifica o conjunto de condições que causaria a seleção de uma rota de vários caminhos.</span><span class="sxs-lookup"><span data-stu-id="1e773-129">Specifies the set of conditions that would cause the selection of a multi-path route.</span></span> <span data-ttu-id="1e773-130">Esse membro normalmente está no formato IP TOS.</span><span class="sxs-lookup"><span data-stu-id="1e773-130">This member is typically in IP TOS format.</span></span> <span data-ttu-id="1e773-131">Para obter mais informações, consulte [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="1e773-131">For more information, see [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e773-132">**FSD \_ NextHopAS**</span><span class="sxs-lookup"><span data-stu-id="1e773-132">**FSD\_NextHopAS**</span></span>
</dt> <dd>

<span data-ttu-id="1e773-133">Especifica o número do sistema autônomo do próximo salto.</span><span class="sxs-lookup"><span data-stu-id="1e773-133">Specifies the autonomous system number of the next hop.</span></span>

</dd> <dt>

<span data-ttu-id="1e773-134">**\_Prioridade FSD**</span><span class="sxs-lookup"><span data-stu-id="1e773-134">**FSD\_Priority**</span></span>
</dt> <dd>

<span data-ttu-id="1e773-135">Especifica um valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="1e773-135">Specifies a metric value.</span></span> <span data-ttu-id="1e773-136">O Gerenciador de tabela de roteamento usa esse valor para comparar essa entrada de rota com entradas de rota obtidas de outros protocolos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="1e773-136">The routing table manager uses this value to compare this route entry to route entries obtained from other routing protocols.</span></span> <span data-ttu-id="1e773-137">O valor desse membro é definido pelo Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="1e773-137">The value of this member is set by the routing table manager.</span></span>

</dd> <dt>

<span data-ttu-id="1e773-138">**\_Métrica FSD**</span><span class="sxs-lookup"><span data-stu-id="1e773-138">**FSD\_Metric**</span></span>
</dt> <dd>

<span data-ttu-id="1e773-139">Especifica um valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="1e773-139">Specifies a metric value.</span></span> <span data-ttu-id="1e773-140">O Gerenciador de tabela de roteamento usa esse valor para comparar essa entrada de rota com outras entradas de rota obtidas do mesmo protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="1e773-140">The routing table manager uses this value to compare this route entry to other route entries obtained from the same routing protocol.</span></span> <span data-ttu-id="1e773-141">O valor desse membro é definido pelo protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="1e773-141">The value of this member is set by the routing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="1e773-142">**FSD \_ Metric1**</span><span class="sxs-lookup"><span data-stu-id="1e773-142">**FSD\_Metric1**</span></span>
</dt> <dd>

<span data-ttu-id="1e773-143">Especifica um valor de métrica específico de protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="1e773-143">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="1e773-144">Esse valor de métrica está documentado em [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="1e773-144">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e773-145">**FSD \_ Metric2**</span><span class="sxs-lookup"><span data-stu-id="1e773-145">**FSD\_Metric2**</span></span>
</dt> <dd>

<span data-ttu-id="1e773-146">Especifica um valor de métrica específico de protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="1e773-146">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="1e773-147">Esse valor de métrica está documentado em [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="1e773-147">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e773-148">**FSD \_ Metric3**</span><span class="sxs-lookup"><span data-stu-id="1e773-148">**FSD\_Metric3**</span></span>
</dt> <dd>

<span data-ttu-id="1e773-149">Especifica um valor de métrica específico de protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="1e773-149">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="1e773-150">Esse valor de métrica está documentado em [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="1e773-150">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e773-151">**FSD \_ Metric4**</span><span class="sxs-lookup"><span data-stu-id="1e773-151">**FSD\_Metric4**</span></span>
</dt> <dd>

<span data-ttu-id="1e773-152">Especifica um valor de métrica específico de protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="1e773-152">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="1e773-153">Esse valor de métrica está documentado em [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="1e773-153">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e773-154">**FSD \_ Metric5**</span><span class="sxs-lookup"><span data-stu-id="1e773-154">**FSD\_Metric5**</span></span>
</dt> <dd>

<span data-ttu-id="1e773-155">Especifica um valor de métrica específico de protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="1e773-155">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="1e773-156">Esse valor de métrica está documentado em [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="1e773-156">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e773-157">**Sinalizadores de FSD \_**</span><span class="sxs-lookup"><span data-stu-id="1e773-157">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="1e773-158">Especifica se a rota é válida.</span><span class="sxs-lookup"><span data-stu-id="1e773-158">Specifies whether the route is valid.</span></span> <span data-ttu-id="1e773-159">O protocolo de roteamento deve primeiro limpar esses sinalizadores e, em seguida, definir a rota como válida ou inválida.</span><span class="sxs-lookup"><span data-stu-id="1e773-159">The routing protocol should first clear these flags, then set the route as either valid or invalid.</span></span> <span data-ttu-id="1e773-160">O protocolo de roteamento deve usar as macros **ClearRouteFlags ()**, **SetRouteValid ()** e **ClearRouteValid ()** para executar essas operações.</span><span class="sxs-lookup"><span data-stu-id="1e773-160">The routing protocol should use the macros **ClearRouteFlags()**, **SetRouteValid()**, and **ClearRouteValid()** to perform these operations.</span></span> <span data-ttu-id="1e773-161">Essas macros são definidas no RTM. h.</span><span class="sxs-lookup"><span data-stu-id="1e773-161">These macros are defined in Rtm.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e773-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e773-162">Remarks</span></span>

<span data-ttu-id="1e773-163">O Gerenciador de tabela de roteamento usa a **\_ prioridade FSD** e os membros da **\_ métrica FSD** para calcular a melhor rota para uma rede de destino específica.</span><span class="sxs-lookup"><span data-stu-id="1e773-163">The routing table manager uses the **FSD\_Priority** and **FSD\_Metric** members to compute the best route to a particular destination network.</span></span>

<span data-ttu-id="1e773-164">Os membros da **\_ métrica \[ 1-5 \] do FSD** são para conformidade com MIB II.</span><span class="sxs-lookup"><span data-stu-id="1e773-164">The **FSD\_Metric\[1-5\]** members are for MIB II conformance.</span></span> <span data-ttu-id="1e773-165">Os agentes MIB II exibem apenas esses valores de métrica.</span><span class="sxs-lookup"><span data-stu-id="1e773-165">MIB II agents display only these metric values.</span></span> <span data-ttu-id="1e773-166">Eles não exibem o valor da métrica **\_ métrica FSD** .</span><span class="sxs-lookup"><span data-stu-id="1e773-166">They do not display the **FSD\_Metric** metric value.</span></span> <span data-ttu-id="1e773-167">Para que a **\_ métrica FSD** seja exibida, o protocolo de roteamento também deve armazenar o valor em um dos membros **FSD \_ métrica \[ 1-5 \]** .</span><span class="sxs-lookup"><span data-stu-id="1e773-167">To have the **FSD\_Metric** displayed, the routing protocol should also store the value in one of the **FSD\_Metric\[1-5\]** members.</span></span>

<span data-ttu-id="1e773-168">O Gerenciador de tabela de roteamento não usa os valores de métrica nos membros da **métrica do FSD \_ \[ 1-5 \]** ao calcular a melhor rota para uma rede de destino.</span><span class="sxs-lookup"><span data-stu-id="1e773-168">The routing table manager does not use the metric values in the **FSD\_Metric\[1-5\]** members when computing the best route to a destination network.</span></span> <span data-ttu-id="1e773-169">Portanto, o protocolo de roteamento deve garantir que o membro de **\_ métrica FSD** tenha um valor de métrica apropriado.</span><span class="sxs-lookup"><span data-stu-id="1e773-169">Therefore, the routing protocol should ensure that the **FSD\_Metric** member has an appropriate metric value.</span></span>

<span data-ttu-id="1e773-170">Um protocolo de roteamento pode usar **os \_ sinalizadores FSD** para marcar uma rota como inválida, se a rota não deve ser usada por outros protocolos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="1e773-170">A routing protocol could use the **FSD\_Flags** to mark a route as invalid, if the route should not be used by other routing protocols.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e773-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e773-171">Requirements</span></span>



| <span data-ttu-id="1e773-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e773-172">Requirement</span></span> | <span data-ttu-id="1e773-173">Valor</span><span class="sxs-lookup"><span data-stu-id="1e773-173">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1e773-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e773-174">Minimum supported client</span></span><br/> | <span data-ttu-id="1e773-175">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1e773-175">None supported</span></span><br/>                                                        |
| <span data-ttu-id="1e773-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e773-176">Minimum supported server</span></span><br/> | <span data-ttu-id="1e773-177">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1e773-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1e773-178">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1e773-178">End of server support</span></span><br/>    | <span data-ttu-id="1e773-179">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1e773-179">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="1e773-180">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e773-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e773-181"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e773-181"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e773-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e773-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e773-183">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="1e773-183">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="1e773-184">Estruturas da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="1e773-184">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="1e773-185">**\_rota de IP RTM \_**</span><span class="sxs-lookup"><span data-stu-id="1e773-185">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





