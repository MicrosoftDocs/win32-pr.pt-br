---
description: EnableIPSec&\# 8194; O método de classe WMI habilita o IPsec (Internet Protocol Security) em um adaptador de rede habilitado para TCP/IP.
ms.assetid: 0a45d864-606d-4adb-9b51-62d46a0d68b1
ms.tgt_platform: multiple
title: Método EnableIPSec da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6988d68f9939752e3c8c2c9ace063b895a2d3720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826308"
---
# <a name="enableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="c1fe8-103">Método EnableIPSec da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1fe8-103">EnableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="c1fe8-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableIPSec** habilita o IPsec (Internet Protocol Security) em um adaptador de rede habilitado para TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-104">The **EnableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables Internet Protocol security (IPsec) on a TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="c1fe8-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c1fe8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c1fe8-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c1fe8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c1fe8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1fe8-107">Syntax</span></span>


```mof
uint32 EnableIPSec(
  [in] string IPSecPermitTCPPorts[],
  [in] string IPSecPermitUDPPorts[],
  [in] string IPSecPermitIPProtocols[]
);
```



## <a name="parameters"></a><span data-ttu-id="c1fe8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1fe8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1fe8-109">*IPSecPermitTCPPorts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1fe8-109">*IPSecPermitTCPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-110">Lista de portas a serem concedidas à permissão de acesso para TCP.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-110">List of ports to be granted access permission for TCP.</span></span> <span data-ttu-id="c1fe8-111">Um valor numérico de 0 (zero) indica que a permissão de acesso é concedida para todas as portas.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-111">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="c1fe8-112">Uma matriz vazia indica que nenhuma porta deve receber permissão de acesso.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-112">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-113">*IPSecPermitUDPPorts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1fe8-113">*IPSecPermitUDPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-114">Lista de portas a serem concedidas à permissão de acesso para UDP.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-114">List of ports to be granted access permission for UDP.</span></span> <span data-ttu-id="c1fe8-115">Um valor numérico de 0 (zero) indica que a permissão de acesso é concedida para todas as portas.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-115">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="c1fe8-116">Uma matriz vazia indica que nenhuma porta deve receber permissão de acesso.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-116">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-117">*IPSecPermitIPProtocols* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1fe8-117">*IPSecPermitIPProtocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-118">Lista de protocolos permitidos para execução no IP.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-118">List of protocols permitted to run over the IP.</span></span> <span data-ttu-id="c1fe8-119">Um valor numérico de 0 (zero) indica que a permissão de acesso é concedida para todos os protocolos.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-119">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="c1fe8-120">Uma matriz vazia indica que nenhum protocolo recebe permissão de acesso.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-120">An empty array indicates that no protocols are granted access permission.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1fe8-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1fe8-121">Return value</span></span>

<span data-ttu-id="c1fe8-122">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando uma reinicialização não é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e qualquer outro número se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="c1fe8-123">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c1fe8-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c1fe8-124">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c1fe8-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c1fe8-125">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-126">0</span><span class="sxs-lookup"><span data-stu-id="c1fe8-126">0</span></span>

<span data-ttu-id="c1fe8-127">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-128">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-129">1</span><span class="sxs-lookup"><span data-stu-id="c1fe8-129">1</span></span>

<span data-ttu-id="c1fe8-130">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-131">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-132">64</span><span class="sxs-lookup"><span data-stu-id="c1fe8-132">64</span></span>

<span data-ttu-id="c1fe8-133">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-134">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-135">65</span><span class="sxs-lookup"><span data-stu-id="c1fe8-135">65</span></span>

<span data-ttu-id="c1fe8-136">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-137">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-138">66</span><span class="sxs-lookup"><span data-stu-id="c1fe8-138">66</span></span>

<span data-ttu-id="c1fe8-139">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-140">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-141">67</span><span class="sxs-lookup"><span data-stu-id="c1fe8-141">67</span></span>

<span data-ttu-id="c1fe8-142">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-143">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-144">68</span><span class="sxs-lookup"><span data-stu-id="c1fe8-144">68</span></span>

<span data-ttu-id="c1fe8-145">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-146">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-147">69</span><span class="sxs-lookup"><span data-stu-id="c1fe8-147">69</span></span>

<span data-ttu-id="c1fe8-148">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-149">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-150">70</span><span class="sxs-lookup"><span data-stu-id="c1fe8-150">70</span></span>

<span data-ttu-id="c1fe8-151">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-152">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-153">71</span><span class="sxs-lookup"><span data-stu-id="c1fe8-153">71</span></span>

<span data-ttu-id="c1fe8-154">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-155">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-156">72</span><span class="sxs-lookup"><span data-stu-id="c1fe8-156">72</span></span>

<span data-ttu-id="c1fe8-157">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-158">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-159">73</span><span class="sxs-lookup"><span data-stu-id="c1fe8-159">73</span></span>

<span data-ttu-id="c1fe8-160">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-161">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-162">74</span><span class="sxs-lookup"><span data-stu-id="c1fe8-162">74</span></span>

<span data-ttu-id="c1fe8-163">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-164">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-165">75</span><span class="sxs-lookup"><span data-stu-id="c1fe8-165">75</span></span>

<span data-ttu-id="c1fe8-166">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-167">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-168">76</span><span class="sxs-lookup"><span data-stu-id="c1fe8-168">76</span></span>

<span data-ttu-id="c1fe8-169">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-170">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-171">77</span><span class="sxs-lookup"><span data-stu-id="c1fe8-171">77</span></span>

<span data-ttu-id="c1fe8-172">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-173">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-174">78</span><span class="sxs-lookup"><span data-stu-id="c1fe8-174">78</span></span>

