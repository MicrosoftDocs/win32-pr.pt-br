---
description: O método estático da classe WMI SetForwardBufferMemory é usado para especificar a quantidade de memória que o IP aloca para armazenar dados de pacote na fila de pacotes do roteador.
ms.assetid: e76452e8-2ee8-4d39-9405-33b0aeeac74d
ms.tgt_platform: multiple
title: Método SetForwardBufferMemory da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetForwardBufferMemory
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 30179610e6eee121a86119fa347067b40ef04c2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826489"
---
# <a name="setforwardbuffermemory-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8770c-103">Método SetForwardBufferMemory da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="8770c-103">SetForwardBufferMemory method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8770c-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetForwardBufferMemory** é usado para especificar a quantidade de memória que o IP aloca para armazenar dados de pacote na fila de pacotes do roteador.</span><span class="sxs-lookup"><span data-stu-id="8770c-104">The **SetForwardBufferMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to specify how much memory IP allocates to store packet data in the router packet queue.</span></span>

<span data-ttu-id="8770c-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8770c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8770c-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8770c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8770c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8770c-107">Syntax</span></span>


```mof
uint32 SetForwardBufferMemory(
  [in] uint32 ForwardBufferMemory
);
```



## <a name="parameters"></a><span data-ttu-id="8770c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8770c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8770c-109">*ForwardBufferMemory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8770c-109">*ForwardBufferMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8770c-110">Tamanho, em bytes, da fila de pacotes do roteador usada para armazenar dados de pacote.</span><span class="sxs-lookup"><span data-stu-id="8770c-110">Size, in bytes, of the router packet queue used to store packet data.</span></span> <span data-ttu-id="8770c-111">O valor padrão é 74240 (pacotes de 50 1480 bytes, arredondado para um múltiplo de 256).</span><span class="sxs-lookup"><span data-stu-id="8770c-111">The default value is 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8770c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8770c-112">Return value</span></span>

<span data-ttu-id="8770c-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="8770c-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="8770c-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8770c-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8770c-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8770c-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8770c-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="8770c-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-117">0</span><span class="sxs-lookup"><span data-stu-id="8770c-117">0</span></span>

<span data-ttu-id="8770c-118">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="8770c-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-119">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="8770c-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-120">1</span><span class="sxs-lookup"><span data-stu-id="8770c-120">1</span></span>

<span data-ttu-id="8770c-121">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="8770c-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-122">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="8770c-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-123">64</span><span class="sxs-lookup"><span data-stu-id="8770c-123">64</span></span>

<span data-ttu-id="8770c-124">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="8770c-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-125">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="8770c-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-126">65</span><span class="sxs-lookup"><span data-stu-id="8770c-126">65</span></span>

<span data-ttu-id="8770c-127">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="8770c-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-128">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="8770c-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-129">66</span><span class="sxs-lookup"><span data-stu-id="8770c-129">66</span></span>

<span data-ttu-id="8770c-130">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="8770c-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-131">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="8770c-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-132">67</span><span class="sxs-lookup"><span data-stu-id="8770c-132">67</span></span>

<span data-ttu-id="8770c-133">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="8770c-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-134">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="8770c-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-135">68</span><span class="sxs-lookup"><span data-stu-id="8770c-135">68</span></span>

<span data-ttu-id="8770c-136">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="8770c-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-137">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="8770c-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-138">69</span><span class="sxs-lookup"><span data-stu-id="8770c-138">69</span></span>

<span data-ttu-id="8770c-139">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="8770c-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-140">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="8770c-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-141">70</span><span class="sxs-lookup"><span data-stu-id="8770c-141">70</span></span>

<span data-ttu-id="8770c-142">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="8770c-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-143">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="8770c-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-144">71</span><span class="sxs-lookup"><span data-stu-id="8770c-144">71</span></span>

<span data-ttu-id="8770c-145">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="8770c-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-146">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="8770c-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-147">72</span><span class="sxs-lookup"><span data-stu-id="8770c-147">72</span></span>

<span data-ttu-id="8770c-148">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="8770c-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-149">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="8770c-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-150">73</span><span class="sxs-lookup"><span data-stu-id="8770c-150">73</span></span>

