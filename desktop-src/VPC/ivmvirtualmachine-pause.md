---
title: Método IVMVirtualMachine PAUSE (VPCCOMInterfaces. h)
description: Pausa a máquina virtual.
ms.assetid: 29ac40c4-7713-4782-8a31-42f2c32b8f7d
keywords:
- Pausar o método virtual PC
- Pausar método virtual PC, interface IVMVirtualMachine
- Virtual PC de interface IVMVirtualMachine, método pause
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Pause
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c953da05d34c999066a6bc87cb1f51983defbd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824594"
---
# <a name="ivmvirtualmachinepause-method"></a><span data-ttu-id="8f96c-106">IVMVirtualMachine: método ause de:P</span><span class="sxs-lookup"><span data-stu-id="8f96c-106">IVMVirtualMachine::Pause method</span></span>

<span data-ttu-id="8f96c-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8f96c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8f96c-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8f96c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8f96c-109">Pausa a VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="8f96c-109">Pauses the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f96c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f96c-110">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="8f96c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f96c-111">Parameters</span></span>

<span data-ttu-id="8f96c-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8f96c-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f96c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f96c-113">Return value</span></span>

<span data-ttu-id="8f96c-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8f96c-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8f96c-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8f96c-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="8f96c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f96c-116">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f96c-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8f96c-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="8f96c-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8f96c-118">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="8f96c-119"><dt>**E \_ FALHA**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="8f96c-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="8f96c-120">A VM já está pausada.</span><span class="sxs-lookup"><span data-stu-id="8f96c-120">The VM is already paused.</span></span><br/>                                         |
| <dl> <span data-ttu-id="8f96c-121"><dt>**HRESULT \_ DO \_ Win32 (erro de \_ acesso \_ negado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="8f96c-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="8f96c-122">O chamador deve ter permissões de acesso de execução para pausar essa VM.</span><span class="sxs-lookup"><span data-stu-id="8f96c-122">The caller must have execute access permissions to pause this VM.</span></span><br/> |
| <dl> <span data-ttu-id="8f96c-123"><dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="8f96c-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="8f96c-124">A operação não foi concluída oportunamente.</span><span class="sxs-lookup"><span data-stu-id="8f96c-124">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="8f96c-125"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="8f96c-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="8f96c-126">A máquina virtual não está em execução.</span><span class="sxs-lookup"><span data-stu-id="8f96c-126">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="8f96c-127"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8f96c-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="8f96c-128">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="8f96c-128">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="8f96c-129"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="8f96c-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="8f96c-130">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="8f96c-130">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="8f96c-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f96c-131">Remarks</span></span>

<span data-ttu-id="8f96c-132">**Pause** não salva o estado atual da VM.</span><span class="sxs-lookup"><span data-stu-id="8f96c-132">**Pause** does not save the current state of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f96c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f96c-133">Requirements</span></span>



| <span data-ttu-id="8f96c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f96c-134">Requirement</span></span> | <span data-ttu-id="8f96c-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8f96c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f96c-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f96c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8f96c-137">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8f96c-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8f96c-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f96c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8f96c-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8f96c-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8f96c-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8f96c-140">End of client support</span></span><br/>    | <span data-ttu-id="8f96c-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8f96c-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8f96c-142">Produto</span><span class="sxs-lookup"><span data-stu-id="8f96c-142">Product</span></span><br/>                  | <span data-ttu-id="8f96c-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8f96c-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8f96c-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f96c-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f96c-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f96c-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8f96c-146">IID</span><span class="sxs-lookup"><span data-stu-id="8f96c-146">IID</span></span><br/>                      | <span data-ttu-id="8f96c-147">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="8f96c-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="8f96c-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f96c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f96c-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="8f96c-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

