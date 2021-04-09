---
description: Define os pares de número/quadro da rede IPX (troca de pacotes entre redes) para esse adaptador de rede.
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: Método SetIPXFrameTypeNetworkPairs da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXFrameTypeNetworkPairs
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: e4d53ec7b5600a767505e517a02fbf87b5a43d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089532"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="3e8ab-103">Método SetIPXFrameTypeNetworkPairs da classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e8ab-103">SetIPXFrameTypeNetworkPairs method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="3e8ab-104">Define os pares de número/quadro da rede IPX (troca de pacotes entre redes) para esse adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="3e8ab-104">Sets the Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span>

<span data-ttu-id="3e8ab-105">O Windows 2000 e o Windows NT 3,51 e superior usam um número de rede IPX para fins de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3e8ab-105">Windows 2000 and Windows NT 3.51 and higher use an IPX network number for routing purposes.</span></span> <span data-ttu-id="3e8ab-106">Ele é atribuído a cada combinação de tipo de quadro/adaptador de rede configurada no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="3e8ab-106">It is assigned to each configured frame type/network adapter combination on your computer system.</span></span> <span data-ttu-id="3e8ab-107">Esse número às vezes é chamado de "número de rede externa".</span><span class="sxs-lookup"><span data-stu-id="3e8ab-107">This number is sometimes referred to as the "external network number."</span></span> <span data-ttu-id="3e8ab-108">Ele deve ser exclusivo para cada segmento de rede.</span><span class="sxs-lookup"><span data-stu-id="3e8ab-108">It must be unique for each network segment.</span></span> <span data-ttu-id="3e8ab-109">Se o tipo de quadro for definido como automático, o número de rede deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="3e8ab-109">If the frame type is set to AUTO, the network number should to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e8ab-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e8ab-110">Syntax</span></span>


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a><span data-ttu-id="3e8ab-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e8ab-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e8ab-112">*IPXNetworkNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e8ab-112">*IPXNetworkNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e8ab-113">Uma matriz de caracteres que identifica exclusivamente um adaptador no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="3e8ab-113">An array of characters that uniquely identify an adapter on the computer system.</span></span> <span data-ttu-id="3e8ab-114">O transporte compatível com IPX/SPX do link do NetWare (NWLink) no Windows 2000 e no Windows NT 3,51 ou superior usa dois tipos diferentes de números de rede.</span><span class="sxs-lookup"><span data-stu-id="3e8ab-114">The NetWare Link (NWLink) IPX/SPX-compatible transport in Windows 2000 and Windows NT 3.51 or higher, uses two different types of network numbers.</span></span> <span data-ttu-id="3e8ab-115">Esse número às vezes é chamado de número de rede externa.</span><span class="sxs-lookup"><span data-stu-id="3e8ab-115">This number is sometimes referred to as the External Network Number.</span></span> <span data-ttu-id="3e8ab-116">Ele deve ser exclusivo para cada segmento de rede.</span><span class="sxs-lookup"><span data-stu-id="3e8ab-116">It must be unique for each network segment.</span></span> <span data-ttu-id="3e8ab-117">Os valores nessa lista de cadeias de caracteres devem ter um valor correspondente no parâmetro IPXFrameType identificando o tipo de quadro de pacote usado para essa rede.</span><span class="sxs-lookup"><span data-stu-id="3e8ab-117">The values in this string list must have a corresponding value in the IPXFrameType parameter identifying the packet frame type used for this network.</span></span>

</dd> <dt>

<span data-ttu-id="3e8ab-118">*IPXFrameType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e8ab-118">*IPXFrameType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e8ab-119">Uma matriz de inteiros de identificadores de tipo de quadro.</span><span class="sxs-lookup"><span data-stu-id="3e8ab-119">An integer array of frame type identifiers.</span></span> <span data-ttu-id="3e8ab-120">Os valores nessa matriz correspondem aos elementos no parâmetro *IPXNetworkNumber* .</span><span class="sxs-lookup"><span data-stu-id="3e8ab-120">The values in this array correspond to the elements in the *IPXNetworkNumber* parameter.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="3e8ab-121">**Ethernet II** (0)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-121">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="3e8ab-122">**Ethernet 802,3** (1)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-122">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="3e8ab-123">**Ethernet 802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-123">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="3e8ab-124">**Ajuste de Ethernet** (3)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-124">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="3e8ab-125">**Automático** (255)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-125">**AUTO** (255)</span></span>


