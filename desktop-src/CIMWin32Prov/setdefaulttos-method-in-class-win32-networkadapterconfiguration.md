---
description: Esse método é obsoleto. Os aplicativos devem usar a API de QoS (qualidade de serviço) para manipular bits de tipo de serviço (TOS).
ms.assetid: 18860c13-7324-4a37-b83c-f3d15c425acb
ms.tgt_platform: multiple
title: Método SetDefaultTOS da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTOS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5df55ff88c87047a48a84a122c8e58c8148a7cff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752960"
---
# <a name="setdefaulttos-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="6c16e-104">Método SetDefaultTOS da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c16e-104">SetDefaultTOS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="6c16e-105">Esse método é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="6c16e-105">This method is obsolete.</span></span> <span data-ttu-id="6c16e-106">Os aplicativos devem usar a API de QoS (qualidade de serviço) para manipular bits de tipo de serviço (TOS).</span><span class="sxs-lookup"><span data-stu-id="6c16e-106">Applications should use the Quality of Service (QoS) API to manipulate Type of Service (TOS) bits.</span></span> <span data-ttu-id="6c16e-107">Para obter mais informações, consulte [Quality of Service](/previous-versions/windows/desktop/qos/qos-start-page).</span><span class="sxs-lookup"><span data-stu-id="6c16e-107">For more information, see [Quality of Service](/previous-versions/windows/desktop/qos/qos-start-page).</span></span>

<span data-ttu-id="6c16e-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="6c16e-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6c16e-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6c16e-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c16e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c16e-110">Syntax</span></span>


```mof
uint32 SetDefaultTOS(
  [in] uint8 DefaultTOS
);
```



## <a name="parameters"></a><span data-ttu-id="6c16e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c16e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c16e-112">*DefaultTOS* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c16e-112">*DefaultTOS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-113">Valor de TOS (tipo de serviço) colocado no cabeçalho dos pacotes de IP de saída.</span><span class="sxs-lookup"><span data-stu-id="6c16e-113">Type of Service (TOS) value put in the header of outgoing IP packets.</span></span> <span data-ttu-id="6c16e-114">Para obter uma definição dos valores, consulte RFC 791.</span><span class="sxs-lookup"><span data-stu-id="6c16e-114">For a definition of the values, see RFC 791.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c16e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c16e-115">Return value</span></span>

<span data-ttu-id="6c16e-116">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="6c16e-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="6c16e-117">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6c16e-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6c16e-118">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6c16e-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6c16e-119">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="6c16e-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-120">0</span><span class="sxs-lookup"><span data-stu-id="6c16e-120">0</span></span>

<span data-ttu-id="6c16e-121">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="6c16e-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-122">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="6c16e-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-123">1</span><span class="sxs-lookup"><span data-stu-id="6c16e-123">1</span></span>

<span data-ttu-id="6c16e-124">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="6c16e-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-125">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="6c16e-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-126">64</span><span class="sxs-lookup"><span data-stu-id="6c16e-126">64</span></span>

<span data-ttu-id="6c16e-127">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="6c16e-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-128">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="6c16e-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-129">65</span><span class="sxs-lookup"><span data-stu-id="6c16e-129">65</span></span>

<span data-ttu-id="6c16e-130">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="6c16e-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-131">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="6c16e-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-132">66</span><span class="sxs-lookup"><span data-stu-id="6c16e-132">66</span></span>

<span data-ttu-id="6c16e-133">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="6c16e-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-134">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="6c16e-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-135">67</span><span class="sxs-lookup"><span data-stu-id="6c16e-135">67</span></span>

<span data-ttu-id="6c16e-136">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="6c16e-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-137">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="6c16e-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-138">68</span><span class="sxs-lookup"><span data-stu-id="6c16e-138">68</span></span>

<span data-ttu-id="6c16e-139">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="6c16e-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-140">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="6c16e-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-141">69</span><span class="sxs-lookup"><span data-stu-id="6c16e-141">69</span></span>

<span data-ttu-id="6c16e-142">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="6c16e-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-143">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="6c16e-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-144">70</span><span class="sxs-lookup"><span data-stu-id="6c16e-144">70</span></span>

<span data-ttu-id="6c16e-145">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="6c16e-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-146">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="6c16e-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-147">71</span><span class="sxs-lookup"><span data-stu-id="6c16e-147">71</span></span>

<span data-ttu-id="6c16e-148">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="6c16e-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-149">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="6c16e-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-150">72</span><span class="sxs-lookup"><span data-stu-id="6c16e-150">72</span></span>

<span data-ttu-id="6c16e-151">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="6c16e-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-152">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="6c16e-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-153">73</span><span class="sxs-lookup"><span data-stu-id="6c16e-153">73</span></span>

<span data-ttu-id="6c16e-154">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="6c16e-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-155">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="6c16e-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-156">74</span><span class="sxs-lookup"><span data-stu-id="6c16e-156">74</span></span>

<span data-ttu-id="6c16e-157">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="6c16e-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-158">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="6c16e-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-159">75</span><span class="sxs-lookup"><span data-stu-id="6c16e-159">75</span></span>

<span data-ttu-id="6c16e-160">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="6c16e-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-161">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="6c16e-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-162">76</span><span class="sxs-lookup"><span data-stu-id="6c16e-162">76</span></span>

<span data-ttu-id="6c16e-163">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="6c16e-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-164">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="6c16e-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-165">77</span><span class="sxs-lookup"><span data-stu-id="6c16e-165">77</span></span>

<span data-ttu-id="6c16e-166">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="6c16e-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-167">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="6c16e-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-168">78</span><span class="sxs-lookup"><span data-stu-id="6c16e-168">78</span></span>

