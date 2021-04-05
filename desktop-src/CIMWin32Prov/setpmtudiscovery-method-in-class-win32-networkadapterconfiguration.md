---
description: O método estático da classe WMI SetPMTUDiscovery é usado para habilitar a descoberta de MTU (unidade de transmissão) máxima sobre o caminho para um host remoto.
ms.assetid: 43c640bb-c4e7-4b4b-9c18-6cc426229954
ms.tgt_platform: multiple
title: Método SetPMTUDiscovery da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUDiscovery
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef3bc9ad5d6203077275f3665c4b0efc98265fbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646415"
---
# <a name="setpmtudiscovery-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f5203-103">Método SetPMTUDiscovery da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5203-103">SetPMTUDiscovery method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f5203-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPMTUDiscovery** é usado para habilitar a descoberta de MTU (unidade de transmissão) máxima sobre o caminho para um host remoto.</span><span class="sxs-lookup"><span data-stu-id="f5203-104">The **SetPMTUDiscovery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable Maximum Transmission Unit (MTU) discovery over the path to a remote host.</span></span>

<span data-ttu-id="f5203-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f5203-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f5203-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f5203-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f5203-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5203-107">Syntax</span></span>


```mof
uint32 SetPMTUDiscovery(
  [in] boolean PMTUDiscoveryEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="f5203-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5203-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5203-109">*PMTUDiscoveryEnabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5203-109">*PMTUDiscoveryEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5203-110">Se for **true**, o TCP será habilitado para tentar descobrir a MTU (unidade de transmissão) máxima ou o maior tamanho de pacote no caminho para um host remoto.</span><span class="sxs-lookup"><span data-stu-id="f5203-110">If **true**, TCP is enabled to attempt to discover the Maximum Transmission Unit (MTU) or largest packet size over the path to a remote host.</span></span> <span data-ttu-id="f5203-111">O padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="f5203-111">The default is **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5203-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5203-112">Return value</span></span>

<span data-ttu-id="f5203-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="f5203-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f5203-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f5203-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f5203-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f5203-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f5203-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="f5203-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-117">0</span><span class="sxs-lookup"><span data-stu-id="f5203-117">0</span></span>

<span data-ttu-id="f5203-118">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="f5203-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-119">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="f5203-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-120">1</span><span class="sxs-lookup"><span data-stu-id="f5203-120">1</span></span>

<span data-ttu-id="f5203-121">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="f5203-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-122">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="f5203-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-123">64</span><span class="sxs-lookup"><span data-stu-id="f5203-123">64</span></span>

<span data-ttu-id="f5203-124">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="f5203-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-125">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="f5203-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-126">65</span><span class="sxs-lookup"><span data-stu-id="f5203-126">65</span></span>

<span data-ttu-id="f5203-127">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="f5203-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-128">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="f5203-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-129">66</span><span class="sxs-lookup"><span data-stu-id="f5203-129">66</span></span>

<span data-ttu-id="f5203-130">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="f5203-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-131">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="f5203-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-132">67</span><span class="sxs-lookup"><span data-stu-id="f5203-132">67</span></span>

<span data-ttu-id="f5203-133">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="f5203-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-134">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="f5203-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-135">68</span><span class="sxs-lookup"><span data-stu-id="f5203-135">68</span></span>

<span data-ttu-id="f5203-136">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="f5203-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-137">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="f5203-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-138">69</span><span class="sxs-lookup"><span data-stu-id="f5203-138">69</span></span>

<span data-ttu-id="f5203-139">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="f5203-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-140">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="f5203-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-141">70</span><span class="sxs-lookup"><span data-stu-id="f5203-141">70</span></span>

<span data-ttu-id="f5203-142">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="f5203-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-143">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="f5203-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-144">71</span><span class="sxs-lookup"><span data-stu-id="f5203-144">71</span></span>

<span data-ttu-id="f5203-145">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="f5203-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-146">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="f5203-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-147">72</span><span class="sxs-lookup"><span data-stu-id="f5203-147">72</span></span>

<span data-ttu-id="f5203-148">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="f5203-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-149">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="f5203-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-150">73</span><span class="sxs-lookup"><span data-stu-id="f5203-150">73</span></span>

<span data-ttu-id="f5203-151">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="f5203-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-152">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="f5203-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-153">74</span><span class="sxs-lookup"><span data-stu-id="f5203-153">74</span></span>

<span data-ttu-id="f5203-154">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="f5203-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-155">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="f5203-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-156">75</span><span class="sxs-lookup"><span data-stu-id="f5203-156">75</span></span>

<span data-ttu-id="f5203-157">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="f5203-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-158">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="f5203-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-159">76</span><span class="sxs-lookup"><span data-stu-id="f5203-159">76</span></span>

<span data-ttu-id="f5203-160">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="f5203-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-161">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="f5203-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-162">77</span><span class="sxs-lookup"><span data-stu-id="f5203-162">77</span></span>

<span data-ttu-id="f5203-163">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="f5203-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-164">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="f5203-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-165">78</span><span class="sxs-lookup"><span data-stu-id="f5203-165">78</span></span>

<span data-ttu-id="f5203-166">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f5203-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-167">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="f5203-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-168">79</span><span class="sxs-lookup"><span data-stu-id="f5203-168">79</span></span>

<span data-ttu-id="f5203-169">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="f5203-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-170">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="f5203-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-171">80</span><span class="sxs-lookup"><span data-stu-id="f5203-171">80</span></span>

<span data-ttu-id="f5203-172">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f5203-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-173">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="f5203-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-174">81</span><span class="sxs-lookup"><span data-stu-id="f5203-174">81</span></span>

<span data-ttu-id="f5203-175">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="f5203-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-176">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="f5203-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-177">82</span><span class="sxs-lookup"><span data-stu-id="f5203-177">82</span></span>

<span data-ttu-id="f5203-178">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="f5203-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-179">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="f5203-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-180">83</span><span class="sxs-lookup"><span data-stu-id="f5203-180">83</span></span>

<span data-ttu-id="f5203-181">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="f5203-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-182">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="f5203-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-183">84</span><span class="sxs-lookup"><span data-stu-id="f5203-183">84</span></span>

<span data-ttu-id="f5203-184">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="f5203-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-185">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="f5203-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-186">85</span><span class="sxs-lookup"><span data-stu-id="f5203-186">85</span></span>

<span data-ttu-id="f5203-187">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="f5203-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-188">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="f5203-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-189">86</span><span class="sxs-lookup"><span data-stu-id="f5203-189">86</span></span>

<span data-ttu-id="f5203-190">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="f5203-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-191">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="f5203-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-192">87</span><span class="sxs-lookup"><span data-stu-id="f5203-192">87</span></span>

<span data-ttu-id="f5203-193">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="f5203-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-194">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="f5203-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-195">88</span><span class="sxs-lookup"><span data-stu-id="f5203-195">88</span></span>

<span data-ttu-id="f5203-196">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="f5203-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-197">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="f5203-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-198">89</span><span class="sxs-lookup"><span data-stu-id="f5203-198">89</span></span>

<span data-ttu-id="f5203-199">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="f5203-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-200">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="f5203-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-201">90</span><span class="sxs-lookup"><span data-stu-id="f5203-201">90</span></span>

<span data-ttu-id="f5203-202">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="f5203-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-203">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="f5203-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-204">91</span><span class="sxs-lookup"><span data-stu-id="f5203-204">91</span></span>

<span data-ttu-id="f5203-205">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="f5203-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-206">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="f5203-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-207">92</span><span class="sxs-lookup"><span data-stu-id="f5203-207">92</span></span>

<span data-ttu-id="f5203-208">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="f5203-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-209">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="f5203-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-210">93</span><span class="sxs-lookup"><span data-stu-id="f5203-210">93</span></span>

<span data-ttu-id="f5203-211">Já existe.</span><span class="sxs-lookup"><span data-stu-id="f5203-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-212">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="f5203-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-213">94</span><span class="sxs-lookup"><span data-stu-id="f5203-213">94</span></span>

<span data-ttu-id="f5203-214">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="f5203-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-215">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="f5203-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-216">95</span><span class="sxs-lookup"><span data-stu-id="f5203-216">95</span></span>

<span data-ttu-id="f5203-217">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="f5203-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-218">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="f5203-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-219">96</span><span class="sxs-lookup"><span data-stu-id="f5203-219">96</span></span>

<span data-ttu-id="f5203-220">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="f5203-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-221">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="f5203-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-222">97</span><span class="sxs-lookup"><span data-stu-id="f5203-222">97</span></span>

<span data-ttu-id="f5203-223">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="f5203-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-224">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="f5203-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-225">98</span><span class="sxs-lookup"><span data-stu-id="f5203-225">98</span></span>

<span data-ttu-id="f5203-226">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="f5203-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-227">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="f5203-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-228">100</span><span class="sxs-lookup"><span data-stu-id="f5203-228">100</span></span>

<span data-ttu-id="f5203-229">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="f5203-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f5203-230">**Outras**</span><span class="sxs-lookup"><span data-stu-id="f5203-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f5203-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f5203-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5203-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5203-232">Remarks</span></span>

<span data-ttu-id="f5203-233">Ao descobrir a MTU do caminho e limitar os segmentos TCP a esse tamanho, o TCP pode eliminar a fragmentação em roteadores ao longo do caminho que conecta redes com MTUs diferentes.</span><span class="sxs-lookup"><span data-stu-id="f5203-233">By discovering the Path MTU and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="f5203-234">A fragmentação afeta negativamente a taxa de transferência de TCP e o congestionamento da rede.</span><span class="sxs-lookup"><span data-stu-id="f5203-234">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="f5203-235">Definir esse parâmetro como **false** faz com que um MTU de 576 bytes seja usado para todas as conexões que não são computadores na sub-rede local</span><span class="sxs-lookup"><span data-stu-id="f5203-235">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet</span></span>

## <a name="examples"></a><span data-ttu-id="f5203-236">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f5203-236">Examples</span></span>

<span data-ttu-id="f5203-237">A amostra [habilitar descoberta PMTU em todos os adaptadores de rede](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) do VBScript permite que um computador descubra automaticamente a unidade de transmissão máxima em uma rede.</span><span class="sxs-lookup"><span data-stu-id="f5203-237">The [Enable PMTU Discovery on all Network Adapters](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) VBScript sample enables a computer to automatically discover the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5203-238">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5203-238">Requirements</span></span>



| <span data-ttu-id="f5203-239">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5203-239">Requirement</span></span> | <span data-ttu-id="f5203-240">Valor</span><span class="sxs-lookup"><span data-stu-id="f5203-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5203-241">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5203-241">Minimum supported client</span></span><br/> | <span data-ttu-id="f5203-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5203-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f5203-243">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5203-243">Minimum supported server</span></span><br/> | <span data-ttu-id="f5203-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5203-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f5203-245">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5203-245">Namespace</span></span><br/>                | <span data-ttu-id="f5203-246">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f5203-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f5203-247">MOF</span><span class="sxs-lookup"><span data-stu-id="f5203-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5203-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5203-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5203-249">DLL</span><span class="sxs-lookup"><span data-stu-id="f5203-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5203-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5203-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5203-251">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5203-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5203-252">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="f5203-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f5203-253">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="f5203-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f5203-254">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="f5203-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f5203-255">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="f5203-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f5203-256">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="f5203-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

