---
description: O método estático da classe WMI SetIPUseZeroBroadcast é usado para definir o uso de difusão zero de IP.
ms.assetid: d20ac6fc-a5d5-4ad9-a2a5-65142b4c7d02
ms.tgt_platform: multiple
title: Método SetIPUseZeroBroadcast da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPUseZeroBroadcast
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 564f122242407f4d6f5dd28da9fd4d151ab6b47f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089328"
---
# <a name="setipusezerobroadcast-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="1b85e-103">Método SetIPUseZeroBroadcast da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b85e-103">SetIPUseZeroBroadcast method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="1b85e-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetIPUseZeroBroadcast** é usado para definir o uso de difusão zero de IP.</span><span class="sxs-lookup"><span data-stu-id="1b85e-104">The **SetIPUseZeroBroadcast** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set IP zero broadcast usage.</span></span>

<span data-ttu-id="1b85e-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1b85e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1b85e-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1b85e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b85e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b85e-107">Syntax</span></span>


```mof
uint32 SetIPUseZeroBroadcast(
  [in] boolean IPUseZeroBroadcast
);
```



## <a name="parameters"></a><span data-ttu-id="1b85e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b85e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b85e-109">*IPUseZeroBroadcast* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b85e-109">*IPUseZeroBroadcast* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-110">Se **for true**, a difusão de IP zero será usada.</span><span class="sxs-lookup"><span data-stu-id="1b85e-110">If **true**, IP zero broadcast is used.</span></span> <span data-ttu-id="1b85e-111">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="1b85e-111">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b85e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b85e-112">Return value</span></span>

<span data-ttu-id="1b85e-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="1b85e-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="1b85e-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1b85e-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1b85e-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1b85e-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1b85e-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="1b85e-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-117">0</span><span class="sxs-lookup"><span data-stu-id="1b85e-117">0</span></span>

<span data-ttu-id="1b85e-118">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="1b85e-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-119">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="1b85e-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-120">1</span><span class="sxs-lookup"><span data-stu-id="1b85e-120">1</span></span>

<span data-ttu-id="1b85e-121">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="1b85e-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-122">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="1b85e-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-123">64</span><span class="sxs-lookup"><span data-stu-id="1b85e-123">64</span></span>

<span data-ttu-id="1b85e-124">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="1b85e-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-125">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="1b85e-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-126">65</span><span class="sxs-lookup"><span data-stu-id="1b85e-126">65</span></span>

<span data-ttu-id="1b85e-127">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="1b85e-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-128">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="1b85e-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-129">66</span><span class="sxs-lookup"><span data-stu-id="1b85e-129">66</span></span>

<span data-ttu-id="1b85e-130">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="1b85e-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-131">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="1b85e-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-132">67</span><span class="sxs-lookup"><span data-stu-id="1b85e-132">67</span></span>

<span data-ttu-id="1b85e-133">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="1b85e-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-134">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="1b85e-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-135">68</span><span class="sxs-lookup"><span data-stu-id="1b85e-135">68</span></span>

<span data-ttu-id="1b85e-136">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="1b85e-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-137">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="1b85e-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-138">69</span><span class="sxs-lookup"><span data-stu-id="1b85e-138">69</span></span>

<span data-ttu-id="1b85e-139">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="1b85e-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-140">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="1b85e-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-141">70</span><span class="sxs-lookup"><span data-stu-id="1b85e-141">70</span></span>

<span data-ttu-id="1b85e-142">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="1b85e-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-143">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="1b85e-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-144">71</span><span class="sxs-lookup"><span data-stu-id="1b85e-144">71</span></span>

<span data-ttu-id="1b85e-145">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="1b85e-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-146">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="1b85e-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-147">72</span><span class="sxs-lookup"><span data-stu-id="1b85e-147">72</span></span>

<span data-ttu-id="1b85e-148">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="1b85e-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-149">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="1b85e-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-150">73</span><span class="sxs-lookup"><span data-stu-id="1b85e-150">73</span></span>