<span data-ttu-id="6c16e-169">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6c16e-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-170">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="6c16e-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-171">79</span><span class="sxs-lookup"><span data-stu-id="6c16e-171">79</span></span>

<span data-ttu-id="6c16e-172">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="6c16e-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-173">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="6c16e-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-174">80</span><span class="sxs-lookup"><span data-stu-id="6c16e-174">80</span></span>

<span data-ttu-id="6c16e-175">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="6c16e-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-176">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="6c16e-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-177">81</span><span class="sxs-lookup"><span data-stu-id="6c16e-177">81</span></span>

<span data-ttu-id="6c16e-178">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="6c16e-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-179">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="6c16e-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-180">82</span><span class="sxs-lookup"><span data-stu-id="6c16e-180">82</span></span>

<span data-ttu-id="6c16e-181">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="6c16e-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-182">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="6c16e-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-183">83</span><span class="sxs-lookup"><span data-stu-id="6c16e-183">83</span></span>

<span data-ttu-id="6c16e-184">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="6c16e-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-185">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="6c16e-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-186">84</span><span class="sxs-lookup"><span data-stu-id="6c16e-186">84</span></span>

<span data-ttu-id="6c16e-187">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="6c16e-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-188">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="6c16e-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-189">85</span><span class="sxs-lookup"><span data-stu-id="6c16e-189">85</span></span>

<span data-ttu-id="6c16e-190">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="6c16e-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-191">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="6c16e-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-192">86</span><span class="sxs-lookup"><span data-stu-id="6c16e-192">86</span></span>

<span data-ttu-id="6c16e-193">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="6c16e-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-194">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="6c16e-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-195">87</span><span class="sxs-lookup"><span data-stu-id="6c16e-195">87</span></span>

<span data-ttu-id="6c16e-196">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="6c16e-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-197">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="6c16e-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-198">88</span><span class="sxs-lookup"><span data-stu-id="6c16e-198">88</span></span>

<span data-ttu-id="6c16e-199">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="6c16e-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-200">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="6c16e-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-201">89</span><span class="sxs-lookup"><span data-stu-id="6c16e-201">89</span></span>

<span data-ttu-id="6c16e-202">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="6c16e-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-203">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="6c16e-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-204">90</span><span class="sxs-lookup"><span data-stu-id="6c16e-204">90</span></span>

<span data-ttu-id="6c16e-205">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="6c16e-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-206">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="6c16e-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-207">91</span><span class="sxs-lookup"><span data-stu-id="6c16e-207">91</span></span>

<span data-ttu-id="6c16e-208">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="6c16e-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-209">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="6c16e-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-210">92</span><span class="sxs-lookup"><span data-stu-id="6c16e-210">92</span></span>

<span data-ttu-id="6c16e-211">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="6c16e-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-212">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="6c16e-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-213">93</span><span class="sxs-lookup"><span data-stu-id="6c16e-213">93</span></span>

<span data-ttu-id="6c16e-214">Já existe.</span><span class="sxs-lookup"><span data-stu-id="6c16e-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-215">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="6c16e-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-216">94</span><span class="sxs-lookup"><span data-stu-id="6c16e-216">94</span></span>

<span data-ttu-id="6c16e-217">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="6c16e-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-218">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="6c16e-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-219">95</span><span class="sxs-lookup"><span data-stu-id="6c16e-219">95</span></span>

<span data-ttu-id="6c16e-220">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="6c16e-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-221">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="6c16e-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-222">96</span><span class="sxs-lookup"><span data-stu-id="6c16e-222">96</span></span>

<span data-ttu-id="6c16e-223">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="6c16e-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-224">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="6c16e-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-225">97</span><span class="sxs-lookup"><span data-stu-id="6c16e-225">97</span></span>

<span data-ttu-id="6c16e-226">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="6c16e-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-227">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="6c16e-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-228">98</span><span class="sxs-lookup"><span data-stu-id="6c16e-228">98</span></span>

<span data-ttu-id="6c16e-229">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="6c16e-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-230">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="6c16e-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-231">100</span><span class="sxs-lookup"><span data-stu-id="6c16e-231">100</span></span>

<span data-ttu-id="6c16e-232">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="6c16e-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6c16e-233">**Outras**</span><span class="sxs-lookup"><span data-stu-id="6c16e-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="6c16e-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="6c16e-234">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c16e-235">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c16e-235">Remarks</span></span>

<span data-ttu-id="6c16e-236">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultTOS** é usado para definir o valor de tos padrão no cabeçalho de pacotes IP de saída.</span><span class="sxs-lookup"><span data-stu-id="6c16e-236">The **SetDefaultTOS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default TOS value in the header of outgoing IP packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c16e-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c16e-237">Requirements</span></span>



| <span data-ttu-id="6c16e-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c16e-238">Requirement</span></span> | <span data-ttu-id="6c16e-239">Valor</span><span class="sxs-lookup"><span data-stu-id="6c16e-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c16e-240">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c16e-240">Minimum supported client</span></span><br/> | <span data-ttu-id="6c16e-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c16e-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c16e-242">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c16e-242">Minimum supported server</span></span><br/> | <span data-ttu-id="6c16e-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c16e-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c16e-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c16e-244">Namespace</span></span><br/>                | <span data-ttu-id="6c16e-245">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6c16e-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6c16e-246">MOF</span><span class="sxs-lookup"><span data-stu-id="6c16e-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c16e-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c16e-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c16e-248">DLL</span><span class="sxs-lookup"><span data-stu-id="6c16e-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c16e-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c16e-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c16e-250">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c16e-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c16e-251">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="6c16e-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="6c16e-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="6c16e-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="6c16e-253">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="6c16e-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="6c16e-254">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="6c16e-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="6c16e-255">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="6c16e-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

