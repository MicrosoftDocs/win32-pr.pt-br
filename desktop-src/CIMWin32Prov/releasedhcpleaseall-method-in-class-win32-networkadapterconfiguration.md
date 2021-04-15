---
description: O método estático da classe WMI ReleaseDHCPLeaseAll libera os endereços IP associados a todos os adaptadores de rede habilitados para DHCP.
ms.assetid: d9f83953-f3da-419d-8c84-649c39b4945e
ms.tgt_platform: multiple
title: Método ReleaseDHCPLeaseAll da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLeaseAll
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e7b1f7cf2f09fa20f7bf19b15e82f536ca0aa50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753978"
---
# <a name="releasedhcpleaseall-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="88ef5-103">Método ReleaseDHCPLeaseAll da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="88ef5-103">ReleaseDHCPLeaseAll method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="88ef5-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ReleaseDHCPLeaseAll** libera os endereços IP associados a todos os adaptadores de rede habilitados para DHCP.</span><span class="sxs-lookup"><span data-stu-id="88ef5-104">The **ReleaseDHCPLeaseAll** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method releases the IP addresses bound to all DHCP-enabled network adapters.</span></span>

> [!Note]  
> <span data-ttu-id="88ef5-105">Aviso se o DHCP estiver habilitado no sistema do computador local, a opção terminará todas as conexões TCP/IP do DHCP.</span><span class="sxs-lookup"><span data-stu-id="88ef5-105">Warning If DHCP is enabled on the local computer system, the option will terminate all DHCP TCP/IP connections.</span></span>

 

<span data-ttu-id="88ef5-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="88ef5-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="88ef5-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="88ef5-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="88ef5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88ef5-108">Syntax</span></span>


```mof
uint32 ReleaseDHCPLeaseAll();
```



## <a name="parameters"></a><span data-ttu-id="88ef5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88ef5-109">Parameters</span></span>

<span data-ttu-id="88ef5-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="88ef5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88ef5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88ef5-111">Return value</span></span>

<span data-ttu-id="88ef5-112">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="88ef5-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="88ef5-113">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="88ef5-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="88ef5-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="88ef5-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="88ef5-115">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="88ef5-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-116">0</span><span class="sxs-lookup"><span data-stu-id="88ef5-116">0</span></span>

<span data-ttu-id="88ef5-117">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="88ef5-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-118">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="88ef5-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-119">1</span><span class="sxs-lookup"><span data-stu-id="88ef5-119">1</span></span>

<span data-ttu-id="88ef5-120">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="88ef5-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-121">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="88ef5-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-122">64</span><span class="sxs-lookup"><span data-stu-id="88ef5-122">64</span></span>

<span data-ttu-id="88ef5-123">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="88ef5-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-124">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="88ef5-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-125">65</span><span class="sxs-lookup"><span data-stu-id="88ef5-125">65</span></span>

<span data-ttu-id="88ef5-126">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="88ef5-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-127">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="88ef5-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-128">66</span><span class="sxs-lookup"><span data-stu-id="88ef5-128">66</span></span>

<span data-ttu-id="88ef5-129">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="88ef5-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-130">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="88ef5-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-131">67</span><span class="sxs-lookup"><span data-stu-id="88ef5-131">67</span></span>

<span data-ttu-id="88ef5-132">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="88ef5-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-133">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="88ef5-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-134">68</span><span class="sxs-lookup"><span data-stu-id="88ef5-134">68</span></span>

<span data-ttu-id="88ef5-135">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="88ef5-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-136">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="88ef5-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-137">69</span><span class="sxs-lookup"><span data-stu-id="88ef5-137">69</span></span>

<span data-ttu-id="88ef5-138">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="88ef5-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-139">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="88ef5-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-140">70</span><span class="sxs-lookup"><span data-stu-id="88ef5-140">70</span></span>

<span data-ttu-id="88ef5-141">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="88ef5-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-142">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="88ef5-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-143">71</span><span class="sxs-lookup"><span data-stu-id="88ef5-143">71</span></span>

<span data-ttu-id="88ef5-144">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="88ef5-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-145">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="88ef5-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-146">72</span><span class="sxs-lookup"><span data-stu-id="88ef5-146">72</span></span>

<span data-ttu-id="88ef5-147">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="88ef5-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-148">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="88ef5-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-149">73</span><span class="sxs-lookup"><span data-stu-id="88ef5-149">73</span></span>

<span data-ttu-id="88ef5-150">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="88ef5-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-151">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="88ef5-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-152">74</span><span class="sxs-lookup"><span data-stu-id="88ef5-152">74</span></span>

<span data-ttu-id="88ef5-153">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="88ef5-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-154">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="88ef5-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-155">75</span><span class="sxs-lookup"><span data-stu-id="88ef5-155">75</span></span>

<span data-ttu-id="88ef5-156">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="88ef5-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-157">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="88ef5-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-158">76</span><span class="sxs-lookup"><span data-stu-id="88ef5-158">76</span></span>

<span data-ttu-id="88ef5-159">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="88ef5-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-160">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="88ef5-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-161">77</span><span class="sxs-lookup"><span data-stu-id="88ef5-161">77</span></span>

<span data-ttu-id="88ef5-162">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="88ef5-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-163">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="88ef5-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-164">78</span><span class="sxs-lookup"><span data-stu-id="88ef5-164">78</span></span>

<span data-ttu-id="88ef5-165">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="88ef5-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-166">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="88ef5-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-167">79</span><span class="sxs-lookup"><span data-stu-id="88ef5-167">79</span></span>

<span data-ttu-id="88ef5-168">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="88ef5-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-169">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="88ef5-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-170">80</span><span class="sxs-lookup"><span data-stu-id="88ef5-170">80</span></span>

