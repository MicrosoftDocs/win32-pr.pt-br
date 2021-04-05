---
description: O método estático da classe WMI SetDefaultTTL é usado para definir o valor de TTL (vida útil) padrão no cabeçalho de pacotes IP de saída.
ms.assetid: 74b060de-512c-407e-9f93-c3b496f8d09d
ms.tgt_platform: multiple
title: Método SetDefaultTTL da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTTL
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 253048b44a836f92646124fb972fe32c135e3b9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826106"
---
# <a name="setdefaultttl-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="70ccc-103">Método SetDefaultTTL da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="70ccc-103">SetDefaultTTL method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="70ccc-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultTTL** é usado para definir o valor de TTL (vida útil) padrão no cabeçalho de pacotes IP de saída.</span><span class="sxs-lookup"><span data-stu-id="70ccc-104">The **SetDefaultTTL** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span>

<span data-ttu-id="70ccc-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="70ccc-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="70ccc-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="70ccc-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="70ccc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70ccc-107">Syntax</span></span>


```mof
uint32 SetDefaultTTL(
  [in] uint8 DefaultTTL
);
```



## <a name="parameters"></a><span data-ttu-id="70ccc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70ccc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70ccc-109">*DefaultTtl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70ccc-109">*DefaultTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-110">Valor de vida útil definido no cabeçalho de pacotes de IP de saída.</span><span class="sxs-lookup"><span data-stu-id="70ccc-110">Time to Live value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="70ccc-111">O valor padrão é 32; Intervalo válido: 1-255</span><span class="sxs-lookup"><span data-stu-id="70ccc-111">The default value is 32; Valid range: 1 - 255</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70ccc-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70ccc-112">Return value</span></span>

<span data-ttu-id="70ccc-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="70ccc-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="70ccc-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="70ccc-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="70ccc-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="70ccc-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="70ccc-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="70ccc-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-117">0</span><span class="sxs-lookup"><span data-stu-id="70ccc-117">0</span></span>

<span data-ttu-id="70ccc-118">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="70ccc-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-119">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="70ccc-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-120">1</span><span class="sxs-lookup"><span data-stu-id="70ccc-120">1</span></span>

<span data-ttu-id="70ccc-121">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="70ccc-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-122">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="70ccc-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-123">64</span><span class="sxs-lookup"><span data-stu-id="70ccc-123">64</span></span>

<span data-ttu-id="70ccc-124">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="70ccc-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-125">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="70ccc-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-126">65</span><span class="sxs-lookup"><span data-stu-id="70ccc-126">65</span></span>

<span data-ttu-id="70ccc-127">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="70ccc-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-128">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="70ccc-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-129">66</span><span class="sxs-lookup"><span data-stu-id="70ccc-129">66</span></span>

<span data-ttu-id="70ccc-130">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="70ccc-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-131">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="70ccc-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-132">67</span><span class="sxs-lookup"><span data-stu-id="70ccc-132">67</span></span>

<span data-ttu-id="70ccc-133">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="70ccc-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-134">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="70ccc-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-135">68</span><span class="sxs-lookup"><span data-stu-id="70ccc-135">68</span></span>

<span data-ttu-id="70ccc-136">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="70ccc-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-137">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="70ccc-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-138">69</span><span class="sxs-lookup"><span data-stu-id="70ccc-138">69</span></span>

<span data-ttu-id="70ccc-139">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="70ccc-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-140">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="70ccc-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-141">70</span><span class="sxs-lookup"><span data-stu-id="70ccc-141">70</span></span>

<span data-ttu-id="70ccc-142">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="70ccc-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-143">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="70ccc-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-144">71</span><span class="sxs-lookup"><span data-stu-id="70ccc-144">71</span></span>

<span data-ttu-id="70ccc-145">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="70ccc-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-146">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="70ccc-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-147">72</span><span class="sxs-lookup"><span data-stu-id="70ccc-147">72</span></span>

