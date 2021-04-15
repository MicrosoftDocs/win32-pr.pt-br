---
title: Propriedade IVMHostInfo ProcessorFeaturesString (VPCCOMInterfaces. h)
description: Recupera os recursos da lista com suporte pelo processador do host.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- Propriedade ProcessorFeaturesString Virtual PC
- Propriedade ProcessorFeaturesString Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade ProcessorFeaturesString
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorFeaturesString
- IVMHostInfo.get_ProcessorFeaturesString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118aaa2eabe7ddb2fd608892775a17eac6a77d16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760797"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a><span data-ttu-id="f5401-106">IVMHostInfo: Propriedade rocessorFeaturesString de:P</span><span class="sxs-lookup"><span data-stu-id="f5401-106">IVMHostInfo::ProcessorFeaturesString property</span></span>

<span data-ttu-id="f5401-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f5401-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f5401-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f5401-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f5401-109">Recupera os recursos da lista com suporte pelo processador do host.</span><span class="sxs-lookup"><span data-stu-id="f5401-109">Retrieves the list features supported by the host processor.</span></span>

<span data-ttu-id="f5401-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f5401-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5401-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5401-111">Syntax</span></span>


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a><span data-ttu-id="f5401-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f5401-112">Property value</span></span>

<span data-ttu-id="f5401-113">Uma lista delimitada por vírgulas de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5401-113">A comma-delimited list of features.</span></span> <span data-ttu-id="f5401-114">Um exemplo seria "MMX, SSE, SSE2, x86-64".</span><span class="sxs-lookup"><span data-stu-id="f5401-114">An example would be "MMX,SSE,SSE2,x86-64".</span></span>



| <span data-ttu-id="f5401-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f5401-115">Value</span></span>                                                                                 | <span data-ttu-id="f5401-116">Significado</span><span class="sxs-lookup"><span data-stu-id="f5401-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5401-117"><dt>"AMD-V"</dt></span><span class="sxs-lookup"><span data-stu-id="f5401-117"><dt>"AMD-V"</dt></span></span> </dl>    | <span data-ttu-id="f5401-118">Dá suporte às extensões de virtualização AMD.</span><span class="sxs-lookup"><span data-stu-id="f5401-118">Supports the AMD Virtualization extensions.</span></span><br/>              |
| <dl> <span data-ttu-id="f5401-119"><dt>"Intel VT"</dt></span><span class="sxs-lookup"><span data-stu-id="f5401-119"><dt>"Intel VT"</dt></span></span> </dl> | <span data-ttu-id="f5401-120">Dá suporte às extensões de tecnologia de virtualização da Intel.</span><span class="sxs-lookup"><span data-stu-id="f5401-120">Supports the Intel Virtualization Technology extensions.</span></span><br/> |
| <dl> <span data-ttu-id="f5401-121"><dt>"HAVD"</dt></span><span class="sxs-lookup"><span data-stu-id="f5401-121"><dt>"HAVD"</dt></span></span> </dl>     | <span data-ttu-id="f5401-122">A virtualização assistida por hardware está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="f5401-122">Hardware Assisted Virtualization is disabled.</span></span><br/>            |
| <dl> <span data-ttu-id="f5401-123"><dt>TER</dt></span><span class="sxs-lookup"><span data-stu-id="f5401-123"><dt>"HAVE"</dt></span></span> </dl>     | <span data-ttu-id="f5401-124">A virtualização assistida por hardware está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f5401-124">Hardware Assisted Virtualization is enabled.</span></span><br/>             |
| <dl> <span data-ttu-id="f5401-125"><dt>TECNOLOGIA</dt></span><span class="sxs-lookup"><span data-stu-id="f5401-125"><dt>"MMX"</dt></span></span> </dl>      | <span data-ttu-id="f5401-126">Dá suporte às extensões de MMX.</span><span class="sxs-lookup"><span data-stu-id="f5401-126">Supports the MMX extensions.</span></span><br/>                             |
| <dl> <span data-ttu-id="f5401-127"><dt>SSE</dt></span><span class="sxs-lookup"><span data-stu-id="f5401-127"><dt>"SSE"</dt></span></span> </dl>      | <span data-ttu-id="f5401-128">Dá suporte às extensões SIMD de streaming.</span><span class="sxs-lookup"><span data-stu-id="f5401-128">Supports the Streaming SIMD Extensions.</span></span><br/>                  |
| <dl> <span data-ttu-id="f5401-129"><dt>EXTENSÕES</dt></span><span class="sxs-lookup"><span data-stu-id="f5401-129"><dt>"SSE2"</dt></span></span> </dl>     | <span data-ttu-id="f5401-130">Dá suporte às extensões SIMD de streaming 2.</span><span class="sxs-lookup"><span data-stu-id="f5401-130">Supports the Streaming SIMD Extensions 2.</span></span><br/>                |
| <dl> <span data-ttu-id="f5401-131"><dt>SSE3</dt></span><span class="sxs-lookup"><span data-stu-id="f5401-131"><dt>"SSE3"</dt></span></span> </dl>     | <span data-ttu-id="f5401-132">Dá suporte às extensões SIMD de streaming 3.</span><span class="sxs-lookup"><span data-stu-id="f5401-132">Supports the Streaming SIMD Extensions 3.</span></span><br/>                |
| <dl> <span data-ttu-id="f5401-133"><dt>"TXTE"</dt></span><span class="sxs-lookup"><span data-stu-id="f5401-133"><dt>"TXTE"</dt></span></span> </dl>     | <span data-ttu-id="f5401-134">Dá suporte às extensões de tecnologia de execução confiável.</span><span class="sxs-lookup"><span data-stu-id="f5401-134">Supports the Trusted Execution Technology extensions.</span></span><br/>    |
| <dl> <span data-ttu-id="f5401-135"><dt>"x86-64"</dt></span><span class="sxs-lookup"><span data-stu-id="f5401-135"><dt>"x86-64"</dt></span></span> </dl>   | <span data-ttu-id="f5401-136">Dá suporte a extensões x86-64.</span><span class="sxs-lookup"><span data-stu-id="f5401-136">Supports x86-64 extensions.</span></span><br/>                              |



 

## <a name="error-codes"></a><span data-ttu-id="f5401-137">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f5401-137">Error codes</span></span>



| <span data-ttu-id="f5401-138">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="f5401-138">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f5401-139">Significado</span><span class="sxs-lookup"><span data-stu-id="f5401-139">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f5401-140"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f5401-140"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f5401-141">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f5401-141">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="f5401-142"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="f5401-142"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f5401-143">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f5401-143">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="f5401-144"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="f5401-144"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f5401-145">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="f5401-145">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f5401-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5401-146">Requirements</span></span>



| <span data-ttu-id="f5401-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5401-147">Requirement</span></span> | <span data-ttu-id="f5401-148">Valor</span><span class="sxs-lookup"><span data-stu-id="f5401-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5401-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5401-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f5401-150">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f5401-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5401-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5401-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f5401-152">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f5401-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f5401-153">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f5401-153">End of client support</span></span><br/>    | <span data-ttu-id="f5401-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f5401-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f5401-155">Produto</span><span class="sxs-lookup"><span data-stu-id="f5401-155">Product</span></span><br/>                  | <span data-ttu-id="f5401-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f5401-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f5401-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5401-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5401-158"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5401-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f5401-159">IID</span><span class="sxs-lookup"><span data-stu-id="f5401-159">IID</span></span><br/>                      | <span data-ttu-id="f5401-160">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="f5401-160">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f5401-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5401-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5401-162">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="f5401-162">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

