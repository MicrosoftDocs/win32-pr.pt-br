---
title: Método IVMKeyboard TypeAsciiText (VPCCOMInterfaces. h)
description: Simula uma série de chaves ASCII que estão sendo digitadas no convidado.
ms.assetid: 6c7fbfed-d495-4f11-a7d1-dc08bd075870
keywords:
- TypeAsciiText do método virtual PC
- Método TypeAsciiText Virtual PC, interface IVMKeyboard
- IVMKeyboard interface virtual PC, método TypeAsciiText
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeAsciiText
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538df9fc3036e43dc36f4ca7425688157e9fca77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085753"
---
# <a name="ivmkeyboardtypeasciitext-method"></a><span data-ttu-id="91e77-106">Método IVMKeyboard:: TypeAsciiText</span><span class="sxs-lookup"><span data-stu-id="91e77-106">IVMKeyboard::TypeAsciiText method</span></span>

<span data-ttu-id="91e77-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="91e77-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="91e77-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="91e77-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="91e77-109">Simula uma série de chaves ASCII que estão sendo digitadas no convidado.</span><span class="sxs-lookup"><span data-stu-id="91e77-109">Simulates a series of ASCII keys being typed into the guest.</span></span>

## <a name="syntax"></a><span data-ttu-id="91e77-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91e77-110">Syntax</span></span>


```C++
HRESULT TypeAsciiText(
  [in] BSTR text
);
```



## <a name="parameters"></a><span data-ttu-id="91e77-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91e77-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91e77-112">*texto* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="91e77-112">*text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91e77-113">A cadeia de caracteres de texto ASCII a ser digitada na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91e77-113">The ASCII text string to be typed inside the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91e77-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91e77-114">Return value</span></span>

<span data-ttu-id="91e77-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="91e77-115">This method can return one of these values.</span></span>



| <span data-ttu-id="91e77-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="91e77-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="91e77-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="91e77-117">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="91e77-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="91e77-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="91e77-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="91e77-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="91e77-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="91e77-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="91e77-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="91e77-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="91e77-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="91e77-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="91e77-123">A cadeia de caracteres especificada está vazia.</span><span class="sxs-lookup"><span data-stu-id="91e77-123">The specified string is empty.</span></span><br/>    |
| <dl> <span data-ttu-id="91e77-124"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="91e77-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="91e77-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="91e77-125">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="91e77-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91e77-126">Requirements</span></span>



| <span data-ttu-id="91e77-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="91e77-127">Requirement</span></span> | <span data-ttu-id="91e77-128">Valor</span><span class="sxs-lookup"><span data-stu-id="91e77-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91e77-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91e77-129">Minimum supported client</span></span><br/> | <span data-ttu-id="91e77-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="91e77-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91e77-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91e77-131">Minimum supported server</span></span><br/> | <span data-ttu-id="91e77-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="91e77-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="91e77-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="91e77-133">End of client support</span></span><br/>    | <span data-ttu-id="91e77-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="91e77-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="91e77-135">Produto</span><span class="sxs-lookup"><span data-stu-id="91e77-135">Product</span></span><br/>                  | <span data-ttu-id="91e77-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="91e77-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="91e77-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91e77-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="91e77-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="91e77-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="91e77-139">IID</span><span class="sxs-lookup"><span data-stu-id="91e77-139">IID</span></span><br/>                      | <span data-ttu-id="91e77-140">IID \_ IVMKeyboard é definido como 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="91e77-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="91e77-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="91e77-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91e77-142">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="91e77-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