<span data-ttu-id="70ccc-148">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="70ccc-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-149">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="70ccc-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-150">73</span><span class="sxs-lookup"><span data-stu-id="70ccc-150">73</span></span>

<span data-ttu-id="70ccc-151">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="70ccc-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-152">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="70ccc-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-153">74</span><span class="sxs-lookup"><span data-stu-id="70ccc-153">74</span></span>

<span data-ttu-id="70ccc-154">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="70ccc-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-155">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="70ccc-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-156">75</span><span class="sxs-lookup"><span data-stu-id="70ccc-156">75</span></span>

<span data-ttu-id="70ccc-157">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="70ccc-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-158">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="70ccc-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-159">76</span><span class="sxs-lookup"><span data-stu-id="70ccc-159">76</span></span>

<span data-ttu-id="70ccc-160">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="70ccc-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-161">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="70ccc-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-162">77</span><span class="sxs-lookup"><span data-stu-id="70ccc-162">77</span></span>

<span data-ttu-id="70ccc-163">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="70ccc-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-164">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="70ccc-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-165">78</span><span class="sxs-lookup"><span data-stu-id="70ccc-165">78</span></span>

<span data-ttu-id="70ccc-166">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="70ccc-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-167">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="70ccc-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-168">79</span><span class="sxs-lookup"><span data-stu-id="70ccc-168">79</span></span>

<span data-ttu-id="70ccc-169">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="70ccc-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-170">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="70ccc-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-171">80</span><span class="sxs-lookup"><span data-stu-id="70ccc-171">80</span></span>

<span data-ttu-id="70ccc-172">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="70ccc-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-173">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="70ccc-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-174">81</span><span class="sxs-lookup"><span data-stu-id="70ccc-174">81</span></span>

<span data-ttu-id="70ccc-175">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="70ccc-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-176">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="70ccc-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-177">82</span><span class="sxs-lookup"><span data-stu-id="70ccc-177">82</span></span>

<span data-ttu-id="70ccc-178">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="70ccc-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-179">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="70ccc-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-180">83</span><span class="sxs-lookup"><span data-stu-id="70ccc-180">83</span></span>

<span data-ttu-id="70ccc-181">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="70ccc-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-182">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="70ccc-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-183">84</span><span class="sxs-lookup"><span data-stu-id="70ccc-183">84</span></span>

<span data-ttu-id="70ccc-184">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="70ccc-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-185">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="70ccc-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-186">85</span><span class="sxs-lookup"><span data-stu-id="70ccc-186">85</span></span>

<span data-ttu-id="70ccc-187">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="70ccc-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-188">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="70ccc-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-189">86</span><span class="sxs-lookup"><span data-stu-id="70ccc-189">86</span></span>

<span data-ttu-id="70ccc-190">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="70ccc-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-191">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="70ccc-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-192">87</span><span class="sxs-lookup"><span data-stu-id="70ccc-192">87</span></span>

<span data-ttu-id="70ccc-193">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="70ccc-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-194">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="70ccc-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-195">88</span><span class="sxs-lookup"><span data-stu-id="70ccc-195">88</span></span>

<span data-ttu-id="70ccc-196">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="70ccc-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-197">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="70ccc-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-198">89</span><span class="sxs-lookup"><span data-stu-id="70ccc-198">89</span></span>

<span data-ttu-id="70ccc-199">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="70ccc-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-200">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="70ccc-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-201">90</span><span class="sxs-lookup"><span data-stu-id="70ccc-201">90</span></span>

<span data-ttu-id="70ccc-202">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="70ccc-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-203">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="70ccc-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-204">91</span><span class="sxs-lookup"><span data-stu-id="70ccc-204">91</span></span>

<span data-ttu-id="70ccc-205">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="70ccc-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-206">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="70ccc-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-207">92</span><span class="sxs-lookup"><span data-stu-id="70ccc-207">92</span></span>

<span data-ttu-id="70ccc-208">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="70ccc-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-209">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="70ccc-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-210">93</span><span class="sxs-lookup"><span data-stu-id="70ccc-210">93</span></span>