<span data-ttu-id="1b85e-151">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="1b85e-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-152">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="1b85e-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-153">74</span><span class="sxs-lookup"><span data-stu-id="1b85e-153">74</span></span>

<span data-ttu-id="1b85e-154">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="1b85e-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-155">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="1b85e-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-156">75</span><span class="sxs-lookup"><span data-stu-id="1b85e-156">75</span></span>

<span data-ttu-id="1b85e-157">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="1b85e-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-158">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="1b85e-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-159">76</span><span class="sxs-lookup"><span data-stu-id="1b85e-159">76</span></span>

<span data-ttu-id="1b85e-160">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="1b85e-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-161">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="1b85e-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-162">77</span><span class="sxs-lookup"><span data-stu-id="1b85e-162">77</span></span>

<span data-ttu-id="1b85e-163">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="1b85e-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-164">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="1b85e-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-165">78</span><span class="sxs-lookup"><span data-stu-id="1b85e-165">78</span></span>

<span data-ttu-id="1b85e-166">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="1b85e-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-167">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="1b85e-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-168">79</span><span class="sxs-lookup"><span data-stu-id="1b85e-168">79</span></span>

<span data-ttu-id="1b85e-169">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="1b85e-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-170">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="1b85e-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-171">80</span><span class="sxs-lookup"><span data-stu-id="1b85e-171">80</span></span>

<span data-ttu-id="1b85e-172">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1b85e-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-173">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="1b85e-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-174">81</span><span class="sxs-lookup"><span data-stu-id="1b85e-174">81</span></span>

<span data-ttu-id="1b85e-175">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="1b85e-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-176">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="1b85e-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-177">82</span><span class="sxs-lookup"><span data-stu-id="1b85e-177">82</span></span>

<span data-ttu-id="1b85e-178">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="1b85e-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-179">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="1b85e-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-180">83</span><span class="sxs-lookup"><span data-stu-id="1b85e-180">83</span></span>

<span data-ttu-id="1b85e-181">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="1b85e-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-182">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="1b85e-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-183">84</span><span class="sxs-lookup"><span data-stu-id="1b85e-183">84</span></span>

<span data-ttu-id="1b85e-184">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="1b85e-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-185">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="1b85e-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-186">85</span><span class="sxs-lookup"><span data-stu-id="1b85e-186">85</span></span>

<span data-ttu-id="1b85e-187">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="1b85e-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-188">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="1b85e-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-189">86</span><span class="sxs-lookup"><span data-stu-id="1b85e-189">86</span></span>

<span data-ttu-id="1b85e-190">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="1b85e-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-191">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="1b85e-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-192">87</span><span class="sxs-lookup"><span data-stu-id="1b85e-192">87</span></span>

<span data-ttu-id="1b85e-193">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="1b85e-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-194">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="1b85e-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-195">88</span><span class="sxs-lookup"><span data-stu-id="1b85e-195">88</span></span>

<span data-ttu-id="1b85e-196">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="1b85e-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-197">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="1b85e-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-198">89</span><span class="sxs-lookup"><span data-stu-id="1b85e-198">89</span></span>

<span data-ttu-id="1b85e-199">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="1b85e-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-200">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="1b85e-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-201">90</span><span class="sxs-lookup"><span data-stu-id="1b85e-201">90</span></span>

<span data-ttu-id="1b85e-202">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="1b85e-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-203">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="1b85e-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-204">91</span><span class="sxs-lookup"><span data-stu-id="1b85e-204">91</span></span>

<span data-ttu-id="1b85e-205">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="1b85e-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-206">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="1b85e-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-207">92</span><span class="sxs-lookup"><span data-stu-id="1b85e-207">92</span></span>

<span data-ttu-id="1b85e-208">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="1b85e-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-209">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="1b85e-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-210">93</span><span class="sxs-lookup"><span data-stu-id="1b85e-210">93</span></span>

