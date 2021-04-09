---
description: SetDNSServerSearchOrder &\# 32; O método de classe WMI usa uma matriz de elementos de cadeia de caracteres para definir a ordem de pesquisa do servidor.
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: Método SetDNSServerSearchOrder da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSServerSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bfe731ea1d89e8e0ad702bfa229a61fba30dfc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010232"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="78dfd-103">Método SetDNSServerSearchOrder da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="78dfd-103">SetDNSServerSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="78dfd-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSServerSearchOrder** usa uma matriz de elementos de cadeia de caracteres para definir a ordem de pesquisa do servidor.</span><span class="sxs-lookup"><span data-stu-id="78dfd-104">The **SetDNSServerSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uses an array of string elements to set the server search order.</span></span>

<span data-ttu-id="78dfd-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="78dfd-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="78dfd-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="78dfd-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="78dfd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78dfd-107">Syntax</span></span>


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="78dfd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78dfd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78dfd-109">*DNSServerSearchOrder* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78dfd-109">*DNSServerSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78dfd-110">Lista de endereços IP do servidor para consultar servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="78dfd-110">List of server IP addresses to query for DNS servers.</span></span>

<span data-ttu-id="78dfd-111">Exemplo: 130.215.24.1 ou 157.54.164.1</span><span class="sxs-lookup"><span data-stu-id="78dfd-111">Example: 130.215.24.1 or 157.54.164.1</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78dfd-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78dfd-112">Return value</span></span>

<span data-ttu-id="78dfd-113">Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="78dfd-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="78dfd-114">Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="78dfd-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="78dfd-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="78dfd-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="78dfd-116">**Conclusão bem-sucedida, nenhuma reinicialização necessária** (0)</span><span class="sxs-lookup"><span data-stu-id="78dfd-116">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-117">**Conclusão bem-sucedida, reinicialização necessária** (1)</span><span class="sxs-lookup"><span data-stu-id="78dfd-117">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-118">**Método sem suporte nesta plataforma** (64)</span><span class="sxs-lookup"><span data-stu-id="78dfd-118">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-119">**Falha desconhecida** (65)</span><span class="sxs-lookup"><span data-stu-id="78dfd-119">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-120">**Máscara de sub-rede inválida** (66)</span><span class="sxs-lookup"><span data-stu-id="78dfd-120">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-121">**Ocorreu um erro ao processar uma instância que foi retornada** (67)</span><span class="sxs-lookup"><span data-stu-id="78dfd-121">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-122">**Parâmetro de entrada inválido** (68)</span><span class="sxs-lookup"><span data-stu-id="78dfd-122">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-123">**Mais de 5 gateways especificados** (69)</span><span class="sxs-lookup"><span data-stu-id="78dfd-123">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-124">**Endereço IP inválido** (70)</span><span class="sxs-lookup"><span data-stu-id="78dfd-124">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-125">**Endereço IP de gateway inválido** (71)</span><span class="sxs-lookup"><span data-stu-id="78dfd-125">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-126">**Ocorreu um erro ao acessar o registro para as informações solicitadas** (72)</span><span class="sxs-lookup"><span data-stu-id="78dfd-126">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-127">**Nome de domínio inválido** (73)</span><span class="sxs-lookup"><span data-stu-id="78dfd-127">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-128">**Nome de host inválido** (74)</span><span class="sxs-lookup"><span data-stu-id="78dfd-128">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-129">**Nenhum servidor WINS primário/secundário definido** (75)</span><span class="sxs-lookup"><span data-stu-id="78dfd-129">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-130">**Arquivo inválido** (76)</span><span class="sxs-lookup"><span data-stu-id="78dfd-130">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-131">**Caminho de sistema inválido** (77)</span><span class="sxs-lookup"><span data-stu-id="78dfd-131">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-132">**Falha na cópia do arquivo** (78)</span><span class="sxs-lookup"><span data-stu-id="78dfd-132">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-133">**Parâmetro de segurança inválido** (79)</span><span class="sxs-lookup"><span data-stu-id="78dfd-133">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-134">**Não é possível configurar o serviço TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="78dfd-134">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-135">**Não é possível configurar o serviço DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="78dfd-135">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-136">**Não é possível renovar a concessão DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="78dfd-136">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-137">**Não é possível liberar a concessão DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="78dfd-137">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-138">**IP não habilitado no adaptador** (84)</span><span class="sxs-lookup"><span data-stu-id="78dfd-138">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-139">**IPX não habilitado no adaptador** (85)</span><span class="sxs-lookup"><span data-stu-id="78dfd-139">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-140">**Erro de limites de número de quadro/rede** (86)</span><span class="sxs-lookup"><span data-stu-id="78dfd-140">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-141">**Tipo de quadro inválido** (87)</span><span class="sxs-lookup"><span data-stu-id="78dfd-141">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-142">**Número de rede inválido** (88)</span><span class="sxs-lookup"><span data-stu-id="78dfd-142">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-143">**Número de rede duplicado** (89)</span><span class="sxs-lookup"><span data-stu-id="78dfd-143">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-144">**Parâmetro fora dos limites** (90)</span><span class="sxs-lookup"><span data-stu-id="78dfd-144">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-145">**Acesso negado** (91)</span><span class="sxs-lookup"><span data-stu-id="78dfd-145">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-146">**Memória insuficiente** (92)</span><span class="sxs-lookup"><span data-stu-id="78dfd-146">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-147">**Já existe** (93)</span><span class="sxs-lookup"><span data-stu-id="78dfd-147">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-148">**Caminho, arquivo ou objeto não encontrado** (94)</span><span class="sxs-lookup"><span data-stu-id="78dfd-148">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-149">**Não é possível notificar o serviço** (95)</span><span class="sxs-lookup"><span data-stu-id="78dfd-149">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-150">**Não é possível notificar o serviço DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="78dfd-150">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-151">**Interface não configurável** (97)</span><span class="sxs-lookup"><span data-stu-id="78dfd-151">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-152">**Nem todas as concessões DHCP puderam ser liberadas/renovadas** (98)</span><span class="sxs-lookup"><span data-stu-id="78dfd-152">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-153">**DHCP não habilitado no adaptador** (100)</span><span class="sxs-lookup"><span data-stu-id="78dfd-153">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="78dfd-154">**Outro** (101 4294967295)</span><span class="sxs-lookup"><span data-stu-id="78dfd-154">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="78dfd-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="78dfd-155">Remarks</span></span>