<span data-ttu-id="8770c-151">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="8770c-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-152">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="8770c-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-153">74</span><span class="sxs-lookup"><span data-stu-id="8770c-153">74</span></span>

<span data-ttu-id="8770c-154">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="8770c-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-155">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="8770c-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-156">75</span><span class="sxs-lookup"><span data-stu-id="8770c-156">75</span></span>

<span data-ttu-id="8770c-157">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="8770c-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-158">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="8770c-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-159">76</span><span class="sxs-lookup"><span data-stu-id="8770c-159">76</span></span>

<span data-ttu-id="8770c-160">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="8770c-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-161">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="8770c-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-162">77</span><span class="sxs-lookup"><span data-stu-id="8770c-162">77</span></span>

<span data-ttu-id="8770c-163">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="8770c-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-164">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="8770c-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-165">78</span><span class="sxs-lookup"><span data-stu-id="8770c-165">78</span></span>

<span data-ttu-id="8770c-166">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="8770c-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-167">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="8770c-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-168">79</span><span class="sxs-lookup"><span data-stu-id="8770c-168">79</span></span>

<span data-ttu-id="8770c-169">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="8770c-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-170">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="8770c-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-171">80</span><span class="sxs-lookup"><span data-stu-id="8770c-171">80</span></span>

<span data-ttu-id="8770c-172">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8770c-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-173">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="8770c-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-174">81</span><span class="sxs-lookup"><span data-stu-id="8770c-174">81</span></span>

<span data-ttu-id="8770c-175">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="8770c-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-176">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="8770c-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-177">82</span><span class="sxs-lookup"><span data-stu-id="8770c-177">82</span></span>

<span data-ttu-id="8770c-178">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="8770c-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-179">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="8770c-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-180">83</span><span class="sxs-lookup"><span data-stu-id="8770c-180">83</span></span>

<span data-ttu-id="8770c-181">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="8770c-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-182">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="8770c-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-183">84</span><span class="sxs-lookup"><span data-stu-id="8770c-183">84</span></span>

<span data-ttu-id="8770c-184">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="8770c-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-185">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="8770c-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-186">85</span><span class="sxs-lookup"><span data-stu-id="8770c-186">85</span></span>

<span data-ttu-id="8770c-187">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="8770c-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-188">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="8770c-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-189">86</span><span class="sxs-lookup"><span data-stu-id="8770c-189">86</span></span>

<span data-ttu-id="8770c-190">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="8770c-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-191">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="8770c-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-192">87</span><span class="sxs-lookup"><span data-stu-id="8770c-192">87</span></span>

<span data-ttu-id="8770c-193">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="8770c-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-194">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="8770c-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-195">88</span><span class="sxs-lookup"><span data-stu-id="8770c-195">88</span></span>

<span data-ttu-id="8770c-196">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="8770c-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-197">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="8770c-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-198">89</span><span class="sxs-lookup"><span data-stu-id="8770c-198">89</span></span>

<span data-ttu-id="8770c-199">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="8770c-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-200">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="8770c-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-201">90</span><span class="sxs-lookup"><span data-stu-id="8770c-201">90</span></span>

<span data-ttu-id="8770c-202">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="8770c-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-203">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="8770c-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-204">91</span><span class="sxs-lookup"><span data-stu-id="8770c-204">91</span></span>

<span data-ttu-id="8770c-205">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="8770c-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-206">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="8770c-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-207">92</span><span class="sxs-lookup"><span data-stu-id="8770c-207">92</span></span>

<span data-ttu-id="8770c-208">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="8770c-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-209">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="8770c-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-210">93</span><span class="sxs-lookup"><span data-stu-id="8770c-210">93</span></span>

<span data-ttu-id="8770c-211">Já existe.</span><span class="sxs-lookup"><span data-stu-id="8770c-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-212">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="8770c-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-213">94</span><span class="sxs-lookup"><span data-stu-id="8770c-213">94</span></span>

<span data-ttu-id="8770c-214">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="8770c-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-215">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="8770c-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-216">95</span><span class="sxs-lookup"><span data-stu-id="8770c-216">95</span></span>

