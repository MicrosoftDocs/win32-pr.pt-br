---
description: O método SetTcpipNetbios é usado para definir a operação padrão de NetBIOS sobre TCP/IP.
ms.assetid: 2c639595-da13-400d-b4d0-432b39460554
ms.tgt_platform: multiple
title: Método SetTcpipNetbios da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpipNetbios
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20ecab5918d00dc5f189464becc0252f2a8c0569
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826693"
---
# <a name="settcpipnetbios-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="66761-103">Método SetTcpipNetbios da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="66761-103">SetTcpipNetbios method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="66761-104">O método **SetTcpipNetbios** é usado para definir a operação padrão de NetBIOS sobre TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="66761-104">The **SetTcpipNetbios** method is used to set the default operation of NetBIOS over TCP/IP.</span></span>

<span data-ttu-id="66761-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="66761-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="66761-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="66761-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="66761-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66761-107">Syntax</span></span>


```mof
uint32 SetTcpipNetbios(
  [in] uint32 TcpipNetbiosOptions
);
```



## <a name="parameters"></a><span data-ttu-id="66761-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66761-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66761-109">*TcpipNetbiosOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66761-109">*TcpipNetbiosOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66761-110">Valor que especifica as configurações possíveis relacionadas ao NetBIOS sobre TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="66761-110">Value that specifies the possible settings related to NetBIOS over TCP/IP.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="66761-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**EnableNetbiosViaDhcp** (0)</span><span class="sxs-lookup"><span data-stu-id="66761-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd>

<span data-ttu-id="66761-112">Habilitar NetBIOS via DHCP</span><span class="sxs-lookup"><span data-stu-id="66761-112">Enable Netbios via DHCP</span></span>

</dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="66761-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**EnableNetbios** (1)</span><span class="sxs-lookup"><span data-stu-id="66761-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**EnableNetbios** (1)</span></span>


</dt> <dd>

<span data-ttu-id="66761-114">Habilitar NetBIOS</span><span class="sxs-lookup"><span data-stu-id="66761-114">Enable Netbios</span></span>

</dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="66761-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**DisableNetbios** (2)</span><span class="sxs-lookup"><span data-stu-id="66761-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**DisableNetbios** (2)</span></span>


</dt> <dd>

<span data-ttu-id="66761-116">Desabilitar NetBIOS</span><span class="sxs-lookup"><span data-stu-id="66761-116">Disable Netbios</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66761-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66761-117">Return value</span></span>

<span data-ttu-id="66761-118">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="66761-118">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="66761-119">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="66761-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="66761-120">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="66761-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="66761-121">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="66761-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="66761-122">0</span><span class="sxs-lookup"><span data-stu-id="66761-122">0</span></span>

<span data-ttu-id="66761-123">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="66761-123">Successful completion.</span></span> <span data-ttu-id="66761-124">Nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="66761-124">No reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="66761-125">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="66761-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="66761-126">1</span><span class="sxs-lookup"><span data-stu-id="66761-126">1</span></span>

<span data-ttu-id="66761-127">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="66761-127">Successful completion.</span></span> <span data-ttu-id="66761-128">É necessário reiniciar.</span><span class="sxs-lookup"><span data-stu-id="66761-128">Reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="66761-129">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="66761-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="66761-130">64</span><span class="sxs-lookup"><span data-stu-id="66761-130">64</span></span>

<span data-ttu-id="66761-131">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="66761-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="66761-132">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="66761-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="66761-133">65</span><span class="sxs-lookup"><span data-stu-id="66761-133">65</span></span>

<span data-ttu-id="66761-134">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="66761-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="66761-135">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="66761-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="66761-136">66</span><span class="sxs-lookup"><span data-stu-id="66761-136">66</span></span>

<span data-ttu-id="66761-137">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="66761-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="66761-138">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="66761-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="66761-139">67</span><span class="sxs-lookup"><span data-stu-id="66761-139">67</span></span>

