---
title: Propriedade IVMDisplay Height (VPCCOMInterfaces. h)
description: Altura da exibição da máquina virtual, em pixels.
ms.assetid: 4fbb7c2b-6d5f-4af6-b8cc-3a7546b15cbd
keywords:
- Propriedade de altura Virtual PC
- Propriedade Height Virtual PC, interface IVMDisplay
- IVMDisplay da interface virtual PC, Propriedade Height
topic_type:
- apiref
api_name:
- IVMDisplay.Height
- IVMDisplay.get_Height
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6ff5746c817dcc81b353f80e2daa345b5587fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009440"
---
# <a name="ivmdisplayheight-property"></a><span data-ttu-id="e396e-106">Propriedade IVMDisplay:: Height</span><span class="sxs-lookup"><span data-stu-id="e396e-106">IVMDisplay::Height property</span></span>

<span data-ttu-id="e396e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e396e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e396e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e396e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e396e-109">Recupera a altura da exibição da máquina virtual, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e396e-109">Retrieves the height of the virtual machine's display, in pixels.</span></span>

<span data-ttu-id="e396e-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e396e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e396e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e396e-111">Syntax</span></span>


```C++
HRESULT get_Height(
  [out, retval] long *displayPixelHeight
);
```



## <a name="property-value"></a><span data-ttu-id="e396e-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e396e-112">Property value</span></span>

<span data-ttu-id="e396e-113">A altura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e396e-113">The height, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e396e-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e396e-114">Error codes</span></span>



| <span data-ttu-id="e396e-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="e396e-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="e396e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="e396e-116">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e396e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e396e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="e396e-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e396e-118">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="e396e-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="e396e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="e396e-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e396e-120">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e396e-121"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="e396e-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="e396e-122">A máquina virtual deve estar em execução para esta operação.</span><span class="sxs-lookup"><span data-stu-id="e396e-122">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="e396e-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e396e-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="e396e-124">A máquina virtual não é válida ou não está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="e396e-124">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="e396e-125"><dt>VM \_ E \_ nenhum \_ </dt> <dt>0xA0040850</dt> de exibição</span><span class="sxs-lookup"><span data-stu-id="e396e-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="e396e-126">Não é possível localizar uma exibição válida para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e396e-126">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="e396e-127"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="e396e-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="e396e-128">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="e396e-128">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="e396e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e396e-129">Requirements</span></span>



| <span data-ttu-id="e396e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e396e-130">Requirement</span></span> | <span data-ttu-id="e396e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e396e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e396e-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e396e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e396e-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e396e-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e396e-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e396e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e396e-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e396e-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e396e-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e396e-136">End of client support</span></span><br/>    | <span data-ttu-id="e396e-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e396e-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e396e-138">Produto</span><span class="sxs-lookup"><span data-stu-id="e396e-138">Product</span></span><br/>                  | <span data-ttu-id="e396e-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e396e-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e396e-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e396e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e396e-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e396e-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e396e-142">IID</span><span class="sxs-lookup"><span data-stu-id="e396e-142">IID</span></span><br/>                      | <span data-ttu-id="e396e-143">IID \_ IVMDisplay é definido como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="e396e-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e396e-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e396e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e396e-145">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="e396e-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

