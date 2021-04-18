---
title: Propriedade IVMMouse UsingAbsoluteCoordinates (VPCCOMInterfaces. h)
description: Recupera se as coordenadas do mouse representam coordenadas absolutas ou relativas.
ms.assetid: 668278f8-28ae-4128-9653-4985bddbe184
keywords:
- Propriedade UsingAbsoluteCoordinates Virtual PC
- Propriedade UsingAbsoluteCoordinates Virtual PC, interface IVMMouse
- IVMMouse interface virtual PC, Propriedade UsingAbsoluteCoordinates
topic_type:
- apiref
api_name:
- IVMMouse.UsingAbsoluteCoordinates
- IVMMouse.get_UsingAbsoluteCoordinates
- IVMMouse.put_UsingAbsoluteCoordinates
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc216466ab8ef0483d3c1a229f6a493d4ba913dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499686"
---
# <a name="ivmmouseusingabsolutecoordinates-property"></a><span data-ttu-id="83fa9-106">Propriedade IVMMouse:: UsingAbsoluteCoordinates</span><span class="sxs-lookup"><span data-stu-id="83fa9-106">IVMMouse::UsingAbsoluteCoordinates property</span></span>

<span data-ttu-id="83fa9-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="83fa9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="83fa9-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="83fa9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="83fa9-109">Recupera se as coordenadas do mouse representam coordenadas absolutas ou relativas.</span><span class="sxs-lookup"><span data-stu-id="83fa9-109">Retrieves whether mouse coordinates represent absolute or relative coordinates.</span></span>

<span data-ttu-id="83fa9-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="83fa9-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="83fa9-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="83fa9-111">Syntax</span></span>


```C++
HRESULT put_UsingAbsoluteCoordinates(
  [in]          VARIANT_BOOL usingAbsoluteCoordinates
);

HRESULT get_UsingAbsoluteCoordinates(
  [out, retval] VARIANT_BOOL *usingAbsoluteCoordinates
);
```



## <a name="property-value"></a><span data-ttu-id="83fa9-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="83fa9-112">Property value</span></span>

<span data-ttu-id="83fa9-113">**Variante \_ TRUE** para definir o dispositivo de mouse para usar coordenadas absolutas, **Variant \_ false** para usar coordenadas relativas.</span><span class="sxs-lookup"><span data-stu-id="83fa9-113">**VARIANT\_TRUE** to set the mouse device to use absolute coordinates, **VARIANT\_FALSE** to use relative coordinates.</span></span>

## <a name="error-codes"></a><span data-ttu-id="83fa9-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="83fa9-114">Error codes</span></span>



| <span data-ttu-id="83fa9-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="83fa9-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="83fa9-116">Significado</span><span class="sxs-lookup"><span data-stu-id="83fa9-116">Meaning</span></span>                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83fa9-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="83fa9-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="83fa9-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="83fa9-118">The operation was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="83fa9-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="83fa9-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="83fa9-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="83fa9-120">The parameter is **NULL**.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="83fa9-121"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="83fa9-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="83fa9-122">A máquina virtual à qual este dispositivo de mouse está anexado não está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="83fa9-122">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                       |
| <dl> <span data-ttu-id="83fa9-123"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="83fa9-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="83fa9-124">Os componentes de integração não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="83fa9-124">Integration components are not installed.</span></span> <span data-ttu-id="83fa9-125">Os componentes de integração são necessários para usar coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="83fa9-125">Integration components are required to use absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="83fa9-126"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="83fa9-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="83fa9-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="83fa9-127">An unexpected error has occurred.</span></span><br/>                                                                          |



## <a name="remarks"></a><span data-ttu-id="83fa9-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="83fa9-128">Remarks</span></span>

<span data-ttu-id="83fa9-129">Essa propriedade é local somente para esse objeto e usará como padrão a **variante \_ false** para um novo objeto [**IVMMouse**](ivmmouse.md) .</span><span class="sxs-lookup"><span data-stu-id="83fa9-129">This property is local only to this object and will default to **VARIANT\_FALSE** for a new [**IVMMouse**](ivmmouse.md) object.</span></span> <span data-ttu-id="83fa9-130">Observe que os componentes de integração devem ser instalados para usar coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="83fa9-130">Note that integration components must be installed in order to use absolute coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="83fa9-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83fa9-131">Requirements</span></span>



| <span data-ttu-id="83fa9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="83fa9-132">Requirement</span></span> | <span data-ttu-id="83fa9-133">Valor</span><span class="sxs-lookup"><span data-stu-id="83fa9-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="83fa9-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83fa9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="83fa9-135">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="83fa9-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="83fa9-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83fa9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="83fa9-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="83fa9-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="83fa9-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="83fa9-138">End of client support</span></span><br/>    | <span data-ttu-id="83fa9-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="83fa9-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="83fa9-140">Produto</span><span class="sxs-lookup"><span data-stu-id="83fa9-140">Product</span></span><br/>                  | <span data-ttu-id="83fa9-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="83fa9-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="83fa9-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83fa9-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="83fa9-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="83fa9-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="83fa9-144">IID</span><span class="sxs-lookup"><span data-stu-id="83fa9-144">IID</span></span><br/>                      | <span data-ttu-id="83fa9-145">IID \_ IVMmouse é definido como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="83fa9-145">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="83fa9-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="83fa9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83fa9-147">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="83fa9-147">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

