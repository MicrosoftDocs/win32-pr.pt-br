---
description: O método estático da classe WMI SetArpUseEtherSNAP é usado para habilitar pacotes Ethernet para usar a codificação de ajuste 802,3.
ms.assetid: 437954c0-ea6b-4559-a4cb-1f66630e70fe
ms.tgt_platform: multiple
title: Método SetArpUseEtherSNAP da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetArpUseEtherSNAP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52e3ce42948d5c40bbde3329b37ee3fa506c47ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826664"
---
# <a name="setarpuseethersnap-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="063c0-103">Método SetArpUseEtherSNAP da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="063c0-103">SetArpUseEtherSNAP method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="063c0-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetArpUseEtherSNAP** é usado para habilitar pacotes Ethernet para usar a codificação de ajuste 802,3.</span><span class="sxs-lookup"><span data-stu-id="063c0-104">The **SetArpUseEtherSNAP** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable ethernet packets to use 802.3 SNAP encoding.</span></span>

<span data-ttu-id="063c0-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="063c0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="063c0-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="063c0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="063c0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="063c0-107">Syntax</span></span>


```mof
uint32 SetArpUseEtherSNAP(
  [in] boolean ArpUseEtherSNAP
);
```



## <a name="parameters"></a><span data-ttu-id="063c0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="063c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="063c0-109">*ArpUseEtherSNAP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="063c0-109">*ArpUseEtherSNAP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="063c0-110">Se **true** , permite que o TCP/IP transmita pacotes Ethernet usando a codificação de ajuste 802,3.</span><span class="sxs-lookup"><span data-stu-id="063c0-110">If **true** enables TCP/IP to transmit Ethernet packets using 802.3 SNAP encoding.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="063c0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="063c0-111">Return value</span></span>

<span data-ttu-id="063c0-112">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="063c0-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="063c0-113">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="063c0-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="063c0-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="063c0-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="063c0-115">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="063c0-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-116">0</span><span class="sxs-lookup"><span data-stu-id="063c0-116">0</span></span>

<span data-ttu-id="063c0-117">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="063c0-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-118">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="063c0-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-119">1</span><span class="sxs-lookup"><span data-stu-id="063c0-119">1</span></span>

<span data-ttu-id="063c0-120">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="063c0-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-121">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="063c0-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-122">64</span><span class="sxs-lookup"><span data-stu-id="063c0-122">64</span></span>

<span data-ttu-id="063c0-123">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="063c0-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-124">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="063c0-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-125">65</span><span class="sxs-lookup"><span data-stu-id="063c0-125">65</span></span>

<span data-ttu-id="063c0-126">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="063c0-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-127">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="063c0-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-128">66</span><span class="sxs-lookup"><span data-stu-id="063c0-128">66</span></span>

<span data-ttu-id="063c0-129">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="063c0-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-130">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="063c0-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-131">67</span><span class="sxs-lookup"><span data-stu-id="063c0-131">67</span></span>

<span data-ttu-id="063c0-132">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="063c0-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-133">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="063c0-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-134">68</span><span class="sxs-lookup"><span data-stu-id="063c0-134">68</span></span>

<span data-ttu-id="063c0-135">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="063c0-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-136">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="063c0-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-137">69</span><span class="sxs-lookup"><span data-stu-id="063c0-137">69</span></span>

<span data-ttu-id="063c0-138">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="063c0-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-139">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="063c0-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-140">70</span><span class="sxs-lookup"><span data-stu-id="063c0-140">70</span></span>

<span data-ttu-id="063c0-141">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="063c0-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-142">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="063c0-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-143">71</span><span class="sxs-lookup"><span data-stu-id="063c0-143">71</span></span>

<span data-ttu-id="063c0-144">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="063c0-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-145">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="063c0-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-146">72</span><span class="sxs-lookup"><span data-stu-id="063c0-146">72</span></span>

<span data-ttu-id="063c0-147">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="063c0-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-148">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="063c0-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-149">73</span><span class="sxs-lookup"><span data-stu-id="063c0-149">73</span></span>

