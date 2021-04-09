---
description: O método estático da classe WMI SetTcpMaxConnectRetransmissions é usado para definir o número de tentativas que o TCP retransmitirá uma solicitação de conexão antes de abortar.
ms.assetid: cb0dfba3-4ef5-4052-94f3-f688a1c55d90
ms.tgt_platform: multiple
title: Método SetTcpMaxConnectRetransmissions da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxConnectRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 160d84c2a466bff34070a6dec4a34804d5a3a7fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089662"
---
# <a name="settcpmaxconnectretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d2ead-103">Método SetTcpMaxConnectRetransmissions da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2ead-103">SetTcpMaxConnectRetransmissions method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d2ead-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpMaxConnectRetransmissions** é usado para definir o número de tentativas que o TCP retransmitirá uma solicitação de conexão antes de abortar.</span><span class="sxs-lookup"><span data-stu-id="d2ead-104">The **SetTcpMaxConnectRetransmissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of attempts TCP will retransmit a connect request before aborting.</span></span>

<span data-ttu-id="d2ead-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d2ead-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d2ead-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d2ead-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ead-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2ead-107">Syntax</span></span>


```mof
uint32 SetTcpMaxConnectRetransmissions(
  [in] uint32 TcpMaxConnectRetransmissions
);
```



## <a name="parameters"></a><span data-ttu-id="d2ead-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2ead-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ead-109">*TcpMaxConnectRetransmissions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2ead-109">*TcpMaxConnectRetransmissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-110">Número de tentativas que o TCP retransmitirá uma solicitação de conexão antes de abortar.</span><span class="sxs-lookup"><span data-stu-id="d2ead-110">Number of attempts TCP will retransmit a connect request before aborting.</span></span> <span data-ttu-id="d2ead-111">O intervalo válido para os valores é 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="d2ead-111">The valid range for values is 0 - 0xFFFFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2ead-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2ead-112">Return value</span></span>

<span data-ttu-id="d2ead-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="d2ead-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="d2ead-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d2ead-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d2ead-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d2ead-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d2ead-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="d2ead-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-117">0</span><span class="sxs-lookup"><span data-stu-id="d2ead-117">0</span></span>

<span data-ttu-id="d2ead-118">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="d2ead-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-119">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="d2ead-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-120">1</span><span class="sxs-lookup"><span data-stu-id="d2ead-120">1</span></span>

<span data-ttu-id="d2ead-121">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="d2ead-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-122">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="d2ead-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-123">64</span><span class="sxs-lookup"><span data-stu-id="d2ead-123">64</span></span>

<span data-ttu-id="d2ead-124">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="d2ead-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-125">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="d2ead-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-126">65</span><span class="sxs-lookup"><span data-stu-id="d2ead-126">65</span></span>

<span data-ttu-id="d2ead-127">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="d2ead-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-128">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="d2ead-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-129">66</span><span class="sxs-lookup"><span data-stu-id="d2ead-129">66</span></span>

<span data-ttu-id="d2ead-130">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="d2ead-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-131">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="d2ead-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-132">67</span><span class="sxs-lookup"><span data-stu-id="d2ead-132">67</span></span>

<span data-ttu-id="d2ead-133">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="d2ead-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-134">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="d2ead-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-135">68</span><span class="sxs-lookup"><span data-stu-id="d2ead-135">68</span></span>

<span data-ttu-id="d2ead-136">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="d2ead-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-137">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="d2ead-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-138">69</span><span class="sxs-lookup"><span data-stu-id="d2ead-138">69</span></span>

<span data-ttu-id="d2ead-139">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="d2ead-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-140">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="d2ead-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-141">70</span><span class="sxs-lookup"><span data-stu-id="d2ead-141">70</span></span>

<span data-ttu-id="d2ead-142">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="d2ead-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-143">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="d2ead-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-144">71</span><span class="sxs-lookup"><span data-stu-id="d2ead-144">71</span></span>

<span data-ttu-id="d2ead-145">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="d2ead-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-146">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="d2ead-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-147">72</span><span class="sxs-lookup"><span data-stu-id="d2ead-147">72</span></span>

<span data-ttu-id="d2ead-148">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="d2ead-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-149">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="d2ead-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-150">73</span><span class="sxs-lookup"><span data-stu-id="d2ead-150">73</span></span>

<span data-ttu-id="d2ead-151">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="d2ead-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-152">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="d2ead-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-153">74</span><span class="sxs-lookup"><span data-stu-id="d2ead-153">74</span></span>

<span data-ttu-id="d2ead-154">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="d2ead-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-155">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="d2ead-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-156">75</span><span class="sxs-lookup"><span data-stu-id="d2ead-156">75</span></span>

<span data-ttu-id="d2ead-157">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="d2ead-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-158">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="d2ead-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-159">76</span><span class="sxs-lookup"><span data-stu-id="d2ead-159">76</span></span>

<span data-ttu-id="d2ead-160">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="d2ead-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-161">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="d2ead-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-162">77</span><span class="sxs-lookup"><span data-stu-id="d2ead-162">77</span></span>

<span data-ttu-id="d2ead-163">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="d2ead-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-164">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="d2ead-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-165">78</span><span class="sxs-lookup"><span data-stu-id="d2ead-165">78</span></span>

<span data-ttu-id="d2ead-166">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d2ead-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-167">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="d2ead-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-168">79</span><span class="sxs-lookup"><span data-stu-id="d2ead-168">79</span></span>

<span data-ttu-id="d2ead-169">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="d2ead-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-170">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="d2ead-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-171">80</span><span class="sxs-lookup"><span data-stu-id="d2ead-171">80</span></span>

<span data-ttu-id="d2ead-172">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d2ead-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-173">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="d2ead-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-174">81</span><span class="sxs-lookup"><span data-stu-id="d2ead-174">81</span></span>

