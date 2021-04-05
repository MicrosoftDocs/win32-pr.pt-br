---
title: Propriedade HorizontalPosition IVMMouse (VPCCOMInterfaces. h)
description: Coordenada x absoluta do mouse.
ms.assetid: 8cf2a247-b6db-49f6-8e19-c862004f26cd
keywords:
- Propriedade HorizontalPosition Virtual PC
- Propriedade HorizontalPosition Virtual PC, interface IVMMouse
- IVMMouse interface virtual PC, Propriedade HorizontalPosition
topic_type:
- apiref
api_name:
- IVMMouse.HorizontalPosition
- IVMMouse.get_HorizontalPosition
- IVMMouse.put_HorizontalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8506ad0d4583b9829ca2b1832686d32e67ded261
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919100"
---
# <a name="ivmmousehorizontalposition-property"></a><span data-ttu-id="cb70f-106">Propriedade IVMMouse:: HorizontalPosition</span><span class="sxs-lookup"><span data-stu-id="cb70f-106">IVMMouse::HorizontalPosition property</span></span>

<span data-ttu-id="cb70f-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cb70f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cb70f-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cb70f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cb70f-109">Recupera a coordenada x absoluta do mouse.</span><span class="sxs-lookup"><span data-stu-id="cb70f-109">Retrieves the absolute x-coordinate of the mouse.</span></span>

<span data-ttu-id="cb70f-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cb70f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb70f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb70f-111">Syntax</span></span>


```C++
HRESULT put_HorizontalPosition(
  [in]          long position
);

HRESULT get_HorizontalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a><span data-ttu-id="cb70f-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cb70f-112">Property value</span></span>

<span data-ttu-id="cb70f-113">A coordenada x que indica a nova posição do mouse.</span><span class="sxs-lookup"><span data-stu-id="cb70f-113">The x-coordinate indicating the new position of the mouse.</span></span> <span data-ttu-id="cb70f-114">Ao usar coordenadas absolutas, esse valor especifica a nova coordenada x do mouse.</span><span class="sxs-lookup"><span data-stu-id="cb70f-114">When using absolute coordinates, this value specifies the new x-coordinate of the mouse.</span></span> <span data-ttu-id="cb70f-115">Ao usar coordenadas relativas, esse valor especifica o número de pixels que o mouse deve ser movido na direção x.</span><span class="sxs-lookup"><span data-stu-id="cb70f-115">When using relative coordinates, this value specifies the number of pixels the mouse should be moved in the x direction.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cb70f-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="cb70f-116">Error codes</span></span>



| <span data-ttu-id="cb70f-117">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="cb70f-117">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="cb70f-118">Significado</span><span class="sxs-lookup"><span data-stu-id="cb70f-118">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb70f-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cb70f-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="cb70f-120">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cb70f-120">The operation was successful.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="cb70f-121"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="cb70f-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="cb70f-122">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cb70f-122">The parameter is **NULL**.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="cb70f-123"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="cb70f-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="cb70f-124">A máquina virtual à qual este dispositivo de mouse está anexado não está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="cb70f-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="cb70f-125"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="cb70f-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="cb70f-126">Os componentes de integração devem ser instalados para recuperar a posição do mouse ou para definir a posição do mouse ao usar coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="cb70f-126">Integration components must be installed to retrieve the mouse position, or to set the mouse position when using absolute coordinates.</span></span><br/>       |
| <dl> <span data-ttu-id="cb70f-127"><dt>VM \_ E \_ usando 0xA0040802 de \_ \_ coordenadas relativas</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cb70f-127"><dt>VM\_E\_USING\_RELATIVE\_COORDINATES</dt> <dt>0xA0040802</dt></span></span> </dl>   | <span data-ttu-id="cb70f-128">O dispositivo de mouse está definido atualmente para usar coordenadas relativas do mouse.</span><span class="sxs-lookup"><span data-stu-id="cb70f-128">The mouse device is currently set to use relative mouse coordinates.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="cb70f-129"><dt>VM \_ E \_ mouse \_ não \_ ativo</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="cb70f-129"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>             | <span data-ttu-id="cb70f-130">As coordenadas absolutas não poderão ser recuperadas se o dispositivo de mouse não estiver ligado ou se não estiver ativo no momento na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb70f-130">The absolute coordinates cannot be retrieved if the mouse device is not powered up, or if it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="cb70f-131"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="cb70f-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="cb70f-132">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="cb70f-132">An unexpected error has occurred.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="cb70f-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb70f-133">Remarks</span></span>

<span data-ttu-id="cb70f-134">Esta propriedade não pode ser recuperada ao usar coordenadas relativas.</span><span class="sxs-lookup"><span data-stu-id="cb70f-134">This property cannot be retrieved when using relative coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb70f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb70f-135">Requirements</span></span>



| <span data-ttu-id="cb70f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb70f-136">Requirement</span></span> | <span data-ttu-id="cb70f-137">Valor</span><span class="sxs-lookup"><span data-stu-id="cb70f-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb70f-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb70f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cb70f-139">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cb70f-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb70f-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb70f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cb70f-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cb70f-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cb70f-142">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="cb70f-142">End of client support</span></span><br/>    | <span data-ttu-id="cb70f-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cb70f-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cb70f-144">Produto</span><span class="sxs-lookup"><span data-stu-id="cb70f-144">Product</span></span><br/>                  | <span data-ttu-id="cb70f-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cb70f-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cb70f-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb70f-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb70f-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb70f-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cb70f-148">IID</span><span class="sxs-lookup"><span data-stu-id="cb70f-148">IID</span></span><br/>                      | <span data-ttu-id="cb70f-149">IID \_ IVMmouse é definido como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="cb70f-149">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="cb70f-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb70f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb70f-151">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="cb70f-151">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

