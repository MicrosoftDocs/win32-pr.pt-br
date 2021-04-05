---
description: O método estático da classe WMI SetMTU é usado para definir a unidade máxima de transmissão (MTU) padrão para uma interface de rede.
ms.assetid: 262c8bd7-1057-4204-80ab-725c60fc9c52
ms.tgt_platform: multiple
title: Método SetMTU da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetMTU
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 466c344892f2c4bf4a1e979ac9c1f50cd709325a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646417"
---
# <a name="setmtu-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d83a2-103">Método SetMTU da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="d83a2-103">SetMTU method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d83a2-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetMTU** é usado para definir a unidade máxima de transmissão (MTU) padrão para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d83a2-104">The **SetMTU** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Maximum Transmission Unit (MTU) for a network interface.</span></span>

<span data-ttu-id="d83a2-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d83a2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d83a2-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d83a2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d83a2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d83a2-107">Syntax</span></span>


```mof
uint32 SetMTU(
  [in] uint32 MTU
);
```



## <a name="parameters"></a><span data-ttu-id="d83a2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d83a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d83a2-109">*MTU* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d83a2-109">*MTU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-110">MTU (unidade máxima de transmissão) padrão para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d83a2-110">Default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="d83a2-111">O intervalo desse valor abrange o tamanho mínimo do pacote (68) para a MTU com suporte da rede subjacente.</span><span class="sxs-lookup"><span data-stu-id="d83a2-111">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d83a2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d83a2-112">Return value</span></span>

<span data-ttu-id="d83a2-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="d83a2-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="d83a2-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d83a2-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d83a2-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d83a2-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d83a2-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="d83a2-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-117">0</span><span class="sxs-lookup"><span data-stu-id="d83a2-117">0</span></span>

<span data-ttu-id="d83a2-118">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d83a2-118">Successful completion.</span></span> <span data-ttu-id="d83a2-119">Nenhuma reinicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="d83a2-119">No reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-120">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="d83a2-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-121">1</span><span class="sxs-lookup"><span data-stu-id="d83a2-121">1</span></span>

<span data-ttu-id="d83a2-122">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d83a2-122">Successful completion.</span></span> <span data-ttu-id="d83a2-123">A reinicialização é obrigatória.</span><span class="sxs-lookup"><span data-stu-id="d83a2-123">Reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-124">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="d83a2-124">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-125">64</span><span class="sxs-lookup"><span data-stu-id="d83a2-125">64</span></span>

<span data-ttu-id="d83a2-126">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="d83a2-126">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-127">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="d83a2-127">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-128">65</span><span class="sxs-lookup"><span data-stu-id="d83a2-128">65</span></span>

<span data-ttu-id="d83a2-129">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="d83a2-129">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-130">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="d83a2-130">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-131">66</span><span class="sxs-lookup"><span data-stu-id="d83a2-131">66</span></span>

<span data-ttu-id="d83a2-132">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="d83a2-132">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-133">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="d83a2-133">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-134">67</span><span class="sxs-lookup"><span data-stu-id="d83a2-134">67</span></span>

<span data-ttu-id="d83a2-135">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="d83a2-135">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-136">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="d83a2-136">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-137">68</span><span class="sxs-lookup"><span data-stu-id="d83a2-137">68</span></span>

<span data-ttu-id="d83a2-138">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="d83a2-138">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-139">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="d83a2-139">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-140">69</span><span class="sxs-lookup"><span data-stu-id="d83a2-140">69</span></span>

<span data-ttu-id="d83a2-141">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="d83a2-141">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-142">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="d83a2-142">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-143">70</span><span class="sxs-lookup"><span data-stu-id="d83a2-143">70</span></span>

<span data-ttu-id="d83a2-144">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="d83a2-144">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-145">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="d83a2-145">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-146">71</span><span class="sxs-lookup"><span data-stu-id="d83a2-146">71</span></span>

<span data-ttu-id="d83a2-147">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="d83a2-147">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-148">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="d83a2-148">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-149">72</span><span class="sxs-lookup"><span data-stu-id="d83a2-149">72</span></span>

<span data-ttu-id="d83a2-150">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="d83a2-150">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-151">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="d83a2-151">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-152">73</span><span class="sxs-lookup"><span data-stu-id="d83a2-152">73</span></span>

