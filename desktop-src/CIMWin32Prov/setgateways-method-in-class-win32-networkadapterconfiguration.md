---
description: Os SetGateways &\# 32; O método de classe WMI especifica uma lista de gateways para rotear pacotes para uma sub-rede que é diferente da sub-rede à qual o adaptador de rede está conectado.
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: Método SetGateways da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 215bfa736a0f9d67ae587ac1f0e1b4aa394b85d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826488"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="7e7a8-103">Método SetGateways da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e7a8-103">SetGateways method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="7e7a8-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetGateways** especifica uma lista de gateways para rotear pacotes para uma sub-rede que é diferente da sub-rede à qual o adaptador de rede está conectado.</span><span class="sxs-lookup"><span data-stu-id="7e7a8-104">The **SetGateways** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method specifies a list of gateways for routing packets to a subnet that is different from the subnet that the network adapter is connected to.</span></span>

<span data-ttu-id="7e7a8-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="7e7a8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7e7a8-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7e7a8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e7a8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e7a8-107">Syntax</span></span>


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a><span data-ttu-id="7e7a8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e7a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e7a8-109">*DefaultIPGateway* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e7a8-109">*DefaultIPGateway* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-110">Lista de endereços IP para gateways em que os pacotes de rede são roteados.</span><span class="sxs-lookup"><span data-stu-id="7e7a8-110">List of IP addresses to gateways where network packets are routed.</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-111">*GatewayCostMetric* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7e7a8-111">*GatewayCostMetric* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-112">Atribui um valor que varia de 1 a 9999, que é usado para calcular as rotas mais rápidas e confiáveis.</span><span class="sxs-lookup"><span data-stu-id="7e7a8-112">Assigns a value that ranges from 1 to 9999, which is used to calculate the fastest and most reliable routes.</span></span> <span data-ttu-id="7e7a8-113">Os valores desse parâmetro correspondem aos valores no parâmetro *DefaultIPGateway* .</span><span class="sxs-lookup"><span data-stu-id="7e7a8-113">The values of this parameter correspond with the values in the *DefaultIPGateway* parameter.</span></span> <span data-ttu-id="7e7a8-114">O valor padrão para um gateway é 1.</span><span class="sxs-lookup"><span data-stu-id="7e7a8-114">The default value for a gateway is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e7a8-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e7a8-115">Return value</span></span>

<span data-ttu-id="7e7a8-116">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando uma reinicialização não é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e qualquer outro valor se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="7e7a8-116">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other value if there is an error.</span></span> <span data-ttu-id="7e7a8-117">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7e7a8-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7e7a8-118">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7e7a8-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7e7a8-119">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-120">0</span><span class="sxs-lookup"><span data-stu-id="7e7a8-120">0</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-121">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-121">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-122">1</span><span class="sxs-lookup"><span data-stu-id="7e7a8-122">1</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-123">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-124">64</span><span class="sxs-lookup"><span data-stu-id="7e7a8-124">64</span></span>

