---
description: O método estático da classe WMI SetNumForwardPackets é usado para definir o número de cabeçalhos de pacotes IP alocados para a fila de pacotes do roteador. Quando todos os cabeçalhos estiverem em uso, o roteador começará a descartar os pacotes da fila aleatoriamente.
ms.assetid: cadc7565-4cad-4e0f-a1eb-bf99d333bb28
ms.tgt_platform: multiple
title: Método SetNumForwardPackets da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetNumForwardPackets
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f46ecd62766b5df642dff1e52614171a513a8fca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646416"
---
# <a name="setnumforwardpackets-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="b773d-104">Método SetNumForwardPackets da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="b773d-104">SetNumForwardPackets method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="b773d-105">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetNumForwardPackets** é usado para definir o número de cabeçalhos de pacotes IP alocados para a fila de pacotes do roteador.</span><span class="sxs-lookup"><span data-stu-id="b773d-105">The **SetNumForwardPackets** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="b773d-106">Quando todos os cabeçalhos estiverem em uso, o roteador começará a descartar os pacotes da fila aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="b773d-106">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span>

<span data-ttu-id="b773d-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b773d-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b773d-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b773d-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b773d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b773d-109">Syntax</span></span>


```mof
uint32 SetNumForwardPackets(
  [in] uint32 NumForwardPackets
);
```



## <a name="parameters"></a><span data-ttu-id="b773d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b773d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b773d-111">*NumForwardPackets* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b773d-111">*NumForwardPackets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b773d-112">Número de cabeçalhos de pacote IP alocados para a fila de pacotes do roteador.</span><span class="sxs-lookup"><span data-stu-id="b773d-112">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="b773d-113">Isso deve ser pelo menos tão grande quanto o valor da propriedade [**ForwardBufferMemory**](win32-networkadapterconfiguration.md) dividido pelo tamanho máximo de dados IP das redes conectadas ao roteador.</span><span class="sxs-lookup"><span data-stu-id="b773d-113">This should be at least as large as the value of the [**ForwardBufferMemory**](win32-networkadapterconfiguration.md) property divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="b773d-114">Não deve ser maior do que o valor de **ForwardBufferMemory** dividido por 256, pois pelo menos 256 bytes de memória de buffer de encaminhamento são necessários para cada pacote.</span><span class="sxs-lookup"><span data-stu-id="b773d-114">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are required by each packet.</span></span> <span data-ttu-id="b773d-115">O número ideal de pacotes de encaminhamento para um determinado tamanho de **ForwardBufferMemory** depende do tipo de tráfego que é feito na rede e estará entre esses dois valores.</span><span class="sxs-lookup"><span data-stu-id="b773d-115">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic carried on the network, and will be somewhere between these two values.</span></span> <span data-ttu-id="b773d-116">Se o roteador estiver desabilitado, esse parâmetro será ignorado e nenhum cabeçalho será alocado.</span><span class="sxs-lookup"><span data-stu-id="b773d-116">If the router is disabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="b773d-117">Intervalo válido: 1-0xFFFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="b773d-117">Valid range: 1 - 0xFFFFFFFE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b773d-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b773d-118">Return value</span></span>

<span data-ttu-id="b773d-119">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="b773d-119">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="b773d-120">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b773d-120">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b773d-121">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b773d-121">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b773d-122">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="b773d-122">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-123">0</span><span class="sxs-lookup"><span data-stu-id="b773d-123">0</span></span>

<span data-ttu-id="b773d-124">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="b773d-124">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-125">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="b773d-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-126">1</span><span class="sxs-lookup"><span data-stu-id="b773d-126">1</span></span>

<span data-ttu-id="b773d-127">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="b773d-127">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-128">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="b773d-128">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-129">64</span><span class="sxs-lookup"><span data-stu-id="b773d-129">64</span></span>

<span data-ttu-id="b773d-130">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="b773d-130">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-131">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="b773d-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-132">65</span><span class="sxs-lookup"><span data-stu-id="b773d-132">65</span></span>

<span data-ttu-id="b773d-133">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="b773d-133">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-134">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="b773d-134">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-135">66</span><span class="sxs-lookup"><span data-stu-id="b773d-135">66</span></span>

