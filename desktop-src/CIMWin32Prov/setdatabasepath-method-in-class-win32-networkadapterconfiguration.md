---
description: O método estático da classe WMI setbasepath define o caminho para os arquivos de banco de dados da Internet padrão (HOSTs, LMHOSTs, NETWORKs e PROTOCOLs).
ms.assetid: 373fef0f-9cdf-4785-8d73-3f00bbd60ae2
ms.tgt_platform: multiple
title: Método DatabasePath da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDatabasePath
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b66a9979ec97d4ceda16acad6488d3b84d5d3a54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501099"
---
# <a name="setdatabasepath-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="2bcfe-103">Método DatabasePath da \_ classe Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bcfe-103">SetDatabasePath method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="2bcfe-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **setbasepath** define o caminho para os arquivos de banco de dados da Internet padrão (hosts, Lmhosts, Networks e Protocols).</span><span class="sxs-lookup"><span data-stu-id="2bcfe-104">The **SetDatabasePath** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method sets the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span>

<span data-ttu-id="2bcfe-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2bcfe-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2bcfe-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2bcfe-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2bcfe-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2bcfe-107">Syntax</span></span>


```mof
uint32 SetDatabasePath(
  [in] string DatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="2bcfe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bcfe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bcfe-109">*DatabasePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2bcfe-109">*DatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-110">Caminho de arquivo válido para arquivos de banco de dados da Internet padrão (HOSTs, LMHOSTs, redes e protocolos) usados pela interface do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-110">Valid file path to standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS) used by the Windows Sockets interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bcfe-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2bcfe-111">Return value</span></span>

<span data-ttu-id="2bcfe-112">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (um) para uma conclusão bem-sucedida quando uma reinicialização é necessária, um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, a different number if there is an error.</span></span> <span data-ttu-id="2bcfe-113">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2bcfe-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2bcfe-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2bcfe-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2bcfe-115">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-116">0</span><span class="sxs-lookup"><span data-stu-id="2bcfe-116">0</span></span>

<span data-ttu-id="2bcfe-117">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-118">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-119">1</span><span class="sxs-lookup"><span data-stu-id="2bcfe-119">1</span></span>

<span data-ttu-id="2bcfe-120">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-121">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-122">64</span><span class="sxs-lookup"><span data-stu-id="2bcfe-122">64</span></span>

<span data-ttu-id="2bcfe-123">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-124">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-125">65</span><span class="sxs-lookup"><span data-stu-id="2bcfe-125">65</span></span>

<span data-ttu-id="2bcfe-126">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-127">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-128">66</span><span class="sxs-lookup"><span data-stu-id="2bcfe-128">66</span></span>

<span data-ttu-id="2bcfe-129">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-130">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-131">67</span><span class="sxs-lookup"><span data-stu-id="2bcfe-131">67</span></span>

<span data-ttu-id="2bcfe-132">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-133">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-134">68</span><span class="sxs-lookup"><span data-stu-id="2bcfe-134">68</span></span>

<span data-ttu-id="2bcfe-135">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-136">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-137">69</span><span class="sxs-lookup"><span data-stu-id="2bcfe-137">69</span></span>

<span data-ttu-id="2bcfe-138">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-139">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-140">70</span><span class="sxs-lookup"><span data-stu-id="2bcfe-140">70</span></span>

<span data-ttu-id="2bcfe-141">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-142">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-143">71</span><span class="sxs-lookup"><span data-stu-id="2bcfe-143">71</span></span>

<span data-ttu-id="2bcfe-144">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-145">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-146">72</span><span class="sxs-lookup"><span data-stu-id="2bcfe-146">72</span></span>

<span data-ttu-id="2bcfe-147">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-148">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-149">73</span><span class="sxs-lookup"><span data-stu-id="2bcfe-149">73</span></span>

<span data-ttu-id="2bcfe-150">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-151">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-152">74</span><span class="sxs-lookup"><span data-stu-id="2bcfe-152">74</span></span>

<span data-ttu-id="2bcfe-153">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-154">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-155">75</span><span class="sxs-lookup"><span data-stu-id="2bcfe-155">75</span></span>

<span data-ttu-id="2bcfe-156">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-157">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-158">76</span><span class="sxs-lookup"><span data-stu-id="2bcfe-158">76</span></span>

<span data-ttu-id="2bcfe-159">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-160">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-161">77</span><span class="sxs-lookup"><span data-stu-id="2bcfe-161">77</span></span>

<span data-ttu-id="2bcfe-162">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-163">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-164">78</span><span class="sxs-lookup"><span data-stu-id="2bcfe-164">78</span></span>

<span data-ttu-id="2bcfe-165">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-166">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-167">79</span><span class="sxs-lookup"><span data-stu-id="2bcfe-167">79</span></span>

<span data-ttu-id="2bcfe-168">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-169">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-170">80</span><span class="sxs-lookup"><span data-stu-id="2bcfe-170">80</span></span>

<span data-ttu-id="2bcfe-171">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-172">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-173">81</span><span class="sxs-lookup"><span data-stu-id="2bcfe-173">81</span></span>

<span data-ttu-id="2bcfe-174">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-175">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-176">82</span><span class="sxs-lookup"><span data-stu-id="2bcfe-176">82</span></span>

<span data-ttu-id="2bcfe-177">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-178">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-179">83</span><span class="sxs-lookup"><span data-stu-id="2bcfe-179">83</span></span>

<span data-ttu-id="2bcfe-180">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-181">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-182">84</span><span class="sxs-lookup"><span data-stu-id="2bcfe-182">84</span></span>

<span data-ttu-id="2bcfe-183">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-184">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-185">85</span><span class="sxs-lookup"><span data-stu-id="2bcfe-185">85</span></span>

<span data-ttu-id="2bcfe-186">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-187">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-188">86</span><span class="sxs-lookup"><span data-stu-id="2bcfe-188">86</span></span>

<span data-ttu-id="2bcfe-189">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-190">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-191">87</span><span class="sxs-lookup"><span data-stu-id="2bcfe-191">87</span></span>

<span data-ttu-id="2bcfe-192">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-193">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-194">88</span><span class="sxs-lookup"><span data-stu-id="2bcfe-194">88</span></span>

<span data-ttu-id="2bcfe-195">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-196">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-197">89</span><span class="sxs-lookup"><span data-stu-id="2bcfe-197">89</span></span>

<span data-ttu-id="2bcfe-198">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-199">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-200">90</span><span class="sxs-lookup"><span data-stu-id="2bcfe-200">90</span></span>

<span data-ttu-id="2bcfe-201">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-202">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-203">91</span><span class="sxs-lookup"><span data-stu-id="2bcfe-203">91</span></span>

<span data-ttu-id="2bcfe-204">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-205">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-206">92</span><span class="sxs-lookup"><span data-stu-id="2bcfe-206">92</span></span>

<span data-ttu-id="2bcfe-207">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-208">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-209">93</span><span class="sxs-lookup"><span data-stu-id="2bcfe-209">93</span></span>

<span data-ttu-id="2bcfe-210">Já existe.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-211">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-212">94</span><span class="sxs-lookup"><span data-stu-id="2bcfe-212">94</span></span>

<span data-ttu-id="2bcfe-213">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-214">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-215">95</span><span class="sxs-lookup"><span data-stu-id="2bcfe-215">95</span></span>

<span data-ttu-id="2bcfe-216">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-217">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-218">96</span><span class="sxs-lookup"><span data-stu-id="2bcfe-218">96</span></span>

<span data-ttu-id="2bcfe-219">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-220">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-221">97</span><span class="sxs-lookup"><span data-stu-id="2bcfe-221">97</span></span>

<span data-ttu-id="2bcfe-222">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-223">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-224">98</span><span class="sxs-lookup"><span data-stu-id="2bcfe-224">98</span></span>

<span data-ttu-id="2bcfe-225">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-226">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-227">100</span><span class="sxs-lookup"><span data-stu-id="2bcfe-227">100</span></span>

<span data-ttu-id="2bcfe-228">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2bcfe-229">**Outras**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="2bcfe-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="2bcfe-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bcfe-231">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bcfe-231">Remarks</span></span>

<span data-ttu-id="2bcfe-232">Esse método é usado pela interface do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="2bcfe-232">This method is used by the Windows Sockets interface.</span></span> <span data-ttu-id="2bcfe-233">O caminho padrão é% SystemRoot% \\ System32 \\ drivers \\ .</span><span class="sxs-lookup"><span data-stu-id="2bcfe-233">The default path is %SystemRoot%\\system32\\drivers\\ .</span></span>

## <a name="examples"></a><span data-ttu-id="2bcfe-234">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2bcfe-234">Examples</span></span>

<span data-ttu-id="2bcfe-235">O exemplo de [Modificar o caminho do banco de dados para todos os adaptadores de rede de](https://Gallery.TechNet.Microsoft.Com/94bfa42f-f6a3-482f-8d5a-5445a2475bee) VBScript na galeria do TechNet usa DatabasePath para definir o caminho para os arquivos de banco de dados da Internet padrão (hosts, Lmhosts, redes, protocolos) usados pela interface do Windows Sockets. </span><span class="sxs-lookup"><span data-stu-id="2bcfe-235">The [Modify the Database Path for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/94bfa42f-f6a3-482f-8d5a-5445a2475bee) VBScript sample on TechNet Gallery uses **SetDatabasePath** to set the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, PROTOCOLS) used by the Windows Sockets interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bcfe-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bcfe-236">Requirements</span></span>



| <span data-ttu-id="2bcfe-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bcfe-237">Requirement</span></span> | <span data-ttu-id="2bcfe-238">Valor</span><span class="sxs-lookup"><span data-stu-id="2bcfe-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bcfe-239">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2bcfe-239">Minimum supported client</span></span><br/> | <span data-ttu-id="2bcfe-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bcfe-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2bcfe-241">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2bcfe-241">Minimum supported server</span></span><br/> | <span data-ttu-id="2bcfe-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2bcfe-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2bcfe-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="2bcfe-243">Namespace</span></span><br/>                | <span data-ttu-id="2bcfe-244">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2bcfe-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2bcfe-245">MOF</span><span class="sxs-lookup"><span data-stu-id="2bcfe-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bcfe-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2bcfe-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bcfe-247">DLL</span><span class="sxs-lookup"><span data-stu-id="2bcfe-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bcfe-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bcfe-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bcfe-249">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bcfe-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bcfe-250">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="2bcfe-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2bcfe-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="2bcfe-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="2bcfe-252">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="2bcfe-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="2bcfe-253">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="2bcfe-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="2bcfe-254">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="2bcfe-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

