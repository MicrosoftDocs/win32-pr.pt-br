---
description: O método estático da classe WMI SetKeepAliveInterval é usado para definir o intervalo que separa as retransmissões Keep Alive até que uma resposta seja recebida.
ms.assetid: 83415000-124a-44a7-93cc-92ce9df143aa
ms.tgt_platform: multiple
title: Método SetKeepAliveInterval da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveInterval
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ce6a1491fd9e414f503d0165216794c67db0e97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089326"
---
# <a name="setkeepaliveinterval-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="683b1-103">Método SetKeepAliveInterval da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="683b1-103">SetKeepAliveInterval method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="683b1-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetKeepAliveInterval** é usado para definir o intervalo que separa as retransmissões Keep Alive até que uma resposta seja recebida.</span><span class="sxs-lookup"><span data-stu-id="683b1-104">The **SetKeepAliveInterval** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the interval separating Keep Alive Retransmissions until a response is received.</span></span>

<span data-ttu-id="683b1-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="683b1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="683b1-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="683b1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="683b1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="683b1-107">Syntax</span></span>


```mof
uint32 SetKeepAliveInterval(
  [in] uint32 KeepAliveInterval
);
```



## <a name="parameters"></a><span data-ttu-id="683b1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="683b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="683b1-109">*KeepAliveInterval* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="683b1-109">*KeepAliveInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="683b1-110">Valor, em milissegundos, para o intervalo que separa as retransmissões Keep Alive até que uma resposta seja recebida.</span><span class="sxs-lookup"><span data-stu-id="683b1-110">Value, in milliseconds, for the interval separating Keep Alive Retransmissions until a response is received.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="683b1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="683b1-111">Return value</span></span>

<span data-ttu-id="683b1-112">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="683b1-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="683b1-113">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="683b1-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="683b1-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="683b1-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="683b1-115">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="683b1-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-116">0</span><span class="sxs-lookup"><span data-stu-id="683b1-116">0</span></span>

<span data-ttu-id="683b1-117">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="683b1-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-118">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="683b1-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-119">1</span><span class="sxs-lookup"><span data-stu-id="683b1-119">1</span></span>

<span data-ttu-id="683b1-120">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="683b1-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-121">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="683b1-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-122">64</span><span class="sxs-lookup"><span data-stu-id="683b1-122">64</span></span>

<span data-ttu-id="683b1-123">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="683b1-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-124">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="683b1-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-125">65</span><span class="sxs-lookup"><span data-stu-id="683b1-125">65</span></span>

<span data-ttu-id="683b1-126">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="683b1-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-127">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="683b1-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-128">66</span><span class="sxs-lookup"><span data-stu-id="683b1-128">66</span></span>

<span data-ttu-id="683b1-129">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="683b1-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-130">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="683b1-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-131">67</span><span class="sxs-lookup"><span data-stu-id="683b1-131">67</span></span>

<span data-ttu-id="683b1-132">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="683b1-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-133">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="683b1-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-134">68</span><span class="sxs-lookup"><span data-stu-id="683b1-134">68</span></span>

<span data-ttu-id="683b1-135">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="683b1-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-136">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="683b1-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-137">69</span><span class="sxs-lookup"><span data-stu-id="683b1-137">69</span></span>

<span data-ttu-id="683b1-138">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="683b1-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-139">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="683b1-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-140">70</span><span class="sxs-lookup"><span data-stu-id="683b1-140">70</span></span>

<span data-ttu-id="683b1-141">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="683b1-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-142">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="683b1-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-143">71</span><span class="sxs-lookup"><span data-stu-id="683b1-143">71</span></span>

<span data-ttu-id="683b1-144">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="683b1-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-145">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="683b1-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-146">72</span><span class="sxs-lookup"><span data-stu-id="683b1-146">72</span></span>

