---
title: Propriedade IVMAccountant DiskBytesWritten (VPCCOMInterfaces. h)
description: Número total de bytes gravados por todos os controladores de armazenamento para esta máquina virtual.
ms.assetid: a2a5730b-a411-48b8-aca8-d09cf09432a9
keywords:
- Propriedade DiskBytesWritten Virtual PC
- Propriedade DiskBytesWritten Virtual PC, interface IVMAccountant
- IVMAccountant interface virtual PC, Propriedade DiskBytesWritten
topic_type:
- apiref
api_name:
- IVMAccountant.DiskBytesWritten
- IVMAccountant.get_DiskBytesWritten
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e9ad27acf538af25daec676289df5e7664b169
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824759"
---
# <a name="ivmaccountantdiskbyteswritten-property"></a><span data-ttu-id="44ca9-106">IVMAccountant: Propriedade iskBytesWritten de:D</span><span class="sxs-lookup"><span data-stu-id="44ca9-106">IVMAccountant::DiskBytesWritten property</span></span>

<span data-ttu-id="44ca9-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="44ca9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="44ca9-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="44ca9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="44ca9-109">Recupera o número total de bytes gravados por todos os controladores de armazenamento para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="44ca9-109">Retrieves the total number of bytes written by all storage controllers for this virtual machine.</span></span>

<span data-ttu-id="44ca9-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="44ca9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="44ca9-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44ca9-111">Syntax</span></span>


```C++
HRESULT get_DiskBytesWritten(
  [out, retval] VARIANT *bytesWritten
);
```



## <a name="property-value"></a><span data-ttu-id="44ca9-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="44ca9-112">Property value</span></span>

<span data-ttu-id="44ca9-113">O número total de bytes.</span><span class="sxs-lookup"><span data-stu-id="44ca9-113">The total number of bytes.</span></span> <span data-ttu-id="44ca9-114">Esses dados são retornados como uma **variante** do tipo **VT \_ decimal**.</span><span class="sxs-lookup"><span data-stu-id="44ca9-114">This data is returned as a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="44ca9-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="44ca9-115">Error codes</span></span>



| <span data-ttu-id="44ca9-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="44ca9-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="44ca9-117">Significado</span><span class="sxs-lookup"><span data-stu-id="44ca9-117">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="44ca9-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="44ca9-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="44ca9-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="44ca9-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="44ca9-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="44ca9-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="44ca9-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="44ca9-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="44ca9-122"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="44ca9-122"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="44ca9-123">A máquina virtual não está em execução.</span><span class="sxs-lookup"><span data-stu-id="44ca9-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="44ca9-124"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="44ca9-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="44ca9-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="44ca9-125">An unexpected error has occurred.</span></span><br/>   |



## <a name="remarks"></a><span data-ttu-id="44ca9-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="44ca9-126">Remarks</span></span>

<span data-ttu-id="44ca9-127">Observe que as estatísticas de e/s de disco são redefinidas para zero quando uma máquina virtual é ligada, redefinida ou restaurada do estado salvo.</span><span class="sxs-lookup"><span data-stu-id="44ca9-127">Note that disk I/O statistics are reset to zero when a virtual machine is powered up, reset, or restored from saved state.</span></span>

## <a name="requirements"></a><span data-ttu-id="44ca9-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44ca9-128">Requirements</span></span>



| <span data-ttu-id="44ca9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="44ca9-129">Requirement</span></span> | <span data-ttu-id="44ca9-130">Valor</span><span class="sxs-lookup"><span data-stu-id="44ca9-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="44ca9-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44ca9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="44ca9-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="44ca9-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44ca9-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44ca9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="44ca9-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="44ca9-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="44ca9-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="44ca9-135">End of client support</span></span><br/>    | <span data-ttu-id="44ca9-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="44ca9-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="44ca9-137">Produto</span><span class="sxs-lookup"><span data-stu-id="44ca9-137">Product</span></span><br/>                  | <span data-ttu-id="44ca9-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="44ca9-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="44ca9-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44ca9-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="44ca9-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="44ca9-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="44ca9-141">IID</span><span class="sxs-lookup"><span data-stu-id="44ca9-141">IID</span></span><br/>                      | <span data-ttu-id="44ca9-142">IID \_ IVMAccountant é definido como 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="44ca9-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="44ca9-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="44ca9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ca9-144">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="44ca9-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

