---
title: Método IVMMouse Click (VPCCOMInterfaces. h)
description: Simula um clique no botão do mouse.
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- Clique em método virtual PC
- Clique em método virtual PC, interface IVMMouse
- IVMMouse interface virtual PC, clique em método
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ea1b861db0a92ad92e689770182d225778aee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455907"
---
# <a name="ivmmouseclick-method"></a><span data-ttu-id="1e79b-106">Método IVMMouse:: Click</span><span class="sxs-lookup"><span data-stu-id="1e79b-106">IVMMouse::Click method</span></span>

<span data-ttu-id="1e79b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1e79b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1e79b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1e79b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1e79b-109">Simula um clique no botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="1e79b-109">Simulates a mouse button click.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e79b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e79b-110">Syntax</span></span>


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="1e79b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e79b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e79b-112">*buttonIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e79b-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e79b-113">O índice do botão que está sendo clicado.</span><span class="sxs-lookup"><span data-stu-id="1e79b-113">The index of the button being clicked.</span></span> <span data-ttu-id="1e79b-114">Para obter uma lista de valores, consulte [**VMMouseButton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="1e79b-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e79b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e79b-115">Return value</span></span>

<span data-ttu-id="1e79b-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1e79b-116">This method can return one of these values.</span></span>



| <span data-ttu-id="1e79b-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1e79b-117">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="1e79b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e79b-118">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e79b-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1e79b-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="1e79b-120">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1e79b-120">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="1e79b-121"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="1e79b-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="1e79b-122">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1e79b-122">The parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="1e79b-123"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="1e79b-123"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="1e79b-124">A máquina virtual à qual este dispositivo de mouse está anexado não está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="1e79b-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="1e79b-125"><dt>**VM \_ E \_ mouse \_ não \_ ativo**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="1e79b-125"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="1e79b-126">A operação não pôde ser concluída porque o dispositivo de mouse não está ligado ou não está ativo no momento na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1e79b-126">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="1e79b-127"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="1e79b-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="1e79b-128">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="1e79b-128">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="1e79b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e79b-129">Requirements</span></span>



| <span data-ttu-id="1e79b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e79b-130">Requirement</span></span> | <span data-ttu-id="1e79b-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1e79b-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e79b-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e79b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1e79b-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1e79b-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e79b-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e79b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1e79b-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1e79b-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1e79b-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1e79b-136">End of client support</span></span><br/>    | <span data-ttu-id="1e79b-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e79b-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1e79b-138">Produto</span><span class="sxs-lookup"><span data-stu-id="1e79b-138">Product</span></span><br/>                  | <span data-ttu-id="1e79b-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1e79b-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1e79b-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e79b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e79b-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e79b-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1e79b-142">IID</span><span class="sxs-lookup"><span data-stu-id="1e79b-142">IID</span></span><br/>                      | <span data-ttu-id="1e79b-143">IID \_ IVMmouse é definido como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="1e79b-143">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="1e79b-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e79b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e79b-145">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="1e79b-145">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

