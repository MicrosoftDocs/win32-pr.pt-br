---
description: O método estático da classe WMI SetTcpWindowSize é usado para definir o tamanho máximo da janela de recepção TCP oferecido pelo sistema.
ms.assetid: c108fd9c-6de4-4f3e-9691-b0b5c1a3dc5f
ms.tgt_platform: multiple
title: Método SetTcpWindowSize da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpWindowSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d4a77acdc81c06d1f78da8bbc0160bd0d21bcfd8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089223"
---
# <a name="settcpwindowsize-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="441a0-103">Método SetTcpWindowSize da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="441a0-103">SetTcpWindowSize method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="441a0-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpWindowSize** é usado para definir o tamanho máximo da janela de recepção TCP oferecido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="441a0-104">The **SetTcpWindowSize** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum TCP Receive Window size offered by the system.</span></span>

<span data-ttu-id="441a0-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="441a0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="441a0-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="441a0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="441a0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="441a0-107">Syntax</span></span>


```mof
uint32 SetTcpWindowSize(
  [in] uint16 TcpWindowSize
);
```



## <a name="parameters"></a><span data-ttu-id="441a0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="441a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="441a0-109">*TcpWindowSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="441a0-109">*TcpWindowSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441a0-110">Tamanho máximo da janela de recepção TCP oferecido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="441a0-110">Maximum TCP receive window size offered by the system.</span></span> <span data-ttu-id="441a0-111">O intervalo válido de valores em bytes é 0-65535.</span><span class="sxs-lookup"><span data-stu-id="441a0-111">The valid range of values in bytes is 0 - 65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="441a0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="441a0-112">Return value</span></span>

<span data-ttu-id="441a0-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="441a0-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="441a0-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="441a0-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="441a0-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="441a0-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="441a0-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="441a0-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-117">0</span><span class="sxs-lookup"><span data-stu-id="441a0-117">0</span></span>

<span data-ttu-id="441a0-118">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="441a0-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-119">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="441a0-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-120">1</span><span class="sxs-lookup"><span data-stu-id="441a0-120">1</span></span>

<span data-ttu-id="441a0-121">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="441a0-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-122">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="441a0-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-123">64</span><span class="sxs-lookup"><span data-stu-id="441a0-123">64</span></span>

<span data-ttu-id="441a0-124">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="441a0-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-125">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="441a0-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-126">65</span><span class="sxs-lookup"><span data-stu-id="441a0-126">65</span></span>

<span data-ttu-id="441a0-127">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="441a0-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-128">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="441a0-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-129">66</span><span class="sxs-lookup"><span data-stu-id="441a0-129">66</span></span>

<span data-ttu-id="441a0-130">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="441a0-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-131">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="441a0-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-132">67</span><span class="sxs-lookup"><span data-stu-id="441a0-132">67</span></span>

<span data-ttu-id="441a0-133">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="441a0-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-134">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="441a0-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-135">68</span><span class="sxs-lookup"><span data-stu-id="441a0-135">68</span></span>

<span data-ttu-id="441a0-136">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="441a0-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-137">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="441a0-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-138">69</span><span class="sxs-lookup"><span data-stu-id="441a0-138">69</span></span>

<span data-ttu-id="441a0-139">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="441a0-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-140">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="441a0-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-141">70</span><span class="sxs-lookup"><span data-stu-id="441a0-141">70</span></span>

<span data-ttu-id="441a0-142">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="441a0-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-143">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="441a0-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-144">71</span><span class="sxs-lookup"><span data-stu-id="441a0-144">71</span></span>

<span data-ttu-id="441a0-145">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="441a0-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-146">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="441a0-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-147">72</span><span class="sxs-lookup"><span data-stu-id="441a0-147">72</span></span>

<span data-ttu-id="441a0-148">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="441a0-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-149">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="441a0-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-150">73</span><span class="sxs-lookup"><span data-stu-id="441a0-150">73</span></span>

<span data-ttu-id="441a0-151">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="441a0-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-152">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="441a0-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-153">74</span><span class="sxs-lookup"><span data-stu-id="441a0-153">74</span></span>

