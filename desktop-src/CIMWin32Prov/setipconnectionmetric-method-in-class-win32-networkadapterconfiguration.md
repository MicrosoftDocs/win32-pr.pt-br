---
description: O método SetIPConnectionMetric é usado para definir a métrica de roteamento associada a este adaptador associado a IP.
ms.assetid: d7f7c0df-51e3-4dc8-8a53-977ecde075df
ms.tgt_platform: multiple
title: Método SetIPConnectionMetric da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPConnectionMetric
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73d6dde0a8faea2aeaf0982459e3c377bb1ac51d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089329"
---
# <a name="setipconnectionmetric-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="2372c-103">Método SetIPConnectionMetric da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="2372c-103">SetIPConnectionMetric method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="2372c-104">O método **SetIPConnectionMetric** é usado para definir a métrica de roteamento associada a este adaptador associado a IP.</span><span class="sxs-lookup"><span data-stu-id="2372c-104">The **SetIPConnectionMetric** method is used to set the routing metric associated with this IP-bound adapter.</span></span>

<span data-ttu-id="2372c-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2372c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2372c-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2372c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2372c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2372c-107">Syntax</span></span>


```mof
uint32 SetIPConnectionMetric(
  [in] uint32 IPConnectionMetric
);
```



## <a name="parameters"></a><span data-ttu-id="2372c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2372c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2372c-109">*IPConnectionMetric* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2372c-109">*IPConnectionMetric* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2372c-110">Indica o custo de usar as rotas configuradas para este adaptador associado a IP.</span><span class="sxs-lookup"><span data-stu-id="2372c-110">Indicates the cost of using the configured routes for this IP-bound adapter.</span></span> <span data-ttu-id="2372c-111">O valor é ponderado para essas rotas na tabela de roteamento de IP.</span><span class="sxs-lookup"><span data-stu-id="2372c-111">The value is weighted for those routes in the IP routing table.</span></span> <span data-ttu-id="2372c-112">Se houver várias rotas para um destino na tabela de roteamento, a rota com a métrica mais baixa será usada.</span><span class="sxs-lookup"><span data-stu-id="2372c-112">If there are multiple routes to a destination in the routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="2372c-113">O intervalo de valores válidos é de 1 a 9999.</span><span class="sxs-lookup"><span data-stu-id="2372c-113">The range of valid values is 1 through 9999.</span></span> <span data-ttu-id="2372c-114">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="2372c-114">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2372c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2372c-115">Return value</span></span>

<span data-ttu-id="2372c-116">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="2372c-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="2372c-117">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2372c-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2372c-118">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2372c-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2372c-119">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="2372c-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-120">0</span><span class="sxs-lookup"><span data-stu-id="2372c-120">0</span></span>

<span data-ttu-id="2372c-121">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="2372c-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-122">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="2372c-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-123">1</span><span class="sxs-lookup"><span data-stu-id="2372c-123">1</span></span>

<span data-ttu-id="2372c-124">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="2372c-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-125">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="2372c-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-126">64</span><span class="sxs-lookup"><span data-stu-id="2372c-126">64</span></span>

<span data-ttu-id="2372c-127">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="2372c-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-128">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="2372c-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-129">65</span><span class="sxs-lookup"><span data-stu-id="2372c-129">65</span></span>

<span data-ttu-id="2372c-130">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="2372c-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-131">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="2372c-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-132">66</span><span class="sxs-lookup"><span data-stu-id="2372c-132">66</span></span>

<span data-ttu-id="2372c-133">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="2372c-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-134">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="2372c-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-135">67</span><span class="sxs-lookup"><span data-stu-id="2372c-135">67</span></span>

<span data-ttu-id="2372c-136">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="2372c-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-137">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="2372c-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-138">68</span><span class="sxs-lookup"><span data-stu-id="2372c-138">68</span></span>

<span data-ttu-id="2372c-139">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="2372c-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-140">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="2372c-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-141">69</span><span class="sxs-lookup"><span data-stu-id="2372c-141">69</span></span>

<span data-ttu-id="2372c-142">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="2372c-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-143">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="2372c-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-144">70</span><span class="sxs-lookup"><span data-stu-id="2372c-144">70</span></span>

<span data-ttu-id="2372c-145">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="2372c-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-146">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="2372c-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-147">71</span><span class="sxs-lookup"><span data-stu-id="2372c-147">71</span></span>

<span data-ttu-id="2372c-148">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="2372c-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-149">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="2372c-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-150">72</span><span class="sxs-lookup"><span data-stu-id="2372c-150">72</span></span>

<span data-ttu-id="2372c-151">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="2372c-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-152">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="2372c-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-153">73</span><span class="sxs-lookup"><span data-stu-id="2372c-153">73</span></span>

<span data-ttu-id="2372c-154">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="2372c-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-155">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="2372c-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-156">74</span><span class="sxs-lookup"><span data-stu-id="2372c-156">74</span></span>

<span data-ttu-id="2372c-157">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="2372c-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-158">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="2372c-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-159">75</span><span class="sxs-lookup"><span data-stu-id="2372c-159">75</span></span>

<span data-ttu-id="2372c-160">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="2372c-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-161">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="2372c-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-162">76</span><span class="sxs-lookup"><span data-stu-id="2372c-162">76</span></span>

<span data-ttu-id="2372c-163">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="2372c-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-164">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="2372c-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-165">77</span><span class="sxs-lookup"><span data-stu-id="2372c-165">77</span></span>

<span data-ttu-id="2372c-166">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="2372c-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-167">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="2372c-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-168">78</span><span class="sxs-lookup"><span data-stu-id="2372c-168">78</span></span>

