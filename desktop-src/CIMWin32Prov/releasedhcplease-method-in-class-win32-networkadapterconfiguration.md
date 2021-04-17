---
description: O método de classe WMI ReleaseDHCPLease libera o endereço IP associado a um adaptador de rede habilitado para DHCP específico.
ms.assetid: 0cf4b531-8626-4388-bffa-e16a4aa8c794
ms.tgt_platform: multiple
title: Método ReleaseDHCPLease da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5520a6b2d0960c1d4258b19f8cd4d600c9b8fe34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755664"
---
# <a name="releasedhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d3f70-103">Método ReleaseDHCPLease da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3f70-103">ReleaseDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d3f70-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ReleaseDHCPLease** libera o endereço IP associado a um adaptador de rede habilitado para DHCP específico.</span><span class="sxs-lookup"><span data-stu-id="d3f70-104">The **ReleaseDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method releases the IP address bound to a specific DHCP-enabled network adapter.</span></span>

<span data-ttu-id="d3f70-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d3f70-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d3f70-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d3f70-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f70-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3f70-107">Syntax</span></span>


```mof
uint32 ReleaseDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="d3f70-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3f70-108">Parameters</span></span>

<span data-ttu-id="d3f70-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d3f70-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3f70-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3f70-110">Return value</span></span>

<span data-ttu-id="d3f70-111">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="d3f70-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="d3f70-112">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d3f70-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d3f70-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d3f70-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d3f70-114">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="d3f70-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-115">0</span><span class="sxs-lookup"><span data-stu-id="d3f70-115">0</span></span>

<span data-ttu-id="d3f70-116">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="d3f70-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-117">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="d3f70-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-118">1</span><span class="sxs-lookup"><span data-stu-id="d3f70-118">1</span></span>

<span data-ttu-id="d3f70-119">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="d3f70-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-120">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="d3f70-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-121">64</span><span class="sxs-lookup"><span data-stu-id="d3f70-121">64</span></span>

<span data-ttu-id="d3f70-122">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="d3f70-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-123">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="d3f70-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-124">65</span><span class="sxs-lookup"><span data-stu-id="d3f70-124">65</span></span>

<span data-ttu-id="d3f70-125">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="d3f70-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-126">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="d3f70-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-127">66</span><span class="sxs-lookup"><span data-stu-id="d3f70-127">66</span></span>

<span data-ttu-id="d3f70-128">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="d3f70-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-129">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="d3f70-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-130">67</span><span class="sxs-lookup"><span data-stu-id="d3f70-130">67</span></span>

<span data-ttu-id="d3f70-131">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="d3f70-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-132">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="d3f70-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-133">68</span><span class="sxs-lookup"><span data-stu-id="d3f70-133">68</span></span>

<span data-ttu-id="d3f70-134">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="d3f70-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-135">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="d3f70-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-136">69</span><span class="sxs-lookup"><span data-stu-id="d3f70-136">69</span></span>

<span data-ttu-id="d3f70-137">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="d3f70-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-138">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="d3f70-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-139">70</span><span class="sxs-lookup"><span data-stu-id="d3f70-139">70</span></span>

<span data-ttu-id="d3f70-140">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="d3f70-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-141">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="d3f70-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-142">71</span><span class="sxs-lookup"><span data-stu-id="d3f70-142">71</span></span>

<span data-ttu-id="d3f70-143">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="d3f70-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-144">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="d3f70-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-145">72</span><span class="sxs-lookup"><span data-stu-id="d3f70-145">72</span></span>

<span data-ttu-id="d3f70-146">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="d3f70-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-147">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="d3f70-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-148">73</span><span class="sxs-lookup"><span data-stu-id="d3f70-148">73</span></span>

<span data-ttu-id="d3f70-149">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="d3f70-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-150">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="d3f70-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-151">74</span><span class="sxs-lookup"><span data-stu-id="d3f70-151">74</span></span>

<span data-ttu-id="d3f70-152">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="d3f70-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-153">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="d3f70-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-154">75</span><span class="sxs-lookup"><span data-stu-id="d3f70-154">75</span></span>

<span data-ttu-id="d3f70-155">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="d3f70-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-156">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="d3f70-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-157">76</span><span class="sxs-lookup"><span data-stu-id="d3f70-157">76</span></span>

<span data-ttu-id="d3f70-158">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="d3f70-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-159">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="d3f70-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-160">77</span><span class="sxs-lookup"><span data-stu-id="d3f70-160">77</span></span>

<span data-ttu-id="d3f70-161">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="d3f70-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-162">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="d3f70-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-163">78</span><span class="sxs-lookup"><span data-stu-id="d3f70-163">78</span></span>

<span data-ttu-id="d3f70-164">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d3f70-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-165">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="d3f70-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-166">79</span><span class="sxs-lookup"><span data-stu-id="d3f70-166">79</span></span>

<span data-ttu-id="d3f70-167">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="d3f70-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-168">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="d3f70-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-169">80</span><span class="sxs-lookup"><span data-stu-id="d3f70-169">80</span></span>

<span data-ttu-id="d3f70-170">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d3f70-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-171">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="d3f70-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-172">81</span><span class="sxs-lookup"><span data-stu-id="d3f70-172">81</span></span>

<span data-ttu-id="d3f70-173">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="d3f70-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-174">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="d3f70-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-175">82</span><span class="sxs-lookup"><span data-stu-id="d3f70-175">82</span></span>

<span data-ttu-id="d3f70-176">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="d3f70-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-177">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="d3f70-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-178">83</span><span class="sxs-lookup"><span data-stu-id="d3f70-178">83</span></span>

<span data-ttu-id="d3f70-179">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="d3f70-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-180">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="d3f70-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-181">84</span><span class="sxs-lookup"><span data-stu-id="d3f70-181">84</span></span>

<span data-ttu-id="d3f70-182">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="d3f70-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-183">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="d3f70-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-184">85</span><span class="sxs-lookup"><span data-stu-id="d3f70-184">85</span></span>

<span data-ttu-id="d3f70-185">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="d3f70-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-186">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="d3f70-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-187">86</span><span class="sxs-lookup"><span data-stu-id="d3f70-187">86</span></span>

<span data-ttu-id="d3f70-188">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="d3f70-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-189">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="d3f70-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-190">87</span><span class="sxs-lookup"><span data-stu-id="d3f70-190">87</span></span>

<span data-ttu-id="d3f70-191">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="d3f70-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-192">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="d3f70-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-193">88</span><span class="sxs-lookup"><span data-stu-id="d3f70-193">88</span></span>

<span data-ttu-id="d3f70-194">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="d3f70-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-195">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="d3f70-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-196">89</span><span class="sxs-lookup"><span data-stu-id="d3f70-196">89</span></span>

<span data-ttu-id="d3f70-197">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="d3f70-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-198">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="d3f70-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-199">90</span><span class="sxs-lookup"><span data-stu-id="d3f70-199">90</span></span>

<span data-ttu-id="d3f70-200">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="d3f70-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-201">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="d3f70-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-202">91</span><span class="sxs-lookup"><span data-stu-id="d3f70-202">91</span></span>

<span data-ttu-id="d3f70-203">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="d3f70-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-204">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="d3f70-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-205">92</span><span class="sxs-lookup"><span data-stu-id="d3f70-205">92</span></span>

<span data-ttu-id="d3f70-206">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="d3f70-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-207">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="d3f70-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-208">93</span><span class="sxs-lookup"><span data-stu-id="d3f70-208">93</span></span>

<span data-ttu-id="d3f70-209">Já existe.</span><span class="sxs-lookup"><span data-stu-id="d3f70-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-210">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="d3f70-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-211">94</span><span class="sxs-lookup"><span data-stu-id="d3f70-211">94</span></span>

<span data-ttu-id="d3f70-212">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="d3f70-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-213">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="d3f70-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-214">95</span><span class="sxs-lookup"><span data-stu-id="d3f70-214">95</span></span>

<span data-ttu-id="d3f70-215">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="d3f70-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-216">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="d3f70-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-217">96</span><span class="sxs-lookup"><span data-stu-id="d3f70-217">96</span></span>

<span data-ttu-id="d3f70-218">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="d3f70-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-219">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="d3f70-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-220">97</span><span class="sxs-lookup"><span data-stu-id="d3f70-220">97</span></span>

<span data-ttu-id="d3f70-221">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="d3f70-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-222">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="d3f70-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-223">98</span><span class="sxs-lookup"><span data-stu-id="d3f70-223">98</span></span>

<span data-ttu-id="d3f70-224">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="d3f70-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-225">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="d3f70-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-226">100</span><span class="sxs-lookup"><span data-stu-id="d3f70-226">100</span></span>

<span data-ttu-id="d3f70-227">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="d3f70-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d3f70-228">**Outras**</span><span class="sxs-lookup"><span data-stu-id="d3f70-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d3f70-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="d3f70-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3f70-230">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3f70-230">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="d3f70-231">Se o DHCP estiver habilitado no sistema de computador local, a opção desabilitará o TCP/IP nesse adaptador de rede específico.</span><span class="sxs-lookup"><span data-stu-id="d3f70-231">If DHCP is enabled on the local computer system, the option disables TCP/IP on this specific network adapter.</span></span> <span data-ttu-id="d3f70-232">A menos que você tenha um caminho alternativo para o sistema de destino, ou seja, outro adaptador de rede associado a TCP/IP, todas as comunicações TCP/IP serão perdidas.</span><span class="sxs-lookup"><span data-stu-id="d3f70-232">Unless you have an alternate path to the target system, that is, another TCP/IP bound network adapter, all TCP/IP communications will be lost.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d3f70-233">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d3f70-233">Examples</span></span>

<span data-ttu-id="d3f70-234">O exemplo de [lançamento renovar IP endereços usando PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell na galeria do TechNet usa o **ReleaseDHCPLease** para liberar e renovar um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="d3f70-234">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **ReleaseDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="d3f70-235">O código VBScript a seguir libera as concessões DHCP para todos os adaptadores de rede vinculados a TCP/IP em um computador.</span><span class="sxs-lookup"><span data-stu-id="d3f70-235">The following VBScript code releases the DHCP leases for all TCP/IP-bound network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    objNetCard.ReleaseDHCPLease() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="d3f70-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3f70-236">Requirements</span></span>



| <span data-ttu-id="d3f70-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3f70-237">Requirement</span></span> | <span data-ttu-id="d3f70-238">Valor</span><span class="sxs-lookup"><span data-stu-id="d3f70-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f70-239">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3f70-239">Minimum supported client</span></span><br/> | <span data-ttu-id="d3f70-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3f70-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3f70-241">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3f70-241">Minimum supported server</span></span><br/> | <span data-ttu-id="d3f70-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3f70-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3f70-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3f70-243">Namespace</span></span><br/>                | <span data-ttu-id="d3f70-244">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d3f70-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d3f70-245">MOF</span><span class="sxs-lookup"><span data-stu-id="d3f70-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3f70-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3f70-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3f70-247">DLL</span><span class="sxs-lookup"><span data-stu-id="d3f70-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3f70-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3f70-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3f70-249">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3f70-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f70-250">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="d3f70-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d3f70-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="d3f70-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="d3f70-252">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="d3f70-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="d3f70-253">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="d3f70-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d3f70-254">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="d3f70-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