<span data-ttu-id="441a0-154">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="441a0-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-155">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="441a0-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-156">75</span><span class="sxs-lookup"><span data-stu-id="441a0-156">75</span></span>

<span data-ttu-id="441a0-157">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="441a0-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-158">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="441a0-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-159">76</span><span class="sxs-lookup"><span data-stu-id="441a0-159">76</span></span>

<span data-ttu-id="441a0-160">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="441a0-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-161">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="441a0-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-162">77</span><span class="sxs-lookup"><span data-stu-id="441a0-162">77</span></span>

<span data-ttu-id="441a0-163">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="441a0-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-164">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="441a0-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-165">78</span><span class="sxs-lookup"><span data-stu-id="441a0-165">78</span></span>

<span data-ttu-id="441a0-166">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="441a0-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-167">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="441a0-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-168">79</span><span class="sxs-lookup"><span data-stu-id="441a0-168">79</span></span>

<span data-ttu-id="441a0-169">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="441a0-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-170">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="441a0-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-171">80</span><span class="sxs-lookup"><span data-stu-id="441a0-171">80</span></span>

<span data-ttu-id="441a0-172">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="441a0-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-173">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="441a0-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-174">81</span><span class="sxs-lookup"><span data-stu-id="441a0-174">81</span></span>

<span data-ttu-id="441a0-175">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="441a0-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-176">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="441a0-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-177">82</span><span class="sxs-lookup"><span data-stu-id="441a0-177">82</span></span>

<span data-ttu-id="441a0-178">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="441a0-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-179">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="441a0-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-180">83</span><span class="sxs-lookup"><span data-stu-id="441a0-180">83</span></span>

<span data-ttu-id="441a0-181">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="441a0-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-182">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="441a0-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-183">84</span><span class="sxs-lookup"><span data-stu-id="441a0-183">84</span></span>

<span data-ttu-id="441a0-184">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="441a0-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-185">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="441a0-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-186">85</span><span class="sxs-lookup"><span data-stu-id="441a0-186">85</span></span>

<span data-ttu-id="441a0-187">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="441a0-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-188">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="441a0-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-189">86</span><span class="sxs-lookup"><span data-stu-id="441a0-189">86</span></span>

<span data-ttu-id="441a0-190">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="441a0-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-191">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="441a0-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-192">87</span><span class="sxs-lookup"><span data-stu-id="441a0-192">87</span></span>

<span data-ttu-id="441a0-193">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="441a0-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-194">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="441a0-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-195">88</span><span class="sxs-lookup"><span data-stu-id="441a0-195">88</span></span>

<span data-ttu-id="441a0-196">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="441a0-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-197">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="441a0-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-198">89</span><span class="sxs-lookup"><span data-stu-id="441a0-198">89</span></span>

<span data-ttu-id="441a0-199">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="441a0-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-200">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="441a0-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-201">90</span><span class="sxs-lookup"><span data-stu-id="441a0-201">90</span></span>

<span data-ttu-id="441a0-202">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="441a0-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-203">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="441a0-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-204">91</span><span class="sxs-lookup"><span data-stu-id="441a0-204">91</span></span>

<span data-ttu-id="441a0-205">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="441a0-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-206">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="441a0-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-207">92</span><span class="sxs-lookup"><span data-stu-id="441a0-207">92</span></span>

<span data-ttu-id="441a0-208">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="441a0-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-209">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="441a0-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-210">93</span><span class="sxs-lookup"><span data-stu-id="441a0-210">93</span></span>

<span data-ttu-id="441a0-211">Já existe.</span><span class="sxs-lookup"><span data-stu-id="441a0-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-212">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="441a0-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-213">94</span><span class="sxs-lookup"><span data-stu-id="441a0-213">94</span></span>

<span data-ttu-id="441a0-214">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="441a0-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-215">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="441a0-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-216">95</span><span class="sxs-lookup"><span data-stu-id="441a0-216">95</span></span>

