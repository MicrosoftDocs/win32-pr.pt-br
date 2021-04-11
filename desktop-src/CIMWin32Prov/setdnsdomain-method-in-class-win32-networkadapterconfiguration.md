---
description: O método de classe WMI SetDNSDomain permite a configuração do domínio DNS.
ms.assetid: a531133e-1b7c-4d85-979d-63bf4f7c9bed
ms.tgt_platform: multiple
title: Método SetDNSDomain da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSDomain
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c440d8cb5c720bf6922707f04bc75e2383755c1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164127"
---
# <a name="setdnsdomain-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="91ab3-103">Método SetDNSDomain da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="91ab3-103">SetDNSDomain method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="91ab3-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSDomain** permite a configuração do domínio DNS.</span><span class="sxs-lookup"><span data-stu-id="91ab3-104">The **SetDNSDomain** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows for the setting of the DNS domain.</span></span>

<span data-ttu-id="91ab3-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="91ab3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="91ab3-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="91ab3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="91ab3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91ab3-107">Syntax</span></span>


```mof
uint32 SetDNSDomain(
  [in] string DNSDomain
);
```



## <a name="parameters"></a><span data-ttu-id="91ab3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91ab3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91ab3-109">*DNSDomain* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91ab3-109">*DNSDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-110">Domínio ao qual o DNS está associado, representado por um nome de organização seguido por um ponto e uma extensão que indica o tipo de organização.</span><span class="sxs-lookup"><span data-stu-id="91ab3-110">Domain with which the DNS is associated, represented by an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="91ab3-111">Exemplo: "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="91ab3-111">Example: "microsoft.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91ab3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91ab3-112">Return value</span></span>

<span data-ttu-id="91ab3-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="91ab3-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required and a different number if there is an error.</span></span> <span data-ttu-id="91ab3-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="91ab3-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="91ab3-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="91ab3-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="91ab3-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="91ab3-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-117">0</span><span class="sxs-lookup"><span data-stu-id="91ab3-117">0</span></span>

<span data-ttu-id="91ab3-118">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="91ab3-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-119">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="91ab3-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-120">1</span><span class="sxs-lookup"><span data-stu-id="91ab3-120">1</span></span>

<span data-ttu-id="91ab3-121">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="91ab3-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-122">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="91ab3-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-123">64</span><span class="sxs-lookup"><span data-stu-id="91ab3-123">64</span></span>

<span data-ttu-id="91ab3-124">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="91ab3-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-125">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="91ab3-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-126">65</span><span class="sxs-lookup"><span data-stu-id="91ab3-126">65</span></span>

<span data-ttu-id="91ab3-127">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="91ab3-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-128">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="91ab3-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-129">66</span><span class="sxs-lookup"><span data-stu-id="91ab3-129">66</span></span>

<span data-ttu-id="91ab3-130">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="91ab3-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-131">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="91ab3-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-132">67</span><span class="sxs-lookup"><span data-stu-id="91ab3-132">67</span></span>

<span data-ttu-id="91ab3-133">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="91ab3-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-134">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="91ab3-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-135">68</span><span class="sxs-lookup"><span data-stu-id="91ab3-135">68</span></span>

<span data-ttu-id="91ab3-136">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="91ab3-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-137">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="91ab3-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-138">69</span><span class="sxs-lookup"><span data-stu-id="91ab3-138">69</span></span>

<span data-ttu-id="91ab3-139">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="91ab3-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-140">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="91ab3-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-141">70</span><span class="sxs-lookup"><span data-stu-id="91ab3-141">70</span></span>

<span data-ttu-id="91ab3-142">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="91ab3-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-143">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="91ab3-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-144">71</span><span class="sxs-lookup"><span data-stu-id="91ab3-144">71</span></span>

<span data-ttu-id="91ab3-145">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="91ab3-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-146">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="91ab3-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-147">72</span><span class="sxs-lookup"><span data-stu-id="91ab3-147">72</span></span>

<span data-ttu-id="91ab3-148">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="91ab3-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-149">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="91ab3-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-150">73</span><span class="sxs-lookup"><span data-stu-id="91ab3-150">73</span></span>

