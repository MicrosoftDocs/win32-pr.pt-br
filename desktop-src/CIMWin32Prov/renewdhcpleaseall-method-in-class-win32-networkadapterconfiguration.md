---
description: O método estático da classe WMI RenewDHCPLeaseAll renova os endereços IP em todos os adaptadores de rede habilitados para DHCP.
ms.assetid: cbe0a607-cb3b-47c4-ad3a-c4fa03fe688c
ms.tgt_platform: multiple
title: Método RenewDHCPLeaseAll da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.RenewDHCPLeaseAll
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3ed94b44a629f619617186415ed3822387c6967
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753582"
---
# <a name="renewdhcpleaseall-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="13cf7-103">Método RenewDHCPLeaseAll da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="13cf7-103">RenewDHCPLeaseAll method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="13cf7-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenewDHCPLeaseAll** renova os endereços IP em todos os adaptadores de rede habilitados para DHCP.</span><span class="sxs-lookup"><span data-stu-id="13cf7-104">The **RenewDHCPLeaseAll** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method renews the IP addresses on all DHCP-enabled network adapters.</span></span>

<span data-ttu-id="13cf7-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="13cf7-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="13cf7-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="13cf7-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="13cf7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13cf7-107">Syntax</span></span>


```mof
uint32 RenewDHCPLeaseAll();
```



## <a name="parameters"></a><span data-ttu-id="13cf7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13cf7-108">Parameters</span></span>

<span data-ttu-id="13cf7-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="13cf7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13cf7-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="13cf7-110">Return value</span></span>

<span data-ttu-id="13cf7-111">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="13cf7-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="13cf7-112">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="13cf7-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="13cf7-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="13cf7-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="13cf7-114">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="13cf7-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-115">0</span><span class="sxs-lookup"><span data-stu-id="13cf7-115">0</span></span>

<span data-ttu-id="13cf7-116">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="13cf7-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-117">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="13cf7-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-118">1</span><span class="sxs-lookup"><span data-stu-id="13cf7-118">1</span></span>

<span data-ttu-id="13cf7-119">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="13cf7-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-120">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="13cf7-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-121">64</span><span class="sxs-lookup"><span data-stu-id="13cf7-121">64</span></span>

<span data-ttu-id="13cf7-122">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="13cf7-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-123">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="13cf7-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-124">65</span><span class="sxs-lookup"><span data-stu-id="13cf7-124">65</span></span>

<span data-ttu-id="13cf7-125">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="13cf7-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-126">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="13cf7-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-127">66</span><span class="sxs-lookup"><span data-stu-id="13cf7-127">66</span></span>

<span data-ttu-id="13cf7-128">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="13cf7-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-129">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="13cf7-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-130">67</span><span class="sxs-lookup"><span data-stu-id="13cf7-130">67</span></span>

<span data-ttu-id="13cf7-131">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="13cf7-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-132">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="13cf7-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-133">68</span><span class="sxs-lookup"><span data-stu-id="13cf7-133">68</span></span>

<span data-ttu-id="13cf7-134">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="13cf7-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-135">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="13cf7-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-136">69</span><span class="sxs-lookup"><span data-stu-id="13cf7-136">69</span></span>

<span data-ttu-id="13cf7-137">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="13cf7-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-138">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="13cf7-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-139">70</span><span class="sxs-lookup"><span data-stu-id="13cf7-139">70</span></span>

<span data-ttu-id="13cf7-140">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="13cf7-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-141">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="13cf7-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-142">71</span><span class="sxs-lookup"><span data-stu-id="13cf7-142">71</span></span>

<span data-ttu-id="13cf7-143">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="13cf7-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-144">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="13cf7-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-145">72</span><span class="sxs-lookup"><span data-stu-id="13cf7-145">72</span></span>

<span data-ttu-id="13cf7-146">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="13cf7-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-147">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="13cf7-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-148">73</span><span class="sxs-lookup"><span data-stu-id="13cf7-148">73</span></span>