<span data-ttu-id="683b1-147">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="683b1-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-148">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="683b1-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-149">73</span><span class="sxs-lookup"><span data-stu-id="683b1-149">73</span></span>

<span data-ttu-id="683b1-150">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="683b1-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-151">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="683b1-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-152">74</span><span class="sxs-lookup"><span data-stu-id="683b1-152">74</span></span>

<span data-ttu-id="683b1-153">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="683b1-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-154">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="683b1-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-155">75</span><span class="sxs-lookup"><span data-stu-id="683b1-155">75</span></span>

<span data-ttu-id="683b1-156">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="683b1-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-157">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="683b1-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-158">76</span><span class="sxs-lookup"><span data-stu-id="683b1-158">76</span></span>

<span data-ttu-id="683b1-159">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="683b1-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-160">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="683b1-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-161">77</span><span class="sxs-lookup"><span data-stu-id="683b1-161">77</span></span>

<span data-ttu-id="683b1-162">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="683b1-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-163">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="683b1-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-164">78</span><span class="sxs-lookup"><span data-stu-id="683b1-164">78</span></span>

<span data-ttu-id="683b1-165">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="683b1-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-166">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="683b1-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-167">79</span><span class="sxs-lookup"><span data-stu-id="683b1-167">79</span></span>

<span data-ttu-id="683b1-168">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="683b1-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-169">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="683b1-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-170">80</span><span class="sxs-lookup"><span data-stu-id="683b1-170">80</span></span>

<span data-ttu-id="683b1-171">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="683b1-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-172">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="683b1-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-173">81</span><span class="sxs-lookup"><span data-stu-id="683b1-173">81</span></span>

<span data-ttu-id="683b1-174">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="683b1-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-175">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="683b1-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-176">82</span><span class="sxs-lookup"><span data-stu-id="683b1-176">82</span></span>

<span data-ttu-id="683b1-177">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="683b1-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-178">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="683b1-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-179">83</span><span class="sxs-lookup"><span data-stu-id="683b1-179">83</span></span>

<span data-ttu-id="683b1-180">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="683b1-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-181">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="683b1-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-182">84</span><span class="sxs-lookup"><span data-stu-id="683b1-182">84</span></span>

<span data-ttu-id="683b1-183">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="683b1-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-184">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="683b1-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-185">85</span><span class="sxs-lookup"><span data-stu-id="683b1-185">85</span></span>

<span data-ttu-id="683b1-186">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="683b1-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-187">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="683b1-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-188">86</span><span class="sxs-lookup"><span data-stu-id="683b1-188">86</span></span>

<span data-ttu-id="683b1-189">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="683b1-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-190">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="683b1-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-191">87</span><span class="sxs-lookup"><span data-stu-id="683b1-191">87</span></span>

<span data-ttu-id="683b1-192">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="683b1-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-193">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="683b1-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-194">88</span><span class="sxs-lookup"><span data-stu-id="683b1-194">88</span></span>

<span data-ttu-id="683b1-195">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="683b1-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-196">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="683b1-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-197">89</span><span class="sxs-lookup"><span data-stu-id="683b1-197">89</span></span>

<span data-ttu-id="683b1-198">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="683b1-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-199">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="683b1-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-200">90</span><span class="sxs-lookup"><span data-stu-id="683b1-200">90</span></span>

<span data-ttu-id="683b1-201">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="683b1-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-202">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="683b1-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-203">91</span><span class="sxs-lookup"><span data-stu-id="683b1-203">91</span></span>

<span data-ttu-id="683b1-204">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="683b1-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-205">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="683b1-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-206">92</span><span class="sxs-lookup"><span data-stu-id="683b1-206">92</span></span>

<span data-ttu-id="683b1-207">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="683b1-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-208">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="683b1-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-209">93</span><span class="sxs-lookup"><span data-stu-id="683b1-209">93</span></span>

