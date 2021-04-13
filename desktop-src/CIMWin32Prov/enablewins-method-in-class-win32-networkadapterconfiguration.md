---
description: EnableWINS ativa &\# 32; O método estático da classe WMI habilita as configurações do Windows Internet Serviço de Nomenclatura (WINS) específicas para TCP/IP, mas independente do adaptador de rede.
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: Método EnableWINS ativa da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 77f5ba32606ff228908e8b7a1559a73ae5139e9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500884"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="6c8ff-103">Método EnableWINS ativa da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c8ff-103">EnableWINS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="6c8ff-104">O método estático da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableWINS ativa** habilita as configurações WINS (Windows Internet serviço de nomenclatura) específicas para TCP/IP, mas independente do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="6c8ff-104">The **EnableWINS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables Windows Internet Naming Service (WINS) settings specific to TCP/IP, but independent of the network adapter.</span></span>

<span data-ttu-id="6c8ff-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="6c8ff-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6c8ff-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6c8ff-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c8ff-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c8ff-107">Syntax</span></span>


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a><span data-ttu-id="6c8ff-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c8ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c8ff-109">*DNSEnabledForWINSResolution* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c8ff-109">*DNSEnabledForWINSResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c8ff-110">Se for **true**, o DNS (sistema de nomes de domínio) será habilitado para resolução de nomes sobre a resolução WINS.</span><span class="sxs-lookup"><span data-stu-id="6c8ff-110">If **true**, the Domain Name System (DNS) is enabled for name resolution over WINS resolution.</span></span>

</dd> <dt>

<span data-ttu-id="6c8ff-111">*WINSEnableLMHostsLookup* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c8ff-111">*WINSEnableLMHostsLookup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c8ff-112">Se **for true**, os arquivos de pesquisa local serão usados.</span><span class="sxs-lookup"><span data-stu-id="6c8ff-112">If **true**, local lookup files are used.</span></span> <span data-ttu-id="6c8ff-113">Arquivos de pesquisa conterão mapeamentos de endereços IP para nomes de host.</span><span class="sxs-lookup"><span data-stu-id="6c8ff-113">Lookup files will contain mappings of IP addresses to host names.</span></span>

</dd> <dt>

<span data-ttu-id="6c8ff-114">*WINSHostLookupFile* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6c8ff-114">*WINSHostLookupFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6c8ff-115">Arquivos de pesquisa que contêm mapeamentos de endereços IP para nomes de host.</span><span class="sxs-lookup"><span data-stu-id="6c8ff-115">Lookup files that contain mappings of IP addresses to host names.</span></span> <span data-ttu-id="6c8ff-116">Se disponível, os arquivos serão encontrados nos drivers% SystemRoot% \\ System32 \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="6c8ff-116">If available, the files will be found in %SystemRoot%\\system32\\drivers\\ .</span></span>

</dd> <dt>

<span data-ttu-id="6c8ff-117">*WINSScopeID* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6c8ff-117">*WINSScopeID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6c8ff-118">O valor do identificador de escopo que será anexado ao final do nome NetBIOS do computador.</span><span class="sxs-lookup"><span data-stu-id="6c8ff-118">Scope identifier value that will be appended to the end of the computer's NetBIOS name.</span></span> <span data-ttu-id="6c8ff-119">Os sistemas que usam o mesmo identificador de escopo podem se comunicar com este computador.</span><span class="sxs-lookup"><span data-stu-id="6c8ff-119">Systems that use the same scope identifier can communicate with this computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c8ff-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c8ff-120">Return value</span></span>