<span data-ttu-id="c1fe8-175">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-176">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-177">79</span><span class="sxs-lookup"><span data-stu-id="c1fe8-177">79</span></span>

<span data-ttu-id="c1fe8-178">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-179">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-180">80</span><span class="sxs-lookup"><span data-stu-id="c1fe8-180">80</span></span>

<span data-ttu-id="c1fe8-181">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-182">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-183">81</span><span class="sxs-lookup"><span data-stu-id="c1fe8-183">81</span></span>

<span data-ttu-id="c1fe8-184">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-185">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-186">82</span><span class="sxs-lookup"><span data-stu-id="c1fe8-186">82</span></span>

<span data-ttu-id="c1fe8-187">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-188">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-189">83</span><span class="sxs-lookup"><span data-stu-id="c1fe8-189">83</span></span>

<span data-ttu-id="c1fe8-190">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-191">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-192">84</span><span class="sxs-lookup"><span data-stu-id="c1fe8-192">84</span></span>

<span data-ttu-id="c1fe8-193">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-194">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-195">85</span><span class="sxs-lookup"><span data-stu-id="c1fe8-195">85</span></span>

<span data-ttu-id="c1fe8-196">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-197">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-198">86</span><span class="sxs-lookup"><span data-stu-id="c1fe8-198">86</span></span>

<span data-ttu-id="c1fe8-199">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-200">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-201">87</span><span class="sxs-lookup"><span data-stu-id="c1fe8-201">87</span></span>

<span data-ttu-id="c1fe8-202">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-203">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-204">88</span><span class="sxs-lookup"><span data-stu-id="c1fe8-204">88</span></span>

<span data-ttu-id="c1fe8-205">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-206">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-207">89</span><span class="sxs-lookup"><span data-stu-id="c1fe8-207">89</span></span>

<span data-ttu-id="c1fe8-208">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-209">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-210">90</span><span class="sxs-lookup"><span data-stu-id="c1fe8-210">90</span></span>

<span data-ttu-id="c1fe8-211">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-212">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-213">91</span><span class="sxs-lookup"><span data-stu-id="c1fe8-213">91</span></span>

<span data-ttu-id="c1fe8-214">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-215">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-216">92</span><span class="sxs-lookup"><span data-stu-id="c1fe8-216">92</span></span>

<span data-ttu-id="c1fe8-217">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-218">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-219">93</span><span class="sxs-lookup"><span data-stu-id="c1fe8-219">93</span></span>

<span data-ttu-id="c1fe8-220">Já existe.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-221">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-222">94</span><span class="sxs-lookup"><span data-stu-id="c1fe8-222">94</span></span>

<span data-ttu-id="c1fe8-223">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-224">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-225">95</span><span class="sxs-lookup"><span data-stu-id="c1fe8-225">95</span></span>

<span data-ttu-id="c1fe8-226">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-227">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-228">96</span><span class="sxs-lookup"><span data-stu-id="c1fe8-228">96</span></span>

<span data-ttu-id="c1fe8-229">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-230">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-231">97</span><span class="sxs-lookup"><span data-stu-id="c1fe8-231">97</span></span>

<span data-ttu-id="c1fe8-232">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-233">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-234">98</span><span class="sxs-lookup"><span data-stu-id="c1fe8-234">98</span></span>

<span data-ttu-id="c1fe8-235">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-235">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-236">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-237">100</span><span class="sxs-lookup"><span data-stu-id="c1fe8-237">100</span></span>

<span data-ttu-id="c1fe8-238">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-238">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c1fe8-239">**Outras**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c1fe8-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="c1fe8-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1fe8-241">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1fe8-241">Remarks</span></span>

<span data-ttu-id="c1fe8-242">As portas são protegidas somente quando a propriedade **IPFilterSecurityEnabled** no [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) é **verdadeira**.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-242">Ports are secured only when the **IPFilterSecurityEnabled** property in [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) is **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="c1fe8-243">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c1fe8-243">Examples</span></span>

<span data-ttu-id="c1fe8-244">A amostra [Ativar IPSec em um adaptador de rede](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) do VBScript, na galeria do TechNet, usa **EnableIPSec** para habilitar a segurança de IP para um adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="c1fe8-244">The [Enable IPSec on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) VBScript sample, on TechNet Gallery, uses **EnableIPSec** to enable IP security for a network adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1fe8-245">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1fe8-245">Requirements</span></span>



| <span data-ttu-id="c1fe8-246">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1fe8-246">Requirement</span></span> | <span data-ttu-id="c1fe8-247">Valor</span><span class="sxs-lookup"><span data-stu-id="c1fe8-247">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1fe8-248">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1fe8-248">Minimum supported client</span></span><br/> | <span data-ttu-id="c1fe8-249">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1fe8-249">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c1fe8-250">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1fe8-250">Minimum supported server</span></span><br/> | <span data-ttu-id="c1fe8-251">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1fe8-251">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c1fe8-252">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1fe8-252">Namespace</span></span><br/>                | <span data-ttu-id="c1fe8-253">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c1fe8-253">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c1fe8-254">MOF</span><span class="sxs-lookup"><span data-stu-id="c1fe8-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1fe8-255"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1fe8-255"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1fe8-256">DLL</span><span class="sxs-lookup"><span data-stu-id="c1fe8-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1fe8-257"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1fe8-257"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1fe8-258">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1fe8-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1fe8-259">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="c1fe8-259">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="c1fe8-260">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="c1fe8-260">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="c1fe8-261">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="c1fe8-261">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="c1fe8-262">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="c1fe8-262">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="c1fe8-263">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="c1fe8-263">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