<span data-ttu-id="7e7a8-125">Não há suporte para o método quando a NIC está no modo DHCP.</span><span class="sxs-lookup"><span data-stu-id="7e7a8-125">Method not supported when the NIC is in DHCP mode.</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-126">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-127">65</span><span class="sxs-lookup"><span data-stu-id="7e7a8-127">65</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-128">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-129">66</span><span class="sxs-lookup"><span data-stu-id="7e7a8-129">66</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-130">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-131">67</span><span class="sxs-lookup"><span data-stu-id="7e7a8-131">67</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-132">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-133">68</span><span class="sxs-lookup"><span data-stu-id="7e7a8-133">68</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-134">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-134">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-135">69</span><span class="sxs-lookup"><span data-stu-id="7e7a8-135">69</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-136">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-136">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-137">70</span><span class="sxs-lookup"><span data-stu-id="7e7a8-137">70</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-138">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-138">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-139">71</span><span class="sxs-lookup"><span data-stu-id="7e7a8-139">71</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-140">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-140">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-141">72</span><span class="sxs-lookup"><span data-stu-id="7e7a8-141">72</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-142">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-142">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-143">73</span><span class="sxs-lookup"><span data-stu-id="7e7a8-143">73</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-144">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-144">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-145">74</span><span class="sxs-lookup"><span data-stu-id="7e7a8-145">74</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-146">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-146">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-147">75</span><span class="sxs-lookup"><span data-stu-id="7e7a8-147">75</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-148">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-148">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-149">76</span><span class="sxs-lookup"><span data-stu-id="7e7a8-149">76</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-150">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-150">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-151">77</span><span class="sxs-lookup"><span data-stu-id="7e7a8-151">77</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-152">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-152">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-153">78</span><span class="sxs-lookup"><span data-stu-id="7e7a8-153">78</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-154">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-154">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-155">79</span><span class="sxs-lookup"><span data-stu-id="7e7a8-155">79</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-156">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-156">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-157">80</span><span class="sxs-lookup"><span data-stu-id="7e7a8-157">80</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-158">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-158">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-159">81</span><span class="sxs-lookup"><span data-stu-id="7e7a8-159">81</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-160">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-160">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-161">82</span><span class="sxs-lookup"><span data-stu-id="7e7a8-161">82</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-162">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-162">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-163">83</span><span class="sxs-lookup"><span data-stu-id="7e7a8-163">83</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-164">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-164">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-165">84</span><span class="sxs-lookup"><span data-stu-id="7e7a8-165">84</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-166">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-166">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-167">85</span><span class="sxs-lookup"><span data-stu-id="7e7a8-167">85</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-168">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-168">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-169">86</span><span class="sxs-lookup"><span data-stu-id="7e7a8-169">86</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-170">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-170">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-171">87</span><span class="sxs-lookup"><span data-stu-id="7e7a8-171">87</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-172">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-172">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-173">88</span><span class="sxs-lookup"><span data-stu-id="7e7a8-173">88</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-174">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-174">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-175">89</span><span class="sxs-lookup"><span data-stu-id="7e7a8-175">89</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-176">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-176">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-177">90</span><span class="sxs-lookup"><span data-stu-id="7e7a8-177">90</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-178">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-178">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-179">91</span><span class="sxs-lookup"><span data-stu-id="7e7a8-179">91</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-180">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-180">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-181">92</span><span class="sxs-lookup"><span data-stu-id="7e7a8-181">92</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-182">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-182">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-183">93</span><span class="sxs-lookup"><span data-stu-id="7e7a8-183">93</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-184">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-184">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-185">94</span><span class="sxs-lookup"><span data-stu-id="7e7a8-185">94</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-186">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-186">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-187">95</span><span class="sxs-lookup"><span data-stu-id="7e7a8-187">95</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-188">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-188">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-189">96</span><span class="sxs-lookup"><span data-stu-id="7e7a8-189">96</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-190">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-190">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-191">97</span><span class="sxs-lookup"><span data-stu-id="7e7a8-191">97</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-192">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-192">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-193">98</span><span class="sxs-lookup"><span data-stu-id="7e7a8-193">98</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-194">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-194">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-195">100</span><span class="sxs-lookup"><span data-stu-id="7e7a8-195">100</span></span>

</dd> <dt>

<span data-ttu-id="7e7a8-196">**Outras**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-196">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="7e7a8-197">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="7e7a8-197">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e7a8-198">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e7a8-198">Remarks</span></span>

<span data-ttu-id="7e7a8-199">Esse método só funciona quando a placa de interface de rede (NIC) está no modo de IP estático.</span><span class="sxs-lookup"><span data-stu-id="7e7a8-199">This method only works when the Network Interface Card (NIC) is in the static IP mode.</span></span>

<span data-ttu-id="7e7a8-200">Para limpar o gateway, defina seu gateway para o mesmo IP usado em [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="7e7a8-200">To clear the gateway, set your gateway to the same IP you use on [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7e7a8-201">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7e7a8-201">Examples</span></span>

<span data-ttu-id="7e7a8-202">O exemplo de VBScript [modificar os gateways para um adaptador de rede](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) configura dois gateways para um adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="7e7a8-202">The [Modify the Gateways for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) VBScript sample configures two gateways for a network adapter.</span></span>

<span data-ttu-id="7e7a8-203">O exemplo [atribuir um endereço IP estático](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript define o endereço IP e o gateway de um computador.</span><span class="sxs-lookup"><span data-stu-id="7e7a8-203">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript sample sets the IP address and gateway of a computer.</span></span>

<span data-ttu-id="7e7a8-204">O [IP estático e, em seguida, ingressar em um domínio](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) do PowerShell de exemplo ajuda na recriação de computadores.</span><span class="sxs-lookup"><span data-stu-id="7e7a8-204">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell sample assists in rebuilding machines.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e7a8-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e7a8-205">Requirements</span></span>



| <span data-ttu-id="7e7a8-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e7a8-206">Requirement</span></span> | <span data-ttu-id="7e7a8-207">Valor</span><span class="sxs-lookup"><span data-stu-id="7e7a8-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e7a8-208">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e7a8-208">Minimum supported client</span></span><br/> | <span data-ttu-id="7e7a8-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e7a8-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7e7a8-210">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e7a8-210">Minimum supported server</span></span><br/> | <span data-ttu-id="7e7a8-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e7a8-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7e7a8-212">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e7a8-212">Namespace</span></span><br/>                | <span data-ttu-id="7e7a8-213">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7e7a8-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7e7a8-214">MOF</span><span class="sxs-lookup"><span data-stu-id="7e7a8-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e7a8-215"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e7a8-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e7a8-216">DLL</span><span class="sxs-lookup"><span data-stu-id="7e7a8-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e7a8-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e7a8-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e7a8-218">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e7a8-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e7a8-219">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="7e7a8-219">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="7e7a8-220">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="7e7a8-220">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="7e7a8-221">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="7e7a8-221">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="7e7a8-222">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="7e7a8-222">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="7e7a8-223">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="7e7a8-223">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