<span data-ttu-id="d83a2-153">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="d83a2-153">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-154">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="d83a2-154">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-155">74</span><span class="sxs-lookup"><span data-stu-id="d83a2-155">74</span></span>

<span data-ttu-id="d83a2-156">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="d83a2-156">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-157">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="d83a2-157">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-158">75</span><span class="sxs-lookup"><span data-stu-id="d83a2-158">75</span></span>

<span data-ttu-id="d83a2-159">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="d83a2-159">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-160">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="d83a2-160">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-161">76</span><span class="sxs-lookup"><span data-stu-id="d83a2-161">76</span></span>

<span data-ttu-id="d83a2-162">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="d83a2-162">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-163">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="d83a2-163">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-164">77</span><span class="sxs-lookup"><span data-stu-id="d83a2-164">77</span></span>

<span data-ttu-id="d83a2-165">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="d83a2-165">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-166">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="d83a2-166">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-167">78</span><span class="sxs-lookup"><span data-stu-id="d83a2-167">78</span></span>

<span data-ttu-id="d83a2-168">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d83a2-168">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-169">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="d83a2-169">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-170">79</span><span class="sxs-lookup"><span data-stu-id="d83a2-170">79</span></span>

<span data-ttu-id="d83a2-171">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="d83a2-171">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-172">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="d83a2-172">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-173">80</span><span class="sxs-lookup"><span data-stu-id="d83a2-173">80</span></span>

<span data-ttu-id="d83a2-174">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d83a2-174">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-175">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="d83a2-175">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-176">81</span><span class="sxs-lookup"><span data-stu-id="d83a2-176">81</span></span>

<span data-ttu-id="d83a2-177">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="d83a2-177">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-178">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="d83a2-178">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-179">82</span><span class="sxs-lookup"><span data-stu-id="d83a2-179">82</span></span>

<span data-ttu-id="d83a2-180">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="d83a2-180">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-181">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="d83a2-181">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-182">83</span><span class="sxs-lookup"><span data-stu-id="d83a2-182">83</span></span>

<span data-ttu-id="d83a2-183">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="d83a2-183">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-184">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="d83a2-184">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-185">84</span><span class="sxs-lookup"><span data-stu-id="d83a2-185">84</span></span>

<span data-ttu-id="d83a2-186">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="d83a2-186">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-187">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="d83a2-187">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-188">85</span><span class="sxs-lookup"><span data-stu-id="d83a2-188">85</span></span>

<span data-ttu-id="d83a2-189">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="d83a2-189">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-190">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="d83a2-190">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-191">86</span><span class="sxs-lookup"><span data-stu-id="d83a2-191">86</span></span>

<span data-ttu-id="d83a2-192">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="d83a2-192">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-193">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="d83a2-193">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-194">87</span><span class="sxs-lookup"><span data-stu-id="d83a2-194">87</span></span>

<span data-ttu-id="d83a2-195">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="d83a2-195">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-196">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="d83a2-196">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-197">88</span><span class="sxs-lookup"><span data-stu-id="d83a2-197">88</span></span>

<span data-ttu-id="d83a2-198">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="d83a2-198">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-199">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="d83a2-199">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-200">89</span><span class="sxs-lookup"><span data-stu-id="d83a2-200">89</span></span>

<span data-ttu-id="d83a2-201">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="d83a2-201">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-202">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="d83a2-202">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-203">90</span><span class="sxs-lookup"><span data-stu-id="d83a2-203">90</span></span>

<span data-ttu-id="d83a2-204">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="d83a2-204">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-205">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="d83a2-205">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-206">91</span><span class="sxs-lookup"><span data-stu-id="d83a2-206">91</span></span>

<span data-ttu-id="d83a2-207">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="d83a2-207">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-208">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="d83a2-208">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-209">92</span><span class="sxs-lookup"><span data-stu-id="d83a2-209">92</span></span>

<span data-ttu-id="d83a2-210">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="d83a2-210">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-211">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="d83a2-211">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-212">93</span><span class="sxs-lookup"><span data-stu-id="d83a2-212">93</span></span>

<span data-ttu-id="d83a2-213">Já existe.</span><span class="sxs-lookup"><span data-stu-id="d83a2-213">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-214">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="d83a2-214">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-215">94</span><span class="sxs-lookup"><span data-stu-id="d83a2-215">94</span></span>