<span data-ttu-id="683b1-210">Já existe.</span><span class="sxs-lookup"><span data-stu-id="683b1-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-211">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="683b1-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-212">94</span><span class="sxs-lookup"><span data-stu-id="683b1-212">94</span></span>

<span data-ttu-id="683b1-213">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="683b1-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-214">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="683b1-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-215">95</span><span class="sxs-lookup"><span data-stu-id="683b1-215">95</span></span>

<span data-ttu-id="683b1-216">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="683b1-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-217">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="683b1-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-218">96</span><span class="sxs-lookup"><span data-stu-id="683b1-218">96</span></span>

<span data-ttu-id="683b1-219">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="683b1-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-220">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="683b1-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-221">97</span><span class="sxs-lookup"><span data-stu-id="683b1-221">97</span></span>

<span data-ttu-id="683b1-222">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="683b1-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-223">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="683b1-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-224">98</span><span class="sxs-lookup"><span data-stu-id="683b1-224">98</span></span>

<span data-ttu-id="683b1-225">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="683b1-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-226">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="683b1-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-227">100</span><span class="sxs-lookup"><span data-stu-id="683b1-227">100</span></span>

<span data-ttu-id="683b1-228">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="683b1-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="683b1-229">**Outras**</span><span class="sxs-lookup"><span data-stu-id="683b1-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="683b1-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="683b1-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="683b1-231">Comentários</span><span class="sxs-lookup"><span data-stu-id="683b1-231">Remarks</span></span>

<span data-ttu-id="683b1-232">Depois que uma resposta é recebida, o atraso até a próxima transmissão Keep Alive é novamente controlado pelo valor da propriedade [**KeepAliveTime**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="683b1-232">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of the [**KeepAliveTime**](win32-networkadapterconfiguration.md) property.</span></span> <span data-ttu-id="683b1-233">A conexão é encerrada depois que o número de retransmissões especificado pela propriedade **TcpMaxDataRetransmissions** não foi respondido</span><span class="sxs-lookup"><span data-stu-id="683b1-233">The connection is terminated after the number of retransmissions specified by the **TcpMaxDataRetransmissions** property have gone unanswered</span></span>

## <a name="examples"></a><span data-ttu-id="683b1-234">Exemplos</span><span class="sxs-lookup"><span data-stu-id="683b1-234">Examples</span></span>

<span data-ttu-id="683b1-235">A amostra [Modificar o intervalo de Keep Alive para todos os adaptadores de rede](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) do VBScript configura o intervalo de Keep Alive para todos os adaptadores de rede em um computador para 300, 00 milissegundos (5 minutos).</span><span class="sxs-lookup"><span data-stu-id="683b1-235">The [Modify the Keep Alive Interval for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) VBScript sample configures the keep alive interval for all network adapters on a computer to 300,00 milliseconds (5 minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="683b1-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="683b1-236">Requirements</span></span>



| <span data-ttu-id="683b1-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="683b1-237">Requirement</span></span> | <span data-ttu-id="683b1-238">Valor</span><span class="sxs-lookup"><span data-stu-id="683b1-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="683b1-239">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="683b1-239">Minimum supported client</span></span><br/> | <span data-ttu-id="683b1-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="683b1-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="683b1-241">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="683b1-241">Minimum supported server</span></span><br/> | <span data-ttu-id="683b1-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="683b1-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="683b1-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="683b1-243">Namespace</span></span><br/>                | <span data-ttu-id="683b1-244">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="683b1-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="683b1-245">MOF</span><span class="sxs-lookup"><span data-stu-id="683b1-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="683b1-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="683b1-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="683b1-247">DLL</span><span class="sxs-lookup"><span data-stu-id="683b1-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="683b1-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="683b1-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="683b1-249">Confira também</span><span class="sxs-lookup"><span data-stu-id="683b1-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="683b1-250">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="683b1-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="683b1-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="683b1-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="683b1-252">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="683b1-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="683b1-253">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="683b1-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="683b1-254">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="683b1-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

