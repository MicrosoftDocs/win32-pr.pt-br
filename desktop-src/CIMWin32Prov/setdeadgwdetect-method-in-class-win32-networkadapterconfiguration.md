---
description: O método estático da classe WMI SetDeadGWDetect é usado para habilitar a detecção de gateway inativo.
ms.assetid: c813aaef-7215-4759-b68f-7808fd203d9c
ms.tgt_platform: multiple
title: Método SetDeadGWDetect da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDeadGWDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83f62d84af193be99850f1a82b720a2983ca77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456941"
---
# <a name="setdeadgwdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="da163-103">Método SetDeadGWDetect da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="da163-103">SetDeadGWDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="da163-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDeadGWDetect** é usado para habilitar a detecção de gateway inativo.</span><span class="sxs-lookup"><span data-stu-id="da163-104">The **SetDeadGWDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable dead gateway detection.</span></span>

<span data-ttu-id="da163-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="da163-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="da163-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="da163-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="da163-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da163-107">Syntax</span></span>


```mof
uint32 SetDeadGWDetect(
  [in] boolean DeadGWDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="da163-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da163-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da163-109">*DeadGWDetectEnabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da163-109">*DeadGWDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da163-110">Se **for true**, a detecção de gateways inativos deverá ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="da163-110">If **true**, dead gateway detection should be enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da163-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da163-111">Return value</span></span>

<span data-ttu-id="da163-112">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="da163-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="da163-113">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="da163-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="da163-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="da163-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="da163-115">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="da163-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="da163-116">0</span><span class="sxs-lookup"><span data-stu-id="da163-116">0</span></span>

<span data-ttu-id="da163-117">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="da163-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="da163-118">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="da163-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="da163-119">1</span><span class="sxs-lookup"><span data-stu-id="da163-119">1</span></span>

<span data-ttu-id="da163-120">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="da163-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="da163-121">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="da163-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="da163-122">64</span><span class="sxs-lookup"><span data-stu-id="da163-122">64</span></span>

<span data-ttu-id="da163-123">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="da163-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="da163-124">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="da163-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="da163-125">65</span><span class="sxs-lookup"><span data-stu-id="da163-125">65</span></span>

<span data-ttu-id="da163-126">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="da163-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="da163-127">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="da163-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="da163-128">66</span><span class="sxs-lookup"><span data-stu-id="da163-128">66</span></span>

<span data-ttu-id="da163-129">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="da163-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="da163-130">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="da163-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="da163-131">67</span><span class="sxs-lookup"><span data-stu-id="da163-131">67</span></span>

<span data-ttu-id="da163-132">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="da163-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="da163-133">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="da163-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="da163-134">68</span><span class="sxs-lookup"><span data-stu-id="da163-134">68</span></span>

<span data-ttu-id="da163-135">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="da163-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="da163-136">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="da163-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="da163-137">69</span><span class="sxs-lookup"><span data-stu-id="da163-137">69</span></span>

<span data-ttu-id="da163-138">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="da163-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="da163-139">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="da163-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="da163-140">70</span><span class="sxs-lookup"><span data-stu-id="da163-140">70</span></span>

<span data-ttu-id="da163-141">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="da163-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="da163-142">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="da163-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="da163-143">71</span><span class="sxs-lookup"><span data-stu-id="da163-143">71</span></span>

<span data-ttu-id="da163-144">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="da163-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="da163-145">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="da163-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="da163-146">72</span><span class="sxs-lookup"><span data-stu-id="da163-146">72</span></span>

<span data-ttu-id="da163-147">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="da163-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="da163-148">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="da163-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="da163-149">73</span><span class="sxs-lookup"><span data-stu-id="da163-149">73</span></span>

<span data-ttu-id="da163-150">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="da163-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="da163-151">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="da163-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="da163-152">74</span><span class="sxs-lookup"><span data-stu-id="da163-152">74</span></span>

<span data-ttu-id="da163-153">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="da163-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="da163-154">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="da163-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="da163-155">75</span><span class="sxs-lookup"><span data-stu-id="da163-155">75</span></span>

<span data-ttu-id="da163-156">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="da163-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="da163-157">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="da163-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="da163-158">76</span><span class="sxs-lookup"><span data-stu-id="da163-158">76</span></span>

<span data-ttu-id="da163-159">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="da163-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="da163-160">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="da163-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="da163-161">77</span><span class="sxs-lookup"><span data-stu-id="da163-161">77</span></span>

<span data-ttu-id="da163-162">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="da163-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="da163-163">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="da163-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="da163-164">78</span><span class="sxs-lookup"><span data-stu-id="da163-164">78</span></span>

<span data-ttu-id="da163-165">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="da163-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="da163-166">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="da163-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="da163-167">79</span><span class="sxs-lookup"><span data-stu-id="da163-167">79</span></span>

<span data-ttu-id="da163-168">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="da163-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="da163-169">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="da163-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="da163-170">80</span><span class="sxs-lookup"><span data-stu-id="da163-170">80</span></span>

<span data-ttu-id="da163-171">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="da163-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="da163-172">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="da163-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="da163-173">81</span><span class="sxs-lookup"><span data-stu-id="da163-173">81</span></span>

<span data-ttu-id="da163-174">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="da163-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="da163-175">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="da163-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="da163-176">82</span><span class="sxs-lookup"><span data-stu-id="da163-176">82</span></span>

<span data-ttu-id="da163-177">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="da163-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="da163-178">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="da163-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="da163-179">83</span><span class="sxs-lookup"><span data-stu-id="da163-179">83</span></span>

<span data-ttu-id="da163-180">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="da163-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="da163-181">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="da163-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="da163-182">84</span><span class="sxs-lookup"><span data-stu-id="da163-182">84</span></span>

<span data-ttu-id="da163-183">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="da163-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="da163-184">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="da163-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="da163-185">85</span><span class="sxs-lookup"><span data-stu-id="da163-185">85</span></span>

<span data-ttu-id="da163-186">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="da163-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="da163-187">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="da163-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="da163-188">86</span><span class="sxs-lookup"><span data-stu-id="da163-188">86</span></span>

<span data-ttu-id="da163-189">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="da163-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="da163-190">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="da163-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="da163-191">87</span><span class="sxs-lookup"><span data-stu-id="da163-191">87</span></span>

<span data-ttu-id="da163-192">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="da163-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="da163-193">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="da163-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="da163-194">88</span><span class="sxs-lookup"><span data-stu-id="da163-194">88</span></span>

<span data-ttu-id="da163-195">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="da163-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="da163-196">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="da163-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="da163-197">89</span><span class="sxs-lookup"><span data-stu-id="da163-197">89</span></span>

<span data-ttu-id="da163-198">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="da163-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="da163-199">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="da163-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="da163-200">90</span><span class="sxs-lookup"><span data-stu-id="da163-200">90</span></span>

<span data-ttu-id="da163-201">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="da163-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="da163-202">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="da163-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="da163-203">91</span><span class="sxs-lookup"><span data-stu-id="da163-203">91</span></span>

<span data-ttu-id="da163-204">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="da163-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="da163-205">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="da163-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="da163-206">92</span><span class="sxs-lookup"><span data-stu-id="da163-206">92</span></span>

<span data-ttu-id="da163-207">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="da163-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="da163-208">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="da163-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="da163-209">93</span><span class="sxs-lookup"><span data-stu-id="da163-209">93</span></span>

<span data-ttu-id="da163-210">Já existe.</span><span class="sxs-lookup"><span data-stu-id="da163-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="da163-211">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="da163-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="da163-212">94</span><span class="sxs-lookup"><span data-stu-id="da163-212">94</span></span>

<span data-ttu-id="da163-213">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="da163-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="da163-214">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="da163-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="da163-215">95</span><span class="sxs-lookup"><span data-stu-id="da163-215">95</span></span>

<span data-ttu-id="da163-216">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="da163-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="da163-217">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="da163-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="da163-218">96</span><span class="sxs-lookup"><span data-stu-id="da163-218">96</span></span>

<span data-ttu-id="da163-219">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="da163-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="da163-220">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="da163-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="da163-221">97</span><span class="sxs-lookup"><span data-stu-id="da163-221">97</span></span>

<span data-ttu-id="da163-222">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="da163-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="da163-223">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="da163-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="da163-224">98</span><span class="sxs-lookup"><span data-stu-id="da163-224">98</span></span>

<span data-ttu-id="da163-225">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="da163-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="da163-226">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="da163-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="da163-227">100</span><span class="sxs-lookup"><span data-stu-id="da163-227">100</span></span>

<span data-ttu-id="da163-228">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="da163-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="da163-229">**Outras**</span><span class="sxs-lookup"><span data-stu-id="da163-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="da163-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="da163-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da163-231">Comentários</span><span class="sxs-lookup"><span data-stu-id="da163-231">Remarks</span></span>

<span data-ttu-id="da163-232">Com esse recurso habilitado, o TCP solicita que o IP mude para um gateway de backup se ele retransmitir um segmento várias vezes sem receber uma resposta.</span><span class="sxs-lookup"><span data-stu-id="da163-232">With this feature enabled, TCP asks IP to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

## <a name="examples"></a><span data-ttu-id="da163-233">Exemplos</span><span class="sxs-lookup"><span data-stu-id="da163-233">Examples</span></span>

<span data-ttu-id="da163-234">A amostra [habilitar a detecção de gateway inativo para todos os adaptadores de rede do](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) VBScript na galeria do TechNet usa **SetDeadGWDetect** para configurar todos os adaptadores de rede em um computador para detectar automaticamente gateways inativos.</span><span class="sxs-lookup"><span data-stu-id="da163-234">The [Enable Dead Gateway Detection for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) VBScript sample on TechNet Gallery uses **SetDeadGWDetect** to configure all network adapters on a computer to automatically detect dead gateways.</span></span>

## <a name="requirements"></a><span data-ttu-id="da163-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da163-235">Requirements</span></span>



| <span data-ttu-id="da163-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="da163-236">Requirement</span></span> | <span data-ttu-id="da163-237">Valor</span><span class="sxs-lookup"><span data-stu-id="da163-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da163-238">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da163-238">Minimum supported client</span></span><br/> | <span data-ttu-id="da163-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da163-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da163-240">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da163-240">Minimum supported server</span></span><br/> | <span data-ttu-id="da163-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da163-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da163-242">Namespace</span><span class="sxs-lookup"><span data-stu-id="da163-242">Namespace</span></span><br/>                | <span data-ttu-id="da163-243">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="da163-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="da163-244">MOF</span><span class="sxs-lookup"><span data-stu-id="da163-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da163-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da163-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="da163-246">DLL</span><span class="sxs-lookup"><span data-stu-id="da163-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da163-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da163-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da163-248">Confira também</span><span class="sxs-lookup"><span data-stu-id="da163-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da163-249">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="da163-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="da163-250">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="da163-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="da163-251">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="da163-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="da163-252">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="da163-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="da163-253">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="da163-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

