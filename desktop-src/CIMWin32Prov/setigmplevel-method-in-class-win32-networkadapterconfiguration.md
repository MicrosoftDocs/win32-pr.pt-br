---
description: O método estático da classe WMI SetIGMPLevel é usado para definir a extensão à qual o sistema dá suporte a multicast de IP e participa do protocolo de gerenciamento de grupo da Internet.
ms.assetid: 38877576-aa23-4841-b3ae-1a02bfdd70d8
ms.tgt_platform: multiple
title: Método SetIGMPLevel da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIGMPLevel
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 97ead4df1d45b110c3d0a91976dc8eca6ffd72c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500984"
---
# <a name="setigmplevel-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="09d63-103">Método SetIGMPLevel da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="09d63-103">SetIGMPLevel method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="09d63-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetIGMPLevel** é usado para definir a extensão à qual o sistema dá suporte a multicast de IP e participa do protocolo de gerenciamento de grupo da Internet.</span><span class="sxs-lookup"><span data-stu-id="09d63-104">The **SetIGMPLevel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span>

<span data-ttu-id="09d63-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="09d63-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="09d63-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="09d63-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="09d63-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09d63-107">Syntax</span></span>


```mof
uint32 SetIGMPLevel(
  [in] uint8 IGMPLevel
);
```



## <a name="parameters"></a><span data-ttu-id="09d63-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09d63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09d63-109">*IGMPLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09d63-109">*IGMPLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d63-110">Tipo de dados: **inteiro**</span><span class="sxs-lookup"><span data-stu-id="09d63-110">Data type: **Integer**</span></span>

<span data-ttu-id="09d63-111">Define o nível no qual o sistema dá suporte a multicast IP e participa do protocolo de gerenciamento de grupo da Internet.</span><span class="sxs-lookup"><span data-stu-id="09d63-111">Sets the level at which the system supports IP multicast and participates in the Internet Group Management Protocol.</span></span> <span data-ttu-id="09d63-112">No nível 0, o sistema não fornece suporte a multicast.</span><span class="sxs-lookup"><span data-stu-id="09d63-112">At level 0, the system provides no multicast support.</span></span> <span data-ttu-id="09d63-113">No nível 1, o sistema só pode enviar pacotes multicast de IP.</span><span class="sxs-lookup"><span data-stu-id="09d63-113">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="09d63-114">No nível 2, o sistema pode enviar pacotes multicast IP e participar totalmente do IGMP para receber pacotes multicast.</span><span class="sxs-lookup"><span data-stu-id="09d63-114">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="09d63-115">**Sem multicast** (0)</span><span class="sxs-lookup"><span data-stu-id="09d63-115">**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="09d63-116">**Multicast de IP** (1)</span><span class="sxs-lookup"><span data-stu-id="09d63-116">**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="09d63-117">**IP & multicast IGMP** (2)</span><span class="sxs-lookup"><span data-stu-id="09d63-117">**IP & IGMP multicast** (2)</span></span>


<span data-ttu-id="09d63-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="09d63-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="09d63-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09d63-119">Return value</span></span>

<span data-ttu-id="09d63-120">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="09d63-120">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="09d63-121">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="09d63-121">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="09d63-122">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="09d63-122">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="09d63-123">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="09d63-123">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-124">0</span><span class="sxs-lookup"><span data-stu-id="09d63-124">0</span></span>

<span data-ttu-id="09d63-125">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="09d63-125">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-126">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="09d63-126">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-127">1</span><span class="sxs-lookup"><span data-stu-id="09d63-127">1</span></span>

<span data-ttu-id="09d63-128">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="09d63-128">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-129">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="09d63-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-130">64</span><span class="sxs-lookup"><span data-stu-id="09d63-130">64</span></span>

<span data-ttu-id="09d63-131">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="09d63-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-132">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="09d63-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-133">65</span><span class="sxs-lookup"><span data-stu-id="09d63-133">65</span></span>

<span data-ttu-id="09d63-134">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="09d63-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-135">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="09d63-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-136">66</span><span class="sxs-lookup"><span data-stu-id="09d63-136">66</span></span>