<span data-ttu-id="1b85e-211">Já existe.</span><span class="sxs-lookup"><span data-stu-id="1b85e-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-212">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="1b85e-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-213">94</span><span class="sxs-lookup"><span data-stu-id="1b85e-213">94</span></span>

<span data-ttu-id="1b85e-214">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="1b85e-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-215">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="1b85e-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-216">95</span><span class="sxs-lookup"><span data-stu-id="1b85e-216">95</span></span>

<span data-ttu-id="1b85e-217">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="1b85e-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-218">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="1b85e-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-219">96</span><span class="sxs-lookup"><span data-stu-id="1b85e-219">96</span></span>

<span data-ttu-id="1b85e-220">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="1b85e-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-221">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="1b85e-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-222">97</span><span class="sxs-lookup"><span data-stu-id="1b85e-222">97</span></span>

<span data-ttu-id="1b85e-223">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="1b85e-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-224">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="1b85e-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-225">98</span><span class="sxs-lookup"><span data-stu-id="1b85e-225">98</span></span>

<span data-ttu-id="1b85e-226">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="1b85e-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-227">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="1b85e-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-228">100</span><span class="sxs-lookup"><span data-stu-id="1b85e-228">100</span></span>

<span data-ttu-id="1b85e-229">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="1b85e-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1b85e-230">**Outras**</span><span class="sxs-lookup"><span data-stu-id="1b85e-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1b85e-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="1b85e-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b85e-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b85e-232">Remarks</span></span>

<span data-ttu-id="1b85e-233">Se o parâmetro *IPUseZeroBroadcast* for definido como **true**, o IP usará difusões sem zero (0.0.0.0) em vez de uma difusão (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="1b85e-233">If the *IPUseZeroBroadcast* parameter is set to **TRUE**, then IP will use zero-broadcasts (0.0.0.0) instead of one-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="1b85e-234">A maioria dos sistemas usa difusões de uma, mas os sistemas derivados de implementações do BSD usam difusões sem zeros.</span><span class="sxs-lookup"><span data-stu-id="1b85e-234">Most systems use one-broadcasts, but systems derived from BSD implementations use zero-broadcasts.</span></span> <span data-ttu-id="1b85e-235">Os sistemas que usam difusões diferentes não interoperarão na mesma rede.</span><span class="sxs-lookup"><span data-stu-id="1b85e-235">Systems that use different broadcasts will not interoperate on the same network.</span></span>

## <a name="examples"></a><span data-ttu-id="1b85e-236">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1b85e-236">Examples</span></span>

<span data-ttu-id="1b85e-237">A amostra [modificar Zero-Broadcast usar para todos os adaptadores de rede do](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3) VBScript configura um computador para usar difusões sem zeros (0.0.0.0) em vez de uma difusão (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="1b85e-237">The [Modify Zero-Broadcast Use for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3) VBScript sample configures a computer to use zero-broadcasts (0.0.0.0) rather than one-broadcasts (255.255.255.255).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b85e-238">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b85e-238">Requirements</span></span>



| <span data-ttu-id="1b85e-239">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b85e-239">Requirement</span></span> | <span data-ttu-id="1b85e-240">Valor</span><span class="sxs-lookup"><span data-stu-id="1b85e-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b85e-241">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b85e-241">Minimum supported client</span></span><br/> | <span data-ttu-id="1b85e-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b85e-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b85e-243">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b85e-243">Minimum supported server</span></span><br/> | <span data-ttu-id="1b85e-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b85e-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b85e-245">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b85e-245">Namespace</span></span><br/>                | <span data-ttu-id="1b85e-246">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1b85e-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1b85e-247">MOF</span><span class="sxs-lookup"><span data-stu-id="1b85e-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b85e-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b85e-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b85e-249">DLL</span><span class="sxs-lookup"><span data-stu-id="1b85e-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b85e-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b85e-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b85e-251">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b85e-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b85e-252">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="1b85e-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1b85e-253">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="1b85e-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="1b85e-254">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="1b85e-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="1b85e-255">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="1b85e-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="1b85e-256">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="1b85e-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