<span data-ttu-id="66761-140">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="66761-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="66761-141">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="66761-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="66761-142">68</span><span class="sxs-lookup"><span data-stu-id="66761-142">68</span></span>

<span data-ttu-id="66761-143">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="66761-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="66761-144">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="66761-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="66761-145">69</span><span class="sxs-lookup"><span data-stu-id="66761-145">69</span></span>

<span data-ttu-id="66761-146">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="66761-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="66761-147">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="66761-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="66761-148">70</span><span class="sxs-lookup"><span data-stu-id="66761-148">70</span></span>

<span data-ttu-id="66761-149">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="66761-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="66761-150">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="66761-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="66761-151">71</span><span class="sxs-lookup"><span data-stu-id="66761-151">71</span></span>

<span data-ttu-id="66761-152">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="66761-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="66761-153">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="66761-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="66761-154">72</span><span class="sxs-lookup"><span data-stu-id="66761-154">72</span></span>

<span data-ttu-id="66761-155">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="66761-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="66761-156">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="66761-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="66761-157">73</span><span class="sxs-lookup"><span data-stu-id="66761-157">73</span></span>

<span data-ttu-id="66761-158">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="66761-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="66761-159">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="66761-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="66761-160">74</span><span class="sxs-lookup"><span data-stu-id="66761-160">74</span></span>

<span data-ttu-id="66761-161">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="66761-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="66761-162">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="66761-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="66761-163">75</span><span class="sxs-lookup"><span data-stu-id="66761-163">75</span></span>

<span data-ttu-id="66761-164">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="66761-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="66761-165">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="66761-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="66761-166">76</span><span class="sxs-lookup"><span data-stu-id="66761-166">76</span></span>

<span data-ttu-id="66761-167">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="66761-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="66761-168">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="66761-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="66761-169">77</span><span class="sxs-lookup"><span data-stu-id="66761-169">77</span></span>

<span data-ttu-id="66761-170">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="66761-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="66761-171">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="66761-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="66761-172">78</span><span class="sxs-lookup"><span data-stu-id="66761-172">78</span></span>

<span data-ttu-id="66761-173">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="66761-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="66761-174">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="66761-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="66761-175">79</span><span class="sxs-lookup"><span data-stu-id="66761-175">79</span></span>

<span data-ttu-id="66761-176">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="66761-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="66761-177">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="66761-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="66761-178">80</span><span class="sxs-lookup"><span data-stu-id="66761-178">80</span></span>

<span data-ttu-id="66761-179">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="66761-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="66761-180">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="66761-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="66761-181">81</span><span class="sxs-lookup"><span data-stu-id="66761-181">81</span></span>

<span data-ttu-id="66761-182">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="66761-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="66761-183">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="66761-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="66761-184">82</span><span class="sxs-lookup"><span data-stu-id="66761-184">82</span></span>

<span data-ttu-id="66761-185">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="66761-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="66761-186">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="66761-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="66761-187">83</span><span class="sxs-lookup"><span data-stu-id="66761-187">83</span></span>

<span data-ttu-id="66761-188">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="66761-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="66761-189">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="66761-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="66761-190">84</span><span class="sxs-lookup"><span data-stu-id="66761-190">84</span></span>

<span data-ttu-id="66761-191">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="66761-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="66761-192">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="66761-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="66761-193">85</span><span class="sxs-lookup"><span data-stu-id="66761-193">85</span></span>

<span data-ttu-id="66761-194">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="66761-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="66761-195">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="66761-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="66761-196">86</span><span class="sxs-lookup"><span data-stu-id="66761-196">86</span></span>

<span data-ttu-id="66761-197">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="66761-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="66761-198">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="66761-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="66761-199">87</span><span class="sxs-lookup"><span data-stu-id="66761-199">87</span></span>

<span data-ttu-id="66761-200">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="66761-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="66761-201">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="66761-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="66761-202">88</span><span class="sxs-lookup"><span data-stu-id="66761-202">88</span></span>

