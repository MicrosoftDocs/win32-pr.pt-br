---
title: Método de retomada IVMVirtualMachine (VPCCOMInterfaces. h)
description: Retoma a VM.
ms.assetid: 4a2d6b64-8dcf-484e-940d-b0180aba9f01
keywords:
- Método de retomada Virtual PC
- Método de retomada Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método resume
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Resume
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c24af1e1a00aa0fa29acc077faf48287c0307414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824650"
---
# <a name="ivmvirtualmachineresume-method"></a><span data-ttu-id="9f875-106">Método IVMVirtualMachine:: resume</span><span class="sxs-lookup"><span data-stu-id="9f875-106">IVMVirtualMachine::Resume method</span></span>

<span data-ttu-id="9f875-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9f875-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9f875-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9f875-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9f875-109">Retoma a VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="9f875-109">Resumes the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f875-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f875-110">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="9f875-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f875-111">Parameters</span></span>

<span data-ttu-id="9f875-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9f875-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f875-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f875-113">Return value</span></span>

<span data-ttu-id="9f875-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="9f875-114">This method can return one of these values.</span></span>



| <span data-ttu-id="9f875-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9f875-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="9f875-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f875-116">Description</span></span>                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9f875-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9f875-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="9f875-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9f875-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="9f875-119"><dt>**E \_ FALHA**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="9f875-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="9f875-120">A VM não está pausada.</span><span class="sxs-lookup"><span data-stu-id="9f875-120">The VM is not paused.</span></span><br/>                                              |
| <dl> <span data-ttu-id="9f875-121"><dt>**HRESULT \_ DO \_ Win32 (erro de \_ acesso \_ negado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="9f875-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="9f875-122">O chamador deve ter permissões de acesso de execução para retomar essa VM.</span><span class="sxs-lookup"><span data-stu-id="9f875-122">The caller must have execute access permissions to resume this VM.</span></span><br/> |
| <dl> <span data-ttu-id="9f875-123"><dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="9f875-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="9f875-124">A operação não foi concluída oportunamente.</span><span class="sxs-lookup"><span data-stu-id="9f875-124">The operation did not complete in a timely manner.</span></span><br/>                 |
| <dl> <span data-ttu-id="9f875-125"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="9f875-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="9f875-126">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="9f875-126">The VM is not running.</span></span><br/>                                             |
| <dl> <span data-ttu-id="9f875-127"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9f875-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="9f875-128">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="9f875-128">The configuration is unknown.</span></span><br/>                                      |
| <dl> <span data-ttu-id="9f875-129"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="9f875-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="9f875-130">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="9f875-130">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="9f875-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f875-131">Requirements</span></span>



| <span data-ttu-id="9f875-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f875-132">Requirement</span></span> | <span data-ttu-id="9f875-133">Valor</span><span class="sxs-lookup"><span data-stu-id="9f875-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f875-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f875-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9f875-135">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9f875-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9f875-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f875-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9f875-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9f875-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9f875-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="9f875-138">End of client support</span></span><br/>    | <span data-ttu-id="9f875-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9f875-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9f875-140">Produto</span><span class="sxs-lookup"><span data-stu-id="9f875-140">Product</span></span><br/>                  | <span data-ttu-id="9f875-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9f875-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9f875-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f875-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f875-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f875-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9f875-144">IID</span><span class="sxs-lookup"><span data-stu-id="9f875-144">IID</span></span><br/>                      | <span data-ttu-id="9f875-145">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="9f875-145">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="9f875-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f875-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f875-147">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="9f875-147">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

