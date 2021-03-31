---
title: Método getbutton IVMMouse (VPCCOMInterfaces. h)
description: Recupera o estado atual do botão do mouse especificado.
ms.assetid: eb534f88-387d-42fb-bfc3-bca17685021e
keywords:
- PC virtual do método getbutton
- Método getbutton Virtual PC, interface IVMMouse
- IVMMouse interface virtual PC, método getbutton
topic_type:
- apiref
api_name:
- IVMMouse.GetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73929a1fc9dfaa3942ed49f8a449343a594eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645139"
---
# <a name="ivmmousegetbutton-method"></a><span data-ttu-id="398d7-106">Método IVMMouse:: getbutton</span><span class="sxs-lookup"><span data-stu-id="398d7-106">IVMMouse::GetButton method</span></span>

<span data-ttu-id="398d7-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="398d7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="398d7-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="398d7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="398d7-109">Recupera o estado atual (para cima ou para baixo) do botão do mouse especificado.</span><span class="sxs-lookup"><span data-stu-id="398d7-109">Retrieves the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="398d7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="398d7-110">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]          VMMouseButton buttonIndex,
  [out, retval] VARIANT_BOOL  *isDown
);
```



## <a name="parameters"></a><span data-ttu-id="398d7-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="398d7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="398d7-112">*buttonIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="398d7-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398d7-113">O índice do botão cujo estado está sendo solicitado.</span><span class="sxs-lookup"><span data-stu-id="398d7-113">The index of the button whose state is being requested.</span></span> <span data-ttu-id="398d7-114">Para obter uma lista de valores, consulte [**VMMouseButton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="398d7-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="398d7-115">*IsDown* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="398d7-115">*isDown* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="398d7-116">O estado do botão indicado.</span><span class="sxs-lookup"><span data-stu-id="398d7-116">The state of the indicated button.</span></span> <span data-ttu-id="398d7-117">**True** se o botão estiver inoperante no momento na máquina virtual; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="398d7-117">**TRUE** if the button is currently down in the virtual machine, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="398d7-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="398d7-118">Return value</span></span>

<span data-ttu-id="398d7-119">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="398d7-119">This method can return one of these values.</span></span>



| <span data-ttu-id="398d7-120">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="398d7-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="398d7-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="398d7-121">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="398d7-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="398d7-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="398d7-123">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="398d7-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="398d7-124"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="398d7-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                | <span data-ttu-id="398d7-125">O parâmetro *IsDown* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="398d7-125">The *isDown* parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="398d7-126"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="398d7-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="398d7-127">O parâmetro *buttonIndex* não é válido.</span><span class="sxs-lookup"><span data-stu-id="398d7-127">The *buttonIndex* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="398d7-128"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="398d7-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="398d7-129">A máquina virtual à qual este dispositivo de mouse está anexado não está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="398d7-129">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="398d7-130"><dt>**VM \_ E \_ mouse \_ não \_ ativo**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="398d7-130"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="398d7-131">O dispositivo de mouse não foi ligado.</span><span class="sxs-lookup"><span data-stu-id="398d7-131">The mouse device has not been powered up.</span></span><br/>                                            |
| <dl> <span data-ttu-id="398d7-132"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="398d7-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="398d7-133">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="398d7-133">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="398d7-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="398d7-134">Requirements</span></span>



| <span data-ttu-id="398d7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="398d7-135">Requirement</span></span> | <span data-ttu-id="398d7-136">Valor</span><span class="sxs-lookup"><span data-stu-id="398d7-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="398d7-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="398d7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="398d7-138">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="398d7-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="398d7-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="398d7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="398d7-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="398d7-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="398d7-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="398d7-141">End of client support</span></span><br/>    | <span data-ttu-id="398d7-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="398d7-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="398d7-143">Produto</span><span class="sxs-lookup"><span data-stu-id="398d7-143">Product</span></span><br/>                  | <span data-ttu-id="398d7-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="398d7-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="398d7-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="398d7-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="398d7-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="398d7-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="398d7-147">IID</span><span class="sxs-lookup"><span data-stu-id="398d7-147">IID</span></span><br/>                      | <span data-ttu-id="398d7-148">IID \_ IVMmouse é definido como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="398d7-148">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="398d7-149">Consulte também</span><span class="sxs-lookup"><span data-stu-id="398d7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="398d7-150">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="398d7-150">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

