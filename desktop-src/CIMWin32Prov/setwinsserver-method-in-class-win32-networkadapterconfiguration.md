---
description: O método de classe WMI SetWINSServer define os servidores WINS (Windows Internet Serviço de Nomenclatura) primários e secundários neste adaptador de rede associado a TCP/IP. Esse método é aplicado independentemente do adaptador de rede.
ms.assetid: fa8ce436-b67e-4975-a5c5-1a7d6aab4c8e
ms.tgt_platform: multiple
title: Método SetWINSServer da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetWINSServer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49bfb0103a7d9cbbd6ea3faa0e1a868bac7b0196
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751800"
---
# <a name="setwinsserver-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="4efc1-104">Método SetWINSServer da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="4efc1-104">SetWINSServer method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="4efc1-105">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetWINSServer** define os servidores WINS (Windows Internet serviço de nomenclatura) primários e secundários neste adaptador de rede associado a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4efc1-105">The **SetWINSServer** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span> <span data-ttu-id="4efc1-106">Esse método é aplicado independentemente do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="4efc1-106">This method is applied independently of the network adapter.</span></span>

<span data-ttu-id="4efc1-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4efc1-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4efc1-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4efc1-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4efc1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4efc1-109">Syntax</span></span>


```mof
uint32 SetWINSServer(
  [in] string WINSPrimaryServer,
  [in] string WINSSecondaryServer
);
```



## <a name="parameters"></a><span data-ttu-id="4efc1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4efc1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4efc1-111">*WINSPrimaryServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4efc1-111">*WINSPrimaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-112">Endereço IP do servidor WINS primário.</span><span class="sxs-lookup"><span data-stu-id="4efc1-112">IP address of the primary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="4efc1-113">Sempre verifique a validade desse endereço IP quando ele for de uma fonte desconhecida ou uma fonte na qual você não confia.</span><span class="sxs-lookup"><span data-stu-id="4efc1-113">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> <dt>

<span data-ttu-id="4efc1-114">*WINSSecondaryServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4efc1-114">*WINSSecondaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-115">Endereço IP do servidor WINS secundário.</span><span class="sxs-lookup"><span data-stu-id="4efc1-115">IP address of the secondary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="4efc1-116">Sempre verifique a validade desse endereço IP quando ele for de uma fonte desconhecida ou uma fonte na qual você não confia.</span><span class="sxs-lookup"><span data-stu-id="4efc1-116">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4efc1-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4efc1-117">Return value</span></span>

<span data-ttu-id="4efc1-118">Retorna um valor inteiro de 0 (zero) após a conclusão bem-sucedida e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="4efc1-118">Returns an integer value of 0 (zero) on successful completion, and any other number to indicate an error.</span></span> <span data-ttu-id="4efc1-119">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="4efc1-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4efc1-120">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="4efc1-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4efc1-121">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="4efc1-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-122">0</span><span class="sxs-lookup"><span data-stu-id="4efc1-122">0</span></span>

<span data-ttu-id="4efc1-123">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="4efc1-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-124">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="4efc1-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-125">1</span><span class="sxs-lookup"><span data-stu-id="4efc1-125">1</span></span>

<span data-ttu-id="4efc1-126">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="4efc1-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-127">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="4efc1-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-128">64</span><span class="sxs-lookup"><span data-stu-id="4efc1-128">64</span></span>

<span data-ttu-id="4efc1-129">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="4efc1-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-130">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="4efc1-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-131">65</span><span class="sxs-lookup"><span data-stu-id="4efc1-131">65</span></span>

<span data-ttu-id="4efc1-132">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="4efc1-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-133">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="4efc1-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-134">66</span><span class="sxs-lookup"><span data-stu-id="4efc1-134">66</span></span>

<span data-ttu-id="4efc1-135">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="4efc1-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-136">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="4efc1-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-137">67</span><span class="sxs-lookup"><span data-stu-id="4efc1-137">67</span></span>

<span data-ttu-id="4efc1-138">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="4efc1-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-139">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="4efc1-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-140">68</span><span class="sxs-lookup"><span data-stu-id="4efc1-140">68</span></span>

<span data-ttu-id="4efc1-141">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="4efc1-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-142">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="4efc1-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-143">69</span><span class="sxs-lookup"><span data-stu-id="4efc1-143">69</span></span>

<span data-ttu-id="4efc1-144">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="4efc1-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-145">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="4efc1-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-146">70</span><span class="sxs-lookup"><span data-stu-id="4efc1-146">70</span></span>

