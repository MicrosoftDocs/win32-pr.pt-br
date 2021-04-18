---
description: O método estático da classe WMI setkeepalivetime é usado para definir a frequência com que o TCP tenta verificar se uma conexão ociosa ainda está disponível enviando um pacote keep alive.
ms.assetid: 8640b109-928b-46fc-8dce-9ee5dcbd94e3
ms.tgt_platform: multiple
title: Método setkeepalivetime da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1dc2674f3c09626749b4c7ac6151349401670e27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749316"
---
# <a name="setkeepalivetime-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="886b5-103">Método setkeepalivetime da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="886b5-103">SetKeepAliveTime method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="886b5-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **setkeepalivetime** é usado para definir a frequência com que o TCP tenta verificar se uma conexão ociosa ainda está disponível enviando um pacote keep alive.</span><span class="sxs-lookup"><span data-stu-id="886b5-104">The **SetKeepAliveTime** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set how often TCP attempts to verify that an idle connection is still available by sending a Keep Alive packet.</span></span>

<span data-ttu-id="886b5-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="886b5-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="886b5-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="886b5-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="886b5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="886b5-107">Syntax</span></span>


```mof
uint32 SetKeepAliveTime(
  [in] uint32 KeepAliveTime
);
```



## <a name="parameters"></a><span data-ttu-id="886b5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="886b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="886b5-109">*KeepAliveTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="886b5-109">*KeepAliveTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="886b5-110">Intervalo, em milissegundos, o TCP aguarda para verificar se uma conexão ociosa ainda está disponível.</span><span class="sxs-lookup"><span data-stu-id="886b5-110">Interval, in milliseconds, the TCP waits to check that an idle connection is still available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="886b5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="886b5-111">Return value</span></span>

<span data-ttu-id="886b5-112">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="886b5-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="886b5-113">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="886b5-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="886b5-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="886b5-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="886b5-115">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="886b5-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-116">0</span><span class="sxs-lookup"><span data-stu-id="886b5-116">0</span></span>

<span data-ttu-id="886b5-117">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="886b5-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-118">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="886b5-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-119">1</span><span class="sxs-lookup"><span data-stu-id="886b5-119">1</span></span>

<span data-ttu-id="886b5-120">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="886b5-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-121">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="886b5-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-122">64</span><span class="sxs-lookup"><span data-stu-id="886b5-122">64</span></span>

<span data-ttu-id="886b5-123">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="886b5-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-124">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="886b5-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-125">65</span><span class="sxs-lookup"><span data-stu-id="886b5-125">65</span></span>

<span data-ttu-id="886b5-126">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="886b5-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-127">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="886b5-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-128">66</span><span class="sxs-lookup"><span data-stu-id="886b5-128">66</span></span>

<span data-ttu-id="886b5-129">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="886b5-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-130">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="886b5-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-131">67</span><span class="sxs-lookup"><span data-stu-id="886b5-131">67</span></span>

<span data-ttu-id="886b5-132">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="886b5-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-133">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="886b5-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-134">68</span><span class="sxs-lookup"><span data-stu-id="886b5-134">68</span></span>

<span data-ttu-id="886b5-135">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="886b5-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-136">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="886b5-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-137">69</span><span class="sxs-lookup"><span data-stu-id="886b5-137">69</span></span>

<span data-ttu-id="886b5-138">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="886b5-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-139">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="886b5-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-140">70</span><span class="sxs-lookup"><span data-stu-id="886b5-140">70</span></span>

<span data-ttu-id="886b5-141">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="886b5-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-142">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="886b5-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-143">71</span><span class="sxs-lookup"><span data-stu-id="886b5-143">71</span></span>

<span data-ttu-id="886b5-144">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="886b5-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-145">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="886b5-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-146">72</span><span class="sxs-lookup"><span data-stu-id="886b5-146">72</span></span>

<span data-ttu-id="886b5-147">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="886b5-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-148">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="886b5-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-149">73</span><span class="sxs-lookup"><span data-stu-id="886b5-149">73</span></span>