<span data-ttu-id="91ab3-151">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="91ab3-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-152">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="91ab3-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-153">74</span><span class="sxs-lookup"><span data-stu-id="91ab3-153">74</span></span>

<span data-ttu-id="91ab3-154">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="91ab3-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-155">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="91ab3-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-156">75</span><span class="sxs-lookup"><span data-stu-id="91ab3-156">75</span></span>

<span data-ttu-id="91ab3-157">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="91ab3-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-158">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="91ab3-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-159">76</span><span class="sxs-lookup"><span data-stu-id="91ab3-159">76</span></span>

<span data-ttu-id="91ab3-160">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="91ab3-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-161">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="91ab3-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-162">77</span><span class="sxs-lookup"><span data-stu-id="91ab3-162">77</span></span>

<span data-ttu-id="91ab3-163">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="91ab3-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-164">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="91ab3-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-165">78</span><span class="sxs-lookup"><span data-stu-id="91ab3-165">78</span></span>

<span data-ttu-id="91ab3-166">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="91ab3-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-167">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="91ab3-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-168">79</span><span class="sxs-lookup"><span data-stu-id="91ab3-168">79</span></span>

<span data-ttu-id="91ab3-169">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="91ab3-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-170">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="91ab3-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-171">80</span><span class="sxs-lookup"><span data-stu-id="91ab3-171">80</span></span>

<span data-ttu-id="91ab3-172">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="91ab3-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-173">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="91ab3-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-174">81</span><span class="sxs-lookup"><span data-stu-id="91ab3-174">81</span></span>

<span data-ttu-id="91ab3-175">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="91ab3-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-176">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="91ab3-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-177">82</span><span class="sxs-lookup"><span data-stu-id="91ab3-177">82</span></span>

<span data-ttu-id="91ab3-178">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="91ab3-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-179">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="91ab3-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-180">83</span><span class="sxs-lookup"><span data-stu-id="91ab3-180">83</span></span>

<span data-ttu-id="91ab3-181">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="91ab3-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-182">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="91ab3-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-183">84</span><span class="sxs-lookup"><span data-stu-id="91ab3-183">84</span></span>

<span data-ttu-id="91ab3-184">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="91ab3-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-185">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="91ab3-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-186">85</span><span class="sxs-lookup"><span data-stu-id="91ab3-186">85</span></span>

<span data-ttu-id="91ab3-187">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="91ab3-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-188">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="91ab3-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-189">86</span><span class="sxs-lookup"><span data-stu-id="91ab3-189">86</span></span>

<span data-ttu-id="91ab3-190">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="91ab3-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-191">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="91ab3-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-192">87</span><span class="sxs-lookup"><span data-stu-id="91ab3-192">87</span></span>

<span data-ttu-id="91ab3-193">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="91ab3-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-194">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="91ab3-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-195">88</span><span class="sxs-lookup"><span data-stu-id="91ab3-195">88</span></span>

<span data-ttu-id="91ab3-196">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="91ab3-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-197">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="91ab3-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-198">89</span><span class="sxs-lookup"><span data-stu-id="91ab3-198">89</span></span>

<span data-ttu-id="91ab3-199">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="91ab3-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-200">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="91ab3-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-201">90</span><span class="sxs-lookup"><span data-stu-id="91ab3-201">90</span></span>

<span data-ttu-id="91ab3-202">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="91ab3-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-203">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="91ab3-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-204">91</span><span class="sxs-lookup"><span data-stu-id="91ab3-204">91</span></span>

<span data-ttu-id="91ab3-205">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="91ab3-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-206">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="91ab3-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-207">92</span><span class="sxs-lookup"><span data-stu-id="91ab3-207">92</span></span>

<span data-ttu-id="91ab3-208">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="91ab3-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-209">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="91ab3-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-210">93</span><span class="sxs-lookup"><span data-stu-id="91ab3-210">93</span></span>

<span data-ttu-id="91ab3-211">Já existe.</span><span class="sxs-lookup"><span data-stu-id="91ab3-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-212">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="91ab3-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-213">94</span><span class="sxs-lookup"><span data-stu-id="91ab3-213">94</span></span>

<span data-ttu-id="91ab3-214">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="91ab3-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-215">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="91ab3-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-216">95</span><span class="sxs-lookup"><span data-stu-id="91ab3-216">95</span></span>

