---
title: Propriedade IVMMouse ScrollWheelPosition (VPCCOMInterfaces. h)
description: Ajusta a coordenada z do mouse (somente relativo).
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- Propriedade ScrollWheelPosition Virtual PC
- Propriedade ScrollWheelPosition Virtual PC, interface IVMMouse
- IVMMouse interface virtual PC, Propriedade ScrollWheelPosition
topic_type:
- apiref
api_name:
- IVMMouse.ScrollWheelPosition
- IVMMouse.put_ScrollWheelPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e374011dc87ad00d4edef1f33e9787d5a2e6d787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645138"
---
# <a name="ivmmousescrollwheelposition-property"></a><span data-ttu-id="a1593-106">Propriedade IVMMouse:: ScrollWheelPosition</span><span class="sxs-lookup"><span data-stu-id="a1593-106">IVMMouse::ScrollWheelPosition property</span></span>

<span data-ttu-id="a1593-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a1593-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a1593-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a1593-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a1593-109">Ajusta a coordenada z do mouse (somente relativo).</span><span class="sxs-lookup"><span data-stu-id="a1593-109">Adjusts the z-coordinate of the mouse (relative only).</span></span>

<span data-ttu-id="a1593-110">Essa propriedade é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="a1593-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1593-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1593-111">Syntax</span></span>


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a><span data-ttu-id="a1593-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a1593-112">Property value</span></span>

<span data-ttu-id="a1593-113">A coordenada z que indica o número de pixels que o mouse deve ser movido ao longo do eixo z.</span><span class="sxs-lookup"><span data-stu-id="a1593-113">The z-coordinate indicating the number of pixels the mouse is to be moved along the z-axis.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a1593-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a1593-114">Error codes</span></span>



| <span data-ttu-id="a1593-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="a1593-115">Name/value</span></span>                                                                                                                                                                     | <span data-ttu-id="a1593-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a1593-116">Meaning</span></span>                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a1593-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a1593-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                        | <span data-ttu-id="a1593-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a1593-118">The operation was successful.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="a1593-119"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="a1593-119"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>             | <span data-ttu-id="a1593-120">A máquina virtual à qual este dispositivo de mouse está anexado não está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="a1593-120">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>         |
| <dl> <span data-ttu-id="a1593-121"><dt>VM \_ E \_ mouse \_ não \_ ativo</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="a1593-121"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>           | <span data-ttu-id="a1593-122">O dispositivo de mouse não foi ligado ou não está ativo no momento na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1593-122">The mouse device has not been powered up, or is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="a1593-123"><dt>VM \_ E \_ usando 0xA0040801 de \_ \_ coordenadas absolutas</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a1593-123"><dt>VM\_E\_USING\_ABSOLUTE\_COORDINATES</dt> <dt>0xA0040801</dt></span></span> </dl> | <span data-ttu-id="a1593-124">A posição da roda de rolagem não pode ser definida quando o dispositivo do mouse está usando coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="a1593-124">The scroll wheel position cannot be set when the mouse device is using absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="a1593-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="a1593-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                  | <span data-ttu-id="a1593-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="a1593-126">An unexpected error has occurred.</span></span><br/>                                                            |



## <a name="requirements"></a><span data-ttu-id="a1593-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1593-127">Requirements</span></span>



| <span data-ttu-id="a1593-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1593-128">Requirement</span></span> | <span data-ttu-id="a1593-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a1593-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1593-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1593-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a1593-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a1593-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a1593-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1593-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a1593-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a1593-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a1593-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a1593-134">End of client support</span></span><br/>    | <span data-ttu-id="a1593-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a1593-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a1593-136">Produto</span><span class="sxs-lookup"><span data-stu-id="a1593-136">Product</span></span><br/>                  | <span data-ttu-id="a1593-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a1593-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a1593-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1593-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1593-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1593-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a1593-140">IID</span><span class="sxs-lookup"><span data-stu-id="a1593-140">IID</span></span><br/>                      | <span data-ttu-id="a1593-141">IID \_ IVMmouse é definido como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="a1593-141">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="a1593-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a1593-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1593-143">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="a1593-143">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