<span data-ttu-id="b773d-136">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="b773d-136">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-137">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="b773d-137">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-138">67</span><span class="sxs-lookup"><span data-stu-id="b773d-138">67</span></span>

<span data-ttu-id="b773d-139">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="b773d-139">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-140">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="b773d-140">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-141">68</span><span class="sxs-lookup"><span data-stu-id="b773d-141">68</span></span>

<span data-ttu-id="b773d-142">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="b773d-142">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-143">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="b773d-143">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-144">69</span><span class="sxs-lookup"><span data-stu-id="b773d-144">69</span></span>

<span data-ttu-id="b773d-145">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="b773d-145">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-146">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="b773d-146">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-147">70</span><span class="sxs-lookup"><span data-stu-id="b773d-147">70</span></span>

<span data-ttu-id="b773d-148">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="b773d-148">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-149">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="b773d-149">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-150">71</span><span class="sxs-lookup"><span data-stu-id="b773d-150">71</span></span>

<span data-ttu-id="b773d-151">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="b773d-151">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-152">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="b773d-152">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-153">72</span><span class="sxs-lookup"><span data-stu-id="b773d-153">72</span></span>

<span data-ttu-id="b773d-154">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="b773d-154">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-155">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="b773d-155">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-156">73</span><span class="sxs-lookup"><span data-stu-id="b773d-156">73</span></span>

<span data-ttu-id="b773d-157">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="b773d-157">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-158">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="b773d-158">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-159">74</span><span class="sxs-lookup"><span data-stu-id="b773d-159">74</span></span>

<span data-ttu-id="b773d-160">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="b773d-160">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-161">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="b773d-161">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-162">75</span><span class="sxs-lookup"><span data-stu-id="b773d-162">75</span></span>

<span data-ttu-id="b773d-163">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="b773d-163">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-164">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="b773d-164">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-165">76</span><span class="sxs-lookup"><span data-stu-id="b773d-165">76</span></span>

<span data-ttu-id="b773d-166">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="b773d-166">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-167">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="b773d-167">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-168">77</span><span class="sxs-lookup"><span data-stu-id="b773d-168">77</span></span>

<span data-ttu-id="b773d-169">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="b773d-169">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-170">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="b773d-170">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-171">78</span><span class="sxs-lookup"><span data-stu-id="b773d-171">78</span></span>

<span data-ttu-id="b773d-172">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b773d-172">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-173">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="b773d-173">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-174">79</span><span class="sxs-lookup"><span data-stu-id="b773d-174">79</span></span>

<span data-ttu-id="b773d-175">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="b773d-175">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-176">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="b773d-176">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-177">80</span><span class="sxs-lookup"><span data-stu-id="b773d-177">80</span></span>

<span data-ttu-id="b773d-178">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b773d-178">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-179">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="b773d-179">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-180">81</span><span class="sxs-lookup"><span data-stu-id="b773d-180">81</span></span>

<span data-ttu-id="b773d-181">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="b773d-181">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-182">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="b773d-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-183">82</span><span class="sxs-lookup"><span data-stu-id="b773d-183">82</span></span>

<span data-ttu-id="b773d-184">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="b773d-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-185">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="b773d-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-186">83</span><span class="sxs-lookup"><span data-stu-id="b773d-186">83</span></span>

<span data-ttu-id="b773d-187">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="b773d-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-188">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="b773d-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-189">84</span><span class="sxs-lookup"><span data-stu-id="b773d-189">84</span></span>

<span data-ttu-id="b773d-190">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="b773d-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-191">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="b773d-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-192">85</span><span class="sxs-lookup"><span data-stu-id="b773d-192">85</span></span>

<span data-ttu-id="b773d-193">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="b773d-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-194">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="b773d-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-195">86</span><span class="sxs-lookup"><span data-stu-id="b773d-195">86</span></span>

<span data-ttu-id="b773d-196">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="b773d-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-197">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="b773d-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-198">87</span><span class="sxs-lookup"><span data-stu-id="b773d-198">87</span></span>

<span data-ttu-id="b773d-199">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="b773d-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-200">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="b773d-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-201">88</span><span class="sxs-lookup"><span data-stu-id="b773d-201">88</span></span>

<span data-ttu-id="b773d-202">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="b773d-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-203">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="b773d-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-204">89</span><span class="sxs-lookup"><span data-stu-id="b773d-204">89</span></span>