<span data-ttu-id="09d63-137">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="09d63-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-138">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="09d63-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-139">67</span><span class="sxs-lookup"><span data-stu-id="09d63-139">67</span></span>

<span data-ttu-id="09d63-140">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="09d63-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-141">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="09d63-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-142">68</span><span class="sxs-lookup"><span data-stu-id="09d63-142">68</span></span>

<span data-ttu-id="09d63-143">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="09d63-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-144">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="09d63-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-145">69</span><span class="sxs-lookup"><span data-stu-id="09d63-145">69</span></span>

<span data-ttu-id="09d63-146">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="09d63-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-147">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="09d63-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-148">70</span><span class="sxs-lookup"><span data-stu-id="09d63-148">70</span></span>

<span data-ttu-id="09d63-149">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="09d63-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-150">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="09d63-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-151">71</span><span class="sxs-lookup"><span data-stu-id="09d63-151">71</span></span>

<span data-ttu-id="09d63-152">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="09d63-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-153">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="09d63-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-154">72</span><span class="sxs-lookup"><span data-stu-id="09d63-154">72</span></span>

<span data-ttu-id="09d63-155">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="09d63-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-156">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="09d63-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-157">73</span><span class="sxs-lookup"><span data-stu-id="09d63-157">73</span></span>

<span data-ttu-id="09d63-158">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="09d63-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-159">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="09d63-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-160">74</span><span class="sxs-lookup"><span data-stu-id="09d63-160">74</span></span>

<span data-ttu-id="09d63-161">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="09d63-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-162">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="09d63-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-163">75</span><span class="sxs-lookup"><span data-stu-id="09d63-163">75</span></span>

<span data-ttu-id="09d63-164">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="09d63-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-165">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="09d63-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-166">76</span><span class="sxs-lookup"><span data-stu-id="09d63-166">76</span></span>

<span data-ttu-id="09d63-167">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="09d63-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-168">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="09d63-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-169">77</span><span class="sxs-lookup"><span data-stu-id="09d63-169">77</span></span>

<span data-ttu-id="09d63-170">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="09d63-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-171">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="09d63-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-172">78</span><span class="sxs-lookup"><span data-stu-id="09d63-172">78</span></span>

<span data-ttu-id="09d63-173">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="09d63-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-174">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="09d63-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-175">79</span><span class="sxs-lookup"><span data-stu-id="09d63-175">79</span></span>

<span data-ttu-id="09d63-176">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="09d63-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-177">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="09d63-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-178">80</span><span class="sxs-lookup"><span data-stu-id="09d63-178">80</span></span>

<span data-ttu-id="09d63-179">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="09d63-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-180">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="09d63-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-181">81</span><span class="sxs-lookup"><span data-stu-id="09d63-181">81</span></span>

<span data-ttu-id="09d63-182">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="09d63-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-183">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="09d63-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-184">82</span><span class="sxs-lookup"><span data-stu-id="09d63-184">82</span></span>

<span data-ttu-id="09d63-185">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="09d63-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-186">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="09d63-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-187">83</span><span class="sxs-lookup"><span data-stu-id="09d63-187">83</span></span>

<span data-ttu-id="09d63-188">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="09d63-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-189">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="09d63-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-190">84</span><span class="sxs-lookup"><span data-stu-id="09d63-190">84</span></span>

<span data-ttu-id="09d63-191">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="09d63-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-192">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="09d63-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-193">85</span><span class="sxs-lookup"><span data-stu-id="09d63-193">85</span></span>

<span data-ttu-id="09d63-194">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="09d63-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-195">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="09d63-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-196">86</span><span class="sxs-lookup"><span data-stu-id="09d63-196">86</span></span>

<span data-ttu-id="09d63-197">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="09d63-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-198">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="09d63-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-199">87</span><span class="sxs-lookup"><span data-stu-id="09d63-199">87</span></span>

<span data-ttu-id="09d63-200">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="09d63-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-201">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="09d63-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-202">88</span><span class="sxs-lookup"><span data-stu-id="09d63-202">88</span></span>

