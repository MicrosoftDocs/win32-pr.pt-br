---
description: Define o número de rede virtual de intercâmbio de pacotes entre redes (IPX) no sistema de computador de destino.
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Método SetIPXVirtualNetworkNumber da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXVirtualNetworkNumber
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: ed6e6802a17ef6ec4393d2ae0c5ec43f0e21d247
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762760"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="5b232-103">Método SetIPXVirtualNetworkNumber da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b232-103">SetIPXVirtualNetworkNumber method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="5b232-104">Define o número de rede virtual de intercâmbio de pacotes entre redes (IPX) no sistema de computador de destino.</span><span class="sxs-lookup"><span data-stu-id="5b232-104">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span> <span data-ttu-id="5b232-105">O Windows 2000 e o Windows NT 3,51 ou superior usam um número de rede interno para roteamento interno.</span><span class="sxs-lookup"><span data-stu-id="5b232-105">Windows 2000 and Windows NT 3.51 or greater uses an internal network number for internal routing.</span></span> <span data-ttu-id="5b232-106">O número de rede interno também é conhecido como um número de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5b232-106">The internal network number is also known as a virtual network number.</span></span> <span data-ttu-id="5b232-107">Ele identifica exclusivamente o sistema de computador na rede.</span><span class="sxs-lookup"><span data-stu-id="5b232-107">It uniquely identifies the computer system on the network.</span></span> <span data-ttu-id="5b232-108">O método retorna um valor inteiro que pode ser interpretado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5b232-108">The method returns an integer value that can be interpretted as follows:</span></span>

## <a name="syntax"></a><span data-ttu-id="5b232-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b232-109">Syntax</span></span>


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a><span data-ttu-id="5b232-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b232-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b232-111">*IPXVirtualNetNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5b232-111">*IPXVirtualNetNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b232-112">O número da rede virtual para este sistema.</span><span class="sxs-lookup"><span data-stu-id="5b232-112">The virtual network number for this system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b232-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b232-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="5b232-114">**Conclusão bem-sucedida, nenhuma reinicialização necessária** (0)</span><span class="sxs-lookup"><span data-stu-id="5b232-114">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-115">**Conclusão bem-sucedida, reinicialização necessária** (1)</span><span class="sxs-lookup"><span data-stu-id="5b232-115">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-116">**Método sem suporte nesta plataforma** (64)</span><span class="sxs-lookup"><span data-stu-id="5b232-116">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-117">**Falha desconhecida** (65)</span><span class="sxs-lookup"><span data-stu-id="5b232-117">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-118">**Máscara de sub-rede inválida** (66)</span><span class="sxs-lookup"><span data-stu-id="5b232-118">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-119">**Ocorreu um erro ao processar uma instância que foi retornada** (67)</span><span class="sxs-lookup"><span data-stu-id="5b232-119">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-120">**Parâmetro de entrada inválido** (68)</span><span class="sxs-lookup"><span data-stu-id="5b232-120">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-121">**Mais de 5 gateways especificados** (69)</span><span class="sxs-lookup"><span data-stu-id="5b232-121">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-122">**Endereço IP inválido** (70)</span><span class="sxs-lookup"><span data-stu-id="5b232-122">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-123">**Endereço IP de gateway inválido** (71)</span><span class="sxs-lookup"><span data-stu-id="5b232-123">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-124">**Ocorreu um erro ao acessar o registro para as informações solicitadas** (72)</span><span class="sxs-lookup"><span data-stu-id="5b232-124">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-125">**Nome de domínio inválido** (73)</span><span class="sxs-lookup"><span data-stu-id="5b232-125">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-126">**Nome de host inválido** (74)</span><span class="sxs-lookup"><span data-stu-id="5b232-126">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-127">**Nenhum servidor WINS primário/secundário definido** (75)</span><span class="sxs-lookup"><span data-stu-id="5b232-127">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-128">**Arquivo inválido** (76)</span><span class="sxs-lookup"><span data-stu-id="5b232-128">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-129">**Caminho de sistema inválido** (77)</span><span class="sxs-lookup"><span data-stu-id="5b232-129">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-130">**Falha na cópia do arquivo** (78)</span><span class="sxs-lookup"><span data-stu-id="5b232-130">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-131">**Parâmetro de segurança inválido** (79)</span><span class="sxs-lookup"><span data-stu-id="5b232-131">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-132">**Não é possível configurar o serviço TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="5b232-132">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-133">**Não é possível configurar o serviço DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="5b232-133">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-134">**Não é possível renovar a concessão DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="5b232-134">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-135">**Não é possível liberar a concessão DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="5b232-135">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-136">**IP não habilitado no adaptador** (84)</span><span class="sxs-lookup"><span data-stu-id="5b232-136">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-137">**IPX não habilitado no adaptador** (85)</span><span class="sxs-lookup"><span data-stu-id="5b232-137">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-138">**Erro de limites de número de quadro/rede** (86)</span><span class="sxs-lookup"><span data-stu-id="5b232-138">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-139">**Tipo de quadro inválido** (87)</span><span class="sxs-lookup"><span data-stu-id="5b232-139">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-140">**Número de rede inválido** (88)</span><span class="sxs-lookup"><span data-stu-id="5b232-140">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-141">**Número de rede duplicado** (89)</span><span class="sxs-lookup"><span data-stu-id="5b232-141">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-142">**Parâmetro fora dos limites** (90)</span><span class="sxs-lookup"><span data-stu-id="5b232-142">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-143">**Acesso negado** (91)</span><span class="sxs-lookup"><span data-stu-id="5b232-143">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-144">**Memória insuficiente** (92)</span><span class="sxs-lookup"><span data-stu-id="5b232-144">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-145">**Já existe** (93)</span><span class="sxs-lookup"><span data-stu-id="5b232-145">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-146">**Caminho, arquivo ou objeto não encontrado** (94)</span><span class="sxs-lookup"><span data-stu-id="5b232-146">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-147">**Não é possível notificar o serviço** (95)</span><span class="sxs-lookup"><span data-stu-id="5b232-147">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-148">**Não é possível notificar o serviço DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="5b232-148">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-149">**Interface não configurável** (97)</span><span class="sxs-lookup"><span data-stu-id="5b232-149">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-150">**Nem todas as concessões DHCP puderam ser liberadas/renovadas** (98)</span><span class="sxs-lookup"><span data-stu-id="5b232-150">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-151">**DHCP não habilitado no adaptador** (100)</span><span class="sxs-lookup"><span data-stu-id="5b232-151">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="5b232-152">**Outro** (101 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="5b232-152">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5b232-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b232-153">Requirements</span></span>



| <span data-ttu-id="5b232-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b232-154">Requirement</span></span> | <span data-ttu-id="5b232-155">Valor</span><span class="sxs-lookup"><span data-stu-id="5b232-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b232-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b232-156">Minimum supported client</span></span><br/> | <span data-ttu-id="5b232-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b232-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b232-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b232-158">Minimum supported server</span></span><br/> | <span data-ttu-id="5b232-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b232-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b232-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b232-160">Namespace</span></span><br/>                | <span data-ttu-id="5b232-161">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5b232-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5b232-162">MOF</span><span class="sxs-lookup"><span data-stu-id="5b232-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b232-163"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b232-163"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b232-164">DLL</span><span class="sxs-lookup"><span data-stu-id="5b232-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b232-165"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b232-165"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b232-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b232-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b232-167">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="5b232-167">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




