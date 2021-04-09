---
description: O método estático da classe WMI SetTcpUseRFC1122UrgentPointer é usado para especificar se o TCP usa a especificação RFC 1122 para dados urgentes ou o modo usado pelos sistemas derivados do BSD (Berkeley Software Design).
ms.assetid: f8d07690-2723-4bc3-b15f-a24d575456a7
ms.tgt_platform: multiple
title: Método SetTcpUseRFC1122UrgentPointer da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpUseRFC1122UrgentPointer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 928a809211288eb7f024c735ce033b819e5d49f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089224"
---
# <a name="settcpuserfc1122urgentpointer-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="2abee-103">Método SetTcpUseRFC1122UrgentPointer da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="2abee-103">SetTcpUseRFC1122UrgentPointer method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="2abee-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpUseRFC1122UrgentPointer** é usado para especificar se o TCP usa a especificação RFC 1122 para dados urgentes ou o modo usado pelos sistemas derivados do BSD (Berkeley Software Design).</span><span class="sxs-lookup"><span data-stu-id="2abee-104">The **SetTcpUseRFC1122UrgentPointer** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to specify whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span>

<span data-ttu-id="2abee-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2abee-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2abee-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2abee-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2abee-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2abee-107">Syntax</span></span>


```mof
uint32 SetTcpUseRFC1122UrgentPointer(
  [in] boolean TcpUseRFC1122UrgentPointer
);
```



## <a name="parameters"></a><span data-ttu-id="2abee-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2abee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2abee-109">*TcpUseRFC1122UrgentPointer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2abee-109">*TcpUseRFC1122UrgentPointer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2abee-110">Se **for true**, o TCP usará a especificação RFC 1122.</span><span class="sxs-lookup"><span data-stu-id="2abee-110">If **true**, TCP uses the RFC 1122 specification.</span></span> <span data-ttu-id="2abee-111">Se for **falso**, os dados urgentes serão enviados no modo usado por sistemas derivados do BSD.</span><span class="sxs-lookup"><span data-stu-id="2abee-111">If **false**, urgent data is sent in the mode used by BSD-derived systems.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2abee-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2abee-112">Return value</span></span>

<span data-ttu-id="2abee-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="2abee-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="2abee-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2abee-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2abee-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2abee-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2abee-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="2abee-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-117">0</span><span class="sxs-lookup"><span data-stu-id="2abee-117">0</span></span>

<span data-ttu-id="2abee-118">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="2abee-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-119">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="2abee-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-120">1</span><span class="sxs-lookup"><span data-stu-id="2abee-120">1</span></span>

<span data-ttu-id="2abee-121">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="2abee-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-122">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="2abee-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-123">64</span><span class="sxs-lookup"><span data-stu-id="2abee-123">64</span></span>

<span data-ttu-id="2abee-124">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="2abee-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-125">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="2abee-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-126">65</span><span class="sxs-lookup"><span data-stu-id="2abee-126">65</span></span>

<span data-ttu-id="2abee-127">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="2abee-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-128">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="2abee-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-129">66</span><span class="sxs-lookup"><span data-stu-id="2abee-129">66</span></span>

<span data-ttu-id="2abee-130">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="2abee-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-131">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="2abee-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-132">67</span><span class="sxs-lookup"><span data-stu-id="2abee-132">67</span></span>

<span data-ttu-id="2abee-133">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="2abee-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-134">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="2abee-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-135">68</span><span class="sxs-lookup"><span data-stu-id="2abee-135">68</span></span>

<span data-ttu-id="2abee-136">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="2abee-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-137">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="2abee-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-138">69</span><span class="sxs-lookup"><span data-stu-id="2abee-138">69</span></span>

<span data-ttu-id="2abee-139">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="2abee-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-140">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="2abee-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-141">70</span><span class="sxs-lookup"><span data-stu-id="2abee-141">70</span></span>

<span data-ttu-id="2abee-142">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="2abee-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-143">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="2abee-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-144">71</span><span class="sxs-lookup"><span data-stu-id="2abee-144">71</span></span>