<span data-ttu-id="09d63-203">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="09d63-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-204">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="09d63-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-205">89</span><span class="sxs-lookup"><span data-stu-id="09d63-205">89</span></span>

<span data-ttu-id="09d63-206">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="09d63-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-207">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="09d63-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-208">90</span><span class="sxs-lookup"><span data-stu-id="09d63-208">90</span></span>

<span data-ttu-id="09d63-209">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="09d63-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-210">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="09d63-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-211">91</span><span class="sxs-lookup"><span data-stu-id="09d63-211">91</span></span>

<span data-ttu-id="09d63-212">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="09d63-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-213">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="09d63-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-214">92</span><span class="sxs-lookup"><span data-stu-id="09d63-214">92</span></span>

<span data-ttu-id="09d63-215">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="09d63-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-216">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="09d63-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-217">93</span><span class="sxs-lookup"><span data-stu-id="09d63-217">93</span></span>

<span data-ttu-id="09d63-218">Já existe.</span><span class="sxs-lookup"><span data-stu-id="09d63-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-219">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="09d63-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-220">94</span><span class="sxs-lookup"><span data-stu-id="09d63-220">94</span></span>

<span data-ttu-id="09d63-221">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="09d63-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-222">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="09d63-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-223">95</span><span class="sxs-lookup"><span data-stu-id="09d63-223">95</span></span>

<span data-ttu-id="09d63-224">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="09d63-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-225">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="09d63-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-226">96</span><span class="sxs-lookup"><span data-stu-id="09d63-226">96</span></span>

<span data-ttu-id="09d63-227">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="09d63-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-228">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="09d63-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-229">97</span><span class="sxs-lookup"><span data-stu-id="09d63-229">97</span></span>

<span data-ttu-id="09d63-230">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="09d63-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-231">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="09d63-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-232">98</span><span class="sxs-lookup"><span data-stu-id="09d63-232">98</span></span>

<span data-ttu-id="09d63-233">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="09d63-233">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-234">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="09d63-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-235">100</span><span class="sxs-lookup"><span data-stu-id="09d63-235">100</span></span>

<span data-ttu-id="09d63-236">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="09d63-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="09d63-237">**Outras**</span><span class="sxs-lookup"><span data-stu-id="09d63-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="09d63-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="09d63-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="09d63-239">Exemplos</span><span class="sxs-lookup"><span data-stu-id="09d63-239">Examples</span></span>

<span data-ttu-id="09d63-240">A amostra [Modificar o nível IGMP para todos os adaptadores de rede do](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) VBScript desabilita o multicast IGMP em um computador.</span><span class="sxs-lookup"><span data-stu-id="09d63-240">The [Modify the IGMP Level for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) VBScript sample disables IGMP multicasting on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="09d63-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09d63-241">Requirements</span></span>



| <span data-ttu-id="09d63-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="09d63-242">Requirement</span></span> | <span data-ttu-id="09d63-243">Valor</span><span class="sxs-lookup"><span data-stu-id="09d63-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09d63-244">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09d63-244">Minimum supported client</span></span><br/> | <span data-ttu-id="09d63-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09d63-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="09d63-246">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09d63-246">Minimum supported server</span></span><br/> | <span data-ttu-id="09d63-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09d63-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="09d63-248">Namespace</span><span class="sxs-lookup"><span data-stu-id="09d63-248">Namespace</span></span><br/>                | <span data-ttu-id="09d63-249">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="09d63-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="09d63-250">MOF</span><span class="sxs-lookup"><span data-stu-id="09d63-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09d63-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09d63-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="09d63-252">DLL</span><span class="sxs-lookup"><span data-stu-id="09d63-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09d63-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09d63-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09d63-254">Confira também</span><span class="sxs-lookup"><span data-stu-id="09d63-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09d63-255">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="09d63-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="09d63-256">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="09d63-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="09d63-257">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="09d63-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="09d63-258">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="09d63-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="09d63-259">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="09d63-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