<span data-ttu-id="886b5-150">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="886b5-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-151">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="886b5-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-152">74</span><span class="sxs-lookup"><span data-stu-id="886b5-152">74</span></span>

<span data-ttu-id="886b5-153">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="886b5-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-154">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="886b5-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-155">75</span><span class="sxs-lookup"><span data-stu-id="886b5-155">75</span></span>

<span data-ttu-id="886b5-156">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="886b5-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-157">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="886b5-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-158">76</span><span class="sxs-lookup"><span data-stu-id="886b5-158">76</span></span>

<span data-ttu-id="886b5-159">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="886b5-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-160">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="886b5-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-161">77</span><span class="sxs-lookup"><span data-stu-id="886b5-161">77</span></span>

<span data-ttu-id="886b5-162">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="886b5-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-163">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="886b5-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-164">78</span><span class="sxs-lookup"><span data-stu-id="886b5-164">78</span></span>

<span data-ttu-id="886b5-165">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="886b5-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-166">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="886b5-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-167">79</span><span class="sxs-lookup"><span data-stu-id="886b5-167">79</span></span>

<span data-ttu-id="886b5-168">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="886b5-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-169">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="886b5-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-170">80</span><span class="sxs-lookup"><span data-stu-id="886b5-170">80</span></span>

<span data-ttu-id="886b5-171">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="886b5-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-172">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="886b5-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-173">81</span><span class="sxs-lookup"><span data-stu-id="886b5-173">81</span></span>

<span data-ttu-id="886b5-174">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="886b5-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-175">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="886b5-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-176">82</span><span class="sxs-lookup"><span data-stu-id="886b5-176">82</span></span>

<span data-ttu-id="886b5-177">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="886b5-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-178">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="886b5-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-179">83</span><span class="sxs-lookup"><span data-stu-id="886b5-179">83</span></span>

<span data-ttu-id="886b5-180">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="886b5-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-181">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="886b5-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-182">84</span><span class="sxs-lookup"><span data-stu-id="886b5-182">84</span></span>

<span data-ttu-id="886b5-183">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="886b5-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-184">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="886b5-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-185">85</span><span class="sxs-lookup"><span data-stu-id="886b5-185">85</span></span>

<span data-ttu-id="886b5-186">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="886b5-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-187">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="886b5-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-188">86</span><span class="sxs-lookup"><span data-stu-id="886b5-188">86</span></span>

<span data-ttu-id="886b5-189">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="886b5-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-190">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="886b5-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-191">87</span><span class="sxs-lookup"><span data-stu-id="886b5-191">87</span></span>

<span data-ttu-id="886b5-192">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="886b5-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-193">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="886b5-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-194">88</span><span class="sxs-lookup"><span data-stu-id="886b5-194">88</span></span>

<span data-ttu-id="886b5-195">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="886b5-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-196">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="886b5-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-197">89</span><span class="sxs-lookup"><span data-stu-id="886b5-197">89</span></span>

<span data-ttu-id="886b5-198">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="886b5-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-199">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="886b5-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-200">90</span><span class="sxs-lookup"><span data-stu-id="886b5-200">90</span></span>

<span data-ttu-id="886b5-201">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="886b5-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-202">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="886b5-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-203">91</span><span class="sxs-lookup"><span data-stu-id="886b5-203">91</span></span>

<span data-ttu-id="886b5-204">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="886b5-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-205">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="886b5-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-206">92</span><span class="sxs-lookup"><span data-stu-id="886b5-206">92</span></span>

<span data-ttu-id="886b5-207">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="886b5-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-208">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="886b5-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-209">93</span><span class="sxs-lookup"><span data-stu-id="886b5-209">93</span></span>

<span data-ttu-id="886b5-210">Já existe.</span><span class="sxs-lookup"><span data-stu-id="886b5-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-211">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="886b5-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-212">94</span><span class="sxs-lookup"><span data-stu-id="886b5-212">94</span></span>

