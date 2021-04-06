---
description: O método estático da classe WMI SetDNSSuffixSearchOrder usa uma matriz de elementos de cadeia de caracteres para definir a ordem de pesquisa de sufixo.
ms.assetid: 1ad9fc99-8c57-43d4-92d2-b12f2c1451cb
ms.tgt_platform: multiple
title: Método SetDNSSuffixSearchOrder da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSSuffixSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10088b1d0722f968e5d3742984baa91ec3e423aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826521"
---
# <a name="setdnssuffixsearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="75c7f-103">Método SetDNSSuffixSearchOrder da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="75c7f-103">SetDNSSuffixSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="75c7f-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSSuffixSearchOrder** usa uma matriz de elementos de cadeia de caracteres para definir a ordem de pesquisa de sufixo.</span><span class="sxs-lookup"><span data-stu-id="75c7f-104">The **SetDNSSuffixSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method uses an array of string elements to set the suffix search order.</span></span>

<span data-ttu-id="75c7f-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="75c7f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="75c7f-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="75c7f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="75c7f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75c7f-107">Syntax</span></span>


```mof
uint32 SetDNSSuffixSearchOrder(
  [in] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="75c7f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75c7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75c7f-109">*DNSDomainSuffixSearchOrder* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75c7f-109">*DNSDomainSuffixSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-110">Lista de sufixos de servidor para consultar servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="75c7f-110">List of server suffixes to query for DNS servers.</span></span> <span data-ttu-id="75c7f-111">O local do registro do sufixo DNS é **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **tcpip \| nameserver**</span><span class="sxs-lookup"><span data-stu-id="75c7f-111">The registry location of the DNS suffix is **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Tcpip\|NameServer**</span></span>

<span data-ttu-id="75c7f-112">Exemplo: "suffix1.company.com", "suffix2.company.com"</span><span class="sxs-lookup"><span data-stu-id="75c7f-112">Example: "suffix1.company.com", "suffix2.company.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75c7f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75c7f-113">Return value</span></span>

<span data-ttu-id="75c7f-114">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="75c7f-114">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="75c7f-115">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="75c7f-115">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="75c7f-116">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="75c7f-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="75c7f-117">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="75c7f-117">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-118">0</span><span class="sxs-lookup"><span data-stu-id="75c7f-118">0</span></span>

<span data-ttu-id="75c7f-119">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="75c7f-119">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-120">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="75c7f-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-121">1</span><span class="sxs-lookup"><span data-stu-id="75c7f-121">1</span></span>

<span data-ttu-id="75c7f-122">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="75c7f-122">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-123">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="75c7f-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-124">64</span><span class="sxs-lookup"><span data-stu-id="75c7f-124">64</span></span>

<span data-ttu-id="75c7f-125">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="75c7f-125">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-126">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="75c7f-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-127">65</span><span class="sxs-lookup"><span data-stu-id="75c7f-127">65</span></span>

<span data-ttu-id="75c7f-128">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="75c7f-128">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-129">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="75c7f-129">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-130">66</span><span class="sxs-lookup"><span data-stu-id="75c7f-130">66</span></span>

<span data-ttu-id="75c7f-131">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="75c7f-131">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-132">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="75c7f-132">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-133">67</span><span class="sxs-lookup"><span data-stu-id="75c7f-133">67</span></span>

<span data-ttu-id="75c7f-134">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="75c7f-134">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-135">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="75c7f-135">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-136">68</span><span class="sxs-lookup"><span data-stu-id="75c7f-136">68</span></span>

<span data-ttu-id="75c7f-137">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="75c7f-137">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-138">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="75c7f-138">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-139">69</span><span class="sxs-lookup"><span data-stu-id="75c7f-139">69</span></span>

<span data-ttu-id="75c7f-140">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="75c7f-140">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-141">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="75c7f-141">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-142">70</span><span class="sxs-lookup"><span data-stu-id="75c7f-142">70</span></span>

<span data-ttu-id="75c7f-143">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="75c7f-143">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-144">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="75c7f-144">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-145">71</span><span class="sxs-lookup"><span data-stu-id="75c7f-145">71</span></span>

<span data-ttu-id="75c7f-146">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="75c7f-146">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-147">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="75c7f-147">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-148">72</span><span class="sxs-lookup"><span data-stu-id="75c7f-148">72</span></span>

<span data-ttu-id="75c7f-149">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="75c7f-149">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-150">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="75c7f-150">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-151">73</span><span class="sxs-lookup"><span data-stu-id="75c7f-151">73</span></span>

<span data-ttu-id="75c7f-152">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="75c7f-152">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-153">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="75c7f-153">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-154">74</span><span class="sxs-lookup"><span data-stu-id="75c7f-154">74</span></span>

<span data-ttu-id="75c7f-155">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="75c7f-155">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-156">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="75c7f-156">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-157">75</span><span class="sxs-lookup"><span data-stu-id="75c7f-157">75</span></span>

<span data-ttu-id="75c7f-158">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="75c7f-158">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-159">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="75c7f-159">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-160">76</span><span class="sxs-lookup"><span data-stu-id="75c7f-160">76</span></span>

<span data-ttu-id="75c7f-161">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="75c7f-161">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-162">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="75c7f-162">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-163">77</span><span class="sxs-lookup"><span data-stu-id="75c7f-163">77</span></span>

<span data-ttu-id="75c7f-164">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="75c7f-164">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-165">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="75c7f-165">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-166">78</span><span class="sxs-lookup"><span data-stu-id="75c7f-166">78</span></span>

<span data-ttu-id="75c7f-167">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="75c7f-167">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-168">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="75c7f-168">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-169">79</span><span class="sxs-lookup"><span data-stu-id="75c7f-169">79</span></span>

<span data-ttu-id="75c7f-170">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="75c7f-170">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-171">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="75c7f-171">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-172">80</span><span class="sxs-lookup"><span data-stu-id="75c7f-172">80</span></span>

<span data-ttu-id="75c7f-173">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="75c7f-173">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-174">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="75c7f-174">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-175">81</span><span class="sxs-lookup"><span data-stu-id="75c7f-175">81</span></span>

<span data-ttu-id="75c7f-176">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="75c7f-176">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-177">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="75c7f-177">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-178">82</span><span class="sxs-lookup"><span data-stu-id="75c7f-178">82</span></span>

<span data-ttu-id="75c7f-179">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="75c7f-179">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-180">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="75c7f-180">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-181">83</span><span class="sxs-lookup"><span data-stu-id="75c7f-181">83</span></span>

<span data-ttu-id="75c7f-182">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="75c7f-182">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-183">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="75c7f-183">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-184">84</span><span class="sxs-lookup"><span data-stu-id="75c7f-184">84</span></span>

<span data-ttu-id="75c7f-185">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="75c7f-185">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-186">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="75c7f-186">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-187">85</span><span class="sxs-lookup"><span data-stu-id="75c7f-187">85</span></span>

<span data-ttu-id="75c7f-188">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="75c7f-188">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-189">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="75c7f-189">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-190">86</span><span class="sxs-lookup"><span data-stu-id="75c7f-190">86</span></span>

<span data-ttu-id="75c7f-191">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="75c7f-191">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-192">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="75c7f-192">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-193">87</span><span class="sxs-lookup"><span data-stu-id="75c7f-193">87</span></span>

<span data-ttu-id="75c7f-194">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="75c7f-194">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-195">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="75c7f-195">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-196">88</span><span class="sxs-lookup"><span data-stu-id="75c7f-196">88</span></span>

<span data-ttu-id="75c7f-197">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="75c7f-197">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-198">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="75c7f-198">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-199">89</span><span class="sxs-lookup"><span data-stu-id="75c7f-199">89</span></span>

<span data-ttu-id="75c7f-200">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="75c7f-200">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-201">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="75c7f-201">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-202">90</span><span class="sxs-lookup"><span data-stu-id="75c7f-202">90</span></span>

<span data-ttu-id="75c7f-203">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="75c7f-203">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-204">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="75c7f-204">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-205">91</span><span class="sxs-lookup"><span data-stu-id="75c7f-205">91</span></span>

<span data-ttu-id="75c7f-206">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="75c7f-206">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-207">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="75c7f-207">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-208">92</span><span class="sxs-lookup"><span data-stu-id="75c7f-208">92</span></span>

<span data-ttu-id="75c7f-209">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="75c7f-209">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-210">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="75c7f-210">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-211">93</span><span class="sxs-lookup"><span data-stu-id="75c7f-211">93</span></span>

<span data-ttu-id="75c7f-212">Já existe.</span><span class="sxs-lookup"><span data-stu-id="75c7f-212">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-213">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="75c7f-213">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-214">94</span><span class="sxs-lookup"><span data-stu-id="75c7f-214">94</span></span>

<span data-ttu-id="75c7f-215">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="75c7f-215">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-216">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="75c7f-216">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-217">95</span><span class="sxs-lookup"><span data-stu-id="75c7f-217">95</span></span>

<span data-ttu-id="75c7f-218">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="75c7f-218">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-219">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="75c7f-219">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-220">96</span><span class="sxs-lookup"><span data-stu-id="75c7f-220">96</span></span>

<span data-ttu-id="75c7f-221">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="75c7f-221">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-222">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="75c7f-222">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-223">97</span><span class="sxs-lookup"><span data-stu-id="75c7f-223">97</span></span>

<span data-ttu-id="75c7f-224">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="75c7f-224">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-225">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="75c7f-225">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-226">98</span><span class="sxs-lookup"><span data-stu-id="75c7f-226">98</span></span>

<span data-ttu-id="75c7f-227">Nem todas as concessões DHCP são liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="75c7f-227">Not all DHCP leases are released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-228">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="75c7f-228">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-229">100</span><span class="sxs-lookup"><span data-stu-id="75c7f-229">100</span></span>

<span data-ttu-id="75c7f-230">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="75c7f-230">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="75c7f-231">**Outras**</span><span class="sxs-lookup"><span data-stu-id="75c7f-231">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="75c7f-232">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="75c7f-232">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75c7f-233">Comentários</span><span class="sxs-lookup"><span data-stu-id="75c7f-233">Remarks</span></span>

<span data-ttu-id="75c7f-234">Essa é uma chamada independente de instância que se aplica a todos os adaptadores, mas somente ao Windows.</span><span class="sxs-lookup"><span data-stu-id="75c7f-234">This is an instance-independent call that applies to all adapters but only for Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="75c7f-235">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75c7f-235">Examples</span></span>

<span data-ttu-id="75c7f-236">A amostra de código [Modificar a ordem de pesquisa de sufixo DNS para todos os adaptadores de rede](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) VBScript configura um computador para usar dois sufixos DNS ao executar pesquisas de DNS.</span><span class="sxs-lookup"><span data-stu-id="75c7f-236">The [Modify the DNS Suffix Search Order for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) VBScript code sample configures a computer to use two DNS suffixes when performing DNS searches.</span></span>

<span data-ttu-id="75c7f-237">A amostra [Ativar configurações de DHCP em um computador de](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript define todas as configurações normalmente necessárias para habilitar o DHCP em um computador.</span><span class="sxs-lookup"><span data-stu-id="75c7f-237">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample configures all the settings typically required to enable DHCP on a computer.</span></span>

<span data-ttu-id="75c7f-238">O código do PowerShell a seguir define a ordem de pesquisa de sufixo DNS.</span><span class="sxs-lookup"><span data-stu-id="75c7f-238">The following PowerShell code sets the DNS suffix search order.</span></span>


```PowerShell
#First store the suffixes to set in a variable
$suffixes = 'microsoft.com', 'google.com', 'yahoo.com'