<span data-ttu-id="2372c-169">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2372c-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-170">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="2372c-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-171">79</span><span class="sxs-lookup"><span data-stu-id="2372c-171">79</span></span>

<span data-ttu-id="2372c-172">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="2372c-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-173">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="2372c-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-174">80</span><span class="sxs-lookup"><span data-stu-id="2372c-174">80</span></span>

<span data-ttu-id="2372c-175">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2372c-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-176">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="2372c-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-177">81</span><span class="sxs-lookup"><span data-stu-id="2372c-177">81</span></span>

<span data-ttu-id="2372c-178">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="2372c-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-179">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="2372c-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-180">82</span><span class="sxs-lookup"><span data-stu-id="2372c-180">82</span></span>

<span data-ttu-id="2372c-181">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="2372c-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-182">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="2372c-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-183">83</span><span class="sxs-lookup"><span data-stu-id="2372c-183">83</span></span>

<span data-ttu-id="2372c-184">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="2372c-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-185">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="2372c-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-186">84</span><span class="sxs-lookup"><span data-stu-id="2372c-186">84</span></span>

<span data-ttu-id="2372c-187">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="2372c-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-188">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="2372c-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-189">85</span><span class="sxs-lookup"><span data-stu-id="2372c-189">85</span></span>

<span data-ttu-id="2372c-190">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="2372c-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-191">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="2372c-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-192">86</span><span class="sxs-lookup"><span data-stu-id="2372c-192">86</span></span>

<span data-ttu-id="2372c-193">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="2372c-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-194">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="2372c-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-195">87</span><span class="sxs-lookup"><span data-stu-id="2372c-195">87</span></span>

<span data-ttu-id="2372c-196">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="2372c-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-197">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="2372c-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-198">88</span><span class="sxs-lookup"><span data-stu-id="2372c-198">88</span></span>

<span data-ttu-id="2372c-199">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="2372c-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-200">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="2372c-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-201">89</span><span class="sxs-lookup"><span data-stu-id="2372c-201">89</span></span>

<span data-ttu-id="2372c-202">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="2372c-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-203">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="2372c-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-204">90</span><span class="sxs-lookup"><span data-stu-id="2372c-204">90</span></span>

<span data-ttu-id="2372c-205">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="2372c-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-206">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="2372c-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-207">91</span><span class="sxs-lookup"><span data-stu-id="2372c-207">91</span></span>

<span data-ttu-id="2372c-208">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="2372c-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-209">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="2372c-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-210">92</span><span class="sxs-lookup"><span data-stu-id="2372c-210">92</span></span>

<span data-ttu-id="2372c-211">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="2372c-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-212">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="2372c-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-213">93</span><span class="sxs-lookup"><span data-stu-id="2372c-213">93</span></span>

<span data-ttu-id="2372c-214">Já existe.</span><span class="sxs-lookup"><span data-stu-id="2372c-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-215">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="2372c-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-216">94</span><span class="sxs-lookup"><span data-stu-id="2372c-216">94</span></span>

<span data-ttu-id="2372c-217">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="2372c-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-218">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="2372c-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-219">95</span><span class="sxs-lookup"><span data-stu-id="2372c-219">95</span></span>

<span data-ttu-id="2372c-220">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="2372c-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-221">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="2372c-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-222">96</span><span class="sxs-lookup"><span data-stu-id="2372c-222">96</span></span>

<span data-ttu-id="2372c-223">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="2372c-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-224">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="2372c-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-225">97</span><span class="sxs-lookup"><span data-stu-id="2372c-225">97</span></span>

<span data-ttu-id="2372c-226">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="2372c-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-227">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="2372c-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-228">98</span><span class="sxs-lookup"><span data-stu-id="2372c-228">98</span></span>

<span data-ttu-id="2372c-229">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="2372c-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-230">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="2372c-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-231">100</span><span class="sxs-lookup"><span data-stu-id="2372c-231">100</span></span>

<span data-ttu-id="2372c-232">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="2372c-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2372c-233">**Outras**</span><span class="sxs-lookup"><span data-stu-id="2372c-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="2372c-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="2372c-234">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="2372c-235">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2372c-235">Examples</span></span>

<span data-ttu-id="2372c-236">A amostra [Modificar a métrica de conexão de IP para um adaptador de rede](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) do VBScript define a métrica de conexão IP para um adaptador de rede como 100.</span><span class="sxs-lookup"><span data-stu-id="2372c-236">The [Modify the IP Connection Metric for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) VBScript sample sets the IP connection metric for a network adapter to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="2372c-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2372c-237">Requirements</span></span>



| <span data-ttu-id="2372c-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="2372c-238">Requirement</span></span> | <span data-ttu-id="2372c-239">Valor</span><span class="sxs-lookup"><span data-stu-id="2372c-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2372c-240">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2372c-240">Minimum supported client</span></span><br/> | <span data-ttu-id="2372c-241">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2372c-241">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="2372c-242">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2372c-242">Minimum supported server</span></span><br/> | <span data-ttu-id="2372c-243">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2372c-243">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="2372c-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="2372c-244">Namespace</span></span><br/>                | <span data-ttu-id="2372c-245">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2372c-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2372c-246">MOF</span><span class="sxs-lookup"><span data-stu-id="2372c-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2372c-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2372c-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2372c-248">DLL</span><span class="sxs-lookup"><span data-stu-id="2372c-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2372c-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2372c-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2372c-250">Confira também</span><span class="sxs-lookup"><span data-stu-id="2372c-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2372c-251">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="2372c-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2372c-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="2372c-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="2372c-253">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="2372c-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="2372c-254">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="2372c-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="2372c-255">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="2372c-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

