---
title: Propriedade ispulsation IVMGuestOS (VPCCOMInterfaces. h)
description: Determina se a máquina virtual tem uma pulsação.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- PC virtual de propriedade ispulsação
- Propriedade ispulsação Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, ispulsação de propriedade
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faad446749cbf3cdb75d6e8fa7469022cc004ea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105783720"
---
# <a name="ivmguestosisheartbeating-property"></a><span data-ttu-id="66503-106">Propriedade IVMGuestOS:: ispulsação</span><span class="sxs-lookup"><span data-stu-id="66503-106">IVMGuestOS::IsHeartbeating property</span></span>

<span data-ttu-id="66503-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="66503-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="66503-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="66503-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="66503-109">Determina se a máquina virtual tem uma pulsação.</span><span class="sxs-lookup"><span data-stu-id="66503-109">Determines whether the virtual machine has a heartbeat.</span></span>

<span data-ttu-id="66503-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="66503-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="66503-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66503-111">Syntax</span></span>


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a><span data-ttu-id="66503-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="66503-112">Property value</span></span>

<span data-ttu-id="66503-113">**Variante \_ TRUE** se uma pulsação for detectada, **variante \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="66503-113">**VARIANT\_TRUE** if a heartbeat is detected, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="66503-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="66503-114">Error codes</span></span>



| <span data-ttu-id="66503-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="66503-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="66503-116">Significado</span><span class="sxs-lookup"><span data-stu-id="66503-116">Meaning</span></span>                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="66503-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="66503-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="66503-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="66503-118">The operation was successful.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="66503-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="66503-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="66503-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="66503-120">The parameter is **NULL**.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="66503-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="66503-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="66503-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="66503-122">The configuration is unknown.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="66503-123"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="66503-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="66503-124">A máquina virtual deve estar em execução para esta operação.</span><span class="sxs-lookup"><span data-stu-id="66503-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="66503-125"><dt>VM \_ E \_ adições \_ não \_ </dt> <dt>0xA0040504</dt> disp.</span><span class="sxs-lookup"><span data-stu-id="66503-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="66503-126">A máquina virtual não está totalmente inicializada, o recurso componentes de integração não está instalado ou a versão instalada não oferece suporte a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="66503-126">The virtual machine is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="66503-127"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="66503-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="66503-128">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="66503-128">An unexpected error has occurred.</span></span><br/>                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="66503-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="66503-129">Remarks</span></span>

<span data-ttu-id="66503-130">Quando os componentes de integração são instalados no sistema operacional convidado, um ' tique ' regular ou pulsação é enviado da sessão de máquina virtual para o Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="66503-130">When integration components is installed in the guest operating system, a regular 'tick' or heartbeat is sent from the virtual machine session to Windows Virtual PC.</span></span> <span data-ttu-id="66503-131">Se o sistema operacional convidado estiver muito carregado, será possível que o Virtual PC receba menos pulsações do que o esperado.</span><span class="sxs-lookup"><span data-stu-id="66503-131">If the guest operating system is heavily loaded, it's possible that Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="66503-132">Se nenhuma pulsação for detectada, é possível que o sistema operacional convidado não esteja respondendo ou tenha falhado.</span><span class="sxs-lookup"><span data-stu-id="66503-132">If no heartbeat is detected, it is possible that the guest operating system is not responding or is crashed.</span></span>

<span data-ttu-id="66503-133">Por padrão, uma máquina virtual produz dez tiques de pulsação por minuto.</span><span class="sxs-lookup"><span data-stu-id="66503-133">By default, a virtual machine produces ten heartbeat ticks per minute.</span></span> <span data-ttu-id="66503-134">Se nenhuma marcação de pulsação for detectada por um minuto inteiro, o Windows Virtual PC tentará reiniciar a sessão da máquina virtual uma vez a cada dez segundos por até dois minutos.</span><span class="sxs-lookup"><span data-stu-id="66503-134">If no heartbeat ticks are detected for an entire minute, Windows Virtual PC will attempt to restart the virtual machine session once every ten seconds for up to two minutes.</span></span> <span data-ttu-id="66503-135">Esse comportamento é controlado pelos seguintes valores de chave no arquivo de configuração da sessão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="66503-135">This behavior is controlled by the following key values in the virtual machine session's configuration file.</span></span>



