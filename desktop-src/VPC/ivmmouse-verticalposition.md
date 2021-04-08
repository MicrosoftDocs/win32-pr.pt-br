---
title: Propriedade IVMMouse VerticalPosition (VPCCOMInterfaces. h)
description: Coordenada y absoluta do mouse.
ms.assetid: 02fd3677-95d8-44b4-b398-d3ec62e5d9f0
keywords:
- Propriedade VerticalPosition Virtual PC
- Propriedade VerticalPosition Virtual PC, interface IVMMouse
- IVMMouse interface virtual PC, Propriedade VerticalPosition
topic_type:
- apiref
api_name:
- IVMMouse.VerticalPosition
- IVMMouse.get_VerticalPosition
- IVMMouse.put_VerticalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64712f557a3fcd59181e8ce65d835b630da68e48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919099"
---
# <a name="ivmmouseverticalposition-property"></a><span data-ttu-id="e7907-106">Propriedade IVMMouse:: VerticalPosition</span><span class="sxs-lookup"><span data-stu-id="e7907-106">IVMMouse::VerticalPosition property</span></span>

<span data-ttu-id="e7907-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e7907-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e7907-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e7907-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e7907-109">Recupera a coordenada y absoluta do mouse.</span><span class="sxs-lookup"><span data-stu-id="e7907-109">Retrieves the absolute y-coordinate of the mouse.</span></span>

<span data-ttu-id="e7907-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e7907-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7907-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7907-111">Syntax</span></span>


```C++
HRESULT put_VerticalPosition(
  [in]          long position
);

HRESULT get_VerticalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a><span data-ttu-id="e7907-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e7907-112">Property value</span></span>

<span data-ttu-id="e7907-113">A coordenada y que indica a nova posição do mouse.</span><span class="sxs-lookup"><span data-stu-id="e7907-113">The y-coordinate indicating the new position of the mouse.</span></span> <span data-ttu-id="e7907-114">Ao usar coordenadas absolutas, esse valor especifica a nova coordenada y do mouse.</span><span class="sxs-lookup"><span data-stu-id="e7907-114">When using absolute coordinates, this value specifies the new y-coordinate of the mouse.</span></span> <span data-ttu-id="e7907-115">Ao usar coordenadas relativas, esse valor especifica o número de pixels que o mouse deve ser movido na direção y.</span><span class="sxs-lookup"><span data-stu-id="e7907-115">When using relative coordinates, this value specifies the number of pixels the mouse should be moved in the y direction.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e7907-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e7907-116">Error codes</span></span>



| <span data-ttu-id="e7907-117">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="e7907-117">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="e7907-118">Significado</span><span class="sxs-lookup"><span data-stu-id="e7907-118">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e7907-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e7907-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="e7907-120">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e7907-120">The operation was successful.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="e7907-121"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="e7907-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="e7907-122">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e7907-122">The parameter is **NULL**.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="e7907-123"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="e7907-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="e7907-124">A máquina virtual à qual este dispositivo de mouse está anexado não está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="e7907-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="e7907-125"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="e7907-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="e7907-126">Os componentes de integração devem ser instalados para recuperar a posição do mouse ou para definir a posição do mouse ao usar coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="e7907-126">Integration components must be installed to retrieve the mouse position, or to set the mouse position when using absolute coordinates.</span></span><br/>       |
| <dl> <span data-ttu-id="e7907-127"><dt>VM \_ E \_ usando 0xA0040802 de \_ \_ coordenadas relativas</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e7907-127"><dt>VM\_E\_USING\_RELATIVE\_COORDINATES</dt> <dt>0xA0040802</dt></span></span> </dl>   | <span data-ttu-id="e7907-128">O dispositivo de mouse está definido atualmente para usar coordenadas relativas do mouse.</span><span class="sxs-lookup"><span data-stu-id="e7907-128">The mouse device is currently set to use relative mouse coordinates.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="e7907-129"><dt>VM \_ E \_ mouse \_ não \_ ativo</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="e7907-129"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>             | <span data-ttu-id="e7907-130">As coordenadas absolutas não poderão ser recuperadas se o dispositivo de mouse não estiver ligado ou se não estiver ativo no momento na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e7907-130">The absolute coordinates cannot be retrieved if the mouse device is not powered up, or if it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="e7907-131"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="e7907-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="e7907-132">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="e7907-132">An unexpected error has occurred.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="e7907-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7907-133">Remarks</span></span>

<span data-ttu-id="e7907-134">Esta propriedade não pode ser recuperada ao usar coordenadas relativas.</span><span class="sxs-lookup"><span data-stu-id="e7907-134">This property cannot be retrieved when using relative coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7907-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7907-135">Requirements</span></span>



| <span data-ttu-id="e7907-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7907-136">Requirement</span></span> | <span data-ttu-id="e7907-137">Valor</span><span class="sxs-lookup"><span data-stu-id="e7907-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7907-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7907-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e7907-139">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e7907-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7907-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7907-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e7907-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e7907-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e7907-142">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e7907-142">End of client support</span></span><br/>    | <span data-ttu-id="e7907-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7907-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e7907-144">Produto</span><span class="sxs-lookup"><span data-stu-id="e7907-144">Product</span></span><br/>                  | <span data-ttu-id="e7907-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e7907-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e7907-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7907-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7907-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7907-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e7907-148">IID</span><span class="sxs-lookup"><span data-stu-id="e7907-148">IID</span></span><br/>                      | <span data-ttu-id="e7907-149">IID \_ IVMmouse é definido como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="e7907-149">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="e7907-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7907-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7907-151">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="e7907-151">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