<span data-ttu-id="4efc1-147">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="4efc1-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-148">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="4efc1-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-149">71</span><span class="sxs-lookup"><span data-stu-id="4efc1-149">71</span></span>

<span data-ttu-id="4efc1-150">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="4efc1-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-151">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="4efc1-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-152">72</span><span class="sxs-lookup"><span data-stu-id="4efc1-152">72</span></span>

<span data-ttu-id="4efc1-153">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="4efc1-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-154">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="4efc1-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-155">73</span><span class="sxs-lookup"><span data-stu-id="4efc1-155">73</span></span>

<span data-ttu-id="4efc1-156">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="4efc1-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-157">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="4efc1-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-158">74</span><span class="sxs-lookup"><span data-stu-id="4efc1-158">74</span></span>

<span data-ttu-id="4efc1-159">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="4efc1-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-160">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="4efc1-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-161">75</span><span class="sxs-lookup"><span data-stu-id="4efc1-161">75</span></span>

<span data-ttu-id="4efc1-162">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="4efc1-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-163">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="4efc1-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-164">76</span><span class="sxs-lookup"><span data-stu-id="4efc1-164">76</span></span>

<span data-ttu-id="4efc1-165">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="4efc1-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-166">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="4efc1-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-167">77</span><span class="sxs-lookup"><span data-stu-id="4efc1-167">77</span></span>

<span data-ttu-id="4efc1-168">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="4efc1-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-169">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="4efc1-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-170">78</span><span class="sxs-lookup"><span data-stu-id="4efc1-170">78</span></span>

<span data-ttu-id="4efc1-171">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="4efc1-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-172">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="4efc1-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-173">79</span><span class="sxs-lookup"><span data-stu-id="4efc1-173">79</span></span>

<span data-ttu-id="4efc1-174">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="4efc1-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-175">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="4efc1-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-176">80</span><span class="sxs-lookup"><span data-stu-id="4efc1-176">80</span></span>

<span data-ttu-id="4efc1-177">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4efc1-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-178">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="4efc1-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-179">81</span><span class="sxs-lookup"><span data-stu-id="4efc1-179">81</span></span>

<span data-ttu-id="4efc1-180">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="4efc1-180">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-181">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="4efc1-181">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-182">82</span><span class="sxs-lookup"><span data-stu-id="4efc1-182">82</span></span>

<span data-ttu-id="4efc1-183">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="4efc1-183">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-184">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="4efc1-184">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-185">83</span><span class="sxs-lookup"><span data-stu-id="4efc1-185">83</span></span>

<span data-ttu-id="4efc1-186">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="4efc1-186">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-187">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="4efc1-187">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-188">84</span><span class="sxs-lookup"><span data-stu-id="4efc1-188">84</span></span>

<span data-ttu-id="4efc1-189">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="4efc1-189">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-190">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="4efc1-190">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-191">85</span><span class="sxs-lookup"><span data-stu-id="4efc1-191">85</span></span>

<span data-ttu-id="4efc1-192">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="4efc1-192">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-193">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="4efc1-193">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-194">86</span><span class="sxs-lookup"><span data-stu-id="4efc1-194">86</span></span>

<span data-ttu-id="4efc1-195">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="4efc1-195">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-196">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="4efc1-196">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-197">87</span><span class="sxs-lookup"><span data-stu-id="4efc1-197">87</span></span>

<span data-ttu-id="4efc1-198">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="4efc1-198">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-199">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="4efc1-199">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-200">88</span><span class="sxs-lookup"><span data-stu-id="4efc1-200">88</span></span>

<span data-ttu-id="4efc1-201">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="4efc1-201">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-202">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="4efc1-202">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-203">89</span><span class="sxs-lookup"><span data-stu-id="4efc1-203">89</span></span>

<span data-ttu-id="4efc1-204">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="4efc1-204">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-205">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="4efc1-205">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-206">90</span><span class="sxs-lookup"><span data-stu-id="4efc1-206">90</span></span>

<span data-ttu-id="4efc1-207">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="4efc1-207">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-208">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="4efc1-208">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-209">91</span><span class="sxs-lookup"><span data-stu-id="4efc1-209">91</span></span>

<span data-ttu-id="4efc1-210">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="4efc1-210">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-211">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="4efc1-211">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-212">92</span><span class="sxs-lookup"><span data-stu-id="4efc1-212">92</span></span>

<span data-ttu-id="4efc1-213">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="4efc1-213">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-214">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="4efc1-214">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-215">93</span><span class="sxs-lookup"><span data-stu-id="4efc1-215">93</span></span>