<span data-ttu-id="441a0-217">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="441a0-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-218">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="441a0-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-219">96</span><span class="sxs-lookup"><span data-stu-id="441a0-219">96</span></span>

<span data-ttu-id="441a0-220">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="441a0-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-221">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="441a0-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-222">97</span><span class="sxs-lookup"><span data-stu-id="441a0-222">97</span></span>

<span data-ttu-id="441a0-223">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="441a0-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-224">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="441a0-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-225">98</span><span class="sxs-lookup"><span data-stu-id="441a0-225">98</span></span>

<span data-ttu-id="441a0-226">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="441a0-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-227">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="441a0-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-228">100</span><span class="sxs-lookup"><span data-stu-id="441a0-228">100</span></span>

<span data-ttu-id="441a0-229">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="441a0-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="441a0-230">**Outras**</span><span class="sxs-lookup"><span data-stu-id="441a0-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="441a0-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="441a0-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="441a0-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="441a0-232">Remarks</span></span>

<span data-ttu-id="441a0-233">A janela de recepção especifica o número de bytes que um remetente pode transmitir sem receber uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="441a0-233">The receive window specifies the number of bytes a sender can transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="441a0-234">Em geral, as janelas de recebimento maiores melhoram o desempenho em redes de alto atraso e alta largura de banda.</span><span class="sxs-lookup"><span data-stu-id="441a0-234">In general, larger receive windows improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="441a0-235">Para a eficiência, a janela de recebimento deve ser um múltiplo par do MSS (tamanho máximo de segmento) do TCP.</span><span class="sxs-lookup"><span data-stu-id="441a0-235">For efficiency, the receive window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span>

> [!Note]  
> <span data-ttu-id="441a0-236">Windows Vista: esse método acessa a `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` entrada do registro, que não é usada na implementação atual do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="441a0-236">Windows Vista: This method accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

## <a name="examples"></a><span data-ttu-id="441a0-237">Exemplos</span><span class="sxs-lookup"><span data-stu-id="441a0-237">Examples</span></span>

<span data-ttu-id="441a0-238">O exemplo de [Modificar o tamanho da janela TCP para todos os adaptadores de rede](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) do VBScript define o tamanho da janela TCP para todos os adaptadores de rede em um computador.</span><span class="sxs-lookup"><span data-stu-id="441a0-238">The [Modify the TCP Window Size for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) VBScript sample sets the TCP window size for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="441a0-239">Requisitos</span><span class="sxs-lookup"><span data-stu-id="441a0-239">Requirements</span></span>



| <span data-ttu-id="441a0-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="441a0-240">Requirement</span></span> | <span data-ttu-id="441a0-241">Valor</span><span class="sxs-lookup"><span data-stu-id="441a0-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="441a0-242">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="441a0-242">Minimum supported client</span></span><br/> | <span data-ttu-id="441a0-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="441a0-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="441a0-244">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="441a0-244">Minimum supported server</span></span><br/> | <span data-ttu-id="441a0-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="441a0-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="441a0-246">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="441a0-246">End of client support</span></span><br/>    | <span data-ttu-id="441a0-247">Windows 7</span><span class="sxs-lookup"><span data-stu-id="441a0-247">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="441a0-248">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="441a0-248">End of server support</span></span><br/>    | <span data-ttu-id="441a0-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="441a0-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="441a0-250">Namespace</span><span class="sxs-lookup"><span data-stu-id="441a0-250">Namespace</span></span><br/>                | <span data-ttu-id="441a0-251">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="441a0-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="441a0-252">MOF</span><span class="sxs-lookup"><span data-stu-id="441a0-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="441a0-253"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="441a0-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="441a0-254">DLL</span><span class="sxs-lookup"><span data-stu-id="441a0-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="441a0-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="441a0-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="441a0-256">Confira também</span><span class="sxs-lookup"><span data-stu-id="441a0-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="441a0-257">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="441a0-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="441a0-258">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="441a0-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="441a0-259">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="441a0-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="441a0-260">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="441a0-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="441a0-261">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="441a0-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