<span data-ttu-id="13cf7-149">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="13cf7-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-150">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="13cf7-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-151">74</span><span class="sxs-lookup"><span data-stu-id="13cf7-151">74</span></span>

<span data-ttu-id="13cf7-152">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="13cf7-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-153">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="13cf7-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-154">75</span><span class="sxs-lookup"><span data-stu-id="13cf7-154">75</span></span>

<span data-ttu-id="13cf7-155">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="13cf7-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-156">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="13cf7-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-157">76</span><span class="sxs-lookup"><span data-stu-id="13cf7-157">76</span></span>

<span data-ttu-id="13cf7-158">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="13cf7-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-159">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="13cf7-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-160">77</span><span class="sxs-lookup"><span data-stu-id="13cf7-160">77</span></span>

<span data-ttu-id="13cf7-161">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="13cf7-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-162">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="13cf7-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-163">78</span><span class="sxs-lookup"><span data-stu-id="13cf7-163">78</span></span>

<span data-ttu-id="13cf7-164">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="13cf7-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-165">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="13cf7-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-166">79</span><span class="sxs-lookup"><span data-stu-id="13cf7-166">79</span></span>

<span data-ttu-id="13cf7-167">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="13cf7-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-168">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="13cf7-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-169">80</span><span class="sxs-lookup"><span data-stu-id="13cf7-169">80</span></span>

<span data-ttu-id="13cf7-170">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="13cf7-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-171">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="13cf7-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-172">81</span><span class="sxs-lookup"><span data-stu-id="13cf7-172">81</span></span>

<span data-ttu-id="13cf7-173">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="13cf7-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-174">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="13cf7-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-175">82</span><span class="sxs-lookup"><span data-stu-id="13cf7-175">82</span></span>

<span data-ttu-id="13cf7-176">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="13cf7-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-177">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="13cf7-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-178">83</span><span class="sxs-lookup"><span data-stu-id="13cf7-178">83</span></span>

<span data-ttu-id="13cf7-179">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="13cf7-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-180">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="13cf7-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-181">84</span><span class="sxs-lookup"><span data-stu-id="13cf7-181">84</span></span>

<span data-ttu-id="13cf7-182">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="13cf7-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-183">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="13cf7-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-184">85</span><span class="sxs-lookup"><span data-stu-id="13cf7-184">85</span></span>

<span data-ttu-id="13cf7-185">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="13cf7-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-186">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="13cf7-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-187">86</span><span class="sxs-lookup"><span data-stu-id="13cf7-187">86</span></span>

<span data-ttu-id="13cf7-188">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="13cf7-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-189">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="13cf7-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-190">87</span><span class="sxs-lookup"><span data-stu-id="13cf7-190">87</span></span>

<span data-ttu-id="13cf7-191">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="13cf7-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-192">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="13cf7-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-193">88</span><span class="sxs-lookup"><span data-stu-id="13cf7-193">88</span></span>

<span data-ttu-id="13cf7-194">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="13cf7-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-195">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="13cf7-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-196">89</span><span class="sxs-lookup"><span data-stu-id="13cf7-196">89</span></span>

<span data-ttu-id="13cf7-197">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="13cf7-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-198">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="13cf7-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-199">90</span><span class="sxs-lookup"><span data-stu-id="13cf7-199">90</span></span>

<span data-ttu-id="13cf7-200">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="13cf7-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-201">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="13cf7-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-202">91</span><span class="sxs-lookup"><span data-stu-id="13cf7-202">91</span></span>

<span data-ttu-id="13cf7-203">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="13cf7-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-204">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="13cf7-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-205">92</span><span class="sxs-lookup"><span data-stu-id="13cf7-205">92</span></span>

<span data-ttu-id="13cf7-206">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="13cf7-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-207">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="13cf7-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-208">93</span><span class="sxs-lookup"><span data-stu-id="13cf7-208">93</span></span>

