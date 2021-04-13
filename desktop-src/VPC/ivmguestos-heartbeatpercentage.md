---
title: Propriedade IVMGuestOS HeartbeatPercentage (VPCCOMInterfaces. h)
description: Porcentagem de pulsações esperadas recebidas no último minuto.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- Propriedade HeartbeatPercentage Virtual PC
- Propriedade HeartbeatPercentage Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade HeartbeatPercentage
topic_type:
- apiref
api_name:
- IVMGuestOS.HeartbeatPercentage
- IVMGuestOS.get_HeartbeatPercentage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22d568ed85281e8940b69afd1c72e76e2f208a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499715"
---
# <a name="ivmguestosheartbeatpercentage-property"></a><span data-ttu-id="6963a-106">Propriedade IVMGuestOS:: HeartbeatPercentage</span><span class="sxs-lookup"><span data-stu-id="6963a-106">IVMGuestOS::HeartbeatPercentage property</span></span>

<span data-ttu-id="6963a-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6963a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6963a-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6963a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6963a-109">Recupera a porcentagem de pulsações esperadas recebidas no último minuto.</span><span class="sxs-lookup"><span data-stu-id="6963a-109">Retrieves the percentage of expected heartbeats received over the past minute.</span></span>

<span data-ttu-id="6963a-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="6963a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6963a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6963a-111">Syntax</span></span>


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a><span data-ttu-id="6963a-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6963a-112">Property value</span></span>

<span data-ttu-id="6963a-113">A porcentagem de pulsações esperadas recebidas no último minuto.</span><span class="sxs-lookup"><span data-stu-id="6963a-113">The percentage of expected heartbeats received over the past minute.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6963a-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6963a-114">Error codes</span></span>



| <span data-ttu-id="6963a-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="6963a-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="6963a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="6963a-116">Meaning</span></span>                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6963a-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6963a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="6963a-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6963a-118">The operation was successful.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="6963a-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="6963a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="6963a-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6963a-120">The parameter is **NULL**.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="6963a-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6963a-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="6963a-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="6963a-122">The configuration is unknown.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="6963a-123"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="6963a-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="6963a-124">A máquina virtual (VM) deve estar em execução para esta operação.</span><span class="sxs-lookup"><span data-stu-id="6963a-124">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="6963a-125"><dt>VM \_ E \_ adições \_ não \_ </dt> <dt>0xA0040504</dt> disp.</span><span class="sxs-lookup"><span data-stu-id="6963a-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="6963a-126">A VM não está totalmente inicializada, o recurso componentes de integração não está instalado ou a versão instalada não oferece suporte a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="6963a-126">The VM is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="6963a-127"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="6963a-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="6963a-128">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="6963a-128">An unexpected error has occurred.</span></span><br/>                                                                                                        |



## <a name="remarks"></a><span data-ttu-id="6963a-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="6963a-129">Remarks</span></span>

<span data-ttu-id="6963a-130">Os componentes de integração enviarão uma pulsação periódica para o Windows Virtual PC enquanto o sistema operacional convidado estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="6963a-130">Integration components will send a periodic heartbeat to Windows Virtual PC while the guest operating system is running.</span></span> <span data-ttu-id="6963a-131">Se o sistema operacional convidado estiver muito carregado, será possível que o Windows Virtual PC receba menos pulsações do que o esperado.</span><span class="sxs-lookup"><span data-stu-id="6963a-131">If the guest operating system is heavily loaded, it's possible that Windows Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="6963a-132">Se a porcentagem de pulsação cair para zero, é possível que o sistema operacional convidado não esteja respondendo ou tenha falhado.</span><span class="sxs-lookup"><span data-stu-id="6963a-132">If the heartbeat percentage drops to zero, it is possible that the guest operating system is not responding or is crashed.</span></span> <span data-ttu-id="6963a-133">A máquina virtual deve estar em execução (ou seja, totalmente inicializada e não desligada) e os componentes de integração devem ser instalados quando essa propriedade é chamada.</span><span class="sxs-lookup"><span data-stu-id="6963a-133">The virtual machine must be running (that is, fully booted and not shutting down) and integration components must be installed when this property is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="6963a-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6963a-134">Requirements</span></span>



| <span data-ttu-id="6963a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6963a-135">Requirement</span></span> | <span data-ttu-id="6963a-136">Valor</span><span class="sxs-lookup"><span data-stu-id="6963a-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6963a-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6963a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6963a-138">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6963a-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6963a-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6963a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6963a-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6963a-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6963a-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6963a-141">End of client support</span></span><br/>    | <span data-ttu-id="6963a-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6963a-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6963a-143">Produto</span><span class="sxs-lookup"><span data-stu-id="6963a-143">Product</span></span><br/>                  | <span data-ttu-id="6963a-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6963a-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6963a-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6963a-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6963a-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6963a-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6963a-147">IID</span><span class="sxs-lookup"><span data-stu-id="6963a-147">IID</span></span><br/>                      | <span data-ttu-id="6963a-148">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="6963a-148">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6963a-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="6963a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6963a-150">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="6963a-150">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

