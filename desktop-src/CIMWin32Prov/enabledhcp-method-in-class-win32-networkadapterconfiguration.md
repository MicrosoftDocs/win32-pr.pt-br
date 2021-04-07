---
description: O método de classe WMI EnableDHCP habilita o protocolo DHCP para serviço com esse adaptador de rede. O DHCP permite que os endereços IP sejam alocados dinamicamente.
ms.assetid: 8c61d731-77a3-4ef4-bad9-26edaca60892
ms.tgt_platform: multiple
title: Método EnableDHCP da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDHCP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 002dedd3b0165053fea98dda035316676af638f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920295"
---
# <a name="enabledhcp-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8db8e-104">Método EnableDHCP da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="8db8e-104">EnableDHCP method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8db8e-105">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableDHCP** habilita o protocolo DHCP para serviço com esse adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="8db8e-105">The **EnableDHCP** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span> <span data-ttu-id="8db8e-106">O DHCP permite que os endereços IP sejam alocados dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="8db8e-106">DHCP allows IP addresses to be dynamically allocated.</span></span>

<span data-ttu-id="8db8e-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8db8e-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8db8e-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8db8e-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8db8e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8db8e-109">Syntax</span></span>


```mof
uint32 EnableDHCP();
```



## <a name="parameters"></a><span data-ttu-id="8db8e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8db8e-110">Parameters</span></span>

<span data-ttu-id="8db8e-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8db8e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8db8e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8db8e-112">Return value</span></span>

<span data-ttu-id="8db8e-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando uma reinicialização não é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e qualquer outro número se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="8db8e-113">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="8db8e-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8db8e-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8db8e-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8db8e-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8db8e-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="8db8e-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-117">0</span><span class="sxs-lookup"><span data-stu-id="8db8e-117">0</span></span>

<span data-ttu-id="8db8e-118">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="8db8e-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-119">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="8db8e-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-120">1</span><span class="sxs-lookup"><span data-stu-id="8db8e-120">1</span></span>

<span data-ttu-id="8db8e-121">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="8db8e-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-122">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="8db8e-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-123">64</span><span class="sxs-lookup"><span data-stu-id="8db8e-123">64</span></span>

<span data-ttu-id="8db8e-124">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="8db8e-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-125">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="8db8e-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-126">65</span><span class="sxs-lookup"><span data-stu-id="8db8e-126">65</span></span>

<span data-ttu-id="8db8e-127">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="8db8e-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-128">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="8db8e-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-129">66</span><span class="sxs-lookup"><span data-stu-id="8db8e-129">66</span></span>

<span data-ttu-id="8db8e-130">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="8db8e-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-131">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="8db8e-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-132">67</span><span class="sxs-lookup"><span data-stu-id="8db8e-132">67</span></span>

<span data-ttu-id="8db8e-133">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="8db8e-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-134">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="8db8e-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-135">68</span><span class="sxs-lookup"><span data-stu-id="8db8e-135">68</span></span>

<span data-ttu-id="8db8e-136">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="8db8e-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-137">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="8db8e-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-138">69</span><span class="sxs-lookup"><span data-stu-id="8db8e-138">69</span></span>

<span data-ttu-id="8db8e-139">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="8db8e-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-140">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="8db8e-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-141">70</span><span class="sxs-lookup"><span data-stu-id="8db8e-141">70</span></span>

<span data-ttu-id="8db8e-142">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="8db8e-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-143">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="8db8e-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-144">71</span><span class="sxs-lookup"><span data-stu-id="8db8e-144">71</span></span>

<span data-ttu-id="8db8e-145">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="8db8e-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-146">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="8db8e-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-147">72</span><span class="sxs-lookup"><span data-stu-id="8db8e-147">72</span></span>

<span data-ttu-id="8db8e-148">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="8db8e-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-149">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="8db8e-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-150">73</span><span class="sxs-lookup"><span data-stu-id="8db8e-150">73</span></span>

<span data-ttu-id="8db8e-151">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="8db8e-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-152">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="8db8e-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-153">74</span><span class="sxs-lookup"><span data-stu-id="8db8e-153">74</span></span>

<span data-ttu-id="8db8e-154">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="8db8e-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-155">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="8db8e-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-156">75</span><span class="sxs-lookup"><span data-stu-id="8db8e-156">75</span></span>

<span data-ttu-id="8db8e-157">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="8db8e-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-158">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="8db8e-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-159">76</span><span class="sxs-lookup"><span data-stu-id="8db8e-159">76</span></span>

