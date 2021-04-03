---
description: O método de classe WMI EnableStatic permite endereçamento TCP/IP estático para o adaptador de rede de destino. Como resultado, o DHCP para esse adaptador de rede está desabilitado.
ms.assetid: d0076424-58c0-4cfe-b55b-44c0f2620388
ms.tgt_platform: multiple
title: Método EnableStatic da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableStatic
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 74a7b9ca8c8016cca5a78f2e7fe753f00398193e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646310"
---
# <a name="enablestatic-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="c22d1-104">Método EnableStatic da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="c22d1-104">EnableStatic method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="c22d1-105">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableStatic** permite endereçamento TCP/IP estático para o adaptador de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="c22d1-105">The **EnableStatic** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables static TCP/IP addressing for the target network adapter.</span></span> <span data-ttu-id="c22d1-106">Como resultado, o DHCP para esse adaptador de rede está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c22d1-106">As a result, DHCP for this network adapter is disabled.</span></span>

<span data-ttu-id="c22d1-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c22d1-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c22d1-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c22d1-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c22d1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c22d1-109">Syntax</span></span>


```mof
uint32 EnableStatic(
  [in] string IPAddress[],
  [in] string SubnetMask[]
);
```



## <a name="parameters"></a><span data-ttu-id="c22d1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c22d1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c22d1-111">*IPAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c22d1-111">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-112">Lista todos os endereços IP estáticos para o adaptador de rede atual.</span><span class="sxs-lookup"><span data-stu-id="c22d1-112">Lists all of the static IP addresses for the current network adapter.</span></span>

<span data-ttu-id="c22d1-113">Exemplo: 155.34.22.0.</span><span class="sxs-lookup"><span data-stu-id="c22d1-113">Example: 155.34.22.0.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-114">*Submáscara de rede* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c22d1-114">*SubnetMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-115">Máscaras de sub-rede que complementam os valores no parâmetro *IPAddress* .</span><span class="sxs-lookup"><span data-stu-id="c22d1-115">Subnet masks that complement the values in the *IPAddress* parameter.</span></span>

<span data-ttu-id="c22d1-116">Exemplo: 255.255.0.0.</span><span class="sxs-lookup"><span data-stu-id="c22d1-116">Example: 255.255.0.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c22d1-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c22d1-117">Return value</span></span>

<span data-ttu-id="c22d1-118">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando uma reinicialização não é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e qualquer outro número se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="c22d1-118">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="c22d1-119">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c22d1-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c22d1-120">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c22d1-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c22d1-121">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="c22d1-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-122">0</span><span class="sxs-lookup"><span data-stu-id="c22d1-122">0</span></span>

<span data-ttu-id="c22d1-123">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="c22d1-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-124">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="c22d1-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-125">1</span><span class="sxs-lookup"><span data-stu-id="c22d1-125">1</span></span>

<span data-ttu-id="c22d1-126">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="c22d1-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-127">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="c22d1-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-128">64</span><span class="sxs-lookup"><span data-stu-id="c22d1-128">64</span></span>

<span data-ttu-id="c22d1-129">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="c22d1-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-130">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="c22d1-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-131">65</span><span class="sxs-lookup"><span data-stu-id="c22d1-131">65</span></span>

<span data-ttu-id="c22d1-132">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="c22d1-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-133">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="c22d1-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-134">66</span><span class="sxs-lookup"><span data-stu-id="c22d1-134">66</span></span>

<span data-ttu-id="c22d1-135">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="c22d1-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-136">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="c22d1-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-137">67</span><span class="sxs-lookup"><span data-stu-id="c22d1-137">67</span></span>

<span data-ttu-id="c22d1-138">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="c22d1-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-139">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="c22d1-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-140">68</span><span class="sxs-lookup"><span data-stu-id="c22d1-140">68</span></span>

<span data-ttu-id="c22d1-141">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="c22d1-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-142">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="c22d1-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-143">69</span><span class="sxs-lookup"><span data-stu-id="c22d1-143">69</span></span>

<span data-ttu-id="c22d1-144">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="c22d1-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-145">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="c22d1-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-146">70</span><span class="sxs-lookup"><span data-stu-id="c22d1-146">70</span></span>

<span data-ttu-id="c22d1-147">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="c22d1-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-148">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="c22d1-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-149">71</span><span class="sxs-lookup"><span data-stu-id="c22d1-149">71</span></span>

