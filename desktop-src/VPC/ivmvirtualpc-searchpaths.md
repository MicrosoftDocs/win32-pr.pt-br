---
title: Propriedade IVMVirtualPC SearchPaths (VPCCOMInterfaces. h)
description: Caminhos do sistema de arquivos que são usados para localizar arquivos associados ao Windows Virtual PC.
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- Propriedade SearchPaths Virtual PC
- Propriedade SearchPaths Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, Propriedade SearchPaths
topic_type:
- apiref
api_name:
- IVMVirtualPC.SearchPaths
- IVMVirtualPC.get_SearchPaths
- IVMVirtualPC.put_SearchPaths
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287eb07bc9205f9b6f0851bd8809f9a49dcf3242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644211"
---
# <a name="ivmvirtualpcsearchpaths-property"></a><span data-ttu-id="dfda7-106">Propriedade IVMVirtualPC:: SearchPaths</span><span class="sxs-lookup"><span data-stu-id="dfda7-106">IVMVirtualPC::SearchPaths property</span></span>

<span data-ttu-id="dfda7-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dfda7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dfda7-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dfda7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dfda7-109">Recupera e define os caminhos do sistema de arquivos que são usados para localizar arquivos associados ao Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="dfda7-109">Retrieves and sets the file system paths that are used to find files associated with Windows Virtual PC.</span></span>

<span data-ttu-id="dfda7-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="dfda7-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfda7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfda7-111">Syntax</span></span>


```C++
HRESULT put_SearchPaths(
  [in]          VARIANT searchPaths
);

HRESULT get_SearchPaths(
  [out, retval] VARIANT *searchPaths
);
```



## <a name="property-value"></a><span data-ttu-id="dfda7-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="dfda7-112">Property value</span></span>

<span data-ttu-id="dfda7-113">Especifica um SafeArray que contém um caminho de sistema de arquivos para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="dfda7-113">Specifies a safearray containing a file system path for each entry.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dfda7-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="dfda7-114">Error codes</span></span>



| <span data-ttu-id="dfda7-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="dfda7-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="dfda7-116">Significado</span><span class="sxs-lookup"><span data-stu-id="dfda7-116">Meaning</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dfda7-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dfda7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="dfda7-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dfda7-118">The operation was successful.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="dfda7-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="dfda7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="dfda7-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfda7-120">The parameter is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="dfda7-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="dfda7-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="dfda7-122">O parâmetro *searchPaths* não é válido e não pôde ser analisado em uma matriz de caminhos.</span><span class="sxs-lookup"><span data-stu-id="dfda7-122">The *searchPaths* parameter is not valid and could not be parsed into an array of paths.</span></span><br/>                                    |
| <dl> <span data-ttu-id="dfda7-123"><dt>HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="dfda7-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="dfda7-124">O sistema não pode localizar um diretório especificado no parâmetro *searchPaths* .</span><span class="sxs-lookup"><span data-stu-id="dfda7-124">The system cannot find a directory specified in the *searchPaths* parameter.</span></span><br/>                                                |
| <dl> <span data-ttu-id="dfda7-125"><dt>HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="dfda7-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="dfda7-126">O sistema não pode localizar um caminho especificado pelo parâmetro *searchPaths* .</span><span class="sxs-lookup"><span data-stu-id="dfda7-126">The system cannot find a path specified by the *searchPaths* parameter.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="dfda7-127"><dt>HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="dfda7-127"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="dfda7-128">Um caminho especificado no parâmetro *searchPaths* contém caracteres ilegais.</span><span class="sxs-lookup"><span data-stu-id="dfda7-128">A path specified in the *searchPaths* parameter contains illegal characters.</span></span> <span data-ttu-id="dfda7-129">Os caracteres ilegais são " \* ? <>/ \| ": ".</span><span class="sxs-lookup"><span data-stu-id="dfda7-129">The illegal characters are "\*?<>/\|":".</span></span><br/> |
| <dl> <span data-ttu-id="dfda7-130"><dt>HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="dfda7-130"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="dfda7-131">Um caminho contido no parâmetro *searchPaths* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="dfda7-131">A path contained in the *searchPaths* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="dfda7-132">Um caminho absoluto é necessário.</span><span class="sxs-lookup"><span data-stu-id="dfda7-132">An absolute path is required.</span></span><br/>          |
| <dl> <span data-ttu-id="dfda7-133"><dt>HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="dfda7-133"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="dfda7-134">O caminho especificado no parâmetro *searchPaths* é muito longo.</span><span class="sxs-lookup"><span data-stu-id="dfda7-134">The path specified in the *searchPaths* parameter is too long.</span></span> <span data-ttu-id="dfda7-135">O comprimento do caminho deve ter menos de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="dfda7-135">The length of the path must be less than 260 characters.</span></span><br/>     |
| <dl> <span data-ttu-id="dfda7-136"><dt>VM \_ E \_ pref \_ não \_ encontrado</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="dfda7-136"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl>                       | <span data-ttu-id="dfda7-137">A preferência não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="dfda7-137">The preference was not found.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="dfda7-138"><dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dfda7-138"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="dfda7-139">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="dfda7-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                        |
| <dl> <span data-ttu-id="dfda7-140"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="dfda7-140"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="dfda7-141">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="dfda7-141">An unexpected error has occurred.</span></span><br/>                                                                                           |



## <a name="requirements"></a><span data-ttu-id="dfda7-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfda7-142">Requirements</span></span>



| <span data-ttu-id="dfda7-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfda7-143">Requirement</span></span> | <span data-ttu-id="dfda7-144">Valor</span><span class="sxs-lookup"><span data-stu-id="dfda7-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfda7-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfda7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="dfda7-146">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dfda7-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dfda7-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfda7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="dfda7-148">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dfda7-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dfda7-149">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="dfda7-149">End of client support</span></span><br/>    | <span data-ttu-id="dfda7-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfda7-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dfda7-151">Produto</span><span class="sxs-lookup"><span data-stu-id="dfda7-151">Product</span></span><br/>                  | <span data-ttu-id="dfda7-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dfda7-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dfda7-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfda7-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfda7-154"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfda7-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dfda7-155">IID</span><span class="sxs-lookup"><span data-stu-id="dfda7-155">IID</span></span><br/>                      | <span data-ttu-id="dfda7-156">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="dfda7-156">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="dfda7-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfda7-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfda7-158">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="dfda7-158">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

