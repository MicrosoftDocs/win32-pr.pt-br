---
description: O método estático da classe WMI EnableIPFilterSec é usado para habilitar o IPsec (segurança do protocolo Internet) globalmente em todos os adaptadores de rede vinculados por IP.
ms.assetid: 565acc18-61e7-473e-b2cc-41f0e8c29193
ms.tgt_platform: multiple
title: Método EnableIPFilterSec da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableIPFilterSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3429e2c2ba78e013da9195961b76ff84ffda9b68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826309"
---
# <a name="enableipfiltersec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="a15d4-103">Método EnableIPFilterSec da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="a15d4-103">EnableIPFilterSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="a15d4-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableIPFilterSec** é usado para habilitar o IPsec (segurança do protocolo Internet) globalmente em todos os adaptadores de rede vinculados por IP.</span><span class="sxs-lookup"><span data-stu-id="a15d4-104">The **EnableIPFilterSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable Internet Protocol security (IPsec) globally across all IP-bound network adapters.</span></span>

<span data-ttu-id="a15d4-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a15d4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a15d4-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a15d4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a15d4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a15d4-107">Syntax</span></span>


```mof
uint32 EnableIPFilterSec(
  [in] boolean IPFilterSecurityEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="a15d4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a15d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a15d4-109">*IPFilterSecurityEnabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a15d4-109">*IPFilterSecurityEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-110">Se **for true**, o IPSec será habilitado globalmente em todos os adaptadores de rede vinculados por IP.</span><span class="sxs-lookup"><span data-stu-id="a15d4-110">If **true**, IPsec is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="a15d4-111">Se **for false**, todo o tráfego de porta e protocolo tem permissão para fluir sem filtro.</span><span class="sxs-lookup"><span data-stu-id="a15d4-111">If **false**, all port and protocol traffic is allowed to flow unfiltered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a15d4-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a15d4-112">Return value</span></span>

<span data-ttu-id="a15d4-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando uma reinicialização não é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e qualquer outro número se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="a15d4-113">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="a15d4-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a15d4-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a15d4-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a15d4-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a15d4-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="a15d4-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-117">0</span><span class="sxs-lookup"><span data-stu-id="a15d4-117">0</span></span>

<span data-ttu-id="a15d4-118">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="a15d4-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-119">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="a15d4-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-120">1</span><span class="sxs-lookup"><span data-stu-id="a15d4-120">1</span></span>

<span data-ttu-id="a15d4-121">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="a15d4-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-122">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="a15d4-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-123">64</span><span class="sxs-lookup"><span data-stu-id="a15d4-123">64</span></span>

<span data-ttu-id="a15d4-124">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="a15d4-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-125">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="a15d4-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-126">65</span><span class="sxs-lookup"><span data-stu-id="a15d4-126">65</span></span>

<span data-ttu-id="a15d4-127">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="a15d4-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-128">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="a15d4-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-129">66</span><span class="sxs-lookup"><span data-stu-id="a15d4-129">66</span></span>

<span data-ttu-id="a15d4-130">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="a15d4-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-131">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="a15d4-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-132">67</span><span class="sxs-lookup"><span data-stu-id="a15d4-132">67</span></span>

<span data-ttu-id="a15d4-133">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="a15d4-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-134">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="a15d4-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-135">68</span><span class="sxs-lookup"><span data-stu-id="a15d4-135">68</span></span>

<span data-ttu-id="a15d4-136">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="a15d4-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-137">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="a15d4-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-138">69</span><span class="sxs-lookup"><span data-stu-id="a15d4-138">69</span></span>

<span data-ttu-id="a15d4-139">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="a15d4-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-140">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="a15d4-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-141">70</span><span class="sxs-lookup"><span data-stu-id="a15d4-141">70</span></span>

<span data-ttu-id="a15d4-142">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="a15d4-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-143">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="a15d4-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-144">71</span><span class="sxs-lookup"><span data-stu-id="a15d4-144">71</span></span>

<span data-ttu-id="a15d4-145">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="a15d4-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-146">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="a15d4-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-147">72</span><span class="sxs-lookup"><span data-stu-id="a15d4-147">72</span></span>

<span data-ttu-id="a15d4-148">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="a15d4-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-149">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="a15d4-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-150">73</span><span class="sxs-lookup"><span data-stu-id="a15d4-150">73</span></span>

<span data-ttu-id="a15d4-151">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="a15d4-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-152">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="a15d4-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-153">74</span><span class="sxs-lookup"><span data-stu-id="a15d4-153">74</span></span>

<span data-ttu-id="a15d4-154">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="a15d4-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-155">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="a15d4-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-156">75</span><span class="sxs-lookup"><span data-stu-id="a15d4-156">75</span></span>

<span data-ttu-id="a15d4-157">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="a15d4-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-158">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="a15d4-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-159">76</span><span class="sxs-lookup"><span data-stu-id="a15d4-159">76</span></span>

<span data-ttu-id="a15d4-160">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="a15d4-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-161">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="a15d4-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-162">77</span><span class="sxs-lookup"><span data-stu-id="a15d4-162">77</span></span>

<span data-ttu-id="a15d4-163">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="a15d4-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-164">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="a15d4-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-165">78</span><span class="sxs-lookup"><span data-stu-id="a15d4-165">78</span></span>

<span data-ttu-id="a15d4-166">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a15d4-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-167">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="a15d4-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-168">79</span><span class="sxs-lookup"><span data-stu-id="a15d4-168">79</span></span>

<span data-ttu-id="a15d4-169">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="a15d4-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-170">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="a15d4-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-171">80</span><span class="sxs-lookup"><span data-stu-id="a15d4-171">80</span></span>

<span data-ttu-id="a15d4-172">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="a15d4-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-173">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="a15d4-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-174">81</span><span class="sxs-lookup"><span data-stu-id="a15d4-174">81</span></span>

<span data-ttu-id="a15d4-175">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="a15d4-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-176">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="a15d4-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-177">82</span><span class="sxs-lookup"><span data-stu-id="a15d4-177">82</span></span>

<span data-ttu-id="a15d4-178">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="a15d4-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-179">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="a15d4-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-180">83</span><span class="sxs-lookup"><span data-stu-id="a15d4-180">83</span></span>

<span data-ttu-id="a15d4-181">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="a15d4-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-182">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="a15d4-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-183">84</span><span class="sxs-lookup"><span data-stu-id="a15d4-183">84</span></span>

<span data-ttu-id="a15d4-184">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="a15d4-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-185">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="a15d4-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-186">85</span><span class="sxs-lookup"><span data-stu-id="a15d4-186">85</span></span>

<span data-ttu-id="a15d4-187">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="a15d4-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-188">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="a15d4-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-189">86</span><span class="sxs-lookup"><span data-stu-id="a15d4-189">86</span></span>

<span data-ttu-id="a15d4-190">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="a15d4-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-191">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="a15d4-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-192">87</span><span class="sxs-lookup"><span data-stu-id="a15d4-192">87</span></span>

<span data-ttu-id="a15d4-193">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="a15d4-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-194">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="a15d4-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-195">88</span><span class="sxs-lookup"><span data-stu-id="a15d4-195">88</span></span>

<span data-ttu-id="a15d4-196">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="a15d4-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-197">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="a15d4-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-198">89</span><span class="sxs-lookup"><span data-stu-id="a15d4-198">89</span></span>

<span data-ttu-id="a15d4-199">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="a15d4-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-200">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="a15d4-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-201">90</span><span class="sxs-lookup"><span data-stu-id="a15d4-201">90</span></span>

<span data-ttu-id="a15d4-202">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="a15d4-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-203">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="a15d4-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-204">91</span><span class="sxs-lookup"><span data-stu-id="a15d4-204">91</span></span>

<span data-ttu-id="a15d4-205">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="a15d4-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-206">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="a15d4-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-207">92</span><span class="sxs-lookup"><span data-stu-id="a15d4-207">92</span></span>

<span data-ttu-id="a15d4-208">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="a15d4-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-209">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="a15d4-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-210">93</span><span class="sxs-lookup"><span data-stu-id="a15d4-210">93</span></span>

<span data-ttu-id="a15d4-211">Já existe.</span><span class="sxs-lookup"><span data-stu-id="a15d4-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-212">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="a15d4-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-213">94</span><span class="sxs-lookup"><span data-stu-id="a15d4-213">94</span></span>

<span data-ttu-id="a15d4-214">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="a15d4-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-215">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="a15d4-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-216">95</span><span class="sxs-lookup"><span data-stu-id="a15d4-216">95</span></span>

<span data-ttu-id="a15d4-217">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="a15d4-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-218">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="a15d4-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-219">96</span><span class="sxs-lookup"><span data-stu-id="a15d4-219">96</span></span>

<span data-ttu-id="a15d4-220">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="a15d4-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-221">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="a15d4-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-222">97</span><span class="sxs-lookup"><span data-stu-id="a15d4-222">97</span></span>

<span data-ttu-id="a15d4-223">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="a15d4-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-224">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="a15d4-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-225">98</span><span class="sxs-lookup"><span data-stu-id="a15d4-225">98</span></span>

<span data-ttu-id="a15d4-226">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="a15d4-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-227">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="a15d4-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-228">100</span><span class="sxs-lookup"><span data-stu-id="a15d4-228">100</span></span>

<span data-ttu-id="a15d4-229">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="a15d4-229">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a15d4-230">**Outras**</span><span class="sxs-lookup"><span data-stu-id="a15d4-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="a15d4-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="a15d4-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a15d4-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="a15d4-232">Remarks</span></span>

<span data-ttu-id="a15d4-233">Com a segurança habilitada, as características de segurança operacional para qualquer adaptador de rede podem ser controladas usando o método [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) específico do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="a15d4-233">With security enabled, the operational security characteristics for any one network adapter can be controlled by using the network adapter-specific [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="a15d4-234">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a15d4-234">Examples</span></span>

<span data-ttu-id="a15d4-235">O código a seguir, extraído do exemplo [habilitar segurança do ipfilter em todos os adaptadores de rede](https://Gallery.TechNet.Microsoft.Com/f8e56021-5a54-4554-b7b6-d76cc40d8d1d) na galeria do TechNet, habilita a segurança de filtro IP para todos os adaptadores de rede instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="a15d4-235">The following code, taken from the [Enable IPFilter Security on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/f8e56021-5a54-4554-b7b6-d76cc40d8d1d) sample on TechNet Gallery, enables IP filter security for all the network adapters installed in a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
objNetworkSettings.EnableIPFilterSec(True)
```



## <a name="requirements"></a><span data-ttu-id="a15d4-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a15d4-236">Requirements</span></span>



| <span data-ttu-id="a15d4-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="a15d4-237">Requirement</span></span> | <span data-ttu-id="a15d4-238">Valor</span><span class="sxs-lookup"><span data-stu-id="a15d4-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a15d4-239">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a15d4-239">Minimum supported client</span></span><br/> | <span data-ttu-id="a15d4-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a15d4-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a15d4-241">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a15d4-241">Minimum supported server</span></span><br/> | <span data-ttu-id="a15d4-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a15d4-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a15d4-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="a15d4-243">Namespace</span></span><br/>                | <span data-ttu-id="a15d4-244">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a15d4-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a15d4-245">MOF</span><span class="sxs-lookup"><span data-stu-id="a15d4-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a15d4-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a15d4-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a15d4-247">DLL</span><span class="sxs-lookup"><span data-stu-id="a15d4-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a15d4-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a15d4-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a15d4-249">Confira também</span><span class="sxs-lookup"><span data-stu-id="a15d4-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a15d4-250">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="a15d4-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="a15d4-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="a15d4-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="a15d4-252">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="a15d4-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="a15d4-253">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="a15d4-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="a15d4-254">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="a15d4-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

