---
description: O método de classe WMI DisableIPSec é usado para desabilitar o IPsec (Internet Protocol Security) neste adaptador de rede habilitado para TCP/IP.
ms.assetid: 6fff2721-1ee2-42b4-bbf9-fd36b97318e3
ms.tgt_platform: multiple
title: Método DisableIPSec da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.DisableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b2a17bbfa0f10c08edb581b4a4bf51173facfea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756439"
---
# <a name="disableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="c504e-103">Método DisableIPSec da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="c504e-103">DisableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="c504e-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DisableIPSec** é usado para desabilitar o IPsec (Internet Protocol Security) neste adaptador de rede habilitado para TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="c504e-104">The **DisableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method is used to disable Internet Protocol security (IPsec) on this TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="c504e-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c504e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c504e-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c504e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c504e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c504e-107">Syntax</span></span>


```mof
uint32 DisableIPSec();
```



## <a name="parameters"></a><span data-ttu-id="c504e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c504e-108">Parameters</span></span>

<span data-ttu-id="c504e-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c504e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c504e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c504e-110">Return value</span></span>

<span data-ttu-id="c504e-111">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando uma reinicialização não é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e qualquer outro número se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="c504e-111">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="c504e-112">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c504e-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c504e-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c504e-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c504e-114">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="c504e-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-115">0</span><span class="sxs-lookup"><span data-stu-id="c504e-115">0</span></span>

<span data-ttu-id="c504e-116">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="c504e-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-117">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="c504e-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-118">1</span><span class="sxs-lookup"><span data-stu-id="c504e-118">1</span></span>

<span data-ttu-id="c504e-119">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="c504e-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-120">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="c504e-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-121">64</span><span class="sxs-lookup"><span data-stu-id="c504e-121">64</span></span>

<span data-ttu-id="c504e-122">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="c504e-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-123">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="c504e-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-124">65</span><span class="sxs-lookup"><span data-stu-id="c504e-124">65</span></span>

<span data-ttu-id="c504e-125">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="c504e-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-126">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="c504e-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-127">66</span><span class="sxs-lookup"><span data-stu-id="c504e-127">66</span></span>

<span data-ttu-id="c504e-128">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="c504e-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-129">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="c504e-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-130">67</span><span class="sxs-lookup"><span data-stu-id="c504e-130">67</span></span>

<span data-ttu-id="c504e-131">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="c504e-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-132">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="c504e-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-133">68</span><span class="sxs-lookup"><span data-stu-id="c504e-133">68</span></span>

<span data-ttu-id="c504e-134">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="c504e-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-135">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="c504e-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-136">69</span><span class="sxs-lookup"><span data-stu-id="c504e-136">69</span></span>

<span data-ttu-id="c504e-137">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="c504e-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-138">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="c504e-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-139">70</span><span class="sxs-lookup"><span data-stu-id="c504e-139">70</span></span>

<span data-ttu-id="c504e-140">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="c504e-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-141">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="c504e-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-142">71</span><span class="sxs-lookup"><span data-stu-id="c504e-142">71</span></span>

<span data-ttu-id="c504e-143">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="c504e-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-144">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="c504e-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-145">72</span><span class="sxs-lookup"><span data-stu-id="c504e-145">72</span></span>

<span data-ttu-id="c504e-146">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="c504e-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-147">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="c504e-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-148">73</span><span class="sxs-lookup"><span data-stu-id="c504e-148">73</span></span>

<span data-ttu-id="c504e-149">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="c504e-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-150">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="c504e-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-151">74</span><span class="sxs-lookup"><span data-stu-id="c504e-151">74</span></span>

<span data-ttu-id="c504e-152">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="c504e-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-153">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="c504e-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-154">75</span><span class="sxs-lookup"><span data-stu-id="c504e-154">75</span></span>

<span data-ttu-id="c504e-155">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="c504e-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-156">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="c504e-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-157">76</span><span class="sxs-lookup"><span data-stu-id="c504e-157">76</span></span>

<span data-ttu-id="c504e-158">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="c504e-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-159">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="c504e-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-160">77</span><span class="sxs-lookup"><span data-stu-id="c504e-160">77</span></span>

<span data-ttu-id="c504e-161">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="c504e-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-162">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="c504e-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-163">78</span><span class="sxs-lookup"><span data-stu-id="c504e-163">78</span></span>

<span data-ttu-id="c504e-164">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c504e-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-165">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="c504e-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-166">79</span><span class="sxs-lookup"><span data-stu-id="c504e-166">79</span></span>

<span data-ttu-id="c504e-167">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="c504e-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-168">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="c504e-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-169">80</span><span class="sxs-lookup"><span data-stu-id="c504e-169">80</span></span>

<span data-ttu-id="c504e-170">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="c504e-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-171">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="c504e-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-172">81</span><span class="sxs-lookup"><span data-stu-id="c504e-172">81</span></span>

<span data-ttu-id="c504e-173">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="c504e-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-174">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="c504e-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-175">82</span><span class="sxs-lookup"><span data-stu-id="c504e-175">82</span></span>

<span data-ttu-id="c504e-176">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="c504e-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-177">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="c504e-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-178">83</span><span class="sxs-lookup"><span data-stu-id="c504e-178">83</span></span>