<span data-ttu-id="c22d1-150">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="c22d1-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-151">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="c22d1-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-152">72</span><span class="sxs-lookup"><span data-stu-id="c22d1-152">72</span></span>

<span data-ttu-id="c22d1-153">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="c22d1-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-154">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="c22d1-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-155">73</span><span class="sxs-lookup"><span data-stu-id="c22d1-155">73</span></span>

<span data-ttu-id="c22d1-156">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="c22d1-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-157">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="c22d1-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-158">74</span><span class="sxs-lookup"><span data-stu-id="c22d1-158">74</span></span>

<span data-ttu-id="c22d1-159">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="c22d1-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-160">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="c22d1-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-161">75</span><span class="sxs-lookup"><span data-stu-id="c22d1-161">75</span></span>

<span data-ttu-id="c22d1-162">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="c22d1-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-163">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="c22d1-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-164">76</span><span class="sxs-lookup"><span data-stu-id="c22d1-164">76</span></span>

<span data-ttu-id="c22d1-165">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="c22d1-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-166">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="c22d1-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-167">77</span><span class="sxs-lookup"><span data-stu-id="c22d1-167">77</span></span>

<span data-ttu-id="c22d1-168">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="c22d1-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-169">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="c22d1-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-170">78</span><span class="sxs-lookup"><span data-stu-id="c22d1-170">78</span></span>

<span data-ttu-id="c22d1-171">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c22d1-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-172">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="c22d1-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-173">79</span><span class="sxs-lookup"><span data-stu-id="c22d1-173">79</span></span>

<span data-ttu-id="c22d1-174">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="c22d1-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-175">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="c22d1-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-176">80</span><span class="sxs-lookup"><span data-stu-id="c22d1-176">80</span></span>

<span data-ttu-id="c22d1-177">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="c22d1-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-178">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="c22d1-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-179">81</span><span class="sxs-lookup"><span data-stu-id="c22d1-179">81</span></span>

<span data-ttu-id="c22d1-180">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="c22d1-180">Unable to configure DHCP service.</span></span> <span data-ttu-id="c22d1-181">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="c22d1-181">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-182">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="c22d1-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-183">82</span><span class="sxs-lookup"><span data-stu-id="c22d1-183">82</span></span>

<span data-ttu-id="c22d1-184">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="c22d1-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-185">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="c22d1-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-186">83</span><span class="sxs-lookup"><span data-stu-id="c22d1-186">83</span></span>

<span data-ttu-id="c22d1-187">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="c22d1-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-188">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="c22d1-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-189">84</span><span class="sxs-lookup"><span data-stu-id="c22d1-189">84</span></span>

<span data-ttu-id="c22d1-190">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="c22d1-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-191">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="c22d1-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-192">85</span><span class="sxs-lookup"><span data-stu-id="c22d1-192">85</span></span>

<span data-ttu-id="c22d1-193">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="c22d1-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-194">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="c22d1-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-195">86</span><span class="sxs-lookup"><span data-stu-id="c22d1-195">86</span></span>

<span data-ttu-id="c22d1-196">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="c22d1-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-197">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="c22d1-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-198">87</span><span class="sxs-lookup"><span data-stu-id="c22d1-198">87</span></span>

<span data-ttu-id="c22d1-199">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="c22d1-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-200">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="c22d1-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-201">88</span><span class="sxs-lookup"><span data-stu-id="c22d1-201">88</span></span>

<span data-ttu-id="c22d1-202">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="c22d1-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-203">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="c22d1-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-204">89</span><span class="sxs-lookup"><span data-stu-id="c22d1-204">89</span></span>

<span data-ttu-id="c22d1-205">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="c22d1-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-206">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="c22d1-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-207">90</span><span class="sxs-lookup"><span data-stu-id="c22d1-207">90</span></span>

<span data-ttu-id="c22d1-208">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="c22d1-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-209">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="c22d1-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-210">91</span><span class="sxs-lookup"><span data-stu-id="c22d1-210">91</span></span>

<span data-ttu-id="c22d1-211">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="c22d1-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-212">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="c22d1-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-213">92</span><span class="sxs-lookup"><span data-stu-id="c22d1-213">92</span></span>

<span data-ttu-id="c22d1-214">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="c22d1-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-215">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="c22d1-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-216">93</span><span class="sxs-lookup"><span data-stu-id="c22d1-216">93</span></span>

