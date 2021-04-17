---
title: Método de _ID IVMParallelPort (VPCCOMInterfaces. h)
description: Recupera o identificador interno da porta paralela.
ms.assetid: a0de74da-0e23-489e-8a89-8deba974e548
keywords:
- _ID o método virtual PC
- _ID método virtual PC, interface IVMParallelPort
- IVMParallelPort interface virtual PC, método de _ID
topic_type:
- apiref
api_name:
- IVMParallelPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 267061204ea92dd8f5cae37fc5cb279e7dc2b010
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763181"
---
# <a name="ivmparallelport_id-method"></a><span data-ttu-id="eb7b0-106">Método IVMParallelPort:: \_ ID</span><span class="sxs-lookup"><span data-stu-id="eb7b0-106">IVMParallelPort::\_ID method</span></span>

<span data-ttu-id="eb7b0-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="eb7b0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="eb7b0-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="eb7b0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="eb7b0-109">Recupera o identificador interno da porta paralela.</span><span class="sxs-lookup"><span data-stu-id="eb7b0-109">Retrieves the internal identifier of the parallel port.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb7b0-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb7b0-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a><span data-ttu-id="eb7b0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb7b0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb7b0-112">*portaid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="eb7b0-112">*portID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb7b0-113">O identificador de porta paralela.</span><span class="sxs-lookup"><span data-stu-id="eb7b0-113">The parallel port identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb7b0-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb7b0-114">Return value</span></span>

<span data-ttu-id="eb7b0-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="eb7b0-115">This method can return one of these values.</span></span>



| <span data-ttu-id="eb7b0-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="eb7b0-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="eb7b0-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb7b0-117">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="eb7b0-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eb7b0-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="eb7b0-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="eb7b0-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="eb7b0-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="eb7b0-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="eb7b0-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="eb7b0-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="eb7b0-122"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="eb7b0-122"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="eb7b0-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="eb7b0-123">An unexpected error has occurred.</span></span><br/>                        |
| <dl> <span data-ttu-id="eb7b0-124"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="eb7b0-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="eb7b0-125">A configuração desta máquina virtual não é válida.</span><span class="sxs-lookup"><span data-stu-id="eb7b0-125">The configuration for this virtual machine is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eb7b0-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb7b0-126">Remarks</span></span>

<span data-ttu-id="eb7b0-127">Essa propriedade não pode ser usada por linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="eb7b0-127">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb7b0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb7b0-128">Requirements</span></span>



| <span data-ttu-id="eb7b0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb7b0-129">Requirement</span></span> | <span data-ttu-id="eb7b0-130">Valor</span><span class="sxs-lookup"><span data-stu-id="eb7b0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb7b0-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb7b0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="eb7b0-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="eb7b0-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eb7b0-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb7b0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="eb7b0-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eb7b0-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="eb7b0-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="eb7b0-135">End of client support</span></span><br/>    | <span data-ttu-id="eb7b0-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eb7b0-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="eb7b0-137">Produto</span><span class="sxs-lookup"><span data-stu-id="eb7b0-137">Product</span></span><br/>                  | <span data-ttu-id="eb7b0-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="eb7b0-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="eb7b0-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb7b0-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb7b0-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb7b0-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="eb7b0-141">IID</span><span class="sxs-lookup"><span data-stu-id="eb7b0-141">IID</span></span><br/>                      | <span data-ttu-id="eb7b0-142">IID \_ IVMParallelPort é definido como 097beecb-0a02-474f-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="eb7b0-142">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="eb7b0-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb7b0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb7b0-144">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="eb7b0-144">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> </dl>

 