<span data-ttu-id="2abee-145">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="2abee-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-146">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="2abee-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-147">72</span><span class="sxs-lookup"><span data-stu-id="2abee-147">72</span></span>

<span data-ttu-id="2abee-148">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="2abee-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-149">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="2abee-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-150">73</span><span class="sxs-lookup"><span data-stu-id="2abee-150">73</span></span>

<span data-ttu-id="2abee-151">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="2abee-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-152">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="2abee-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-153">74</span><span class="sxs-lookup"><span data-stu-id="2abee-153">74</span></span>

<span data-ttu-id="2abee-154">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="2abee-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-155">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="2abee-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-156">75</span><span class="sxs-lookup"><span data-stu-id="2abee-156">75</span></span>

<span data-ttu-id="2abee-157">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="2abee-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-158">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="2abee-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-159">76</span><span class="sxs-lookup"><span data-stu-id="2abee-159">76</span></span>

<span data-ttu-id="2abee-160">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="2abee-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-161">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="2abee-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-162">77</span><span class="sxs-lookup"><span data-stu-id="2abee-162">77</span></span>

<span data-ttu-id="2abee-163">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="2abee-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-164">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="2abee-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-165">78</span><span class="sxs-lookup"><span data-stu-id="2abee-165">78</span></span>

<span data-ttu-id="2abee-166">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2abee-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-167">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="2abee-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-168">79</span><span class="sxs-lookup"><span data-stu-id="2abee-168">79</span></span>

<span data-ttu-id="2abee-169">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="2abee-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-170">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="2abee-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-171">80</span><span class="sxs-lookup"><span data-stu-id="2abee-171">80</span></span>

<span data-ttu-id="2abee-172">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2abee-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-173">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="2abee-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-174">81</span><span class="sxs-lookup"><span data-stu-id="2abee-174">81</span></span>

<span data-ttu-id="2abee-175">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="2abee-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-176">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="2abee-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-177">82</span><span class="sxs-lookup"><span data-stu-id="2abee-177">82</span></span>

<span data-ttu-id="2abee-178">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="2abee-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-179">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="2abee-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-180">83</span><span class="sxs-lookup"><span data-stu-id="2abee-180">83</span></span>

<span data-ttu-id="2abee-181">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="2abee-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-182">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="2abee-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-183">84</span><span class="sxs-lookup"><span data-stu-id="2abee-183">84</span></span>

<span data-ttu-id="2abee-184">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="2abee-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-185">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="2abee-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-186">85</span><span class="sxs-lookup"><span data-stu-id="2abee-186">85</span></span>

<span data-ttu-id="2abee-187">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="2abee-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-188">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="2abee-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-189">86</span><span class="sxs-lookup"><span data-stu-id="2abee-189">86</span></span>

<span data-ttu-id="2abee-190">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="2abee-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-191">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="2abee-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-192">87</span><span class="sxs-lookup"><span data-stu-id="2abee-192">87</span></span>

<span data-ttu-id="2abee-193">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="2abee-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-194">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="2abee-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-195">88</span><span class="sxs-lookup"><span data-stu-id="2abee-195">88</span></span>

<span data-ttu-id="2abee-196">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="2abee-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-197">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="2abee-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-198">89</span><span class="sxs-lookup"><span data-stu-id="2abee-198">89</span></span>

<span data-ttu-id="2abee-199">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="2abee-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-200">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="2abee-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-201">90</span><span class="sxs-lookup"><span data-stu-id="2abee-201">90</span></span>

<span data-ttu-id="2abee-202">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="2abee-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-203">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="2abee-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-204">91</span><span class="sxs-lookup"><span data-stu-id="2abee-204">91</span></span>

<span data-ttu-id="2abee-205">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="2abee-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-206">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="2abee-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-207">92</span><span class="sxs-lookup"><span data-stu-id="2abee-207">92</span></span>

<span data-ttu-id="2abee-208">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="2abee-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-209">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="2abee-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-210">93</span><span class="sxs-lookup"><span data-stu-id="2abee-210">93</span></span>

