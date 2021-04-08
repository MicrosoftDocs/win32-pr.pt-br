---
description: O método estático da classe WMI EnableDNS habilita o DNS (sistema de nomes de domínio) para o serviço.
ms.assetid: 083dccb1-eb38-4ae5-a252-0001759c0f50
ms.tgt_platform: multiple
title: Método EnableDNS da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDNS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc217211455d8804de47b2b3ffc761d4328fa49a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089111"
---
# <a name="enabledns-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="1322f-103">Método EnableDNS da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="1322f-103">EnableDNS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="1322f-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ENABLEDNS** habilita o DNS (sistema de nomes de domínio) para o serviço.</span><span class="sxs-lookup"><span data-stu-id="1322f-104">The **EnableDNS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables the Domain Name System (DNS) for service.</span></span>

<span data-ttu-id="1322f-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1322f-105">This topic uses the Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1322f-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1322f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1322f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1322f-107">Syntax</span></span>


```mof
uint32 EnableDNS(
  [in, optional] string DNSHostName,
  [in, optional] string DNSDomain,
  [in, optional] string DNSServerSearchOrder[],
  [in, optional] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="1322f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1322f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1322f-109">*DNSHostName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1322f-109">*DNSHostName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1322f-110">Nome do host DNS que esse método habilita.</span><span class="sxs-lookup"><span data-stu-id="1322f-110">Name of the DNS host that this method enables.</span></span>

<span data-ttu-id="1322f-111">Exemplo: "corpdns"</span><span class="sxs-lookup"><span data-stu-id="1322f-111">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="1322f-112">*DNSDomain* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1322f-112">*DNSDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1322f-113">Representa um nome de organização seguido por um ponto e uma extensão que indica o tipo de organização.</span><span class="sxs-lookup"><span data-stu-id="1322f-113">Represents an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="1322f-114">Exemplo: "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="1322f-114">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="1322f-115">*DNSServerSearchOrder* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1322f-115">*DNSServerSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1322f-116">Lista de endereços IP do servidor para consultar servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="1322f-116">List of server IP addresses to query for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-117">*DNSDomainSuffixSearchOrder* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1322f-117">*DNSDomainSuffixSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1322f-118">Sufixo de domínio DNS que é anexado a um nome de host durante a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="1322f-118">DNS domain suffix that is appended to a host name during name resolution.</span></span> <span data-ttu-id="1322f-119">Ao resolver um FQDN (nome de domínio totalmente qualificado) de um nome somente de host, o sistema anexa o nome de domínio local.</span><span class="sxs-lookup"><span data-stu-id="1322f-119">When resolving a fully qualified domain name (FQDN) from a host-only name, the system appends the local domain name.</span></span> <span data-ttu-id="1322f-120">Se a resolução de nomes não for bem-sucedida, o sistema usará a lista de sufixos de domínio para criar FQDNs adicionais na ordem listada e, em seguida, consultará os servidores DNS para cada um.</span><span class="sxs-lookup"><span data-stu-id="1322f-120">If the name resolution is not successful, the system uses the domain suffix list to create additional FQDNs in the order listed, and then queries DNS servers for each one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1322f-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1322f-121">Return value</span></span>

<span data-ttu-id="1322f-122">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando uma reinicialização não é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e qualquer outro número se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="1322f-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="1322f-123">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1322f-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1322f-124">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1322f-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1322f-125">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="1322f-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-126">0</span><span class="sxs-lookup"><span data-stu-id="1322f-126">0</span></span>

<span data-ttu-id="1322f-127">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="1322f-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-128">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="1322f-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-129">1</span><span class="sxs-lookup"><span data-stu-id="1322f-129">1</span></span>

<span data-ttu-id="1322f-130">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="1322f-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-131">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="1322f-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-132">64</span><span class="sxs-lookup"><span data-stu-id="1322f-132">64</span></span>

<span data-ttu-id="1322f-133">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="1322f-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-134">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="1322f-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-135">65</span><span class="sxs-lookup"><span data-stu-id="1322f-135">65</span></span>

<span data-ttu-id="1322f-136">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="1322f-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-137">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="1322f-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-138">66</span><span class="sxs-lookup"><span data-stu-id="1322f-138">66</span></span>

<span data-ttu-id="1322f-139">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="1322f-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-140">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="1322f-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-141">67</span><span class="sxs-lookup"><span data-stu-id="1322f-141">67</span></span>

<span data-ttu-id="1322f-142">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="1322f-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-143">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="1322f-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-144">68</span><span class="sxs-lookup"><span data-stu-id="1322f-144">68</span></span>

<span data-ttu-id="1322f-145">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="1322f-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-146">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="1322f-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-147">69</span><span class="sxs-lookup"><span data-stu-id="1322f-147">69</span></span>

<span data-ttu-id="1322f-148">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="1322f-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-149">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="1322f-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-150">70</span><span class="sxs-lookup"><span data-stu-id="1322f-150">70</span></span>

<span data-ttu-id="1322f-151">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="1322f-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-152">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="1322f-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-153">71</span><span class="sxs-lookup"><span data-stu-id="1322f-153">71</span></span>

<span data-ttu-id="1322f-154">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="1322f-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-155">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="1322f-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-156">72</span><span class="sxs-lookup"><span data-stu-id="1322f-156">72</span></span>

<span data-ttu-id="1322f-157">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="1322f-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-158">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="1322f-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-159">73</span><span class="sxs-lookup"><span data-stu-id="1322f-159">73</span></span>

<span data-ttu-id="1322f-160">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="1322f-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-161">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="1322f-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-162">74</span><span class="sxs-lookup"><span data-stu-id="1322f-162">74</span></span>

<span data-ttu-id="1322f-163">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="1322f-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-164">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="1322f-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-165">75</span><span class="sxs-lookup"><span data-stu-id="1322f-165">75</span></span>

<span data-ttu-id="1322f-166">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="1322f-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-167">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="1322f-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-168">76</span><span class="sxs-lookup"><span data-stu-id="1322f-168">76</span></span>

<span data-ttu-id="1322f-169">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="1322f-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-170">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="1322f-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-171">77</span><span class="sxs-lookup"><span data-stu-id="1322f-171">77</span></span>

<span data-ttu-id="1322f-172">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="1322f-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-173">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="1322f-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-174">78</span><span class="sxs-lookup"><span data-stu-id="1322f-174">78</span></span>

<span data-ttu-id="1322f-175">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="1322f-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-176">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="1322f-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-177">79</span><span class="sxs-lookup"><span data-stu-id="1322f-177">79</span></span>

<span data-ttu-id="1322f-178">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="1322f-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-179">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="1322f-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-180">80</span><span class="sxs-lookup"><span data-stu-id="1322f-180">80</span></span>

<span data-ttu-id="1322f-181">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1322f-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-182">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="1322f-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-183">81</span><span class="sxs-lookup"><span data-stu-id="1322f-183">81</span></span>

<span data-ttu-id="1322f-184">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="1322f-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-185">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="1322f-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-186">82</span><span class="sxs-lookup"><span data-stu-id="1322f-186">82</span></span>

<span data-ttu-id="1322f-187">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="1322f-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-188">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="1322f-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-189">83</span><span class="sxs-lookup"><span data-stu-id="1322f-189">83</span></span>

<span data-ttu-id="1322f-190">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="1322f-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-191">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="1322f-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-192">84</span><span class="sxs-lookup"><span data-stu-id="1322f-192">84</span></span>

<span data-ttu-id="1322f-193">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="1322f-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-194">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="1322f-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-195">85</span><span class="sxs-lookup"><span data-stu-id="1322f-195">85</span></span>

<span data-ttu-id="1322f-196">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="1322f-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-197">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="1322f-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-198">86</span><span class="sxs-lookup"><span data-stu-id="1322f-198">86</span></span>

<span data-ttu-id="1322f-199">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="1322f-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-200">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="1322f-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-201">87</span><span class="sxs-lookup"><span data-stu-id="1322f-201">87</span></span>

<span data-ttu-id="1322f-202">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="1322f-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-203">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="1322f-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-204">88</span><span class="sxs-lookup"><span data-stu-id="1322f-204">88</span></span>

<span data-ttu-id="1322f-205">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="1322f-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-206">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="1322f-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-207">89</span><span class="sxs-lookup"><span data-stu-id="1322f-207">89</span></span>

<span data-ttu-id="1322f-208">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="1322f-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-209">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="1322f-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-210">90</span><span class="sxs-lookup"><span data-stu-id="1322f-210">90</span></span>

<span data-ttu-id="1322f-211">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="1322f-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-212">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="1322f-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-213">91</span><span class="sxs-lookup"><span data-stu-id="1322f-213">91</span></span>

<span data-ttu-id="1322f-214">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="1322f-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-215">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="1322f-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-216">92</span><span class="sxs-lookup"><span data-stu-id="1322f-216">92</span></span>

<span data-ttu-id="1322f-217">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="1322f-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-218">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="1322f-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-219">93</span><span class="sxs-lookup"><span data-stu-id="1322f-219">93</span></span>

<span data-ttu-id="1322f-220">Já existe.</span><span class="sxs-lookup"><span data-stu-id="1322f-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-221">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="1322f-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-222">94</span><span class="sxs-lookup"><span data-stu-id="1322f-222">94</span></span>

<span data-ttu-id="1322f-223">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="1322f-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-224">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="1322f-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-225">95</span><span class="sxs-lookup"><span data-stu-id="1322f-225">95</span></span>

<span data-ttu-id="1322f-226">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="1322f-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-227">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="1322f-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-228">96</span><span class="sxs-lookup"><span data-stu-id="1322f-228">96</span></span>

<span data-ttu-id="1322f-229">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="1322f-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-230">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="1322f-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-231">97</span><span class="sxs-lookup"><span data-stu-id="1322f-231">97</span></span>

<span data-ttu-id="1322f-232">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="1322f-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-233">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="1322f-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-234">98</span><span class="sxs-lookup"><span data-stu-id="1322f-234">98</span></span>

<span data-ttu-id="1322f-235">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="1322f-235">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-236">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="1322f-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-237">100</span><span class="sxs-lookup"><span data-stu-id="1322f-237">100</span></span>

<span data-ttu-id="1322f-238">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="1322f-238">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1322f-239">**Outras**</span><span class="sxs-lookup"><span data-stu-id="1322f-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1322f-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="1322f-240">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="1322f-241">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1322f-241">Examples</span></span>

<span data-ttu-id="1322f-242">O exemplo de código a seguir, extraído da amostra de código [Ativar DNS em todos os adaptadores de rede](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) , na galeria do TechNet, HABILITA o DNS para todos os adaptadores de rede em um computador.</span><span class="sxs-lookup"><span data-stu-id="1322f-242">The following code sample, taken from the [Enable DNS on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) VBScript code sample on TechNet Gallery, enables DNS for all network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
strHostName = "fabrikam1" 
arrDNSSuffixes = Array("hr.fabrikam.com", "research.fabrikam.com") 
objNetworkSettings.EnableDNS strHostName, , , arrDNSSuffixes 
```



