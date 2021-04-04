---
title: Propriedade thumbnail IVMDisplay (VPCCOMInterfaces. h)
description: Recupera uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual. | Propriedade thumbnail IVMDisplay (VPCCOMInterfaces. h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Propriedade de miniatura Virtual PC
- Propriedade thumbnail Virtual PC, interface IVMDisplay
- Virtual PC de interface IVMDisplay, propriedade Thumbnail
topic_type:
- apiref
api_name:
- IVMDisplay.Thumbnail
- IVMDisplay.get_Thumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0466af2552fbb108f31de94b3f970d6e7d5571b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930277"
---
# <a name="ivmdisplaythumbnail-property"></a><span data-ttu-id="e5f5c-107">Propriedade IVMDisplay:: thumbnail</span><span class="sxs-lookup"><span data-stu-id="e5f5c-107">IVMDisplay::Thumbnail property</span></span>

<span data-ttu-id="e5f5c-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e5f5c-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e5f5c-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e5f5c-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e5f5c-110">Recupera uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e5f5c-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

<span data-ttu-id="e5f5c-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e5f5c-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5f5c-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5f5c-112">Syntax</span></span>


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a><span data-ttu-id="e5f5c-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e5f5c-113">Property value</span></span>

<span data-ttu-id="e5f5c-114">Uma variante do tipo VT \_ variante de matriz \| VT \_ que contém entradas do tipo VT \_ UI4, uma para cada pixel na miniatura.</span><span class="sxs-lookup"><span data-stu-id="e5f5c-114">A variant of type VT\_ARRAY \| VT\_VARIANT containing entries of type VT\_UI4, one for each pixel in the thumbnail.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e5f5c-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e5f5c-115">Error codes</span></span>



| <span data-ttu-id="e5f5c-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="e5f5c-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e5f5c-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e5f5c-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e5f5c-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e5f5c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e5f5c-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e5f5c-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="e5f5c-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="e5f5c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e5f5c-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e5f5c-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="e5f5c-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="e5f5c-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e5f5c-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="e5f5c-123">An unexpected error has occurred.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e5f5c-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5f5c-124">Remarks</span></span>

<span data-ttu-id="e5f5c-125">Essa interface retorna a miniatura com menos eficiência do que o método [**\_ GenerateThumbnail**](ivmdisplay--generatethumbnail.md) , mas é utilizável de clientes de script.</span><span class="sxs-lookup"><span data-stu-id="e5f5c-125">This interface returns the thumbnail less efficiently than the [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) method, but is usable from scripting clients.</span></span> <span data-ttu-id="e5f5c-126">A miniatura tem sempre 64 pixels de largura por 48 pixels de altura.</span><span class="sxs-lookup"><span data-stu-id="e5f5c-126">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="e5f5c-127">Cada pixel é de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e5f5c-127">Each pixel is 32 bits.</span></span> <span data-ttu-id="e5f5c-128">Os primeiros 64 elementos na matriz são a primeira linha de pixels na miniatura, os próximos 64 elementos são a segunda linha e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e5f5c-128">The first 64 elements in the array is the first row of pixels in the thumbnail, the next 64 elements is the second row, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5f5c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5f5c-129">Requirements</span></span>



| <span data-ttu-id="e5f5c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5f5c-130">Requirement</span></span> | <span data-ttu-id="e5f5c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e5f5c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5f5c-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5f5c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e5f5c-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e5f5c-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e5f5c-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5f5c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e5f5c-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e5f5c-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e5f5c-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e5f5c-136">End of client support</span></span><br/>    | <span data-ttu-id="e5f5c-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e5f5c-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e5f5c-138">Produto</span><span class="sxs-lookup"><span data-stu-id="e5f5c-138">Product</span></span><br/>                  | <span data-ttu-id="e5f5c-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e5f5c-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e5f5c-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5f5c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5f5c-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5f5c-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e5f5c-142">IID</span><span class="sxs-lookup"><span data-stu-id="e5f5c-142">IID</span></span><br/>                      | <span data-ttu-id="e5f5c-143">IID \_ IVMDisplay é definido como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="e5f5c-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e5f5c-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5f5c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5f5c-145">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="e5f5c-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

