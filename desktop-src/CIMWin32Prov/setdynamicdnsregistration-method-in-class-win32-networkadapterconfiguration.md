---
description: O método SetDynamicDNSRegistration indica o registro de DNS dinâmico de endereços IP para este adaptador associado a IP.
ms.assetid: 8e6ca408-3283-40b8-b621-9befdc39b730
ms.tgt_platform: multiple
title: Método SetDynamicDNSRegistration da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDynamicDNSRegistration
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36818205e356f873b391159293e9204a9ced44a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826520"
---
# <a name="setdynamicdnsregistration-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8bbdb-103">Método SetDynamicDNSRegistration da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="8bbdb-103">SetDynamicDNSRegistration method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8bbdb-104">O método **SetDynamicDNSRegistration** indica o registro de DNS dinâmico de endereços IP para este adaptador associado a IP.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-104">The **SetDynamicDNSRegistration** method indicates the dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span>

<span data-ttu-id="8bbdb-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8bbdb-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8bbdb-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8bbdb-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8bbdb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8bbdb-107">Syntax</span></span>


```mof
uint32 SetDynamicDNSRegistration(
  [in]           boolean FullDNSRegistrationEnabled,
  [in, optional] boolean DomainDNSRegistrationEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="8bbdb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8bbdb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bbdb-109">*FullDNSRegistrationEnabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8bbdb-109">*FullDNSRegistrationEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-110">Se **for true**, os endereços IP para essa conexão serão registrados no DNS com o nome DNS completo do computador.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-110">If **true**, the IP addresses for this connection is registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="8bbdb-111">O nome DNS completo do computador é exibido na guia **identificação de rede** do painel de controle do sistema.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-111">The full DNS name of the computer is displayed on the **Network Identification** tab of the system Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-112">*DomainDNSRegistrationEnabled* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8bbdb-112">*DomainDNSRegistrationEnabled* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-113">Se **for true**, os endereços IP para essa conexão serão registrados sob o nome de domínio dessa conexão, além de serem registrados sob o nome DNS completo do computador.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-113">If **true**, the IP addresses for this connection are registered under the domain name of this connection, in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="8bbdb-114">O nome de domínio dessa conexão é definido usando o método [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) ou atribuído pelo DHCP.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-114">The domain name of this connection is either set using the method [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) or assigned by DHCP.</span></span> <span data-ttu-id="8bbdb-115">O nome registrado é o nome do host do computador com o nome de domínio anexado.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-115">The registered name is the host name of the computer with the domain name appended.</span></span> <span data-ttu-id="8bbdb-116">Esse parâmetro tem significado apenas quando *FullDNSRegistrationEnabled* está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-116">This parameter has meaning only when *FullDNSRegistrationEnabled* is enabled.</span></span> <span data-ttu-id="8bbdb-117">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-117">The default value is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bbdb-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8bbdb-118">Return value</span></span>

<span data-ttu-id="8bbdb-119">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-119">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="8bbdb-120">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8bbdb-120">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8bbdb-121">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8bbdb-121">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8bbdb-122">**Conclusão bem-sucedida, nenhuma reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-122">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-123">0</span><span class="sxs-lookup"><span data-stu-id="8bbdb-123">0</span></span>

<span data-ttu-id="8bbdb-124">Conclusão bem-sucedida, nenhuma reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-124">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-125">**Conclusão bem-sucedida, reinicialização necessária**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-126">1</span><span class="sxs-lookup"><span data-stu-id="8bbdb-126">1</span></span>

<span data-ttu-id="8bbdb-127">Conclusão bem-sucedida, reinicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-127">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-128">**Método sem suporte nesta plataforma**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-128">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-129">64</span><span class="sxs-lookup"><span data-stu-id="8bbdb-129">64</span></span>

<span data-ttu-id="8bbdb-130">Método sem suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-130">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-131">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-132">65</span><span class="sxs-lookup"><span data-stu-id="8bbdb-132">65</span></span>

<span data-ttu-id="8bbdb-133">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-133">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-134">**Máscara de sub-rede inválida**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-134">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-135">66</span><span class="sxs-lookup"><span data-stu-id="8bbdb-135">66</span></span>

<span data-ttu-id="8bbdb-136">Máscara de sub-rede inválida.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-136">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-137">**Ocorreu um erro ao processar uma instância que foi retornada**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-137">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-138">67</span><span class="sxs-lookup"><span data-stu-id="8bbdb-138">67</span></span>

<span data-ttu-id="8bbdb-139">Ocorreu um erro ao processar uma instância que foi retornada.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-139">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-140">**Parâmetro de entrada inválido**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-140">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-141">68</span><span class="sxs-lookup"><span data-stu-id="8bbdb-141">68</span></span>

<span data-ttu-id="8bbdb-142">Parâmetro de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-142">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-143">**Mais de 5 gateways especificados**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-143">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-144">69</span><span class="sxs-lookup"><span data-stu-id="8bbdb-144">69</span></span>

<span data-ttu-id="8bbdb-145">Mais de cinco gateways especificados.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-145">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-146">**Endereço IP inválido**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-146">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-147">70</span><span class="sxs-lookup"><span data-stu-id="8bbdb-147">70</span></span>

<span data-ttu-id="8bbdb-148">Endereço IP inválido.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-148">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-149">**Endereço IP de gateway inválido**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-149">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-150">71</span><span class="sxs-lookup"><span data-stu-id="8bbdb-150">71</span></span>

<span data-ttu-id="8bbdb-151">Endereço IP do gateway inválido.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-151">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-152">**Ocorreu um erro ao acessar o registro para as informações solicitadas**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-152">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-153">72</span><span class="sxs-lookup"><span data-stu-id="8bbdb-153">72</span></span>

<span data-ttu-id="8bbdb-154">Ocorreu um erro ao acessar o registro para obter as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-154">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-155">**Nome de domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-155">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-156">73</span><span class="sxs-lookup"><span data-stu-id="8bbdb-156">73</span></span>

<span data-ttu-id="8bbdb-157">Nome de domínio inválido.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-157">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-158">**Nome de host inválido**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-158">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-159">74</span><span class="sxs-lookup"><span data-stu-id="8bbdb-159">74</span></span>

<span data-ttu-id="8bbdb-160">Nome de host inválido.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-160">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-161">**Nenhum servidor WINS primário/secundário definido**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-161">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-162">75</span><span class="sxs-lookup"><span data-stu-id="8bbdb-162">75</span></span>

<span data-ttu-id="8bbdb-163">Nenhum servidor WINS primário ou secundário definido.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-163">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-164">**Arquivo inválido**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-164">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-165">76</span><span class="sxs-lookup"><span data-stu-id="8bbdb-165">76</span></span>

<span data-ttu-id="8bbdb-166">Arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-166">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-167">**Caminho de sistema inválido**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-167">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-168">77</span><span class="sxs-lookup"><span data-stu-id="8bbdb-168">77</span></span>

<span data-ttu-id="8bbdb-169">Caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-169">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-170">**Falha na cópia do arquivo**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-170">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-171">78</span><span class="sxs-lookup"><span data-stu-id="8bbdb-171">78</span></span>

<span data-ttu-id="8bbdb-172">Falha na cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-172">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-173">**Parâmetro de segurança inválido**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-173">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-174">79</span><span class="sxs-lookup"><span data-stu-id="8bbdb-174">79</span></span>

<span data-ttu-id="8bbdb-175">Parâmetro de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-175">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-176">**Não é possível configurar o serviço TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-176">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-177">80</span><span class="sxs-lookup"><span data-stu-id="8bbdb-177">80</span></span>

<span data-ttu-id="8bbdb-178">Não é possível configurar o serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-178">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-179">**Não é possível configurar o serviço DHCP**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-179">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-180">81</span><span class="sxs-lookup"><span data-stu-id="8bbdb-180">81</span></span>

<span data-ttu-id="8bbdb-181">Não é possível configurar o serviço DHCP.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-181">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-182">**Não é possível renovar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-183">82</span><span class="sxs-lookup"><span data-stu-id="8bbdb-183">82</span></span>

<span data-ttu-id="8bbdb-184">Não é possível renovar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-185">**Não é possível liberar a concessão DHCP**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-186">83</span><span class="sxs-lookup"><span data-stu-id="8bbdb-186">83</span></span>

<span data-ttu-id="8bbdb-187">Não é possível liberar a concessão DHCP.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-188">**IP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-189">84</span><span class="sxs-lookup"><span data-stu-id="8bbdb-189">84</span></span>

<span data-ttu-id="8bbdb-190">O IP não está habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-191">**IPX não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-192">85</span><span class="sxs-lookup"><span data-stu-id="8bbdb-192">85</span></span>

<span data-ttu-id="8bbdb-193">IPX não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-194">**Erro de limites de número de quadro/rede**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-195">86</span><span class="sxs-lookup"><span data-stu-id="8bbdb-195">86</span></span>

<span data-ttu-id="8bbdb-196">Erro de limites de número de rede ou quadro.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-197">**Tipo de quadro inválido**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-198">87</span><span class="sxs-lookup"><span data-stu-id="8bbdb-198">87</span></span>

<span data-ttu-id="8bbdb-199">Tipo de quadro inválido.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-200">**Número de rede inválido**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-201">88</span><span class="sxs-lookup"><span data-stu-id="8bbdb-201">88</span></span>

<span data-ttu-id="8bbdb-202">Número de rede inválido.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-203">**Número de rede duplicado**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-204">89</span><span class="sxs-lookup"><span data-stu-id="8bbdb-204">89</span></span>

<span data-ttu-id="8bbdb-205">Número de rede duplicado.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-206">**Parâmetro fora dos limites**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-207">90</span><span class="sxs-lookup"><span data-stu-id="8bbdb-207">90</span></span>

<span data-ttu-id="8bbdb-208">Parâmetro fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-209">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-210">91</span><span class="sxs-lookup"><span data-stu-id="8bbdb-210">91</span></span>

<span data-ttu-id="8bbdb-211">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-212">**Memória insuficiente**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-213">92</span><span class="sxs-lookup"><span data-stu-id="8bbdb-213">92</span></span>

<span data-ttu-id="8bbdb-214">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-215">**Já existe**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-216">93</span><span class="sxs-lookup"><span data-stu-id="8bbdb-216">93</span></span>

<span data-ttu-id="8bbdb-217">Já existe.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-218">**Caminho, arquivo ou objeto não encontrado**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-219">94</span><span class="sxs-lookup"><span data-stu-id="8bbdb-219">94</span></span>

<span data-ttu-id="8bbdb-220">Caminho, arquivo ou objeto não encontrado.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-221">**Não é possível notificar o serviço**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-222">95</span><span class="sxs-lookup"><span data-stu-id="8bbdb-222">95</span></span>

<span data-ttu-id="8bbdb-223">Não é possível notificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-224">**Não é possível notificar o serviço DNS**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-225">96</span><span class="sxs-lookup"><span data-stu-id="8bbdb-225">96</span></span>

<span data-ttu-id="8bbdb-226">Não é possível notificar o serviço DNS.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-227">**Interface não configurável**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-228">97</span><span class="sxs-lookup"><span data-stu-id="8bbdb-228">97</span></span>

<span data-ttu-id="8bbdb-229">Interface não configurável.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-230">**Nem todas as concessões DHCP puderam ser liberadas/renovadas**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-231">98</span><span class="sxs-lookup"><span data-stu-id="8bbdb-231">98</span></span>

<span data-ttu-id="8bbdb-232">Nem todas as concessões DHCP podem ser liberadas ou renovadas.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-233">**DHCP não habilitado no adaptador**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-234">100</span><span class="sxs-lookup"><span data-stu-id="8bbdb-234">100</span></span>

<span data-ttu-id="8bbdb-235">DHCP não habilitado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8bbdb-236">**Outras**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-236">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8bbdb-237">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="8bbdb-237">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="8bbdb-238">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8bbdb-238">Examples</span></span>

<span data-ttu-id="8bbdb-239">A amostra [Modificar registro de DNS dinâmico para um adaptador de rede do](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) VBScript configura o registro de DNS dinâmico para um adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-239">The [Modify Dynamic DNS Registration for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) VBScript sample configures dynamic DNS registration for a network adapter.</span></span>

<span data-ttu-id="8bbdb-240">A amostra do [PowerShell configurar placas de rede iSCSI de acordo com as práticas recomendadas da Microsoft](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) automatiza as definições de configuração para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8bbdb-240">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bbdb-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bbdb-241">Requirements</span></span>



| <span data-ttu-id="8bbdb-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bbdb-242">Requirement</span></span> | <span data-ttu-id="8bbdb-243">Valor</span><span class="sxs-lookup"><span data-stu-id="8bbdb-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bbdb-244">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bbdb-244">Minimum supported client</span></span><br/> | <span data-ttu-id="8bbdb-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bbdb-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8bbdb-246">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bbdb-246">Minimum supported server</span></span><br/> | <span data-ttu-id="8bbdb-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bbdb-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8bbdb-248">Namespace</span><span class="sxs-lookup"><span data-stu-id="8bbdb-248">Namespace</span></span><br/>                | <span data-ttu-id="8bbdb-249">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8bbdb-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8bbdb-250">MOF</span><span class="sxs-lookup"><span data-stu-id="8bbdb-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bbdb-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bbdb-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bbdb-252">DLL</span><span class="sxs-lookup"><span data-stu-id="8bbdb-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bbdb-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bbdb-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bbdb-254">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bbdb-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bbdb-255">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="8bbdb-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8bbdb-256">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="8bbdb-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8bbdb-257">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="8bbdb-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8bbdb-258">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="8bbdb-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8bbdb-259">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="8bbdb-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

