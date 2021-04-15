---
title: Método de _GenerateThumbnail IVMDisplay (VPCCOMInterfaces. h)
description: Recupera uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual. | Método de _GenerateThumbnail IVMDisplay (VPCCOMInterfaces. h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- _GenerateThumbnail o método virtual PC
- _GenerateThumbnail método virtual PC, interface IVMDisplay
- IVMDisplay interface virtual PC, método de _GenerateThumbnail
topic_type:
- apiref
api_name:
- IVMDisplay._GenerateThumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4084549de96330761bca4f4ec6da65ca150c96e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105747502"
---
# <a name="ivmdisplay_generatethumbnail-method"></a><span data-ttu-id="b5d34-107">Método IVMDisplay:: \_ GenerateThumbnail</span><span class="sxs-lookup"><span data-stu-id="b5d34-107">IVMDisplay::\_GenerateThumbnail method</span></span>

<span data-ttu-id="b5d34-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b5d34-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b5d34-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b5d34-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b5d34-110">Recupera uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b5d34-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d34-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5d34-111">Syntax</span></span>


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a><span data-ttu-id="b5d34-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5d34-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5d34-113">*thumbnailImage* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b5d34-113">*thumbnailImage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d34-114">A matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b5d34-114">The array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5d34-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5d34-115">Return value</span></span>

<span data-ttu-id="b5d34-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b5d34-116">This method can return one of these values.</span></span>



| <span data-ttu-id="b5d34-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b5d34-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="b5d34-118">Description</span><span class="sxs-lookup"><span data-stu-id="b5d34-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b5d34-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b5d34-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b5d34-120">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b5d34-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="b5d34-121"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="b5d34-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b5d34-122">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5d34-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="b5d34-123"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="b5d34-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b5d34-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="b5d34-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b5d34-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5d34-125">Remarks</span></span>

<span data-ttu-id="b5d34-126">Essa interface retorna a miniatura com mais eficiência do que a propriedade [**thumbnail**](ivmdisplay-thumbnail.md) , mas não pode ser usada por clientes de script.</span><span class="sxs-lookup"><span data-stu-id="b5d34-126">This interface returns the thumbnail more efficiently than the [**Thumbnail**](ivmdisplay-thumbnail.md) property, but is not usable from scripting clients.</span></span> <span data-ttu-id="b5d34-127">A miniatura tem sempre 64 pixels de largura por 48 pixels de altura.</span><span class="sxs-lookup"><span data-stu-id="b5d34-127">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="b5d34-128">Cada pixel é 32 bits, em que os 8 bits superiores representam o valor azul do pixel, os próximos 8 bits representam o valor verde do pixel e os próximos 8 bits representam o valor vermelho do pixel.</span><span class="sxs-lookup"><span data-stu-id="b5d34-128">Each pixel is 32 bits, where the upper 8 bits represent the blue value of the pixel, the next 8 bits represent the green value of the pixel, and the next 8 bits represent the red value of the pixel.</span></span> <span data-ttu-id="b5d34-129">Os primeiros 64 elementos na matriz são a primeira linha da miniatura, os próximos 64 elementos são a segunda linha e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b5d34-129">The first 64 elements in the array is the first row of the thumbnail, the next 64 elements is the second row, and so on.</span></span> <span data-ttu-id="b5d34-130">Esse método retorna uma matriz estática de pixels, que é mais eficiente do que retornar um **SafeArray** de valores **variantes** , mas não é compatível com clientes de script.</span><span class="sxs-lookup"><span data-stu-id="b5d34-130">This method returns a static array of pixels, which is more efficient than returning a **SAFEARRAY** of **VARIANT** values, but is not compatible with scripting clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d34-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5d34-131">Requirements</span></span>



| <span data-ttu-id="b5d34-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5d34-132">Requirement</span></span> | <span data-ttu-id="b5d34-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b5d34-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d34-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5d34-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d34-135">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b5d34-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5d34-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5d34-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d34-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b5d34-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b5d34-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b5d34-138">End of client support</span></span><br/>    | <span data-ttu-id="b5d34-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b5d34-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b5d34-140">Produto</span><span class="sxs-lookup"><span data-stu-id="b5d34-140">Product</span></span><br/>                  | <span data-ttu-id="b5d34-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b5d34-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b5d34-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5d34-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5d34-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5d34-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b5d34-144">IID</span><span class="sxs-lookup"><span data-stu-id="b5d34-144">IID</span></span><br/>                      | <span data-ttu-id="b5d34-145">IID \_ IVMDisplay é definido como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="b5d34-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b5d34-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5d34-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d34-147">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="b5d34-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