<span data-ttu-id="2abee-211">Já existe.</span><span class="sxs-lookup"><span data-stu-id="2abee-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-212">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="2abee-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-213">94</span><span class="sxs-lookup"><span data-stu-id="2abee-213">94</span></span>

<span data-ttu-id="2abee-214">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="2abee-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-215">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="2abee-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-216">95</span><span class="sxs-lookup"><span data-stu-id="2abee-216">95</span></span>

<span data-ttu-id="2abee-217">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="2abee-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-218">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="2abee-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-219">96</span><span class="sxs-lookup"><span data-stu-id="2abee-219">96</span></span>

<span data-ttu-id="2abee-220">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="2abee-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-221">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="2abee-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-222">97</span><span class="sxs-lookup"><span data-stu-id="2abee-222">97</span></span>

<span data-ttu-id="2abee-223">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="2abee-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-224">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="2abee-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-225">98</span><span class="sxs-lookup"><span data-stu-id="2abee-225">98</span></span>

<span data-ttu-id="2abee-226">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="2abee-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-227">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="2abee-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-228">100</span><span class="sxs-lookup"><span data-stu-id="2abee-228">100</span></span>

<span data-ttu-id="2abee-229">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="2abee-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2abee-230">**Outras**</span><span class="sxs-lookup"><span data-stu-id="2abee-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="2abee-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="2abee-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2abee-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="2abee-232">Remarks</span></span>

<span data-ttu-id="2abee-233">O RFC 1122 e o BSD interpretam o ponteiro urgente no cabeçalho TCP e o comprimento dos dados urgentes de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="2abee-233">RFC 1122 and BSD interpret the urgent pointer in the TCP header and the length of the urgent data differently.</span></span> <span data-ttu-id="2abee-234">Eles não são interoperáveis.</span><span class="sxs-lookup"><span data-stu-id="2abee-234">They are not interoperable.</span></span> <span data-ttu-id="2abee-235">O padrão é o modo BSD.</span><span class="sxs-lookup"><span data-stu-id="2abee-235">The default is BSD mode.</span></span>

## <a name="examples"></a><span data-ttu-id="2abee-236">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2abee-236">Examples</span></span>

<span data-ttu-id="2abee-237">O exemplo [Modificar ponteiro urgente usar para todos os adaptadores de rede](https://Gallery.TechNet.Microsoft.Com/0ff22a90-0be6-4914-8db7-aaf72cbea9cb) configura um computador para usar a especificação RFC 1122 para dados urgentes.</span><span class="sxs-lookup"><span data-stu-id="2abee-237">The [Modify Urgent Pointer Use for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/0ff22a90-0be6-4914-8db7-aaf72cbea9cb) VBScript sample configures a computer to use the RFC 1122 specification for urgent data.</span></span>

## <a name="requirements"></a><span data-ttu-id="2abee-238">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2abee-238">Requirements</span></span>



| <span data-ttu-id="2abee-239">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abee-239">Requirement</span></span> | <span data-ttu-id="2abee-240">Valor</span><span class="sxs-lookup"><span data-stu-id="2abee-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2abee-241">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2abee-241">Minimum supported client</span></span><br/> | <span data-ttu-id="2abee-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2abee-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2abee-243">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2abee-243">Minimum supported server</span></span><br/> | <span data-ttu-id="2abee-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2abee-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2abee-245">Namespace</span><span class="sxs-lookup"><span data-stu-id="2abee-245">Namespace</span></span><br/>                | <span data-ttu-id="2abee-246">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2abee-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2abee-247">MOF</span><span class="sxs-lookup"><span data-stu-id="2abee-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2abee-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2abee-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2abee-249">DLL</span><span class="sxs-lookup"><span data-stu-id="2abee-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2abee-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2abee-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2abee-251">Confira também</span><span class="sxs-lookup"><span data-stu-id="2abee-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2abee-252">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="2abee-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2abee-253">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="2abee-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="2abee-254">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="2abee-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="2abee-255">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="2abee-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="2abee-256">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="2abee-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