<span data-ttu-id="063c0-150">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="063c0-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-151">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="063c0-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-152">74</span><span class="sxs-lookup"><span data-stu-id="063c0-152">74</span></span>

<span data-ttu-id="063c0-153">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="063c0-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-154">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="063c0-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-155">75</span><span class="sxs-lookup"><span data-stu-id="063c0-155">75</span></span>

<span data-ttu-id="063c0-156">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="063c0-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-157">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="063c0-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-158">76</span><span class="sxs-lookup"><span data-stu-id="063c0-158">76</span></span>

<span data-ttu-id="063c0-159">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="063c0-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-160">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="063c0-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-161">77</span><span class="sxs-lookup"><span data-stu-id="063c0-161">77</span></span>

<span data-ttu-id="063c0-162">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="063c0-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-163">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="063c0-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-164">78</span><span class="sxs-lookup"><span data-stu-id="063c0-164">78</span></span>

<span data-ttu-id="063c0-165">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="063c0-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-166">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="063c0-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-167">79</span><span class="sxs-lookup"><span data-stu-id="063c0-167">79</span></span>

<span data-ttu-id="063c0-168">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="063c0-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-169">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="063c0-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-170">80</span><span class="sxs-lookup"><span data-stu-id="063c0-170">80</span></span>

<span data-ttu-id="063c0-171">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="063c0-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-172">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="063c0-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-173">81</span><span class="sxs-lookup"><span data-stu-id="063c0-173">81</span></span>

<span data-ttu-id="063c0-174">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="063c0-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-175">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="063c0-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-176">82</span><span class="sxs-lookup"><span data-stu-id="063c0-176">82</span></span>

<span data-ttu-id="063c0-177">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="063c0-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-178">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="063c0-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-179">83</span><span class="sxs-lookup"><span data-stu-id="063c0-179">83</span></span>

<span data-ttu-id="063c0-180">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="063c0-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-181">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="063c0-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-182">84</span><span class="sxs-lookup"><span data-stu-id="063c0-182">84</span></span>

<span data-ttu-id="063c0-183">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="063c0-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-184">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="063c0-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-185">85</span><span class="sxs-lookup"><span data-stu-id="063c0-185">85</span></span>

<span data-ttu-id="063c0-186">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="063c0-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-187">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="063c0-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-188">86</span><span class="sxs-lookup"><span data-stu-id="063c0-188">86</span></span>

<span data-ttu-id="063c0-189">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="063c0-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-190">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="063c0-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-191">87</span><span class="sxs-lookup"><span data-stu-id="063c0-191">87</span></span>

<span data-ttu-id="063c0-192">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="063c0-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-193">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="063c0-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-194">88</span><span class="sxs-lookup"><span data-stu-id="063c0-194">88</span></span>

<span data-ttu-id="063c0-195">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="063c0-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-196">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="063c0-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-197">89</span><span class="sxs-lookup"><span data-stu-id="063c0-197">89</span></span>

<span data-ttu-id="063c0-198">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="063c0-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-199">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="063c0-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-200">90</span><span class="sxs-lookup"><span data-stu-id="063c0-200">90</span></span>

<span data-ttu-id="063c0-201">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="063c0-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-202">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="063c0-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-203">91</span><span class="sxs-lookup"><span data-stu-id="063c0-203">91</span></span>

<span data-ttu-id="063c0-204">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="063c0-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-205">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="063c0-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-206">92</span><span class="sxs-lookup"><span data-stu-id="063c0-206">92</span></span>

<span data-ttu-id="063c0-207">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="063c0-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-208">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="063c0-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-209">93</span><span class="sxs-lookup"><span data-stu-id="063c0-209">93</span></span>

<span data-ttu-id="063c0-210">Já existe.</span><span class="sxs-lookup"><span data-stu-id="063c0-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-211">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="063c0-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-212">94</span><span class="sxs-lookup"><span data-stu-id="063c0-212">94</span></span>