<span data-ttu-id="88ef5-171">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="88ef5-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-172">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="88ef5-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-173">81</span><span class="sxs-lookup"><span data-stu-id="88ef5-173">81</span></span>

<span data-ttu-id="88ef5-174">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="88ef5-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-175">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="88ef5-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-176">82</span><span class="sxs-lookup"><span data-stu-id="88ef5-176">82</span></span>

<span data-ttu-id="88ef5-177">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="88ef5-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-178">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="88ef5-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-179">83</span><span class="sxs-lookup"><span data-stu-id="88ef5-179">83</span></span>

<span data-ttu-id="88ef5-180">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="88ef5-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-181">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="88ef5-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-182">84</span><span class="sxs-lookup"><span data-stu-id="88ef5-182">84</span></span>

<span data-ttu-id="88ef5-183">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="88ef5-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-184">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="88ef5-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-185">85</span><span class="sxs-lookup"><span data-stu-id="88ef5-185">85</span></span>

<span data-ttu-id="88ef5-186">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="88ef5-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-187">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="88ef5-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-188">86</span><span class="sxs-lookup"><span data-stu-id="88ef5-188">86</span></span>

<span data-ttu-id="88ef5-189">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="88ef5-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-190">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="88ef5-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-191">87</span><span class="sxs-lookup"><span data-stu-id="88ef5-191">87</span></span>

<span data-ttu-id="88ef5-192">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="88ef5-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-193">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="88ef5-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-194">88</span><span class="sxs-lookup"><span data-stu-id="88ef5-194">88</span></span>

<span data-ttu-id="88ef5-195">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="88ef5-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-196">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="88ef5-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-197">89</span><span class="sxs-lookup"><span data-stu-id="88ef5-197">89</span></span>

<span data-ttu-id="88ef5-198">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="88ef5-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-199">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="88ef5-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-200">90</span><span class="sxs-lookup"><span data-stu-id="88ef5-200">90</span></span>

<span data-ttu-id="88ef5-201">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="88ef5-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-202">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="88ef5-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-203">91</span><span class="sxs-lookup"><span data-stu-id="88ef5-203">91</span></span>

<span data-ttu-id="88ef5-204">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="88ef5-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-205">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="88ef5-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-206">92</span><span class="sxs-lookup"><span data-stu-id="88ef5-206">92</span></span>

<span data-ttu-id="88ef5-207">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="88ef5-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-208">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="88ef5-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-209">93</span><span class="sxs-lookup"><span data-stu-id="88ef5-209">93</span></span>

<span data-ttu-id="88ef5-210">Já existe.</span><span class="sxs-lookup"><span data-stu-id="88ef5-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-211">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="88ef5-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-212">94</span><span class="sxs-lookup"><span data-stu-id="88ef5-212">94</span></span>

<span data-ttu-id="88ef5-213">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="88ef5-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-214">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="88ef5-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-215">95</span><span class="sxs-lookup"><span data-stu-id="88ef5-215">95</span></span>

<span data-ttu-id="88ef5-216">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="88ef5-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-217">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="88ef5-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-218">96</span><span class="sxs-lookup"><span data-stu-id="88ef5-218">96</span></span>

<span data-ttu-id="88ef5-219">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="88ef5-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-220">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="88ef5-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-221">97</span><span class="sxs-lookup"><span data-stu-id="88ef5-221">97</span></span>

<span data-ttu-id="88ef5-222">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="88ef5-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-223">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="88ef5-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-224">98</span><span class="sxs-lookup"><span data-stu-id="88ef5-224">98</span></span>

<span data-ttu-id="88ef5-225">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="88ef5-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-226">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="88ef5-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-227">100</span><span class="sxs-lookup"><span data-stu-id="88ef5-227">100</span></span>

<span data-ttu-id="88ef5-228">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="88ef5-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-229">**Outras**</span><span class="sxs-lookup"><span data-stu-id="88ef5-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="88ef5-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="88ef5-230">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="88ef5-231">Exemplos</span><span class="sxs-lookup"><span data-stu-id="88ef5-231">Examples</span></span>

<span data-ttu-id="88ef5-232">O exemplo de código VBScript a seguir libera Todas as concessões DHCP atualmente em uso em um computador.</span><span class="sxs-lookup"><span data-stu-id="88ef5-232">The following VBScript code sample releases all the DHCP leases currently in use on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
objNetworkSettings.ReleaseDHCPLeaseAll() 
```



## <a name="requirements"></a><span data-ttu-id="88ef5-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88ef5-233">Requirements</span></span>



| <span data-ttu-id="88ef5-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="88ef5-234">Requirement</span></span> | <span data-ttu-id="88ef5-235">Valor</span><span class="sxs-lookup"><span data-stu-id="88ef5-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88ef5-236">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88ef5-236">Minimum supported client</span></span><br/> | <span data-ttu-id="88ef5-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88ef5-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88ef5-238">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88ef5-238">Minimum supported server</span></span><br/> | <span data-ttu-id="88ef5-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88ef5-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88ef5-240">Namespace</span><span class="sxs-lookup"><span data-stu-id="88ef5-240">Namespace</span></span><br/>                | <span data-ttu-id="88ef5-241">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="88ef5-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88ef5-242">MOF</span><span class="sxs-lookup"><span data-stu-id="88ef5-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88ef5-243"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88ef5-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88ef5-244">DLL</span><span class="sxs-lookup"><span data-stu-id="88ef5-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88ef5-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88ef5-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ef5-246">Confira também</span><span class="sxs-lookup"><span data-stu-id="88ef5-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ef5-247">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="88ef5-247">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="88ef5-248">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="88ef5-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="88ef5-249">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="88ef5-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="88ef5-250">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="88ef5-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="88ef5-251">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="88ef5-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