<span data-ttu-id="c22d1-217">Já existe.</span><span class="sxs-lookup"><span data-stu-id="c22d1-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-218">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="c22d1-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-219">94</span><span class="sxs-lookup"><span data-stu-id="c22d1-219">94</span></span>

<span data-ttu-id="c22d1-220">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="c22d1-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-221">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="c22d1-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-222">95</span><span class="sxs-lookup"><span data-stu-id="c22d1-222">95</span></span>

<span data-ttu-id="c22d1-223">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="c22d1-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-224">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="c22d1-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-225">96</span><span class="sxs-lookup"><span data-stu-id="c22d1-225">96</span></span>

<span data-ttu-id="c22d1-226">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="c22d1-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-227">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="c22d1-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-228">97</span><span class="sxs-lookup"><span data-stu-id="c22d1-228">97</span></span>

<span data-ttu-id="c22d1-229">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="c22d1-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-230">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="c22d1-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-231">98</span><span class="sxs-lookup"><span data-stu-id="c22d1-231">98</span></span>

<span data-ttu-id="c22d1-232">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="c22d1-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-233">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="c22d1-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-234">100</span><span class="sxs-lookup"><span data-stu-id="c22d1-234">100</span></span>

<span data-ttu-id="c22d1-235">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="c22d1-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-236">**2147786788**</span><span class="sxs-lookup"><span data-stu-id="c22d1-236">**2147786788**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-237">Bloqueio de gravação não habilitado.</span><span class="sxs-lookup"><span data-stu-id="c22d1-237">Write lock not enabled.</span></span> <span data-ttu-id="c22d1-238">Para obter mais informações, consulte [**INetCfgLock:: AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c22d1-238">For more information, see [**INetCfgLock::AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c22d1-239">**Outras**</span><span class="sxs-lookup"><span data-stu-id="c22d1-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c22d1-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="c22d1-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c22d1-241">Comentários</span><span class="sxs-lookup"><span data-stu-id="c22d1-241">Remarks</span></span>

<span data-ttu-id="c22d1-242">Ao usar o **EnableStatic** para alterar o endereço IP do computador remoto, ao ser conectado por meio desse adaptador, você provavelmente perderá a conexão com o computador remoto e receberá uma mensagem de erro de RPC não disponível.</span><span class="sxs-lookup"><span data-stu-id="c22d1-242">When using **EnableStatic** to change the IP address of the remote computer, while being connected through that adapter, you will likely loose connection to the remote computer, and receive an RPC not available error-message.</span></span> <span data-ttu-id="c22d1-243">(no entanto, as configurações são alteradas).</span><span class="sxs-lookup"><span data-stu-id="c22d1-243">(the settings are changed however).</span></span> <span data-ttu-id="c22d1-244">Para evitar esse cenário, considere alterar o gateway e/ou as configurações de DNS antes de definir o endereço IP do adaptador.</span><span class="sxs-lookup"><span data-stu-id="c22d1-244">To avoid this scenario, consider changing the Gateway and/or DNS-settings prior to setting the adapter's IP-address.</span></span>

<span data-ttu-id="c22d1-245">Ao usar **EnableStatic** para dar um adaptador a uma configuração de IP estático, a função retorna um "81-não é possível configurar o serviço DHCP" se o adaptador já estiver configurado com um endereço estático.</span><span class="sxs-lookup"><span data-stu-id="c22d1-245">When using **EnableStatic** to give an adapter a static IP configuration, the function returns an "81 - Unable to configure DHCP service" if the adapter is already configured with a static address.</span></span> <span data-ttu-id="c22d1-246">No entanto, a função ainda terá sucesso na configuração com a nova operação.</span><span class="sxs-lookup"><span data-stu-id="c22d1-246">However, the function still succeeds in setting with the new operation.</span></span>

## <a name="examples"></a><span data-ttu-id="c22d1-247">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c22d1-247">Examples</span></span>

<span data-ttu-id="c22d1-248">O [IP estático e, em seguida, ingressar em um](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) exemplo de código do PowerShell de domínio, na galeria do TechNet, usa **EnableStatic** para adicionar um IP estático a um computador local.</span><span class="sxs-lookup"><span data-stu-id="c22d1-248">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell code sample, on TechNet Gallery, uses **EnableStatic** to add a static IP to a local machine.</span></span>

<span data-ttu-id="c22d1-249">O exemplo de código do VBScript [atribuir um endereço IP estático](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) , na galeria do TechNet, usa **EnableStatic** para definir o endereço IP de um computador.</span><span class="sxs-lookup"><span data-stu-id="c22d1-249">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript code example, on TechNet Gallery, uses **EnableStatic** to set the IP address of a computer.</span></span>

<span data-ttu-id="c22d1-250">O exemplo de VBScript a seguir demonstra como desabilitar o uso do DHCP em uma instância do [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c22d1-250">The following VBScript sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="c22d1-251">Nesse caso, especificamos o adaptador com um índice de 0.</span><span class="sxs-lookup"><span data-stu-id="c22d1-251">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="c22d1-252">O índice correto deve ser selecionado em instâncias do Win32 \_ adaptador para outras interfaces.</span><span class="sxs-lookup"><span data-stu-id="c22d1-252">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="c22d1-253">Esse script se aplica somente a sistemas baseados em NT altere as IPADDR e as variáveis de sub-rede abaixo para os valores que você deseja aplicar ao adaptador.</span><span class="sxs-lookup"><span data-stu-id="c22d1-253">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=1")

ipaddr = Array("1.1.1.1")
subnet = Array("255.255.255.0")


RetVal = Adapter.EnableStatic(ipaddr,subnet)

if RetVal = 0 then 
 WScript.Echo "DHCP disabled, using static IP address"
else 
 WScript.Echo "DHCP disable failed"
end if
```



<span data-ttu-id="c22d1-254">O exemplo do Perl a seguir demonstra como desabilitar o uso do DHCP em uma instância do [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c22d1-254">The following Perl sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="c22d1-255">Nesse caso, especificamos o adaptador com um índice de 0.</span><span class="sxs-lookup"><span data-stu-id="c22d1-255">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="c22d1-256">O índice correto deve ser selecionado em instâncias do Win32 \_ adaptador para outras interfaces.</span><span class="sxs-lookup"><span data-stu-id="c22d1-256">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="c22d1-257">Esse script se aplica somente a sistemas baseados em NT altere as IPADDR e as variáveis de sub-rede abaixo para os valores que você deseja aplicar ao adaptador.</span><span class="sxs-lookup"><span data-stu-id="c22d1-257">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```
use strict;
use Win32::OLE;

my ($Adapter, @ipaddr, @subnet, $RetVal);  
eval { $Adapter = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_NetworkAdapterConfiguration.Index=\"0\""); };