<span data-ttu-id="6c8ff-121">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária; 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária; um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="6c8ff-121">Returns a value of 0 (zero) for a successful completion when no reboot is required; 1 (one) for a successful completion when a reboot is required; a different number if there is an error.</span></span> <span data-ttu-id="6c8ff-122">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6c8ff-122">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6c8ff-123">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6c8ff-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6c8ff-124">**Conclusão bem-sucedida, nenhuma reinicialização necessária** (0)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-124">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-125">**Conclusão bem-sucedida, reinicialização necessária** (1)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-125">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-126">**Método sem suporte nesta plataforma** (64)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-126">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-127">**Falha desconhecida** (65)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-127">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-128">**Máscara de sub-rede inválida** (66)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-128">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-129">**Ocorreu um erro ao processar uma instância que foi retornada** (67)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-129">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-130">**Parâmetro de entrada inválido** (68)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-130">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-131">**Mais de 5 gateways especificados** (69)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-131">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-132">**Endereço IP inválido** (70)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-132">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-133">**Endereço IP de gateway inválido** (71)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-133">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-134">**Ocorreu um erro ao acessar o registro para as informações solicitadas** (72)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-134">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-135">**Nome de domínio inválido** (73)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-135">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-136">**Nome de host inválido** (74)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-136">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-137">**Nenhum servidor WINS primário/secundário definido** (75)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-137">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-138">**Arquivo inválido** (76)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-138">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-139">**Caminho de sistema inválido** (77)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-139">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-140">**Falha na cópia do arquivo** (78)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-140">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-141">**Parâmetro de segurança inválido** (79)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-141">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-142">**Não é possível configurar o serviço TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-142">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-143">**Não é possível configurar o serviço DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-143">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-144">**Não é possível renovar a concessão DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-144">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-145">**Não é possível liberar a concessão DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-145">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-146">**IP não habilitado no adaptador** (84)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-146">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-147">**IPX não habilitado no adaptador** (85)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-147">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-148">**Erro de limites de número de quadro/rede** (86)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-148">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-149">**Tipo de quadro inválido** (87)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-149">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-150">**Número de rede inválido** (88)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-150">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-151">**Número de rede duplicado** (89)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-151">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-152">**Parâmetro fora dos limites** (90)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-152">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-153">**Acesso negado** (91)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-153">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-154">**Memória insuficiente** (92)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-154">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-155">**Já existe** (93)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-155">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-156">**Caminho, arquivo ou objeto não encontrado** (94)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-156">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-157">**Não é possível notificar o serviço** (95)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-157">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-158">**Não é possível notificar o serviço DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-158">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-159">**Interface não configurável** (97)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-159">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-160">**Nem todas as concessões DHCP puderam ser liberadas/renovadas** (98)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-160">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-161">**DHCP não habilitado no adaptador** (100)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-161">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="6c8ff-162">**Outro** (101 4294967295)</span><span class="sxs-lookup"><span data-stu-id="6c8ff-162">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="6c8ff-163">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6c8ff-163">Examples</span></span>

<span data-ttu-id="6c8ff-164">O exemplo de código [Ativar WINS para todos os adaptadores de rede](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript, na galeria do TechNet, usa **EnableWINS ativa** para habilitar o WINS em todos os adaptadores de rede instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="6c8ff-164">The [Enable WINS for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript code sample, on TechNet Gallery, uses **EnableWINS** to Enables WINS on all the network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8ff-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c8ff-165">Requirements</span></span>



| <span data-ttu-id="6c8ff-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c8ff-166">Requirement</span></span> | <span data-ttu-id="6c8ff-167">Valor</span><span class="sxs-lookup"><span data-stu-id="6c8ff-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8ff-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c8ff-168">Minimum supported client</span></span><br/> | <span data-ttu-id="6c8ff-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c8ff-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c8ff-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c8ff-170">Minimum supported server</span></span><br/> | <span data-ttu-id="6c8ff-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c8ff-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c8ff-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c8ff-172">Namespace</span></span><br/>                | <span data-ttu-id="6c8ff-173">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6c8ff-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6c8ff-174">MOF</span><span class="sxs-lookup"><span data-stu-id="6c8ff-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c8ff-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c8ff-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c8ff-176">DLL</span><span class="sxs-lookup"><span data-stu-id="6c8ff-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c8ff-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c8ff-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c8ff-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c8ff-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c8ff-179">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="6c8ff-179">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="6c8ff-180">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="6c8ff-180">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="6c8ff-181">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="6c8ff-181">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="6c8ff-182">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="6c8ff-182">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="6c8ff-183">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="6c8ff-183">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