<span data-ttu-id="886b5-213">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="886b5-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-214">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="886b5-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-215">95</span><span class="sxs-lookup"><span data-stu-id="886b5-215">95</span></span>

<span data-ttu-id="886b5-216">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="886b5-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-217">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="886b5-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-218">96</span><span class="sxs-lookup"><span data-stu-id="886b5-218">96</span></span>

<span data-ttu-id="886b5-219">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="886b5-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-220">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="886b5-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-221">97</span><span class="sxs-lookup"><span data-stu-id="886b5-221">97</span></span>

<span data-ttu-id="886b5-222">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="886b5-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-223">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="886b5-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-224">98</span><span class="sxs-lookup"><span data-stu-id="886b5-224">98</span></span>

<span data-ttu-id="886b5-225">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="886b5-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-226">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="886b5-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-227">100</span><span class="sxs-lookup"><span data-stu-id="886b5-227">100</span></span>

<span data-ttu-id="886b5-228">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="886b5-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="886b5-229">**Outras**</span><span class="sxs-lookup"><span data-stu-id="886b5-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="886b5-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="886b5-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="886b5-231">Comentários</span><span class="sxs-lookup"><span data-stu-id="886b5-231">Remarks</span></span>

<span data-ttu-id="886b5-232">Se o sistema remoto ainda estiver acessível e funcionando, ele irá reconhecer a transmissão Keep Alive.</span><span class="sxs-lookup"><span data-stu-id="886b5-232">If the remote system is still reachable and functioning, it will acknowledge the Keep Alive transmission.</span></span> <span data-ttu-id="886b5-233">Os pacotes Keep Alive não são enviados por padrão.</span><span class="sxs-lookup"><span data-stu-id="886b5-233">Keep Alive packets are not sent by default.</span></span> <span data-ttu-id="886b5-234">Esse recurso pode ser habilitado em uma conexão por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="886b5-234">This feature may be enabled in a connection by an application.</span></span>

## <a name="examples"></a><span data-ttu-id="886b5-235">Exemplos</span><span class="sxs-lookup"><span data-stu-id="886b5-235">Examples</span></span>

<span data-ttu-id="886b5-236">O exemplo de [Modificar o tempo de Keep Alive para todos os adaptadores de rede](https://Gallery.TechNet.Microsoft.Com/35c1b0ac-285d-4baa-be6e-d3fb0b461676) do VBScript configura o tempo de Keep Alive para todos os adaptadores de rede em um computador a 300.000 milissegundos (5 minutos).</span><span class="sxs-lookup"><span data-stu-id="886b5-236">The [Modify Keep Alive Time for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/35c1b0ac-285d-4baa-be6e-d3fb0b461676) VBScript sample configures the keep alive time for all network adapters on a computer to 300,000 milliseconds (5 minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="886b5-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="886b5-237">Requirements</span></span>



| <span data-ttu-id="886b5-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="886b5-238">Requirement</span></span> | <span data-ttu-id="886b5-239">Valor</span><span class="sxs-lookup"><span data-stu-id="886b5-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="886b5-240">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="886b5-240">Minimum supported client</span></span><br/> | <span data-ttu-id="886b5-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="886b5-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="886b5-242">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="886b5-242">Minimum supported server</span></span><br/> | <span data-ttu-id="886b5-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="886b5-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="886b5-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="886b5-244">Namespace</span></span><br/>                | <span data-ttu-id="886b5-245">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="886b5-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="886b5-246">MOF</span><span class="sxs-lookup"><span data-stu-id="886b5-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="886b5-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="886b5-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="886b5-248">DLL</span><span class="sxs-lookup"><span data-stu-id="886b5-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="886b5-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="886b5-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="886b5-250">Confira também</span><span class="sxs-lookup"><span data-stu-id="886b5-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="886b5-251">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="886b5-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="886b5-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="886b5-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="886b5-253">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="886b5-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="886b5-254">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="886b5-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="886b5-255">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="886b5-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