## <a name="requirements"></a><span data-ttu-id="1322f-243">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1322f-243">Requirements</span></span>



| <span data-ttu-id="1322f-244">Requisito</span><span class="sxs-lookup"><span data-stu-id="1322f-244">Requirement</span></span> | <span data-ttu-id="1322f-245">Valor</span><span class="sxs-lookup"><span data-stu-id="1322f-245">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1322f-246">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1322f-246">Minimum supported client</span></span><br/> | <span data-ttu-id="1322f-247">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1322f-247">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1322f-248">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1322f-248">Minimum supported server</span></span><br/> | <span data-ttu-id="1322f-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1322f-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1322f-250">Namespace</span><span class="sxs-lookup"><span data-stu-id="1322f-250">Namespace</span></span><br/>                | <span data-ttu-id="1322f-251">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1322f-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1322f-252">MOF</span><span class="sxs-lookup"><span data-stu-id="1322f-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1322f-253"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1322f-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1322f-254">DLL</span><span class="sxs-lookup"><span data-stu-id="1322f-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1322f-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1322f-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1322f-256">Confira também</span><span class="sxs-lookup"><span data-stu-id="1322f-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1322f-257">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="1322f-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1322f-258">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="1322f-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="1322f-259">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="1322f-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="1322f-260">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="1322f-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="1322f-261">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="1322f-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