<span data-ttu-id="3e8ab-126"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3e8ab-126"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="3e8ab-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e8ab-127">Return value</span></span>

<dl> <dt>

<span data-ttu-id="3e8ab-128">**Conclusão bem-sucedida, nenhuma reinicialização necessária** (0)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-128">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-129">**Conclusão bem-sucedida, reinicialização necessária** (1)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-129">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-130">**Método sem suporte nesta plataforma** (64)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-130">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-131">**Falha desconhecida** (65)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-131">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-132">**Máscara de sub-rede inválida** (66)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-132">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-133">**Ocorreu um erro ao processar uma instância que foi retornada** (67)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-133">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-134">**Parâmetro de entrada inválido** (68)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-134">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-135">**Mais de 5 gateways especificados** (69)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-135">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-136">**Endereço IP inválido** (70)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-136">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-137">**Endereço IP de gateway inválido** (71)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-137">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-138">**Ocorreu um erro ao acessar o registro para as informações solicitadas** (72)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-138">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-139">**Nome de domínio inválido** (73)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-139">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-140">**Nome de host inválido** (74)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-140">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-141">**Nenhum servidor WINS primário/secundário definido** (75)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-141">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-142">**Arquivo inválido** (76)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-142">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-143">**Caminho de sistema inválido** (77)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-143">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-144">**Falha na cópia do arquivo** (78)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-144">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-145">**Parâmetro de segurança inválido** (79)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-145">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-146">**Não é possível configurar o serviço TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-146">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-147">**Não é possível configurar o serviço DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-147">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-148">**Não é possível renovar a concessão DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-148">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-149">**Não é possível liberar a concessão DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-149">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-150">**IP não habilitado no adaptador** (84)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-150">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-151">**IPX não habilitado no adaptador** (85)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-151">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-152">**Erro de limites de número de quadro/rede** (86)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-152">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-153">**Tipo de quadro inválido** (87)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-153">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-154">**Número de rede inválido** (88)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-154">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-155">**Número de rede duplicado** (89)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-155">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-156">**Parâmetro fora dos limites** (90)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-156">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-157">**Acesso negado** (91)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-157">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-158">**Memória insuficiente** (92)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-158">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-159">**Já existe** (93)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-159">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-160">**Caminho, arquivo ou objeto não encontrado** (94)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-160">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-161">**Não é possível notificar o serviço** (95)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-161">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-162">**Não é possível notificar o serviço DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-162">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-163">**Interface não configurável** (97)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-163">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-164">**Nem todas as concessões DHCP puderam ser liberadas/renovadas** (98)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-164">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-165">**DHCP não habilitado no adaptador** (100)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-165">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="3e8ab-166">**Outro** (101 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="3e8ab-166">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3e8ab-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e8ab-167">Requirements</span></span>



| <span data-ttu-id="3e8ab-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e8ab-168">Requirement</span></span> | <span data-ttu-id="3e8ab-169">Valor</span><span class="sxs-lookup"><span data-stu-id="3e8ab-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e8ab-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e8ab-170">Minimum supported client</span></span><br/> | <span data-ttu-id="3e8ab-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e8ab-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e8ab-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e8ab-172">Minimum supported server</span></span><br/> | <span data-ttu-id="3e8ab-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e8ab-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e8ab-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e8ab-174">Namespace</span></span><br/>                | <span data-ttu-id="3e8ab-175">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3e8ab-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3e8ab-176">MOF</span><span class="sxs-lookup"><span data-stu-id="3e8ab-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e8ab-177"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e8ab-177"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e8ab-178">DLL</span><span class="sxs-lookup"><span data-stu-id="3e8ab-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e8ab-179"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e8ab-179"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e8ab-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e8ab-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e8ab-181">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="3e8ab-181">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