<span data-ttu-id="8770c-217">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="8770c-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-218">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="8770c-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-219">96</span><span class="sxs-lookup"><span data-stu-id="8770c-219">96</span></span>

<span data-ttu-id="8770c-220">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="8770c-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-221">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="8770c-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-222">97</span><span class="sxs-lookup"><span data-stu-id="8770c-222">97</span></span>

<span data-ttu-id="8770c-223">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="8770c-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-224">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="8770c-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-225">98</span><span class="sxs-lookup"><span data-stu-id="8770c-225">98</span></span>

<span data-ttu-id="8770c-226">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="8770c-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-227">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="8770c-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-228">100</span><span class="sxs-lookup"><span data-stu-id="8770c-228">100</span></span>

<span data-ttu-id="8770c-229">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="8770c-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8770c-230">**Outras**</span><span class="sxs-lookup"><span data-stu-id="8770c-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8770c-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="8770c-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8770c-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="8770c-232">Remarks</span></span>

<span data-ttu-id="8770c-233">Quando esse espaço de buffer é preenchido, o roteador começa a descartar os pacotes aleatoriamente de sua fila.</span><span class="sxs-lookup"><span data-stu-id="8770c-233">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span>

<span data-ttu-id="8770c-234">Buffers de dados de fila de pacotes têm 256 bytes de comprimento, portanto, o valor do parâmetro *ForwardBufferMemory* deve ser um múltiplo de 256.</span><span class="sxs-lookup"><span data-stu-id="8770c-234">Packet queue data buffers are 256 bytes in length, so the value of the *ForwardBufferMemory* parameter should be a multiple of 256.</span></span> <span data-ttu-id="8770c-235">Vários buffers são encadeados em pacotes maiores.</span><span class="sxs-lookup"><span data-stu-id="8770c-235">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="8770c-236">O cabeçalho IP de um pacote é armazenado separadamente.</span><span class="sxs-lookup"><span data-stu-id="8770c-236">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="8770c-237">Esse parâmetro será ignorado e nenhum buffer será alocado se o roteador IP não estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="8770c-237">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="8770c-238">O tamanho do buffer pode variar da unidade máxima de transmissão (MTU) da rede até um valor menor que 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="8770c-238">The buffer size can range from the network Maximum Transmission Unit (MTU) to a value smaller than 0xFFFFFFFF.</span></span>

## <a name="examples"></a><span data-ttu-id="8770c-239">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8770c-239">Examples</span></span>

<span data-ttu-id="8770c-240">A amostra [Modificar a memória do buffer de encaminhamento de todos os adaptadores de rede](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) configura a memória do buffer de encaminhamento para todos os adaptadores de rede em um computador.</span><span class="sxs-lookup"><span data-stu-id="8770c-240">The [Modify the Forward Buffer Memory for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) VBScript sample configures the forward buffer memory for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8770c-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8770c-241">Requirements</span></span>



| <span data-ttu-id="8770c-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="8770c-242">Requirement</span></span> | <span data-ttu-id="8770c-243">Valor</span><span class="sxs-lookup"><span data-stu-id="8770c-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8770c-244">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8770c-244">Minimum supported client</span></span><br/> | <span data-ttu-id="8770c-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8770c-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8770c-246">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8770c-246">Minimum supported server</span></span><br/> | <span data-ttu-id="8770c-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8770c-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8770c-248">Namespace</span><span class="sxs-lookup"><span data-stu-id="8770c-248">Namespace</span></span><br/>                | <span data-ttu-id="8770c-249">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8770c-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8770c-250">MOF</span><span class="sxs-lookup"><span data-stu-id="8770c-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8770c-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8770c-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8770c-252">DLL</span><span class="sxs-lookup"><span data-stu-id="8770c-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8770c-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8770c-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8770c-254">Confira também</span><span class="sxs-lookup"><span data-stu-id="8770c-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8770c-255">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="8770c-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8770c-256">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="8770c-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8770c-257">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="8770c-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8770c-258">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="8770c-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8770c-259">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="8770c-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