<span data-ttu-id="d2ead-175">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="d2ead-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-176">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="d2ead-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-177">82</span><span class="sxs-lookup"><span data-stu-id="d2ead-177">82</span></span>

<span data-ttu-id="d2ead-178">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="d2ead-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-179">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="d2ead-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-180">83</span><span class="sxs-lookup"><span data-stu-id="d2ead-180">83</span></span>

<span data-ttu-id="d2ead-181">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="d2ead-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-182">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="d2ead-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-183">84</span><span class="sxs-lookup"><span data-stu-id="d2ead-183">84</span></span>

<span data-ttu-id="d2ead-184">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="d2ead-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-185">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="d2ead-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-186">85</span><span class="sxs-lookup"><span data-stu-id="d2ead-186">85</span></span>

<span data-ttu-id="d2ead-187">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="d2ead-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-188">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="d2ead-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-189">86</span><span class="sxs-lookup"><span data-stu-id="d2ead-189">86</span></span>

<span data-ttu-id="d2ead-190">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="d2ead-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-191">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="d2ead-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-192">87</span><span class="sxs-lookup"><span data-stu-id="d2ead-192">87</span></span>

<span data-ttu-id="d2ead-193">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="d2ead-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-194">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="d2ead-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-195">88</span><span class="sxs-lookup"><span data-stu-id="d2ead-195">88</span></span>

<span data-ttu-id="d2ead-196">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="d2ead-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-197">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="d2ead-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-198">89</span><span class="sxs-lookup"><span data-stu-id="d2ead-198">89</span></span>

<span data-ttu-id="d2ead-199">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="d2ead-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-200">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="d2ead-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-201">90</span><span class="sxs-lookup"><span data-stu-id="d2ead-201">90</span></span>

<span data-ttu-id="d2ead-202">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="d2ead-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-203">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="d2ead-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-204">91</span><span class="sxs-lookup"><span data-stu-id="d2ead-204">91</span></span>

<span data-ttu-id="d2ead-205">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="d2ead-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-206">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="d2ead-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-207">92</span><span class="sxs-lookup"><span data-stu-id="d2ead-207">92</span></span>

<span data-ttu-id="d2ead-208">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="d2ead-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-209">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="d2ead-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-210">93</span><span class="sxs-lookup"><span data-stu-id="d2ead-210">93</span></span>

<span data-ttu-id="d2ead-211">Já existe.</span><span class="sxs-lookup"><span data-stu-id="d2ead-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-212">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="d2ead-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-213">94</span><span class="sxs-lookup"><span data-stu-id="d2ead-213">94</span></span>

<span data-ttu-id="d2ead-214">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="d2ead-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-215">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="d2ead-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-216">95</span><span class="sxs-lookup"><span data-stu-id="d2ead-216">95</span></span>

<span data-ttu-id="d2ead-217">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="d2ead-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-218">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="d2ead-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-219">96</span><span class="sxs-lookup"><span data-stu-id="d2ead-219">96</span></span>

<span data-ttu-id="d2ead-220">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="d2ead-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-221">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="d2ead-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-222">97</span><span class="sxs-lookup"><span data-stu-id="d2ead-222">97</span></span>

<span data-ttu-id="d2ead-223">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="d2ead-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-224">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="d2ead-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-225">98</span><span class="sxs-lookup"><span data-stu-id="d2ead-225">98</span></span>

<span data-ttu-id="d2ead-226">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="d2ead-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-227">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="d2ead-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-228">100</span><span class="sxs-lookup"><span data-stu-id="d2ead-228">100</span></span>

<span data-ttu-id="d2ead-229">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="d2ead-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d2ead-230">**Outras**</span><span class="sxs-lookup"><span data-stu-id="d2ead-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d2ead-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="d2ead-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2ead-232">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2ead-232">Remarks</span></span>

<span data-ttu-id="d2ead-233">O tempo limite de retransmissão inicial é de três segundos e dobra para cada tentativa sucessiva.</span><span class="sxs-lookup"><span data-stu-id="d2ead-233">The initial retransmission timeout is three seconds, and doubles for each successive attempt.</span></span>

## <a name="examples"></a><span data-ttu-id="d2ead-234">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d2ead-234">Examples</span></span>

<span data-ttu-id="d2ead-235">A amostra [Modificar o máximo de retransmissões de conexões TCP permitidas](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) do VBScript configura o número de vezes que o TCP retransmitirá uma tentativa de conexão antes de abandonar o esforço.</span><span class="sxs-lookup"><span data-stu-id="d2ead-235">The [Modify the Maximum Allowed TCP Connection Retransmissions](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) VBScript sample configures the number of times TCP will retransmit a connection attempt before abandoning the effort.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2ead-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2ead-236">Requirements</span></span>



| <span data-ttu-id="d2ead-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2ead-237">Requirement</span></span> | <span data-ttu-id="d2ead-238">Valor</span><span class="sxs-lookup"><span data-stu-id="d2ead-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ead-239">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2ead-239">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ead-240">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2ead-240">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="d2ead-241">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2ead-241">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ead-242">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2ead-242">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="d2ead-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2ead-243">Namespace</span></span><br/>                | <span data-ttu-id="d2ead-244">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d2ead-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d2ead-245">MOF</span><span class="sxs-lookup"><span data-stu-id="d2ead-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2ead-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2ead-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2ead-247">DLL</span><span class="sxs-lookup"><span data-stu-id="d2ead-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2ead-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2ead-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2ead-249">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2ead-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ead-250">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="d2ead-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d2ead-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="d2ead-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="d2ead-252">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="d2ead-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="d2ead-253">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="d2ead-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d2ead-254">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="d2ead-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

