---
title: Propriedade IVMVirtualMachine RdpPipeName (VPCCOMInterfaces. h)
description: Recupera o nome da conexão RDP chamada pipe usado para vídeo e entrada.
ms.assetid: 0c2d0f23-40cd-4a86-96dd-546fb3570871
keywords:
- Propriedade RdpPipeName Virtual PC
- Propriedade RdpPipeName Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade RdpPipeName
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RdpPipeName
- IVMVirtualMachine.get_RdpPipeName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86e49463c5e443a07d1fa86736047435eaf60a06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008803"
---
# <a name="ivmvirtualmachinerdppipename-property"></a><span data-ttu-id="33c83-106">Propriedade IVMVirtualMachine:: RdpPipeName</span><span class="sxs-lookup"><span data-stu-id="33c83-106">IVMVirtualMachine::RdpPipeName property</span></span>

<span data-ttu-id="33c83-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="33c83-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="33c83-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="33c83-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="33c83-109">Recupera o nome da conexão RDP chamada pipe usado para vídeo e entrada.</span><span class="sxs-lookup"><span data-stu-id="33c83-109">Retrieves the name of the RDP connection named pipe used for video and input.</span></span>

<span data-ttu-id="33c83-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="33c83-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="33c83-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33c83-111">Syntax</span></span>


```C++
HRESULT get_RdpPipeName(
  [out, retval] BSTR *RdpPipeName
);
```



## <a name="property-value"></a><span data-ttu-id="33c83-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="33c83-112">Property value</span></span>

<span data-ttu-id="33c83-113">Nome da conexão RDP chamada pipe usado para vídeo e entrada.</span><span class="sxs-lookup"><span data-stu-id="33c83-113">Name of the RDP connection named pipe used for video and input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="33c83-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="33c83-114">Error codes</span></span>

<span data-ttu-id="33c83-115">Se o método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="33c83-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33c83-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33c83-116">Otherwise, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="33c83-117">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="33c83-117">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="33c83-118">Significado</span><span class="sxs-lookup"><span data-stu-id="33c83-118">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="33c83-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="33c83-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="33c83-120">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="33c83-120">The operation was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="33c83-121"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="33c83-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="33c83-122">O parâmetro RdpPipeName é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="33c83-122">The RdpPipeName parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="33c83-123"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="33c83-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="33c83-124">A máquina virtual não está em execução.</span><span class="sxs-lookup"><span data-stu-id="33c83-124">The virtual machine is not running.</span></span><br/>    |
| <dl> <span data-ttu-id="33c83-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="33c83-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="33c83-126">Erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="33c83-126">An unknown error occurred.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="33c83-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33c83-127">Requirements</span></span>



| <span data-ttu-id="33c83-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="33c83-128">Requirement</span></span> | <span data-ttu-id="33c83-129">Valor</span><span class="sxs-lookup"><span data-stu-id="33c83-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c83-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33c83-130">Minimum supported client</span></span><br/> | <span data-ttu-id="33c83-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="33c83-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33c83-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33c83-132">Minimum supported server</span></span><br/> | <span data-ttu-id="33c83-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="33c83-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="33c83-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="33c83-134">End of client support</span></span><br/>    | <span data-ttu-id="33c83-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="33c83-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="33c83-136">Produto</span><span class="sxs-lookup"><span data-stu-id="33c83-136">Product</span></span><br/>                  | <span data-ttu-id="33c83-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="33c83-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="33c83-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33c83-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="33c83-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="33c83-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="33c83-140">IID</span><span class="sxs-lookup"><span data-stu-id="33c83-140">IID</span></span><br/>                      | <span data-ttu-id="33c83-141">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="33c83-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="33c83-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="33c83-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c83-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="33c83-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