<span data-ttu-id="66761-203">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="66761-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="66761-204">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="66761-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="66761-205">89</span><span class="sxs-lookup"><span data-stu-id="66761-205">89</span></span>

<span data-ttu-id="66761-206">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="66761-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="66761-207">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="66761-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="66761-208">90</span><span class="sxs-lookup"><span data-stu-id="66761-208">90</span></span>

<span data-ttu-id="66761-209">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="66761-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="66761-210">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="66761-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="66761-211">91</span><span class="sxs-lookup"><span data-stu-id="66761-211">91</span></span>

<span data-ttu-id="66761-212">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="66761-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="66761-213">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="66761-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="66761-214">92</span><span class="sxs-lookup"><span data-stu-id="66761-214">92</span></span>

<span data-ttu-id="66761-215">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="66761-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="66761-216">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="66761-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="66761-217">93</span><span class="sxs-lookup"><span data-stu-id="66761-217">93</span></span>

<span data-ttu-id="66761-218">Já existe.</span><span class="sxs-lookup"><span data-stu-id="66761-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="66761-219">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="66761-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="66761-220">94</span><span class="sxs-lookup"><span data-stu-id="66761-220">94</span></span>

<span data-ttu-id="66761-221">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="66761-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="66761-222">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="66761-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="66761-223">95</span><span class="sxs-lookup"><span data-stu-id="66761-223">95</span></span>

<span data-ttu-id="66761-224">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="66761-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="66761-225">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="66761-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="66761-226">96</span><span class="sxs-lookup"><span data-stu-id="66761-226">96</span></span>

<span data-ttu-id="66761-227">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="66761-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="66761-228">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="66761-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="66761-229">97</span><span class="sxs-lookup"><span data-stu-id="66761-229">97</span></span>

<span data-ttu-id="66761-230">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="66761-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="66761-231">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="66761-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="66761-232">98</span><span class="sxs-lookup"><span data-stu-id="66761-232">98</span></span>

<span data-ttu-id="66761-233">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="66761-233">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="66761-234">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="66761-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="66761-235">100</span><span class="sxs-lookup"><span data-stu-id="66761-235">100</span></span>

<span data-ttu-id="66761-236">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="66761-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="66761-237">**Outras**</span><span class="sxs-lookup"><span data-stu-id="66761-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="66761-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="66761-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="66761-239">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66761-239">Examples</span></span>

<span data-ttu-id="66761-240">O exemplo de [Modificar o uso de NetBIOS em um adaptador de rede](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) ativa o NetBIOS para um adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="66761-240">The [Modify NetBIOS Use on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) VBScript sample enables NetBIOS for a network adapter.</span></span>

<span data-ttu-id="66761-241">A amostra do [PowerShell configurar placas de rede iSCSI de acordo com as práticas recomendadas da Microsoft](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) automatiza as definições de configuração para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="66761-241">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="66761-242">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66761-242">Requirements</span></span>



| <span data-ttu-id="66761-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="66761-243">Requirement</span></span> | <span data-ttu-id="66761-244">Valor</span><span class="sxs-lookup"><span data-stu-id="66761-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66761-245">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66761-245">Minimum supported client</span></span><br/> | <span data-ttu-id="66761-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66761-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66761-247">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66761-247">Minimum supported server</span></span><br/> | <span data-ttu-id="66761-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66761-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66761-249">Namespace</span><span class="sxs-lookup"><span data-stu-id="66761-249">Namespace</span></span><br/>                | <span data-ttu-id="66761-250">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="66761-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="66761-251">MOF</span><span class="sxs-lookup"><span data-stu-id="66761-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66761-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66761-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="66761-253">DLL</span><span class="sxs-lookup"><span data-stu-id="66761-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66761-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66761-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66761-255">Confira também</span><span class="sxs-lookup"><span data-stu-id="66761-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66761-256">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="66761-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="66761-257">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="66761-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="66761-258">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="66761-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="66761-259">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="66761-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="66761-260">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="66761-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