unless ($@) 
{
 push @ipaddr, "192.168.144.107";
 push @subnet, "255.255.255.0";

 $RetVal = $Adapter->EnableStatic(\@ipaddr, \@subnet);

 if ($RetVal == 0) 
 {
  print "\nDHCP disabled, using static IP address\n";
 }
 else 
 {
  print "\nDHCP disable failed\n";
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="c22d1-258">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c22d1-258">Requirements</span></span>



| <span data-ttu-id="c22d1-259">Requisito</span><span class="sxs-lookup"><span data-stu-id="c22d1-259">Requirement</span></span> | <span data-ttu-id="c22d1-260">Valor</span><span class="sxs-lookup"><span data-stu-id="c22d1-260">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c22d1-261">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c22d1-261">Minimum supported client</span></span><br/> | <span data-ttu-id="c22d1-262">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c22d1-262">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c22d1-263">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c22d1-263">Minimum supported server</span></span><br/> | <span data-ttu-id="c22d1-264">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c22d1-264">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c22d1-265">Namespace</span><span class="sxs-lookup"><span data-stu-id="c22d1-265">Namespace</span></span><br/>                | <span data-ttu-id="c22d1-266">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c22d1-266">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c22d1-267">MOF</span><span class="sxs-lookup"><span data-stu-id="c22d1-267">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c22d1-268"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c22d1-268"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c22d1-269">DLL</span><span class="sxs-lookup"><span data-stu-id="c22d1-269">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c22d1-270"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c22d1-270"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c22d1-271">Confira também</span><span class="sxs-lookup"><span data-stu-id="c22d1-271">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c22d1-272">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="c22d1-272">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="c22d1-273">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="c22d1-273">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="c22d1-274">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="c22d1-274">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="c22d1-275">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="c22d1-275">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="c22d1-276">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="c22d1-276">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

