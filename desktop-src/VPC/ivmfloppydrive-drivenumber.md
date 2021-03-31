---
title: Propriedade IVMFloppyDrive DriveNumber (VPCCOMInterfaces. h)
description: Recupera o índice de base zero do controlador ao qual a unidade de disquete está anexada.
ms.assetid: 79a40cad-d280-4c67-9214-0532569e47e4
keywords:
- Propriedade DriveNumber Virtual PC
- Propriedade DriveNumber Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface virtual PC, Propriedade DriveNumber
topic_type:
- apiref
api_name:
- IVMFloppyDrive.DriveNumber
- IVMFloppyDrive.get_DriveNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2f2aeacaf3067515e9e44c58422cd4c9f31fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824484"
---
# <a name="ivmfloppydrivedrivenumber-property"></a><span data-ttu-id="32d3e-106">IVMFloppyDrive: Propriedade riveNumber de:D</span><span class="sxs-lookup"><span data-stu-id="32d3e-106">IVMFloppyDrive::DriveNumber property</span></span>

<span data-ttu-id="32d3e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="32d3e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="32d3e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="32d3e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="32d3e-109">Recupera o índice de base zero do controlador ao qual a unidade de disquete está anexada.</span><span class="sxs-lookup"><span data-stu-id="32d3e-109">Retrieves the zero-based index of the controller to which the floppy drive is attached.</span></span>

<span data-ttu-id="32d3e-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="32d3e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="32d3e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32d3e-111">Syntax</span></span>


```C++
HRESULT get_DriveNumber(
  [out, retval] long *driveNumber
);
```



## <a name="property-value"></a><span data-ttu-id="32d3e-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="32d3e-112">Property value</span></span>

<span data-ttu-id="32d3e-113">O índice de base zero do controlador.</span><span class="sxs-lookup"><span data-stu-id="32d3e-113">The zero-based index of the controller.</span></span>

## <a name="error-codes"></a><span data-ttu-id="32d3e-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="32d3e-114">Error codes</span></span>



| <span data-ttu-id="32d3e-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="32d3e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="32d3e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="32d3e-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="32d3e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="32d3e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="32d3e-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="32d3e-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="32d3e-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="32d3e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="32d3e-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="32d3e-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="32d3e-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="32d3e-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="32d3e-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="32d3e-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="32d3e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32d3e-123">Requirements</span></span>



| <span data-ttu-id="32d3e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="32d3e-124">Requirement</span></span> | <span data-ttu-id="32d3e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="32d3e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="32d3e-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32d3e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="32d3e-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="32d3e-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32d3e-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32d3e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="32d3e-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="32d3e-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="32d3e-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="32d3e-130">End of client support</span></span><br/>    | <span data-ttu-id="32d3e-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="32d3e-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="32d3e-132">Produto</span><span class="sxs-lookup"><span data-stu-id="32d3e-132">Product</span></span><br/>                  | <span data-ttu-id="32d3e-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="32d3e-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="32d3e-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32d3e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="32d3e-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="32d3e-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="32d3e-136">IID</span><span class="sxs-lookup"><span data-stu-id="32d3e-136">IID</span></span><br/>                      | <span data-ttu-id="32d3e-137">IID \_ IVMFloppyDrive é definido como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="32d3e-137">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="32d3e-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="32d3e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32d3e-139">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="32d3e-139">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