<span data-ttu-id="91ab3-217">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="91ab3-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-218">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="91ab3-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-219">96</span><span class="sxs-lookup"><span data-stu-id="91ab3-219">96</span></span>

<span data-ttu-id="91ab3-220">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="91ab3-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-221">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="91ab3-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-222">97</span><span class="sxs-lookup"><span data-stu-id="91ab3-222">97</span></span>

<span data-ttu-id="91ab3-223">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="91ab3-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-224">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="91ab3-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-225">98</span><span class="sxs-lookup"><span data-stu-id="91ab3-225">98</span></span>

<span data-ttu-id="91ab3-226">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="91ab3-226">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-227">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="91ab3-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-228">100</span><span class="sxs-lookup"><span data-stu-id="91ab3-228">100</span></span>

<span data-ttu-id="91ab3-229">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="91ab3-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="91ab3-230">**Outras**</span><span class="sxs-lookup"><span data-stu-id="91ab3-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="91ab3-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="91ab3-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91ab3-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="91ab3-232">Remarks</span></span>

<span data-ttu-id="91ab3-233">Essa é uma chamada de método dependente de instância que se aplica a uma base por adaptador.</span><span class="sxs-lookup"><span data-stu-id="91ab3-233">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="91ab3-234">A configuração se aplica ao adaptador de destino.</span><span class="sxs-lookup"><span data-stu-id="91ab3-234">The setting applies to the targeted adapter.</span></span>

## <a name="examples"></a><span data-ttu-id="91ab3-235">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91ab3-235">Examples</span></span>

<span data-ttu-id="91ab3-236">O exemplo de código de [atribuir o domínio DNS para um adaptador de rede](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) VBScript na galeria do TechNet usa **SetDNSDomain** para definir o domínio DNS para um adaptador de rede vinculado a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="91ab3-236">The [Assign the DNS Domain for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) VBScript code sample on TechNet gallery uses **SetDNSDomain** to set the DNS domain for a TCP/IP-bound network adapter.</span></span>

<span data-ttu-id="91ab3-237">O exemplo de código [Modificar a configuração de TCP/IP para um computador](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) do VBScript Code na galeria do TechNet usa **SetDNSDomain** para modificar as configurações de TCP/IP de um adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="91ab3-237">The [Modify the TCP/IP Configuration for a Computer](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) VBScript code sample on TechNet Gallery uses **SetDNSDomain** to modify TCP/IP settings for a network adapter.</span></span>

<span data-ttu-id="91ab3-238">A amostra [Ativar configurações de DHCP em um computador](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript na galeria do TechNet usa **SetDNSDomain** para definir todas as configurações normalmente necessárias para habilitar o DHCP em um computador.</span><span class="sxs-lookup"><span data-stu-id="91ab3-238">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample on TechNet Gallery uses **SetDNSDomain** to configure all the settings typically required to enable DHCP on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="91ab3-239">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91ab3-239">Requirements</span></span>



| <span data-ttu-id="91ab3-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="91ab3-240">Requirement</span></span> | <span data-ttu-id="91ab3-241">Valor</span><span class="sxs-lookup"><span data-stu-id="91ab3-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91ab3-242">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91ab3-242">Minimum supported client</span></span><br/> | <span data-ttu-id="91ab3-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91ab3-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91ab3-244">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91ab3-244">Minimum supported server</span></span><br/> | <span data-ttu-id="91ab3-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91ab3-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91ab3-246">Namespace</span><span class="sxs-lookup"><span data-stu-id="91ab3-246">Namespace</span></span><br/>                | <span data-ttu-id="91ab3-247">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="91ab3-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="91ab3-248">MOF</span><span class="sxs-lookup"><span data-stu-id="91ab3-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91ab3-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91ab3-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="91ab3-250">DLL</span><span class="sxs-lookup"><span data-stu-id="91ab3-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91ab3-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91ab3-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91ab3-252">Confira também</span><span class="sxs-lookup"><span data-stu-id="91ab3-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ab3-253">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="91ab3-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="91ab3-254">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="91ab3-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="91ab3-255">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="91ab3-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="91ab3-256">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="91ab3-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="91ab3-257">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="91ab3-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

