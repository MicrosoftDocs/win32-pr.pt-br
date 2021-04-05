---
title: Método IVMVirtualPC FindVirtualMachine (VPCCOMInterfaces. h)
description: Recupera um objeto de máquina virtual que corresponde à configuração solicitada.
ms.assetid: 1c73d6f7-5662-485e-a864-e8e48197f8e4
keywords:
- FindVirtualMachine do método virtual PC
- Método FindVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método FindVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e5702738e16fa7b4f4a263264b0574966d1fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086063"
---
# <a name="ivmvirtualpcfindvirtualmachine-method"></a><span data-ttu-id="ec523-106">Método IVMVirtualPC:: FindVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ec523-106">IVMVirtualPC::FindVirtualMachine method</span></span>

<span data-ttu-id="ec523-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ec523-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ec523-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ec523-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ec523-109">Recupera um objeto de máquina virtual que corresponde à configuração solicitada.</span><span class="sxs-lookup"><span data-stu-id="ec523-109">Retrieves a virtual machine object that matches the requested configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec523-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec523-110">Syntax</span></span>


```C++
HRESULT FindVirtualMachine(
  [in]          BSTR              configurationName,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="ec523-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec523-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec523-112">*ConfigurationName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec523-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec523-113">O nome da máquina virtual a ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="ec523-113">The name of the virtual machine to be found.</span></span>

</dd> <dt>

<span data-ttu-id="ec523-114">*VirtualMachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ec523-114">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ec523-115">Um ponteiro para um novo objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ec523-115">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec523-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ec523-116">Return value</span></span>

<span data-ttu-id="ec523-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ec523-117">This method can return one of these values.</span></span>



| <span data-ttu-id="ec523-118">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ec523-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="ec523-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec523-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec523-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ec523-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="ec523-121">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ec523-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ec523-122"><dt>**S \_ FALSO**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ec523-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="ec523-123">Não foi possível encontrar a configuração especificada.</span><span class="sxs-lookup"><span data-stu-id="ec523-123">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="ec523-124"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="ec523-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="ec523-125">O parâmetro *ConfigurationName* é inválido ou *VirtualMachine* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ec523-125">The *configurationName* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="ec523-126"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="ec523-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="ec523-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="ec523-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="ec523-128"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ec523-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="ec523-129">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="ec523-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ec523-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec523-130">Remarks</span></span>

<span data-ttu-id="ec523-131">Os nomes de máquina virtual não diferenciam maiúsculas de minúsculas, por exemplo, "MyVM" e "MyVM" referem-se à mesma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ec523-131">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec523-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec523-132">Requirements</span></span>



| <span data-ttu-id="ec523-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec523-133">Requirement</span></span> | <span data-ttu-id="ec523-134">Valor</span><span class="sxs-lookup"><span data-stu-id="ec523-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec523-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec523-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ec523-136">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ec523-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ec523-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec523-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ec523-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ec523-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ec523-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ec523-139">End of client support</span></span><br/>    | <span data-ttu-id="ec523-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ec523-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ec523-141">Produto</span><span class="sxs-lookup"><span data-stu-id="ec523-141">Product</span></span><br/>                  | <span data-ttu-id="ec523-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ec523-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ec523-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec523-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec523-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec523-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ec523-145">IID</span><span class="sxs-lookup"><span data-stu-id="ec523-145">IID</span></span><br/>                      | <span data-ttu-id="ec523-146">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="ec523-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ec523-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec523-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec523-148">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="ec523-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