<span data-ttu-id="b773d-205">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="b773d-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-206">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="b773d-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-207">90</span><span class="sxs-lookup"><span data-stu-id="b773d-207">90</span></span>

<span data-ttu-id="b773d-208">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="b773d-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-209">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="b773d-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-210">91</span><span class="sxs-lookup"><span data-stu-id="b773d-210">91</span></span>

<span data-ttu-id="b773d-211">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="b773d-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-212">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="b773d-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-213">92</span><span class="sxs-lookup"><span data-stu-id="b773d-213">92</span></span>

<span data-ttu-id="b773d-214">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="b773d-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-215">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="b773d-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-216">93</span><span class="sxs-lookup"><span data-stu-id="b773d-216">93</span></span>

<span data-ttu-id="b773d-217">Já existe.</span><span class="sxs-lookup"><span data-stu-id="b773d-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-218">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="b773d-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-219">94</span><span class="sxs-lookup"><span data-stu-id="b773d-219">94</span></span>

<span data-ttu-id="b773d-220">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="b773d-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-221">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="b773d-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-222">95</span><span class="sxs-lookup"><span data-stu-id="b773d-222">95</span></span>

<span data-ttu-id="b773d-223">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="b773d-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-224">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="b773d-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-225">96</span><span class="sxs-lookup"><span data-stu-id="b773d-225">96</span></span>

<span data-ttu-id="b773d-226">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="b773d-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-227">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="b773d-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-228">97</span><span class="sxs-lookup"><span data-stu-id="b773d-228">97</span></span>

<span data-ttu-id="b773d-229">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="b773d-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-230">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="b773d-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-231">98</span><span class="sxs-lookup"><span data-stu-id="b773d-231">98</span></span>

<span data-ttu-id="b773d-232">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="b773d-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-233">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="b773d-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-234">100</span><span class="sxs-lookup"><span data-stu-id="b773d-234">100</span></span>

<span data-ttu-id="b773d-235">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="b773d-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b773d-236">**Outras**</span><span class="sxs-lookup"><span data-stu-id="b773d-236">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="b773d-237">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="b773d-237">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b773d-238">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b773d-238">Examples</span></span>

<span data-ttu-id="b773d-239">A amostra [Modificar o número de pacotes encaminhados permitidos](https://Gallery.TechNet.Microsoft.Com/4123c28e-25c4-444e-818b-67bdbcc0cd4c) do VBScript configura o número de pacotes de encaminhamento alocados para a fila de pacotes do roteador.</span><span class="sxs-lookup"><span data-stu-id="b773d-239">The [Modify the Number of Allowed Forward Packets](https://Gallery.TechNet.Microsoft.Com/4123c28e-25c4-444e-818b-67bdbcc0cd4c) VBScript sample configures the number of forward packets allocated to the router packet queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="b773d-240">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b773d-240">Requirements</span></span>



| <span data-ttu-id="b773d-241">Requisito</span><span class="sxs-lookup"><span data-stu-id="b773d-241">Requirement</span></span> | <span data-ttu-id="b773d-242">Valor</span><span class="sxs-lookup"><span data-stu-id="b773d-242">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b773d-243">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b773d-243">Minimum supported client</span></span><br/> | <span data-ttu-id="b773d-244">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b773d-244">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b773d-245">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b773d-245">Minimum supported server</span></span><br/> | <span data-ttu-id="b773d-246">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b773d-246">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b773d-247">Namespace</span><span class="sxs-lookup"><span data-stu-id="b773d-247">Namespace</span></span><br/>                | <span data-ttu-id="b773d-248">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b773d-248">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b773d-249">MOF</span><span class="sxs-lookup"><span data-stu-id="b773d-249">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b773d-250"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b773d-250"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b773d-251">DLL</span><span class="sxs-lookup"><span data-stu-id="b773d-251">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b773d-252"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b773d-252"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b773d-253">Confira também</span><span class="sxs-lookup"><span data-stu-id="b773d-253">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b773d-254">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="b773d-254">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b773d-255">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="b773d-255">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="b773d-256">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="b773d-256">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="b773d-257">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="b773d-257">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="b773d-258">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="b773d-258">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