| <span data-ttu-id="66503-136">Chave de configuração</span><span class="sxs-lookup"><span data-stu-id="66503-136">Configuration key</span></span>                                            | <span data-ttu-id="66503-137">Padrão</span><span class="sxs-lookup"><span data-stu-id="66503-137">Default</span></span>       | <span data-ttu-id="66503-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="66503-138">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66503-139">integração/Microsoft/pulsação/tempo</span><span class="sxs-lookup"><span data-stu-id="66503-139">integration/microsoft/heartbeat/time</span></span><br/>              | <span data-ttu-id="66503-140">60</span><span class="sxs-lookup"><span data-stu-id="66503-140">60</span></span><br/> | <span data-ttu-id="66503-141">O comprimento do bloco de tempo usado para gerar tiques de pulsação, em em segundos.</span><span class="sxs-lookup"><span data-stu-id="66503-141">The length of the block of time used to generate heartbeat ticks, in in seconds.</span></span><br/>                                             |
| <span data-ttu-id="66503-142">integração/Microsoft/pulsação/taxa</span><span class="sxs-lookup"><span data-stu-id="66503-142">integration/microsoft/heartbeat/rate</span></span><br/>              | <span data-ttu-id="66503-143">10</span><span class="sxs-lookup"><span data-stu-id="66503-143">10</span></span><br/> | <span data-ttu-id="66503-144">O número de tiques gerados em cada bloco de tempo de pulsação.</span><span class="sxs-lookup"><span data-stu-id="66503-144">The number of ticks generated in each heartbeat time block.</span></span><br/>                                                                  |
| <span data-ttu-id="66503-145">integração/Microsoft/intervalo de pulsação/falha \_</span><span class="sxs-lookup"><span data-stu-id="66503-145">integration/microsoft/heartbeat/failure\_interval</span></span><br/> | <span data-ttu-id="66503-146">10</span><span class="sxs-lookup"><span data-stu-id="66503-146">10</span></span><br/> | <span data-ttu-id="66503-147">O número de segundos entre as tentativas de reinicialização, uma vez que nenhuma marcação de pulsação é recebida dentro de um bloco de tempo de pulsação específico.</span><span class="sxs-lookup"><span data-stu-id="66503-147">The number of seconds between restart attempts, once no heartbeat ticks are received within a specific heartbeat time block.</span></span><br/> |
| <span data-ttu-id="66503-148">integração/Microsoft/falhas de pulsação \_ /falha</span><span class="sxs-lookup"><span data-stu-id="66503-148">integration/microsoft/heartbeat/failure\_attempts</span></span><br/> | <span data-ttu-id="66503-149">12</span><span class="sxs-lookup"><span data-stu-id="66503-149">12</span></span><br/> | <span data-ttu-id="66503-150">O número de tentativas de reinicialização feitas.</span><span class="sxs-lookup"><span data-stu-id="66503-150">The number of restart attempts made.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="66503-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66503-151">Requirements</span></span>



| <span data-ttu-id="66503-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="66503-152">Requirement</span></span> | <span data-ttu-id="66503-153">Valor</span><span class="sxs-lookup"><span data-stu-id="66503-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="66503-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66503-154">Minimum supported client</span></span><br/> | <span data-ttu-id="66503-155">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="66503-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66503-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66503-156">Minimum supported server</span></span><br/> | <span data-ttu-id="66503-157">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="66503-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="66503-158">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="66503-158">End of client support</span></span><br/>    | <span data-ttu-id="66503-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="66503-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="66503-160">Produto</span><span class="sxs-lookup"><span data-stu-id="66503-160">Product</span></span><br/>                  | <span data-ttu-id="66503-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="66503-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="66503-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66503-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="66503-163"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="66503-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="66503-164">IID</span><span class="sxs-lookup"><span data-stu-id="66503-164">IID</span></span><br/>                      | <span data-ttu-id="66503-165">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="66503-165">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="66503-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="66503-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66503-167">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="66503-167">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