<span data-ttu-id="8db8e-160">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="8db8e-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-161">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="8db8e-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-162">77</span><span class="sxs-lookup"><span data-stu-id="8db8e-162">77</span></span>

<span data-ttu-id="8db8e-163">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="8db8e-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-164">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="8db8e-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-165">78</span><span class="sxs-lookup"><span data-stu-id="8db8e-165">78</span></span>

<span data-ttu-id="8db8e-166">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="8db8e-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-167">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="8db8e-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-168">79</span><span class="sxs-lookup"><span data-stu-id="8db8e-168">79</span></span>

<span data-ttu-id="8db8e-169">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="8db8e-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-170">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="8db8e-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-171">80</span><span class="sxs-lookup"><span data-stu-id="8db8e-171">80</span></span>

<span data-ttu-id="8db8e-172">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8db8e-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-173">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="8db8e-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-174">81</span><span class="sxs-lookup"><span data-stu-id="8db8e-174">81</span></span>

<span data-ttu-id="8db8e-175">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="8db8e-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-176">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="8db8e-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-177">82</span><span class="sxs-lookup"><span data-stu-id="8db8e-177">82</span></span>

<span data-ttu-id="8db8e-178">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="8db8e-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-179">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="8db8e-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-180">83</span><span class="sxs-lookup"><span data-stu-id="8db8e-180">83</span></span>

<span data-ttu-id="8db8e-181">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="8db8e-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-182">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="8db8e-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-183">84</span><span class="sxs-lookup"><span data-stu-id="8db8e-183">84</span></span>

<span data-ttu-id="8db8e-184">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="8db8e-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-185">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="8db8e-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-186">85</span><span class="sxs-lookup"><span data-stu-id="8db8e-186">85</span></span>

<span data-ttu-id="8db8e-187">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="8db8e-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-188">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="8db8e-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-189">86</span><span class="sxs-lookup"><span data-stu-id="8db8e-189">86</span></span>

<span data-ttu-id="8db8e-190">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="8db8e-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-191">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="8db8e-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-192">87</span><span class="sxs-lookup"><span data-stu-id="8db8e-192">87</span></span>

<span data-ttu-id="8db8e-193">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="8db8e-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-194">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="8db8e-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-195">88</span><span class="sxs-lookup"><span data-stu-id="8db8e-195">88</span></span>

<span data-ttu-id="8db8e-196">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="8db8e-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-197">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="8db8e-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-198">89</span><span class="sxs-lookup"><span data-stu-id="8db8e-198">89</span></span>

<span data-ttu-id="8db8e-199">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="8db8e-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-200">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="8db8e-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-201">90</span><span class="sxs-lookup"><span data-stu-id="8db8e-201">90</span></span>

<span data-ttu-id="8db8e-202">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="8db8e-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-203">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="8db8e-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-204">91</span><span class="sxs-lookup"><span data-stu-id="8db8e-204">91</span></span>

<span data-ttu-id="8db8e-205">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="8db8e-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-206">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="8db8e-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-207">92</span><span class="sxs-lookup"><span data-stu-id="8db8e-207">92</span></span>

<span data-ttu-id="8db8e-208">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="8db8e-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-209">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="8db8e-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-210">93</span><span class="sxs-lookup"><span data-stu-id="8db8e-210">93</span></span>

<span data-ttu-id="8db8e-211">Já existe.</span><span class="sxs-lookup"><span data-stu-id="8db8e-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-212">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="8db8e-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-213">94</span><span class="sxs-lookup"><span data-stu-id="8db8e-213">94</span></span>

<span data-ttu-id="8db8e-214">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="8db8e-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-215">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="8db8e-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-216">95</span><span class="sxs-lookup"><span data-stu-id="8db8e-216">95</span></span>

<span data-ttu-id="8db8e-217">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="8db8e-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-218">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="8db8e-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-219">96</span><span class="sxs-lookup"><span data-stu-id="8db8e-219">96</span></span>

<span data-ttu-id="8db8e-220">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="8db8e-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-221">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="8db8e-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-222">97</span><span class="sxs-lookup"><span data-stu-id="8db8e-222">97</span></span>

<span data-ttu-id="8db8e-223">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="8db8e-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-224">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="8db8e-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-225">98</span><span class="sxs-lookup"><span data-stu-id="8db8e-225">98</span></span>

<span data-ttu-id="8db8e-226">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="8db8e-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-227">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="8db8e-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-228">100</span><span class="sxs-lookup"><span data-stu-id="8db8e-228">100</span></span>