<span data-ttu-id="13cf7-209">Já existe.</span><span class="sxs-lookup"><span data-stu-id="13cf7-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-210">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="13cf7-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-211">94</span><span class="sxs-lookup"><span data-stu-id="13cf7-211">94</span></span>

<span data-ttu-id="13cf7-212">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="13cf7-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-213">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="13cf7-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-214">95</span><span class="sxs-lookup"><span data-stu-id="13cf7-214">95</span></span>

<span data-ttu-id="13cf7-215">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="13cf7-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-216">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="13cf7-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-217">96</span><span class="sxs-lookup"><span data-stu-id="13cf7-217">96</span></span>

<span data-ttu-id="13cf7-218">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="13cf7-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-219">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="13cf7-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-220">97</span><span class="sxs-lookup"><span data-stu-id="13cf7-220">97</span></span>

<span data-ttu-id="13cf7-221">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="13cf7-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-222">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="13cf7-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-223">98</span><span class="sxs-lookup"><span data-stu-id="13cf7-223">98</span></span>

<span data-ttu-id="13cf7-224">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="13cf7-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-225">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="13cf7-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-226">100</span><span class="sxs-lookup"><span data-stu-id="13cf7-226">100</span></span>

<span data-ttu-id="13cf7-227">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="13cf7-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="13cf7-228">**Outras**</span><span class="sxs-lookup"><span data-stu-id="13cf7-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="13cf7-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="13cf7-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13cf7-230">Comentários</span><span class="sxs-lookup"><span data-stu-id="13cf7-230">Remarks</span></span>

<span data-ttu-id="13cf7-231">A concessão para o endereço IP atribuído por um servidor DHCP tem uma data de expiração que o cliente deve renovar se pretender continuar usando o endereço IP atribuído.</span><span class="sxs-lookup"><span data-stu-id="13cf7-231">The lease for the IP address assigned by a DHCP server has an expiration date that the client must renew if it intends to continue use of the assigned IP address.</span></span>

## <a name="examples"></a><span data-ttu-id="13cf7-232">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13cf7-232">Examples</span></span>

<span data-ttu-id="13cf7-233">O exemplo do VBScript [renovar todas as concessões DHCP](https://Gallery.TechNet.Microsoft.Com/b29171b8-21b0-492a-b0fe-67e650adca99) na galeria do TechNet renova todas as concessões DHCP em uso no momento em um computador.</span><span class="sxs-lookup"><span data-stu-id="13cf7-233">The [Renew All DHCP Leases](https://Gallery.TechNet.Microsoft.Com/b29171b8-21b0-492a-b0fe-67e650adca99) VBScript example on TechNet Gallery renews all the DHCP leases currently in use on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="13cf7-234">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13cf7-234">Requirements</span></span>



| <span data-ttu-id="13cf7-235">Requisito</span><span class="sxs-lookup"><span data-stu-id="13cf7-235">Requirement</span></span> | <span data-ttu-id="13cf7-236">Valor</span><span class="sxs-lookup"><span data-stu-id="13cf7-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13cf7-237">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13cf7-237">Minimum supported client</span></span><br/> | <span data-ttu-id="13cf7-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13cf7-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13cf7-239">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13cf7-239">Minimum supported server</span></span><br/> | <span data-ttu-id="13cf7-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13cf7-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13cf7-241">Namespace</span><span class="sxs-lookup"><span data-stu-id="13cf7-241">Namespace</span></span><br/>                | <span data-ttu-id="13cf7-242">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="13cf7-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="13cf7-243">MOF</span><span class="sxs-lookup"><span data-stu-id="13cf7-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13cf7-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13cf7-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="13cf7-245">DLL</span><span class="sxs-lookup"><span data-stu-id="13cf7-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13cf7-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13cf7-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13cf7-247">Confira também</span><span class="sxs-lookup"><span data-stu-id="13cf7-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13cf7-248">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="13cf7-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="13cf7-249">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="13cf7-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="13cf7-250">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="13cf7-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="13cf7-251">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="13cf7-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="13cf7-252">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="13cf7-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