<span data-ttu-id="d83a2-216">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="d83a2-216">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-217">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="d83a2-217">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-218">95</span><span class="sxs-lookup"><span data-stu-id="d83a2-218">95</span></span>

<span data-ttu-id="d83a2-219">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="d83a2-219">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-220">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="d83a2-220">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-221">96</span><span class="sxs-lookup"><span data-stu-id="d83a2-221">96</span></span>

<span data-ttu-id="d83a2-222">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="d83a2-222">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-223">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="d83a2-223">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-224">97</span><span class="sxs-lookup"><span data-stu-id="d83a2-224">97</span></span>

<span data-ttu-id="d83a2-225">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="d83a2-225">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-226">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="d83a2-226">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-227">98</span><span class="sxs-lookup"><span data-stu-id="d83a2-227">98</span></span>

<span data-ttu-id="d83a2-228">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="d83a2-228">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-229">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="d83a2-229">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-230">100</span><span class="sxs-lookup"><span data-stu-id="d83a2-230">100</span></span>

<span data-ttu-id="d83a2-231">O DHCP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="d83a2-231">DHCP is not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d83a2-232">**Outras**</span><span class="sxs-lookup"><span data-stu-id="d83a2-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d83a2-233">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="d83a2-233">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d83a2-234">Comentários</span><span class="sxs-lookup"><span data-stu-id="d83a2-234">Remarks</span></span>

<span data-ttu-id="d83a2-235">O MTU é o tamanho máximo do pacote (em bytes) que um transporte transmitirá pela rede subjacente.</span><span class="sxs-lookup"><span data-stu-id="d83a2-235">The MTU is the maximum packet size (in bytes) that a transport will transmit over the underlying network.</span></span> <span data-ttu-id="d83a2-236">O tamanho inclui o cabeçalho de transporte.</span><span class="sxs-lookup"><span data-stu-id="d83a2-236">The size includes the transport header.</span></span>

<span data-ttu-id="d83a2-237">Observe que um datagrama IP pode abranger vários pacotes.</span><span class="sxs-lookup"><span data-stu-id="d83a2-237">Note that an IP datagram can span multiple packets.</span></span> <span data-ttu-id="d83a2-238">Valores maiores que o padrão para a rede subjacente resultam no transporte usando a MTU padrão de rede.</span><span class="sxs-lookup"><span data-stu-id="d83a2-238">Values larger than the default for the underlying network result in the transport using the network default MTU.</span></span> <span data-ttu-id="d83a2-239">Valores menores que 68 resultam no transporte usando um MTU de 68.</span><span class="sxs-lookup"><span data-stu-id="d83a2-239">Values smaller than 68 result in the transport using an MTU of 68.</span></span>

## <a name="examples"></a><span data-ttu-id="d83a2-240">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d83a2-240">Examples</span></span>

<span data-ttu-id="d83a2-241">A amostra [Modificar o MTU para todos os adaptadores de rede](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) do VBScript configura a unidade de transmissão máxima para todos os adaptadores de rede instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="d83a2-241">The [Modify the MTU for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) VBScript sample configures the maximum transmission unit for all network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d83a2-242">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d83a2-242">Requirements</span></span>



| <span data-ttu-id="d83a2-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="d83a2-243">Requirement</span></span> | <span data-ttu-id="d83a2-244">Valor</span><span class="sxs-lookup"><span data-stu-id="d83a2-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d83a2-245">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d83a2-245">Minimum supported client</span></span><br/> | <span data-ttu-id="d83a2-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d83a2-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d83a2-247">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d83a2-247">Minimum supported server</span></span><br/> | <span data-ttu-id="d83a2-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d83a2-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d83a2-249">Namespace</span><span class="sxs-lookup"><span data-stu-id="d83a2-249">Namespace</span></span><br/>                | <span data-ttu-id="d83a2-250">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d83a2-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d83a2-251">MOF</span><span class="sxs-lookup"><span data-stu-id="d83a2-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d83a2-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d83a2-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d83a2-253">DLL</span><span class="sxs-lookup"><span data-stu-id="d83a2-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d83a2-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d83a2-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d83a2-255">Confira também</span><span class="sxs-lookup"><span data-stu-id="d83a2-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d83a2-256">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="d83a2-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d83a2-257">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="d83a2-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="d83a2-258">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="d83a2-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="d83a2-259">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="d83a2-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d83a2-260">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="d83a2-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