<span data-ttu-id="70ccc-211">Já existe.</span><span class="sxs-lookup"><span data-stu-id="70ccc-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-212">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="70ccc-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-213">94</span><span class="sxs-lookup"><span data-stu-id="70ccc-213">94</span></span>

<span data-ttu-id="70ccc-214">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="70ccc-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-215">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="70ccc-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-216">95</span><span class="sxs-lookup"><span data-stu-id="70ccc-216">95</span></span>

<span data-ttu-id="70ccc-217">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="70ccc-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-218">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="70ccc-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-219">96</span><span class="sxs-lookup"><span data-stu-id="70ccc-219">96</span></span>

<span data-ttu-id="70ccc-220">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="70ccc-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-221">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="70ccc-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-222">97</span><span class="sxs-lookup"><span data-stu-id="70ccc-222">97</span></span>

<span data-ttu-id="70ccc-223">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="70ccc-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-224">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="70ccc-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-225">98</span><span class="sxs-lookup"><span data-stu-id="70ccc-225">98</span></span>

<span data-ttu-id="70ccc-226">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="70ccc-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-227">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="70ccc-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-228">100</span><span class="sxs-lookup"><span data-stu-id="70ccc-228">100</span></span>

<span data-ttu-id="70ccc-229">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="70ccc-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="70ccc-230">**Outras**</span><span class="sxs-lookup"><span data-stu-id="70ccc-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="70ccc-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="70ccc-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70ccc-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="70ccc-232">Remarks</span></span>

<span data-ttu-id="70ccc-233">O TTL especifica o número de roteadores que um pacote IP pode passar para alcançar seu destino antes de ser Descartado.</span><span class="sxs-lookup"><span data-stu-id="70ccc-233">The TTL specifies the number of routers an IP packet may pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="70ccc-234">Cada roteador decrementa a contagem TTL de um pacote por um e descarta os pacotes com um TTL igual a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="70ccc-234">Each router decrements the TTL count of a packet by one and discards the packets with a TTL of 0 (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="70ccc-235">Exemplos</span><span class="sxs-lookup"><span data-stu-id="70ccc-235">Examples</span></span>

<span data-ttu-id="70ccc-236">O exemplo de [Modificar o tempo de vida padrão para todos os adaptadores de rede do](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) VBScript usa **SetDefaultTTL** para definir o valor de vida útil padrão no cabeçalho de pacotes IP de saída para 64</span><span class="sxs-lookup"><span data-stu-id="70ccc-236">The [Modify the Default Time-to-Live for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) VBScript sample uses **SetDefaultTTL** to set the default time-to-live value in the header of outgoing IP packets to 64</span></span>

## <a name="requirements"></a><span data-ttu-id="70ccc-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70ccc-237">Requirements</span></span>



| <span data-ttu-id="70ccc-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="70ccc-238">Requirement</span></span> | <span data-ttu-id="70ccc-239">Valor</span><span class="sxs-lookup"><span data-stu-id="70ccc-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70ccc-240">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70ccc-240">Minimum supported client</span></span><br/> | <span data-ttu-id="70ccc-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70ccc-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="70ccc-242">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70ccc-242">Minimum supported server</span></span><br/> | <span data-ttu-id="70ccc-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70ccc-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="70ccc-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="70ccc-244">Namespace</span></span><br/>                | <span data-ttu-id="70ccc-245">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="70ccc-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="70ccc-246">MOF</span><span class="sxs-lookup"><span data-stu-id="70ccc-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70ccc-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70ccc-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="70ccc-248">DLL</span><span class="sxs-lookup"><span data-stu-id="70ccc-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70ccc-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70ccc-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70ccc-250">Confira também</span><span class="sxs-lookup"><span data-stu-id="70ccc-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70ccc-251">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="70ccc-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="70ccc-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="70ccc-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="70ccc-253">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="70ccc-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="70ccc-254">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="70ccc-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="70ccc-255">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="70ccc-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

