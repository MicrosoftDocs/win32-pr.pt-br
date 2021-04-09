---
description: O método estático da classe WMI SetTcpMaxDataRetransmissions é usado para definir o número de vezes que o TCP retransmite um segmento de dados individual antes de abortar a conexão.
ms.assetid: 1b5407ee-8e2b-4aed-a17a-58d960f976f2
ms.tgt_platform: multiple
title: Método SetTcpMaxDataRetransmissions da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxDataRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 59998888eb2aed170b626fb4cb61780cbe0cb6e4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089661"
---
# <a name="settcpmaxdataretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="70070-103">Método SetTcpMaxDataRetransmissions da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="70070-103">SetTcpMaxDataRetransmissions method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="70070-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpMaxDataRetransmissions** é usado para definir o número de vezes que o TCP retransmite um segmento de dados individual antes de abortar a conexão.</span><span class="sxs-lookup"><span data-stu-id="70070-104">The **SetTcpMaxDataRetransmissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of times TCP retransmits an individual data segment before aborting the connection.</span></span>

<span data-ttu-id="70070-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="70070-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="70070-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="70070-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="70070-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70070-107">Syntax</span></span>


```mof
uint32 SetTcpMaxDataRetransmissions(
  [in] uint32 TcpMaxDataRetransmissions
);
```



## <a name="parameters"></a><span data-ttu-id="70070-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70070-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70070-109">*TcpMaxDataRetransmissions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70070-109">*TcpMaxDataRetransmissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70070-110">Número de vezes que o TCP retransmite um segmento de dados individual antes de abortar a conexão.</span><span class="sxs-lookup"><span data-stu-id="70070-110">Number of times TCP retransmits an individual data segment before aborting the connection.</span></span> <span data-ttu-id="70070-111">Intervalo válido: 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="70070-111">Valid range: 0 - 0xFFFFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70070-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70070-112">Return value</span></span>

<span data-ttu-id="70070-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="70070-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="70070-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="70070-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="70070-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="70070-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="70070-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="70070-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="70070-117">0</span><span class="sxs-lookup"><span data-stu-id="70070-117">0</span></span>

<span data-ttu-id="70070-118">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="70070-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="70070-119">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="70070-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="70070-120">1</span><span class="sxs-lookup"><span data-stu-id="70070-120">1</span></span>

<span data-ttu-id="70070-121">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="70070-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="70070-122">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="70070-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="70070-123">64</span><span class="sxs-lookup"><span data-stu-id="70070-123">64</span></span>

<span data-ttu-id="70070-124">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="70070-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="70070-125">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="70070-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="70070-126">65</span><span class="sxs-lookup"><span data-stu-id="70070-126">65</span></span>

<span data-ttu-id="70070-127">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="70070-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="70070-128">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="70070-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="70070-129">66</span><span class="sxs-lookup"><span data-stu-id="70070-129">66</span></span>

<span data-ttu-id="70070-130">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="70070-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="70070-131">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="70070-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="70070-132">67</span><span class="sxs-lookup"><span data-stu-id="70070-132">67</span></span>

<span data-ttu-id="70070-133">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="70070-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="70070-134">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="70070-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="70070-135">68</span><span class="sxs-lookup"><span data-stu-id="70070-135">68</span></span>

<span data-ttu-id="70070-136">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="70070-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="70070-137">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="70070-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="70070-138">69</span><span class="sxs-lookup"><span data-stu-id="70070-138">69</span></span>

<span data-ttu-id="70070-139">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="70070-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="70070-140">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="70070-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="70070-141">70</span><span class="sxs-lookup"><span data-stu-id="70070-141">70</span></span>

<span data-ttu-id="70070-142">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="70070-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="70070-143">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="70070-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="70070-144">71</span><span class="sxs-lookup"><span data-stu-id="70070-144">71</span></span>

<span data-ttu-id="70070-145">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="70070-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="70070-146">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="70070-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="70070-147">72</span><span class="sxs-lookup"><span data-stu-id="70070-147">72</span></span>

<span data-ttu-id="70070-148">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="70070-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="70070-149">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="70070-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="70070-150">73</span><span class="sxs-lookup"><span data-stu-id="70070-150">73</span></span>

<span data-ttu-id="70070-151">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="70070-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="70070-152">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="70070-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="70070-153">74</span><span class="sxs-lookup"><span data-stu-id="70070-153">74</span></span>

<span data-ttu-id="70070-154">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="70070-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="70070-155">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="70070-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="70070-156">75</span><span class="sxs-lookup"><span data-stu-id="70070-156">75</span></span>

<span data-ttu-id="70070-157">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="70070-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="70070-158">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="70070-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="70070-159">76</span><span class="sxs-lookup"><span data-stu-id="70070-159">76</span></span>

<span data-ttu-id="70070-160">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="70070-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="70070-161">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="70070-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="70070-162">77</span><span class="sxs-lookup"><span data-stu-id="70070-162">77</span></span>

<span data-ttu-id="70070-163">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="70070-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="70070-164">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="70070-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="70070-165">78</span><span class="sxs-lookup"><span data-stu-id="70070-165">78</span></span>

<span data-ttu-id="70070-166">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="70070-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="70070-167">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="70070-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="70070-168">79</span><span class="sxs-lookup"><span data-stu-id="70070-168">79</span></span>

<span data-ttu-id="70070-169">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="70070-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="70070-170">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="70070-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="70070-171">80</span><span class="sxs-lookup"><span data-stu-id="70070-171">80</span></span>

<span data-ttu-id="70070-172">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="70070-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="70070-173">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="70070-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="70070-174">81</span><span class="sxs-lookup"><span data-stu-id="70070-174">81</span></span>