<span data-ttu-id="4efc1-216">Já existe.</span><span class="sxs-lookup"><span data-stu-id="4efc1-216">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-217">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="4efc1-217">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-218">94</span><span class="sxs-lookup"><span data-stu-id="4efc1-218">94</span></span>

<span data-ttu-id="4efc1-219">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="4efc1-219">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-220">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="4efc1-220">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-221">95</span><span class="sxs-lookup"><span data-stu-id="4efc1-221">95</span></span>

<span data-ttu-id="4efc1-222">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="4efc1-222">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-223">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="4efc1-223">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-224">96</span><span class="sxs-lookup"><span data-stu-id="4efc1-224">96</span></span>

<span data-ttu-id="4efc1-225">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="4efc1-225">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-226">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="4efc1-226">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-227">97</span><span class="sxs-lookup"><span data-stu-id="4efc1-227">97</span></span>

<span data-ttu-id="4efc1-228">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="4efc1-228">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-229">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="4efc1-229">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-230">98</span><span class="sxs-lookup"><span data-stu-id="4efc1-230">98</span></span>

<span data-ttu-id="4efc1-231">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="4efc1-231">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-232">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="4efc1-232">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-233">100</span><span class="sxs-lookup"><span data-stu-id="4efc1-233">100</span></span>

<span data-ttu-id="4efc1-234">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="4efc1-234">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4efc1-235">**Outras**</span><span class="sxs-lookup"><span data-stu-id="4efc1-235">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="4efc1-236">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="4efc1-236">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4efc1-237">Comentários</span><span class="sxs-lookup"><span data-stu-id="4efc1-237">Remarks</span></span>

<span data-ttu-id="4efc1-238">Se *WINSPrimaryServer* e *WINSSecondaryServer* forem definidos como "" (uma cadeia de caracteres vazia), os servidores WINS explícitos voltarão ao DHCP.</span><span class="sxs-lookup"><span data-stu-id="4efc1-238">If both *WINSPrimaryServer* and *WINSSecondaryServer* are set to "" (an empty string), then explicit WINS servers revert back to DHCP.</span></span>

## <a name="examples"></a><span data-ttu-id="4efc1-239">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4efc1-239">Examples</span></span>

<span data-ttu-id="4efc1-240">[O atribuir um endereço IP recuperado de um banco de dados](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) Exemplo de código VBScript pesquisa um computador em um banco de dados e atribui esse computador ao endereço IP especificado.</span><span class="sxs-lookup"><span data-stu-id="4efc1-240">[The Assign an IP Address Retrieved from a Database](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) VBScript code sample looks up a computer in a database and assigns that computer the specified IP address.</span></span>

<span data-ttu-id="4efc1-241">O exemplo de código VBScript a seguir define o servidor WINS primário e secundário para um adaptador de rede associado a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4efc1-241">The following VBScript code sample sets the primary and secondary WINS server for a TCP/IP-bound network adapter.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    strPrimaryServer = "192.168.1.100" 
    strSecondaryServer = "192.168.1.200" 
    objNetCard.SetWINSServer strPrimaryServer, strSecondaryServer 
Next 
```



## <a name="requirements"></a><span data-ttu-id="4efc1-242">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4efc1-242">Requirements</span></span>



| <span data-ttu-id="4efc1-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="4efc1-243">Requirement</span></span> | <span data-ttu-id="4efc1-244">Valor</span><span class="sxs-lookup"><span data-stu-id="4efc1-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4efc1-245">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4efc1-245">Minimum supported client</span></span><br/> | <span data-ttu-id="4efc1-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4efc1-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4efc1-247">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4efc1-247">Minimum supported server</span></span><br/> | <span data-ttu-id="4efc1-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4efc1-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4efc1-249">Namespace</span><span class="sxs-lookup"><span data-stu-id="4efc1-249">Namespace</span></span><br/>                | <span data-ttu-id="4efc1-250">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4efc1-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4efc1-251">MOF</span><span class="sxs-lookup"><span data-stu-id="4efc1-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4efc1-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4efc1-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4efc1-253">DLL</span><span class="sxs-lookup"><span data-stu-id="4efc1-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4efc1-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4efc1-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4efc1-255">Confira também</span><span class="sxs-lookup"><span data-stu-id="4efc1-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4efc1-256">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="4efc1-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="4efc1-257">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="4efc1-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="4efc1-258">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="4efc1-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="4efc1-259">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="4efc1-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="4efc1-260">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="4efc1-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

