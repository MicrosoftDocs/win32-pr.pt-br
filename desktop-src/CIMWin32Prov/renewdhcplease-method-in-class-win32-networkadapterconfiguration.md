---
description: O método de classe WMI RenewDHCPLease renova o endereço IP em adaptadores de rede específicos habilitados para DHCP.
ms.assetid: b6e5d1fb-db3f-4491-bbac-46b1f2e7206e
ms.tgt_platform: multiple
title: Método RenewDHCPLease da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.RenewDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4603f013c6b4c2c80edd555608b5f59325b6a6d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010292"
---
# <a name="renewdhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="e751c-103">Método RenewDHCPLease da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="e751c-103">RenewDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="e751c-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenewDHCPLease** renova o endereço IP em adaptadores de rede específicos habilitados para DHCP.</span><span class="sxs-lookup"><span data-stu-id="e751c-104">The **RenewDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renews the IP address on specific DHCP-enabled network adapters.</span></span>

<span data-ttu-id="e751c-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="e751c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e751c-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e751c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e751c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e751c-107">Syntax</span></span>


```mof
uint32 RenewDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="e751c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e751c-108">Parameters</span></span>

<span data-ttu-id="e751c-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e751c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e751c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e751c-110">Return value</span></span>

<span data-ttu-id="e751c-111">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="e751c-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="e751c-112">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e751c-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e751c-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e751c-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e751c-114">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="e751c-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-115">0</span><span class="sxs-lookup"><span data-stu-id="e751c-115">0</span></span>

<span data-ttu-id="e751c-116">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="e751c-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-117">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="e751c-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-118">1</span><span class="sxs-lookup"><span data-stu-id="e751c-118">1</span></span>

<span data-ttu-id="e751c-119">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="e751c-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-120">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="e751c-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-121">64</span><span class="sxs-lookup"><span data-stu-id="e751c-121">64</span></span>

<span data-ttu-id="e751c-122">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="e751c-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-123">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="e751c-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-124">65</span><span class="sxs-lookup"><span data-stu-id="e751c-124">65</span></span>

<span data-ttu-id="e751c-125">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="e751c-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-126">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="e751c-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-127">66</span><span class="sxs-lookup"><span data-stu-id="e751c-127">66</span></span>

<span data-ttu-id="e751c-128">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="e751c-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-129">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="e751c-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-130">67</span><span class="sxs-lookup"><span data-stu-id="e751c-130">67</span></span>

<span data-ttu-id="e751c-131">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="e751c-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-132">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="e751c-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-133">68</span><span class="sxs-lookup"><span data-stu-id="e751c-133">68</span></span>

<span data-ttu-id="e751c-134">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="e751c-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-135">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="e751c-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-136">69</span><span class="sxs-lookup"><span data-stu-id="e751c-136">69</span></span>

<span data-ttu-id="e751c-137">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="e751c-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-138">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="e751c-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-139">70</span><span class="sxs-lookup"><span data-stu-id="e751c-139">70</span></span>

<span data-ttu-id="e751c-140">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="e751c-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-141">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="e751c-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-142">71</span><span class="sxs-lookup"><span data-stu-id="e751c-142">71</span></span>

<span data-ttu-id="e751c-143">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="e751c-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-144">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="e751c-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-145">72</span><span class="sxs-lookup"><span data-stu-id="e751c-145">72</span></span>

<span data-ttu-id="e751c-146">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="e751c-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-147">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="e751c-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-148">73</span><span class="sxs-lookup"><span data-stu-id="e751c-148">73</span></span>

<span data-ttu-id="e751c-149">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="e751c-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-150">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="e751c-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-151">74</span><span class="sxs-lookup"><span data-stu-id="e751c-151">74</span></span>

<span data-ttu-id="e751c-152">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="e751c-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-153">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="e751c-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-154">75</span><span class="sxs-lookup"><span data-stu-id="e751c-154">75</span></span>

<span data-ttu-id="e751c-155">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="e751c-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-156">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="e751c-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-157">76</span><span class="sxs-lookup"><span data-stu-id="e751c-157">76</span></span>

<span data-ttu-id="e751c-158">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="e751c-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-159">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="e751c-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-160">77</span><span class="sxs-lookup"><span data-stu-id="e751c-160">77</span></span>

<span data-ttu-id="e751c-161">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="e751c-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-162">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="e751c-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-163">78</span><span class="sxs-lookup"><span data-stu-id="e751c-163">78</span></span>

<span data-ttu-id="e751c-164">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e751c-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-165">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="e751c-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-166">79</span><span class="sxs-lookup"><span data-stu-id="e751c-166">79</span></span>

<span data-ttu-id="e751c-167">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="e751c-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-168">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="e751c-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-169">80</span><span class="sxs-lookup"><span data-stu-id="e751c-169">80</span></span>

<span data-ttu-id="e751c-170">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e751c-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-171">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="e751c-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-172">81</span><span class="sxs-lookup"><span data-stu-id="e751c-172">81</span></span>

<span data-ttu-id="e751c-173">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="e751c-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-174">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="e751c-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-175">82</span><span class="sxs-lookup"><span data-stu-id="e751c-175">82</span></span>

<span data-ttu-id="e751c-176">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="e751c-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-177">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="e751c-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-178">83</span><span class="sxs-lookup"><span data-stu-id="e751c-178">83</span></span>

<span data-ttu-id="e751c-179">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="e751c-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-180">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="e751c-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-181">84</span><span class="sxs-lookup"><span data-stu-id="e751c-181">84</span></span>

<span data-ttu-id="e751c-182">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="e751c-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-183">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="e751c-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-184">85</span><span class="sxs-lookup"><span data-stu-id="e751c-184">85</span></span>

<span data-ttu-id="e751c-185">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="e751c-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-186">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="e751c-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-187">86</span><span class="sxs-lookup"><span data-stu-id="e751c-187">86</span></span>

<span data-ttu-id="e751c-188">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="e751c-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-189">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="e751c-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-190">87</span><span class="sxs-lookup"><span data-stu-id="e751c-190">87</span></span>

<span data-ttu-id="e751c-191">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="e751c-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-192">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="e751c-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-193">88</span><span class="sxs-lookup"><span data-stu-id="e751c-193">88</span></span>

<span data-ttu-id="e751c-194">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="e751c-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-195">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="e751c-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-196">89</span><span class="sxs-lookup"><span data-stu-id="e751c-196">89</span></span>

<span data-ttu-id="e751c-197">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="e751c-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-198">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="e751c-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-199">90</span><span class="sxs-lookup"><span data-stu-id="e751c-199">90</span></span>

<span data-ttu-id="e751c-200">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="e751c-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-201">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="e751c-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-202">91</span><span class="sxs-lookup"><span data-stu-id="e751c-202">91</span></span>

<span data-ttu-id="e751c-203">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="e751c-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-204">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="e751c-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-205">92</span><span class="sxs-lookup"><span data-stu-id="e751c-205">92</span></span>

<span data-ttu-id="e751c-206">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="e751c-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-207">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="e751c-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-208">93</span><span class="sxs-lookup"><span data-stu-id="e751c-208">93</span></span>

<span data-ttu-id="e751c-209">Já existe.</span><span class="sxs-lookup"><span data-stu-id="e751c-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-210">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="e751c-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-211">94</span><span class="sxs-lookup"><span data-stu-id="e751c-211">94</span></span>

<span data-ttu-id="e751c-212">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="e751c-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-213">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="e751c-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-214">95</span><span class="sxs-lookup"><span data-stu-id="e751c-214">95</span></span>

<span data-ttu-id="e751c-215">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="e751c-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-216">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="e751c-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-217">96</span><span class="sxs-lookup"><span data-stu-id="e751c-217">96</span></span>

<span data-ttu-id="e751c-218">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="e751c-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-219">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="e751c-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-220">97</span><span class="sxs-lookup"><span data-stu-id="e751c-220">97</span></span>

<span data-ttu-id="e751c-221">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="e751c-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-222">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="e751c-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-223">98</span><span class="sxs-lookup"><span data-stu-id="e751c-223">98</span></span>

<span data-ttu-id="e751c-224">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="e751c-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-225">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="e751c-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-226">100</span><span class="sxs-lookup"><span data-stu-id="e751c-226">100</span></span>

<span data-ttu-id="e751c-227">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="e751c-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e751c-228">**Outras**</span><span class="sxs-lookup"><span data-stu-id="e751c-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="e751c-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="e751c-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e751c-230">Comentários</span><span class="sxs-lookup"><span data-stu-id="e751c-230">Remarks</span></span>

<span data-ttu-id="e751c-231">A concessão para o endereço IP atribuído por um servidor DHCP tem uma data de expiração que o cliente deve renovar se pretender continuar usando o endereço IP atribuído.</span><span class="sxs-lookup"><span data-stu-id="e751c-231">The lease for the IP address assigned by a DHCP server has an expiration date that the client must renew if it intends to continue use of the assigned IP address.</span></span>

## <a name="examples"></a><span data-ttu-id="e751c-232">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e751c-232">Examples</span></span>

<span data-ttu-id="e751c-233">O exemplo de [lançamento renovar IP endereços usando PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell na galeria do TechNet usa o **RenewDHCPLease** para liberar e renovar um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="e751c-233">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **RenewDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="e751c-234">A amostra [renovar a concessão DHCP para um adaptador de rede](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) do VBScript na galeria do TechNet usa o **RenewDHCPLease** para renovar a concessão DHCP para cada adaptador de rede associado a TCP/IP em um computador.</span><span class="sxs-lookup"><span data-stu-id="e751c-234">The [Renew the DHCP Lease for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) VBScript sample on TechNet Gallery uses **RenewDHCPLease** to renew the DHCP lease for each TCP/IP-bound network adapter in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e751c-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e751c-235">Requirements</span></span>



| <span data-ttu-id="e751c-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="e751c-236">Requirement</span></span> | <span data-ttu-id="e751c-237">Valor</span><span class="sxs-lookup"><span data-stu-id="e751c-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e751c-238">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e751c-238">Minimum supported client</span></span><br/> | <span data-ttu-id="e751c-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e751c-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e751c-240">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e751c-240">Minimum supported server</span></span><br/> | <span data-ttu-id="e751c-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e751c-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e751c-242">Namespace</span><span class="sxs-lookup"><span data-stu-id="e751c-242">Namespace</span></span><br/>                | <span data-ttu-id="e751c-243">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e751c-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e751c-244">MOF</span><span class="sxs-lookup"><span data-stu-id="e751c-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e751c-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e751c-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e751c-246">DLL</span><span class="sxs-lookup"><span data-stu-id="e751c-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e751c-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e751c-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e751c-248">Confira também</span><span class="sxs-lookup"><span data-stu-id="e751c-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e751c-249">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="e751c-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e751c-250">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="e751c-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="e751c-251">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="e751c-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="e751c-252">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="e751c-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="e751c-253">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="e751c-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