<span data-ttu-id="c504e-179">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="c504e-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-180">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="c504e-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-181">84</span><span class="sxs-lookup"><span data-stu-id="c504e-181">84</span></span>

<span data-ttu-id="c504e-182">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="c504e-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-183">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="c504e-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-184">85</span><span class="sxs-lookup"><span data-stu-id="c504e-184">85</span></span>

<span data-ttu-id="c504e-185">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="c504e-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-186">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="c504e-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-187">86</span><span class="sxs-lookup"><span data-stu-id="c504e-187">86</span></span>

<span data-ttu-id="c504e-188">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="c504e-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-189">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="c504e-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-190">87</span><span class="sxs-lookup"><span data-stu-id="c504e-190">87</span></span>

<span data-ttu-id="c504e-191">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="c504e-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-192">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="c504e-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-193">88</span><span class="sxs-lookup"><span data-stu-id="c504e-193">88</span></span>

<span data-ttu-id="c504e-194">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="c504e-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-195">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="c504e-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-196">89</span><span class="sxs-lookup"><span data-stu-id="c504e-196">89</span></span>

<span data-ttu-id="c504e-197">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="c504e-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-198">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="c504e-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-199">90</span><span class="sxs-lookup"><span data-stu-id="c504e-199">90</span></span>

<span data-ttu-id="c504e-200">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="c504e-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-201">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="c504e-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-202">91</span><span class="sxs-lookup"><span data-stu-id="c504e-202">91</span></span>

<span data-ttu-id="c504e-203">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="c504e-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-204">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="c504e-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-205">92</span><span class="sxs-lookup"><span data-stu-id="c504e-205">92</span></span>

<span data-ttu-id="c504e-206">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="c504e-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-207">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="c504e-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-208">93</span><span class="sxs-lookup"><span data-stu-id="c504e-208">93</span></span>

<span data-ttu-id="c504e-209">Já existe.</span><span class="sxs-lookup"><span data-stu-id="c504e-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-210">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="c504e-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-211">94</span><span class="sxs-lookup"><span data-stu-id="c504e-211">94</span></span>

<span data-ttu-id="c504e-212">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="c504e-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-213">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="c504e-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-214">95</span><span class="sxs-lookup"><span data-stu-id="c504e-214">95</span></span>

<span data-ttu-id="c504e-215">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="c504e-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-216">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="c504e-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-217">96</span><span class="sxs-lookup"><span data-stu-id="c504e-217">96</span></span>

<span data-ttu-id="c504e-218">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="c504e-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-219">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="c504e-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-220">97</span><span class="sxs-lookup"><span data-stu-id="c504e-220">97</span></span>

<span data-ttu-id="c504e-221">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="c504e-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-222">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="c504e-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-223">98</span><span class="sxs-lookup"><span data-stu-id="c504e-223">98</span></span>

<span data-ttu-id="c504e-224">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="c504e-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-225">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="c504e-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-226">100</span><span class="sxs-lookup"><span data-stu-id="c504e-226">100</span></span>

<span data-ttu-id="c504e-227">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="c504e-227">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c504e-228">**Outras**</span><span class="sxs-lookup"><span data-stu-id="c504e-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c504e-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="c504e-229">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c504e-230">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c504e-230">Examples</span></span>

<span data-ttu-id="c504e-231">O exemplo de VBScript a seguir desabilita a segurança de IP em um computador.</span><span class="sxs-lookup"><span data-stu-id="c504e-231">The following VBScript sample disables the IP Security on a computer.</span></span> <span data-ttu-id="c504e-232">Observe que a chamada real para DisableIPSec é comentada, para fins de segurança.</span><span class="sxs-lookup"><span data-stu-id="c504e-232">Note that the actual call to DisableIPSec is commented out, for safety purposes.</span></span>


```VB
strServer = "."

Set objWMI = GetObject("winmgmts:\\" & strServer & "\root\cimv2")

strWQL = "select * from Win32_NetworkAdapterConfiguration"
Set objInstances = objWMI.ExecQuery(strWQL,,48)

For Each objInstance in objInstances

 ' Uncomment next line to disable security
 ' intResult = objInstance.DisableIPSec

Next
```



## <a name="requirements"></a><span data-ttu-id="c504e-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c504e-233">Requirements</span></span>



| <span data-ttu-id="c504e-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="c504e-234">Requirement</span></span> | <span data-ttu-id="c504e-235">Valor</span><span class="sxs-lookup"><span data-stu-id="c504e-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c504e-236">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c504e-236">Minimum supported client</span></span><br/> | <span data-ttu-id="c504e-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c504e-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c504e-238">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c504e-238">Minimum supported server</span></span><br/> | <span data-ttu-id="c504e-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c504e-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c504e-240">Namespace</span><span class="sxs-lookup"><span data-stu-id="c504e-240">Namespace</span></span><br/>                | <span data-ttu-id="c504e-241">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c504e-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c504e-242">MOF</span><span class="sxs-lookup"><span data-stu-id="c504e-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c504e-243"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c504e-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c504e-244">DLL</span><span class="sxs-lookup"><span data-stu-id="c504e-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c504e-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c504e-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c504e-246">Confira também</span><span class="sxs-lookup"><span data-stu-id="c504e-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c504e-247">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="c504e-247">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="c504e-248">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="c504e-248">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="c504e-249">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="c504e-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="c504e-250">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="c504e-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="c504e-251">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="c504e-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