#Since this is a static method, get a class object and then call the method. 
$class = [wmiclass]'Win32_NetworkAdapterConfiguration'
$class.SetDNSSuffixSearchOrder($suffixes)
```



## <a name="requirements"></a><span data-ttu-id="75c7f-239">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75c7f-239">Requirements</span></span>



| <span data-ttu-id="75c7f-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="75c7f-240">Requirement</span></span> | <span data-ttu-id="75c7f-241">Valor</span><span class="sxs-lookup"><span data-stu-id="75c7f-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75c7f-242">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75c7f-242">Minimum supported client</span></span><br/> | <span data-ttu-id="75c7f-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75c7f-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75c7f-244">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75c7f-244">Minimum supported server</span></span><br/> | <span data-ttu-id="75c7f-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75c7f-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75c7f-246">Namespace</span><span class="sxs-lookup"><span data-stu-id="75c7f-246">Namespace</span></span><br/>                | <span data-ttu-id="75c7f-247">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="75c7f-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="75c7f-248">MOF</span><span class="sxs-lookup"><span data-stu-id="75c7f-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75c7f-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75c7f-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="75c7f-250">DLL</span><span class="sxs-lookup"><span data-stu-id="75c7f-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75c7f-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75c7f-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75c7f-252">Confira também</span><span class="sxs-lookup"><span data-stu-id="75c7f-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c7f-253">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="75c7f-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="75c7f-254">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="75c7f-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="75c7f-255">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="75c7f-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="75c7f-256">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="75c7f-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="75c7f-257">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="75c7f-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

