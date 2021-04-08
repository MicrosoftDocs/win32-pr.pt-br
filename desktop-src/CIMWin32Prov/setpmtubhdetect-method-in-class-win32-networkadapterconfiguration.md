---
description: O método estático da classe WMI SetPMTUBHDetect é usado para habilitar a detecção de roteadores buraco negro durante a descoberta do caminho MTU.
ms.assetid: a1e45ed9-85a9-4fdd-890a-d578c3f94b72
ms.tgt_platform: multiple
title: Método SetPMTUBHDetect da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUBHDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 098652c6ea0a53f9d3b1f616def3dd8b5e7228af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089325"
---
# <a name="setpmtubhdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="985fb-103">Método SetPMTUBHDetect da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="985fb-103">SetPMTUBHDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="985fb-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPMTUBHDetect** é usado para habilitar a detecção de roteadores buraco negro durante a descoberta do caminho MTU.</span><span class="sxs-lookup"><span data-stu-id="985fb-104">The **SetPMTUBHDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable the detection of Black Hole routers while doing Path MTU Discovery.</span></span>

<span data-ttu-id="985fb-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="985fb-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="985fb-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="985fb-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="985fb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="985fb-107">Syntax</span></span>


```mof
uint32 SetPMTUBHDetect(
  [in] boolean PMTUBHDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="985fb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="985fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="985fb-109">*PMTUBHDetectEnabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="985fb-109">*PMTUBHDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="985fb-110">Se **for true**, o TCP tentará descobrir o buraco negro e rotear pacotes em caminhos de rede diferentes.</span><span class="sxs-lookup"><span data-stu-id="985fb-110">If **true**, TCP attempts to discover Black Hole and route packets in different network paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="985fb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="985fb-111">Return value</span></span>

<span data-ttu-id="985fb-112">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="985fb-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="985fb-113">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="985fb-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="985fb-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="985fb-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="985fb-115">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="985fb-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-116">0</span><span class="sxs-lookup"><span data-stu-id="985fb-116">0</span></span>

<span data-ttu-id="985fb-117">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="985fb-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-118">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="985fb-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-119">1</span><span class="sxs-lookup"><span data-stu-id="985fb-119">1</span></span>

<span data-ttu-id="985fb-120">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="985fb-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-121">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="985fb-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-122">64</span><span class="sxs-lookup"><span data-stu-id="985fb-122">64</span></span>

<span data-ttu-id="985fb-123">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="985fb-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-124">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="985fb-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-125">65</span><span class="sxs-lookup"><span data-stu-id="985fb-125">65</span></span>

<span data-ttu-id="985fb-126">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="985fb-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-127">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="985fb-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-128">66</span><span class="sxs-lookup"><span data-stu-id="985fb-128">66</span></span>

<span data-ttu-id="985fb-129">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="985fb-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-130">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="985fb-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-131">67</span><span class="sxs-lookup"><span data-stu-id="985fb-131">67</span></span>

<span data-ttu-id="985fb-132">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="985fb-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-133">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="985fb-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-134">68</span><span class="sxs-lookup"><span data-stu-id="985fb-134">68</span></span>

<span data-ttu-id="985fb-135">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="985fb-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-136">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="985fb-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-137">69</span><span class="sxs-lookup"><span data-stu-id="985fb-137">69</span></span>

<span data-ttu-id="985fb-138">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="985fb-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-139">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="985fb-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-140">70</span><span class="sxs-lookup"><span data-stu-id="985fb-140">70</span></span>

<span data-ttu-id="985fb-141">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="985fb-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-142">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="985fb-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-143">71</span><span class="sxs-lookup"><span data-stu-id="985fb-143">71</span></span>

<span data-ttu-id="985fb-144">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="985fb-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-145">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="985fb-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-146">72</span><span class="sxs-lookup"><span data-stu-id="985fb-146">72</span></span>

<span data-ttu-id="985fb-147">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="985fb-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-148">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="985fb-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-149">73</span><span class="sxs-lookup"><span data-stu-id="985fb-149">73</span></span>

<span data-ttu-id="985fb-150">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="985fb-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-151">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="985fb-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-152">74</span><span class="sxs-lookup"><span data-stu-id="985fb-152">74</span></span>

<span data-ttu-id="985fb-153">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="985fb-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-154">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="985fb-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-155">75</span><span class="sxs-lookup"><span data-stu-id="985fb-155">75</span></span>

<span data-ttu-id="985fb-156">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="985fb-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-157">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="985fb-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-158">76</span><span class="sxs-lookup"><span data-stu-id="985fb-158">76</span></span>

<span data-ttu-id="985fb-159">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="985fb-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-160">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="985fb-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-161">77</span><span class="sxs-lookup"><span data-stu-id="985fb-161">77</span></span>

<span data-ttu-id="985fb-162">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="985fb-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-163">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="985fb-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-164">78</span><span class="sxs-lookup"><span data-stu-id="985fb-164">78</span></span>

<span data-ttu-id="985fb-165">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="985fb-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-166">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="985fb-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-167">79</span><span class="sxs-lookup"><span data-stu-id="985fb-167">79</span></span>

<span data-ttu-id="985fb-168">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="985fb-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-169">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="985fb-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-170">80</span><span class="sxs-lookup"><span data-stu-id="985fb-170">80</span></span>

<span data-ttu-id="985fb-171">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="985fb-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-172">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="985fb-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-173">81</span><span class="sxs-lookup"><span data-stu-id="985fb-173">81</span></span>

<span data-ttu-id="985fb-174">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="985fb-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-175">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="985fb-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-176">82</span><span class="sxs-lookup"><span data-stu-id="985fb-176">82</span></span>

<span data-ttu-id="985fb-177">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="985fb-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-178">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="985fb-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-179">83</span><span class="sxs-lookup"><span data-stu-id="985fb-179">83</span></span>

<span data-ttu-id="985fb-180">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="985fb-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-181">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="985fb-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-182">84</span><span class="sxs-lookup"><span data-stu-id="985fb-182">84</span></span>

<span data-ttu-id="985fb-183">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="985fb-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-184">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="985fb-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-185">85</span><span class="sxs-lookup"><span data-stu-id="985fb-185">85</span></span>

<span data-ttu-id="985fb-186">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="985fb-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-187">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="985fb-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-188">86</span><span class="sxs-lookup"><span data-stu-id="985fb-188">86</span></span>

<span data-ttu-id="985fb-189">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="985fb-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-190">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="985fb-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-191">87</span><span class="sxs-lookup"><span data-stu-id="985fb-191">87</span></span>

<span data-ttu-id="985fb-192">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="985fb-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-193">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="985fb-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-194">88</span><span class="sxs-lookup"><span data-stu-id="985fb-194">88</span></span>

<span data-ttu-id="985fb-195">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="985fb-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-196">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="985fb-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-197">89</span><span class="sxs-lookup"><span data-stu-id="985fb-197">89</span></span>

<span data-ttu-id="985fb-198">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="985fb-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-199">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="985fb-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-200">90</span><span class="sxs-lookup"><span data-stu-id="985fb-200">90</span></span>

<span data-ttu-id="985fb-201">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="985fb-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-202">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="985fb-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-203">91</span><span class="sxs-lookup"><span data-stu-id="985fb-203">91</span></span>

<span data-ttu-id="985fb-204">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="985fb-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-205">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="985fb-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-206">92</span><span class="sxs-lookup"><span data-stu-id="985fb-206">92</span></span>

<span data-ttu-id="985fb-207">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="985fb-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-208">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="985fb-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-209">93</span><span class="sxs-lookup"><span data-stu-id="985fb-209">93</span></span>

<span data-ttu-id="985fb-210">Já existe.</span><span class="sxs-lookup"><span data-stu-id="985fb-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-211">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="985fb-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-212">94</span><span class="sxs-lookup"><span data-stu-id="985fb-212">94</span></span>

<span data-ttu-id="985fb-213">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="985fb-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-214">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="985fb-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-215">95</span><span class="sxs-lookup"><span data-stu-id="985fb-215">95</span></span>

<span data-ttu-id="985fb-216">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="985fb-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-217">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="985fb-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-218">96</span><span class="sxs-lookup"><span data-stu-id="985fb-218">96</span></span>

<span data-ttu-id="985fb-219">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="985fb-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-220">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="985fb-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-221">97</span><span class="sxs-lookup"><span data-stu-id="985fb-221">97</span></span>

<span data-ttu-id="985fb-222">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="985fb-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-223">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="985fb-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-224">98</span><span class="sxs-lookup"><span data-stu-id="985fb-224">98</span></span>

<span data-ttu-id="985fb-225">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="985fb-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-226">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="985fb-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-227">100</span><span class="sxs-lookup"><span data-stu-id="985fb-227">100</span></span>

<span data-ttu-id="985fb-228">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="985fb-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="985fb-229">**Outras**</span><span class="sxs-lookup"><span data-stu-id="985fb-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="985fb-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="985fb-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="985fb-231">Comentários</span><span class="sxs-lookup"><span data-stu-id="985fb-231">Remarks</span></span>

<span data-ttu-id="985fb-232">Um roteador buraco negro não retorna as mensagens de destino inacessíveis do protocolo ICMP quando precisa fragmentar um datagrama IP com o conjunto de bits não fragmentar.</span><span class="sxs-lookup"><span data-stu-id="985fb-232">A Black Hole router does not return the Internet Control Message Protocol (ICMP) Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="985fb-233">O TCP depende do recebimento dessas mensagens para executar a descoberta de MTU de caminho.</span><span class="sxs-lookup"><span data-stu-id="985fb-233">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span>

<span data-ttu-id="985fb-234">Com esse recurso habilitado, o TCP tentará enviar segmentos sem o bit não fragmentar definido se várias retransmissões de um segmento não forem confirmadas.</span><span class="sxs-lookup"><span data-stu-id="985fb-234">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="985fb-235">Se o segmento for confirmado como resultado, o MSS (tamanho máximo do segmento) será reduzido e o bit não fragmentar será definido em pacotes futuros na conexão.</span><span class="sxs-lookup"><span data-stu-id="985fb-235">If the segment is acknowledged as a result, the maximum segment size (MSS) will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="985fb-236">A habilitação da detecção de buraco negro aumenta o número máximo de retransmissões executadas para um determinado segmento.</span><span class="sxs-lookup"><span data-stu-id="985fb-236">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span>

## <a name="examples"></a><span data-ttu-id="985fb-237">Exemplos</span><span class="sxs-lookup"><span data-stu-id="985fb-237">Examples</span></span>

<span data-ttu-id="985fb-238">A [detecção de modificação de PMTUBH em todos os adaptadores de rede](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) permite a descoberta automática de roteadores de buraco negro ao determinar a unidade de transmissão máxima em uma rede.</span><span class="sxs-lookup"><span data-stu-id="985fb-238">The [Modify PMTUBH Detection on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) enables the auto-discovery of black hole routers when determining the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="985fb-239">Requisitos</span><span class="sxs-lookup"><span data-stu-id="985fb-239">Requirements</span></span>



| <span data-ttu-id="985fb-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="985fb-240">Requirement</span></span> | <span data-ttu-id="985fb-241">Valor</span><span class="sxs-lookup"><span data-stu-id="985fb-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="985fb-242">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="985fb-242">Minimum supported client</span></span><br/> | <span data-ttu-id="985fb-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="985fb-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="985fb-244">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="985fb-244">Minimum supported server</span></span><br/> | <span data-ttu-id="985fb-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="985fb-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="985fb-246">Namespace</span><span class="sxs-lookup"><span data-stu-id="985fb-246">Namespace</span></span><br/>                | <span data-ttu-id="985fb-247">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="985fb-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="985fb-248">MOF</span><span class="sxs-lookup"><span data-stu-id="985fb-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="985fb-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="985fb-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="985fb-250">DLL</span><span class="sxs-lookup"><span data-stu-id="985fb-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="985fb-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="985fb-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="985fb-252">Confira também</span><span class="sxs-lookup"><span data-stu-id="985fb-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="985fb-253">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="985fb-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="985fb-254">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="985fb-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="985fb-255">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="985fb-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="985fb-256">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="985fb-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="985fb-257">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="985fb-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

