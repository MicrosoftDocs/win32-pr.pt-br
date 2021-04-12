---
title: Método de redefinição de IVMVirtualMachine (VPCCOMInterfaces. h)
description: Redefine a máquina virtual.
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- Redefinir o método virtual PC
- Método Reset Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, redefinir método
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45314eef6d837ac00647d477f3652b63221d977c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455689"
---
# <a name="ivmvirtualmachinereset-method"></a><span data-ttu-id="5e309-106">Método IVMVirtualMachine:: Reset</span><span class="sxs-lookup"><span data-stu-id="5e309-106">IVMVirtualMachine::Reset method</span></span>

<span data-ttu-id="5e309-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5e309-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5e309-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5e309-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5e309-109">Redefine a VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="5e309-109">Resets the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e309-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e309-110">Syntax</span></span>


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a><span data-ttu-id="5e309-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e309-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e309-112">*resetTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5e309-112">*resetTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5e309-113">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar o progresso de conclusão da sequência de redefinição da VM.</span><span class="sxs-lookup"><span data-stu-id="5e309-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's reset sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e309-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e309-114">Return value</span></span>

<span data-ttu-id="5e309-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="5e309-115">This method can return one of these values.</span></span>



| <span data-ttu-id="5e309-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5e309-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="5e309-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e309-117">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e309-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5e309-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="5e309-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5e309-119">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="5e309-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="5e309-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="5e309-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5e309-121">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="5e309-122"><dt>**HRESULT \_ DO \_ Win32 (erro de \_ acesso \_ negado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="5e309-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="5e309-123">O chamador deve ter permissões de acesso de execução para redefinir esta VM.</span><span class="sxs-lookup"><span data-stu-id="5e309-123">The caller must have execute access permissions to reset this VM.</span></span><br/> |
| <dl> <span data-ttu-id="5e309-124"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="5e309-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="5e309-125">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="5e309-125">The VM is not running.</span></span><br/>                                            |
| <dl> <span data-ttu-id="5e309-126"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5e309-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="5e309-127">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="5e309-127">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="5e309-128"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="5e309-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="5e309-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="5e309-129">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="5e309-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e309-130">Requirements</span></span>



| <span data-ttu-id="5e309-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e309-131">Requirement</span></span> | <span data-ttu-id="5e309-132">Valor</span><span class="sxs-lookup"><span data-stu-id="5e309-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e309-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e309-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5e309-134">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5e309-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e309-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e309-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5e309-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5e309-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5e309-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="5e309-137">End of client support</span></span><br/>    | <span data-ttu-id="5e309-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5e309-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5e309-139">Produto</span><span class="sxs-lookup"><span data-stu-id="5e309-139">Product</span></span><br/>                  | <span data-ttu-id="5e309-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5e309-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5e309-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e309-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e309-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e309-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5e309-143">IID</span><span class="sxs-lookup"><span data-stu-id="5e309-143">IID</span></span><br/>                      | <span data-ttu-id="5e309-144">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="5e309-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="5e309-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e309-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e309-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="5e309-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

