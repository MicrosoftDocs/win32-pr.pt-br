---
description: O método estático da classe WMI SetTcpNumConnections é usado para definir o número máximo de conexões que o TCP pode ter aberto simultaneamente.
ms.assetid: 50458161-1f28-47f9-b395-09586e859d5d
ms.tgt_platform: multiple
title: Método SetTcpNumConnections da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpNumConnections
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5708c7ce80930c0924b560cc7b84e5af45ad7962
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089225"
---
# <a name="settcpnumconnections-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="987a9-103">Método SetTcpNumConnections da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="987a9-103">SetTcpNumConnections method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="987a9-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpNumConnections** é usado para definir o número máximo de conexões que o TCP pode ter aberto simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="987a9-104">The **SetTcpNumConnections** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum number of connections that TCP may have open simultaneously.</span></span>

<span data-ttu-id="987a9-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="987a9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="987a9-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="987a9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="987a9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="987a9-107">Syntax</span></span>


```mof
uint32 SetTcpNumConnections(
  [in] uint32 TcpNumConnections
);
```



## <a name="parameters"></a><span data-ttu-id="987a9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="987a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="987a9-109">*TcpNumConnections* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="987a9-109">*TcpNumConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="987a9-110">Número máximo de conexões que o TCP pode ter aberto simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="987a9-110">Maximum number of connections that TCP may have open simultaneously.</span></span> <span data-ttu-id="987a9-111">O intervalo válido de valores é 0-0xFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="987a9-111">The valid range of values is 0 - 0xFFFFFE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="987a9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="987a9-112">Return value</span></span>

<span data-ttu-id="987a9-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="987a9-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="987a9-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="987a9-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="987a9-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="987a9-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="987a9-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="987a9-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-117">0</span><span class="sxs-lookup"><span data-stu-id="987a9-117">0</span></span>

<span data-ttu-id="987a9-118">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="987a9-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-119">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="987a9-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-120">1</span><span class="sxs-lookup"><span data-stu-id="987a9-120">1</span></span>

<span data-ttu-id="987a9-121">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="987a9-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-122">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="987a9-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-123">64</span><span class="sxs-lookup"><span data-stu-id="987a9-123">64</span></span>

<span data-ttu-id="987a9-124">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="987a9-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-125">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="987a9-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-126">65</span><span class="sxs-lookup"><span data-stu-id="987a9-126">65</span></span>

<span data-ttu-id="987a9-127">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="987a9-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-128">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="987a9-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-129">66</span><span class="sxs-lookup"><span data-stu-id="987a9-129">66</span></span>

<span data-ttu-id="987a9-130">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="987a9-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-131">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="987a9-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-132">67</span><span class="sxs-lookup"><span data-stu-id="987a9-132">67</span></span>

<span data-ttu-id="987a9-133">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="987a9-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-134">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="987a9-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-135">68</span><span class="sxs-lookup"><span data-stu-id="987a9-135">68</span></span>

<span data-ttu-id="987a9-136">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="987a9-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-137">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="987a9-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-138">69</span><span class="sxs-lookup"><span data-stu-id="987a9-138">69</span></span>

<span data-ttu-id="987a9-139">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="987a9-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-140">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="987a9-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-141">70</span><span class="sxs-lookup"><span data-stu-id="987a9-141">70</span></span>

<span data-ttu-id="987a9-142">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="987a9-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-143">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="987a9-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-144">71</span><span class="sxs-lookup"><span data-stu-id="987a9-144">71</span></span>

<span data-ttu-id="987a9-145">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="987a9-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-146">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="987a9-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-147">72</span><span class="sxs-lookup"><span data-stu-id="987a9-147">72</span></span>

<span data-ttu-id="987a9-148">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="987a9-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-149">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="987a9-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-150">73</span><span class="sxs-lookup"><span data-stu-id="987a9-150">73</span></span>

<span data-ttu-id="987a9-151">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="987a9-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-152">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="987a9-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-153">74</span><span class="sxs-lookup"><span data-stu-id="987a9-153">74</span></span>

<span data-ttu-id="987a9-154">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="987a9-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-155">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="987a9-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-156">75</span><span class="sxs-lookup"><span data-stu-id="987a9-156">75</span></span>

<span data-ttu-id="987a9-157">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="987a9-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-158">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="987a9-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-159">76</span><span class="sxs-lookup"><span data-stu-id="987a9-159">76</span></span>

<span data-ttu-id="987a9-160">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="987a9-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-161">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="987a9-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-162">77</span><span class="sxs-lookup"><span data-stu-id="987a9-162">77</span></span>

<span data-ttu-id="987a9-163">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="987a9-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-164">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="987a9-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-165">78</span><span class="sxs-lookup"><span data-stu-id="987a9-165">78</span></span>

<span data-ttu-id="987a9-166">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="987a9-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-167">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="987a9-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-168">79</span><span class="sxs-lookup"><span data-stu-id="987a9-168">79</span></span>

<span data-ttu-id="987a9-169">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="987a9-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-170">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="987a9-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-171">80</span><span class="sxs-lookup"><span data-stu-id="987a9-171">80</span></span>

<span data-ttu-id="987a9-172">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="987a9-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-173">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="987a9-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-174">81</span><span class="sxs-lookup"><span data-stu-id="987a9-174">81</span></span>

<span data-ttu-id="987a9-175">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="987a9-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-176">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="987a9-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-177">82</span><span class="sxs-lookup"><span data-stu-id="987a9-177">82</span></span>