<span data-ttu-id="8db8e-229">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="8db8e-229">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8db8e-230">**Outras**</span><span class="sxs-lookup"><span data-stu-id="8db8e-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8db8e-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="8db8e-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8db8e-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="8db8e-232">Remarks</span></span>

<span data-ttu-id="8db8e-233">Esse método não limpa nenhum gateway padrão estático presente no computador.</span><span class="sxs-lookup"><span data-stu-id="8db8e-233">This method does not clears any static default gateways present on the machine.</span></span>

## <a name="examples"></a><span data-ttu-id="8db8e-234">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8db8e-234">Examples</span></span>

<span data-ttu-id="8db8e-235">O exemplo de código [Ativar DHCP e atribuir servidores DNS](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) do VBScript na galeria do TechNet usa o EnableDhcp para habilitar o DHCP e atribuir servidores DNS a um computador.</span><span class="sxs-lookup"><span data-stu-id="8db8e-235">The [Enable DHCP and Assign DNS Servers](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) VBScript code sample on TechNet Gallery uses EnableDHCP to enable DHCP and assign DNS servers to a computer.</span></span>

<span data-ttu-id="8db8e-236">O exemplo de código VBScript a seguir demonstra como habilitar o uso do DHCP em uma instância do [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="8db8e-236">The following VBScript code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="8db8e-237">Nesse caso, especificamos o adaptador com um índice de 0.</span><span class="sxs-lookup"><span data-stu-id="8db8e-237">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="8db8e-238">O índice correto deve ser selecionado em instâncias do Win32 \_ adaptador para outras interfaces.</span><span class="sxs-lookup"><span data-stu-id="8db8e-238">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="8db8e-239">Com suporte apenas em plataformas NT.</span><span class="sxs-lookup"><span data-stu-id="8db8e-239">Supported on NT platforms only.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=0")

RetVal = Adapter.EnableDHCP()

if RetVal = 0 then 
 WScript.Echo "DHCP Enabled"
else 
 WScript.Echo "DHCP enable failed"
end if
```



<span data-ttu-id="8db8e-240">O exemplo de código Perl a seguir demonstra como habilitar o uso do DHCP em uma instância do [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="8db8e-240">The following Perl code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="8db8e-241">Nesse caso, especificamos o adaptador com um índice de 0.</span><span class="sxs-lookup"><span data-stu-id="8db8e-241">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="8db8e-242">O índice correto deve ser selecionado em instâncias do Win32 \_ adaptador para outras interfaces.</span><span class="sxs-lookup"><span data-stu-id="8db8e-242">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="8db8e-243">Com suporte apenas em plataformas NT.</span><span class="sxs-lookup"><span data-stu-id="8db8e-243">Supported on NT platforms only.</span></span>

 


```
use strict;
use Win32::OLE;

my ( $Adapter, $RetVal );

eval { $Adapter = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
       Get("Win32_NetworkAdapterConfiguration=0"); };
unless ($@)
{
 print "\n";
 $RetVal = $Adapter->EnableDHCP();
 if ( $RetVal == 0)
 {
  print "DHCP Enabled\n";
 }
 else
 {
  print "DHCP enable failed\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="8db8e-244">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8db8e-244">Requirements</span></span>



| <span data-ttu-id="8db8e-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="8db8e-245">Requirement</span></span> | <span data-ttu-id="8db8e-246">Valor</span><span class="sxs-lookup"><span data-stu-id="8db8e-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8db8e-247">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8db8e-247">Minimum supported client</span></span><br/> | <span data-ttu-id="8db8e-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8db8e-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8db8e-249">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8db8e-249">Minimum supported server</span></span><br/> | <span data-ttu-id="8db8e-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8db8e-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8db8e-251">Namespace</span><span class="sxs-lookup"><span data-stu-id="8db8e-251">Namespace</span></span><br/>                | <span data-ttu-id="8db8e-252">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8db8e-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8db8e-253">MOF</span><span class="sxs-lookup"><span data-stu-id="8db8e-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8db8e-254"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8db8e-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8db8e-255">DLL</span><span class="sxs-lookup"><span data-stu-id="8db8e-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8db8e-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8db8e-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8db8e-257">Confira também</span><span class="sxs-lookup"><span data-stu-id="8db8e-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db8e-258">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="8db8e-258">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8db8e-259">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="8db8e-259">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8db8e-260">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="8db8e-260">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8db8e-261">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="8db8e-261">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8db8e-262">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="8db8e-262">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

