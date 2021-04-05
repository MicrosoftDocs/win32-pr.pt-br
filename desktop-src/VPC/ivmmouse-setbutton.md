---
title: Método SetButton IVMMouse (VPCCOMInterfaces. h)
description: Define o estado atual (para cima ou para baixo) do botão do mouse especificado.
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- Método SetButton Virtual PC
- Método SetButton Virtual PC, interface IVMMouse
- IVMMouse interface virtual PC, método SetButton
topic_type:
- apiref
api_name:
- IVMMouse.SetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d30ae131ac33eeff339b98511fd2da60a1e606
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086221"
---
# <a name="ivmmousesetbutton-method"></a><span data-ttu-id="ff35e-106">Método IVMMouse:: SetButton</span><span class="sxs-lookup"><span data-stu-id="ff35e-106">IVMMouse::SetButton method</span></span>

<span data-ttu-id="ff35e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ff35e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ff35e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ff35e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ff35e-109">Define o estado atual (para cima ou para baixo) do botão do mouse especificado.</span><span class="sxs-lookup"><span data-stu-id="ff35e-109">Sets the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff35e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff35e-110">Syntax</span></span>


```C++
HRESULT SetButton(
  [in] VMMouseButton buttonIndex,
  [in] VARIANT_BOOL  down
);
```



## <a name="parameters"></a><span data-ttu-id="ff35e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff35e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff35e-112">*buttonIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff35e-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff35e-113">O índice do botão.</span><span class="sxs-lookup"><span data-stu-id="ff35e-113">The button index.</span></span> <span data-ttu-id="ff35e-114">Para obter uma lista de valores, consulte [**VMMouseButton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="ff35e-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff35e-115">*para baixo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff35e-115">*down* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff35e-116">O novo estado do botão.</span><span class="sxs-lookup"><span data-stu-id="ff35e-116">The new button state.</span></span> <span data-ttu-id="ff35e-117">Use **true** se o estado do botão for para ser definido como Down e **false** se for definido como up.</span><span class="sxs-lookup"><span data-stu-id="ff35e-117">Use **TRUE** if the button state is to be set to down, and **FALSE** if it is to be set to up.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff35e-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff35e-118">Return value</span></span>

<span data-ttu-id="ff35e-119">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ff35e-119">This method can return one of these values.</span></span>



| <span data-ttu-id="ff35e-120">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ff35e-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="ff35e-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff35e-121">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff35e-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ff35e-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="ff35e-123">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ff35e-123">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="ff35e-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="ff35e-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="ff35e-125">O parâmetro *buttonIndex* não é válido.</span><span class="sxs-lookup"><span data-stu-id="ff35e-125">The *buttonIndex* parameter is not valid.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="ff35e-126"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="ff35e-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="ff35e-127">A máquina virtual à qual este dispositivo de mouse está anexado não está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="ff35e-127">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="ff35e-128"><dt>**VM \_ E \_ mouse \_ não \_ ativo**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="ff35e-128"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="ff35e-129">A operação não pôde ser concluída porque o dispositivo de mouse não está ligado ou não está ativo no momento na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff35e-129">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="ff35e-130"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="ff35e-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="ff35e-131">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="ff35e-131">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="ff35e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff35e-132">Requirements</span></span>



| <span data-ttu-id="ff35e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff35e-133">Requirement</span></span> | <span data-ttu-id="ff35e-134">Valor</span><span class="sxs-lookup"><span data-stu-id="ff35e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff35e-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff35e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ff35e-136">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ff35e-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff35e-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff35e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ff35e-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ff35e-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ff35e-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ff35e-139">End of client support</span></span><br/>    | <span data-ttu-id="ff35e-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ff35e-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ff35e-141">Produto</span><span class="sxs-lookup"><span data-stu-id="ff35e-141">Product</span></span><br/>                  | <span data-ttu-id="ff35e-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ff35e-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ff35e-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff35e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff35e-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff35e-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ff35e-145">IID</span><span class="sxs-lookup"><span data-stu-id="ff35e-145">IID</span></span><br/>                      | <span data-ttu-id="ff35e-146">IID \_ IVMmouse é definido como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="ff35e-146">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="ff35e-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff35e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff35e-148">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="ff35e-148">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