<span data-ttu-id="987a9-178">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="987a9-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-179">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="987a9-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-180">83</span><span class="sxs-lookup"><span data-stu-id="987a9-180">83</span></span>

<span data-ttu-id="987a9-181">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="987a9-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-182">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="987a9-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-183">84</span><span class="sxs-lookup"><span data-stu-id="987a9-183">84</span></span>

<span data-ttu-id="987a9-184">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="987a9-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-185">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="987a9-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-186">85</span><span class="sxs-lookup"><span data-stu-id="987a9-186">85</span></span>

<span data-ttu-id="987a9-187">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="987a9-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-188">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="987a9-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-189">86</span><span class="sxs-lookup"><span data-stu-id="987a9-189">86</span></span>

<span data-ttu-id="987a9-190">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="987a9-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-191">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="987a9-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-192">87</span><span class="sxs-lookup"><span data-stu-id="987a9-192">87</span></span>

<span data-ttu-id="987a9-193">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="987a9-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-194">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="987a9-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-195">88</span><span class="sxs-lookup"><span data-stu-id="987a9-195">88</span></span>

<span data-ttu-id="987a9-196">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="987a9-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-197">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="987a9-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-198">89</span><span class="sxs-lookup"><span data-stu-id="987a9-198">89</span></span>

<span data-ttu-id="987a9-199">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="987a9-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-200">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="987a9-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-201">90</span><span class="sxs-lookup"><span data-stu-id="987a9-201">90</span></span>

<span data-ttu-id="987a9-202">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="987a9-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-203">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="987a9-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-204">91</span><span class="sxs-lookup"><span data-stu-id="987a9-204">91</span></span>

<span data-ttu-id="987a9-205">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="987a9-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-206">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="987a9-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-207">92</span><span class="sxs-lookup"><span data-stu-id="987a9-207">92</span></span>

<span data-ttu-id="987a9-208">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="987a9-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-209">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="987a9-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-210">93</span><span class="sxs-lookup"><span data-stu-id="987a9-210">93</span></span>

<span data-ttu-id="987a9-211">Já existe.</span><span class="sxs-lookup"><span data-stu-id="987a9-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-212">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="987a9-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-213">94</span><span class="sxs-lookup"><span data-stu-id="987a9-213">94</span></span>

<span data-ttu-id="987a9-214">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="987a9-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-215">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="987a9-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-216">95</span><span class="sxs-lookup"><span data-stu-id="987a9-216">95</span></span>

<span data-ttu-id="987a9-217">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="987a9-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-218">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="987a9-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-219">96</span><span class="sxs-lookup"><span data-stu-id="987a9-219">96</span></span>

<span data-ttu-id="987a9-220">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="987a9-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-221">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="987a9-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-222">97</span><span class="sxs-lookup"><span data-stu-id="987a9-222">97</span></span>

<span data-ttu-id="987a9-223">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="987a9-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-224">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="987a9-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-225">98</span><span class="sxs-lookup"><span data-stu-id="987a9-225">98</span></span>

<span data-ttu-id="987a9-226">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="987a9-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-227">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="987a9-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-228">100</span><span class="sxs-lookup"><span data-stu-id="987a9-228">100</span></span>

<span data-ttu-id="987a9-229">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="987a9-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="987a9-230">**Outras**</span><span class="sxs-lookup"><span data-stu-id="987a9-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="987a9-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="987a9-231">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="987a9-232">Exemplos</span><span class="sxs-lookup"><span data-stu-id="987a9-232">Examples</span></span>

<span data-ttu-id="987a9-233">O exemplo [Modificar o número permitido de conexões TCP do](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) VBScript define o número máximo permitido de conexões TCP abertas simultaneamente em um computador como 10.</span><span class="sxs-lookup"><span data-stu-id="987a9-233">The [Modify the Allowed Number of TCP Connections](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) VBScript sample sets the maximum allowed number of simultaneously-opened TCP connections on a computer to 10.</span></span>

## <a name="requirements"></a><span data-ttu-id="987a9-234">Requisitos</span><span class="sxs-lookup"><span data-stu-id="987a9-234">Requirements</span></span>



| <span data-ttu-id="987a9-235">Requisito</span><span class="sxs-lookup"><span data-stu-id="987a9-235">Requirement</span></span> | <span data-ttu-id="987a9-236">Valor</span><span class="sxs-lookup"><span data-stu-id="987a9-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="987a9-237">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="987a9-237">Minimum supported client</span></span><br/> | <span data-ttu-id="987a9-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a9-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="987a9-239">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="987a9-239">Minimum supported server</span></span><br/> | <span data-ttu-id="987a9-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="987a9-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="987a9-241">Namespace</span><span class="sxs-lookup"><span data-stu-id="987a9-241">Namespace</span></span><br/>                | <span data-ttu-id="987a9-242">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="987a9-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="987a9-243">MOF</span><span class="sxs-lookup"><span data-stu-id="987a9-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="987a9-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="987a9-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="987a9-245">DLL</span><span class="sxs-lookup"><span data-stu-id="987a9-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="987a9-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="987a9-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="987a9-247">Confira também</span><span class="sxs-lookup"><span data-stu-id="987a9-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="987a9-248">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="987a9-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="987a9-249">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="987a9-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="987a9-250">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="987a9-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="987a9-251">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="987a9-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="987a9-252">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="987a9-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