<span data-ttu-id="78dfd-156">Essa é uma chamada de método dependente de instância que se aplica a uma base por adaptador.</span><span class="sxs-lookup"><span data-stu-id="78dfd-156">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="78dfd-157">Depois que os servidores DNS estáticos forem especificados para começar a usar o protocolo DHCP em vez de servidores DNS estáticos, você poderá chamar o método sem fornecer os parâmetros "in".</span><span class="sxs-lookup"><span data-stu-id="78dfd-157">After static DNS servers are specified to start using Dynamic Host Configuration Protocol (DHCP) instead of static DNS servers, you can call the method without supplying "in" parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="78dfd-158">Exemplos</span><span class="sxs-lookup"><span data-stu-id="78dfd-158">Examples</span></span>

<span data-ttu-id="78dfd-159">A amostra [definir ordem de pesquisa do servidor DNS para vários computadores em uma unidade organizacional](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) do VBScript na galeria do TechNet recupera ou define a ordem de pesquisa do servidor DNS para vários computadores que pertencem a uma unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="78dfd-159">The [Set DNS Server Search Order for Multiple Computers in an Organizational Unit](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) VBScript sample on TechNet Gallery retrieves or sets DNS Server search order for multiple computers that belongs to one organizational unit.</span></span>

<span data-ttu-id="78dfd-160">A amostra [Modificar a ordem de pesquisa do servidor DNS de um adaptador de rede do](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) VBScript configura um adaptador de rede associado a TCP/IP para usar dois servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="78dfd-160">The [Modify the DNS Server Search Order for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) VBScript sample configures a TCP/IP-bound network adapter to use two DNS servers.</span></span>

## <a name="requirements"></a><span data-ttu-id="78dfd-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78dfd-161">Requirements</span></span>



| <span data-ttu-id="78dfd-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="78dfd-162">Requirement</span></span> | <span data-ttu-id="78dfd-163">Valor</span><span class="sxs-lookup"><span data-stu-id="78dfd-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78dfd-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78dfd-164">Minimum supported client</span></span><br/> | <span data-ttu-id="78dfd-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78dfd-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78dfd-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78dfd-166">Minimum supported server</span></span><br/> | <span data-ttu-id="78dfd-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78dfd-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78dfd-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="78dfd-168">Namespace</span></span><br/>                | <span data-ttu-id="78dfd-169">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="78dfd-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="78dfd-170">MOF</span><span class="sxs-lookup"><span data-stu-id="78dfd-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78dfd-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78dfd-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="78dfd-172">DLL</span><span class="sxs-lookup"><span data-stu-id="78dfd-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78dfd-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78dfd-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78dfd-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="78dfd-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78dfd-175">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="78dfd-175">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="78dfd-176">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="78dfd-176">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="78dfd-177">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="78dfd-177">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="78dfd-178">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="78dfd-178">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="78dfd-179">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="78dfd-179">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