<span data-ttu-id="70070-175">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="70070-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="70070-176">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="70070-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="70070-177">82</span><span class="sxs-lookup"><span data-stu-id="70070-177">82</span></span>

<span data-ttu-id="70070-178">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="70070-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="70070-179">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="70070-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="70070-180">83</span><span class="sxs-lookup"><span data-stu-id="70070-180">83</span></span>

<span data-ttu-id="70070-181">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="70070-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="70070-182">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="70070-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="70070-183">84</span><span class="sxs-lookup"><span data-stu-id="70070-183">84</span></span>

<span data-ttu-id="70070-184">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="70070-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="70070-185">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="70070-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="70070-186">85</span><span class="sxs-lookup"><span data-stu-id="70070-186">85</span></span>

<span data-ttu-id="70070-187">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="70070-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="70070-188">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="70070-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="70070-189">86</span><span class="sxs-lookup"><span data-stu-id="70070-189">86</span></span>

<span data-ttu-id="70070-190">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="70070-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="70070-191">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="70070-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="70070-192">87</span><span class="sxs-lookup"><span data-stu-id="70070-192">87</span></span>

<span data-ttu-id="70070-193">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="70070-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="70070-194">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="70070-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="70070-195">88</span><span class="sxs-lookup"><span data-stu-id="70070-195">88</span></span>

<span data-ttu-id="70070-196">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="70070-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="70070-197">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="70070-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="70070-198">89</span><span class="sxs-lookup"><span data-stu-id="70070-198">89</span></span>

<span data-ttu-id="70070-199">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="70070-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="70070-200">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="70070-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="70070-201">90</span><span class="sxs-lookup"><span data-stu-id="70070-201">90</span></span>

<span data-ttu-id="70070-202">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="70070-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="70070-203">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="70070-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="70070-204">91</span><span class="sxs-lookup"><span data-stu-id="70070-204">91</span></span>

<span data-ttu-id="70070-205">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="70070-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="70070-206">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="70070-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="70070-207">92</span><span class="sxs-lookup"><span data-stu-id="70070-207">92</span></span>

<span data-ttu-id="70070-208">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="70070-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="70070-209">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="70070-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="70070-210">93</span><span class="sxs-lookup"><span data-stu-id="70070-210">93</span></span>

<span data-ttu-id="70070-211">Já existe.</span><span class="sxs-lookup"><span data-stu-id="70070-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="70070-212">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="70070-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="70070-213">94</span><span class="sxs-lookup"><span data-stu-id="70070-213">94</span></span>

<span data-ttu-id="70070-214">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="70070-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="70070-215">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="70070-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="70070-216">95</span><span class="sxs-lookup"><span data-stu-id="70070-216">95</span></span>

<span data-ttu-id="70070-217">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="70070-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="70070-218">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="70070-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="70070-219">96</span><span class="sxs-lookup"><span data-stu-id="70070-219">96</span></span>

<span data-ttu-id="70070-220">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="70070-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="70070-221">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="70070-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="70070-222">97</span><span class="sxs-lookup"><span data-stu-id="70070-222">97</span></span>

<span data-ttu-id="70070-223">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="70070-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="70070-224">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="70070-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="70070-225">98</span><span class="sxs-lookup"><span data-stu-id="70070-225">98</span></span>

<span data-ttu-id="70070-226">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="70070-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="70070-227">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="70070-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="70070-228">100</span><span class="sxs-lookup"><span data-stu-id="70070-228">100</span></span>

<span data-ttu-id="70070-229">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="70070-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="70070-230">**Outras**</span><span class="sxs-lookup"><span data-stu-id="70070-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="70070-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="70070-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70070-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="70070-232">Remarks</span></span>

<span data-ttu-id="70070-233">O tempo limite de retransmissão é duplicado com cada retransmissão sucessiva em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="70070-233">The retransmission timeout doubles with each successive retransmission on a connection.</span></span>

## <a name="examples"></a><span data-ttu-id="70070-234">Exemplos</span><span class="sxs-lookup"><span data-stu-id="70070-234">Examples</span></span>

<span data-ttu-id="70070-235">A amostra [Modificar o máximo de retransmissões de dados TCP permitidas](https://Gallery.TechNet.Microsoft.Com/8a581692-7950-412e-bd28-74f223b27827) configura o número de vezes que o TCP tentará retransmitir um segmento de dados individual antes de abandonar o esforço.</span><span class="sxs-lookup"><span data-stu-id="70070-235">The [Modify the Maximum Allowed TCP Data Retransmissions](https://Gallery.TechNet.Microsoft.Com/8a581692-7950-412e-bd28-74f223b27827) VBScript sample configures the number of times TCP will attempt to retransmit an individual data segment before abandoning the effort.</span></span>

## <a name="requirements"></a><span data-ttu-id="70070-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70070-236">Requirements</span></span>



| <span data-ttu-id="70070-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="70070-237">Requirement</span></span> | <span data-ttu-id="70070-238">Valor</span><span class="sxs-lookup"><span data-stu-id="70070-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70070-239">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70070-239">Minimum supported client</span></span><br/> | <span data-ttu-id="70070-240">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70070-240">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="70070-241">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70070-241">Minimum supported server</span></span><br/> | <span data-ttu-id="70070-242">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70070-242">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="70070-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="70070-243">Namespace</span></span><br/>                | <span data-ttu-id="70070-244">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="70070-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="70070-245">MOF</span><span class="sxs-lookup"><span data-stu-id="70070-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70070-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70070-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="70070-247">DLL</span><span class="sxs-lookup"><span data-stu-id="70070-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70070-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70070-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70070-249">Confira também</span><span class="sxs-lookup"><span data-stu-id="70070-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70070-250">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="70070-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="70070-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="70070-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="70070-252">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="70070-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="70070-253">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="70070-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="70070-254">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="70070-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