<span data-ttu-id="063c0-213">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="063c0-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-214">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="063c0-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-215">95</span><span class="sxs-lookup"><span data-stu-id="063c0-215">95</span></span>

<span data-ttu-id="063c0-216">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="063c0-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-217">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="063c0-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-218">96</span><span class="sxs-lookup"><span data-stu-id="063c0-218">96</span></span>

<span data-ttu-id="063c0-219">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="063c0-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-220">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="063c0-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-221">97</span><span class="sxs-lookup"><span data-stu-id="063c0-221">97</span></span>

<span data-ttu-id="063c0-222">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="063c0-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-223">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="063c0-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-224">98</span><span class="sxs-lookup"><span data-stu-id="063c0-224">98</span></span>

<span data-ttu-id="063c0-225">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="063c0-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-226">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="063c0-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-227">100</span><span class="sxs-lookup"><span data-stu-id="063c0-227">100</span></span>

<span data-ttu-id="063c0-228">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="063c0-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="063c0-229">**Outras**</span><span class="sxs-lookup"><span data-stu-id="063c0-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="063c0-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="063c0-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="063c0-231">Comentários</span><span class="sxs-lookup"><span data-stu-id="063c0-231">Remarks</span></span>

<span data-ttu-id="063c0-232">Por padrão, a pilha transmite pacotes no formato Ethernet digital, Intel, Xerox (DIX).</span><span class="sxs-lookup"><span data-stu-id="063c0-232">By default, the stack transmits packets in Digital, Intel, Xerox (DIX) Ethernet format.</span></span> <span data-ttu-id="063c0-233">Ele sempre recebe os dois formatos.</span><span class="sxs-lookup"><span data-stu-id="063c0-233">It always receives both formats.</span></span>

## <a name="examples"></a><span data-ttu-id="063c0-234">Exemplos</span><span class="sxs-lookup"><span data-stu-id="063c0-234">Examples</span></span>

<span data-ttu-id="063c0-235">O exemplo de código [modificar as consultas ARP para usar o EtherSNAP](https://Gallery.TechNet.Microsoft.Com/2fe24075-fdb1-486d-8c0b-d25075fd8f21) VBScript na galeria do TechNet usa o **SetArpUseEtherSNAP** para configurar os adaptadores de rede em um computador para usar a codificação de encaixe 802,3 para pacotes Ethernet.</span><span class="sxs-lookup"><span data-stu-id="063c0-235">The [Modify ARP Queries to Use EtherSNAP](https://Gallery.TechNet.Microsoft.Com/2fe24075-fdb1-486d-8c0b-d25075fd8f21) VBScript code sample on TechNet Gallery uses **SetArpUseEtherSNAP** to configure the network adapters on a computer to use 802.3 SNAP encoding for Ethernet packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="063c0-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="063c0-236">Requirements</span></span>



| <span data-ttu-id="063c0-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="063c0-237">Requirement</span></span> | <span data-ttu-id="063c0-238">Valor</span><span class="sxs-lookup"><span data-stu-id="063c0-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="063c0-239">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="063c0-239">Minimum supported client</span></span><br/> | <span data-ttu-id="063c0-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="063c0-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="063c0-241">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="063c0-241">Minimum supported server</span></span><br/> | <span data-ttu-id="063c0-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="063c0-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="063c0-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="063c0-243">Namespace</span></span><br/>                | <span data-ttu-id="063c0-244">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="063c0-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="063c0-245">MOF</span><span class="sxs-lookup"><span data-stu-id="063c0-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="063c0-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="063c0-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="063c0-247">DLL</span><span class="sxs-lookup"><span data-stu-id="063c0-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="063c0-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="063c0-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="063c0-249">Confira também</span><span class="sxs-lookup"><span data-stu-id="063c0-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="063c0-250">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="063c0-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="063c0-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="063c0-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="063c0-252">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="063c0-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="063c0-253">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="063c0-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="063c0-254">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="063c0-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

