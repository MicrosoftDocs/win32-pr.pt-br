---
title: Método IVMVirtualPC GetFloppyDiskFiles (VPCCOMInterfaces. h)
description: Recupera uma matriz de arquivos de disquete virtual conhecidos.
ms.assetid: c40f2780-eb84-4e0c-a493-1d1e5706cc8b
keywords:
- GetFloppyDiskFiles do método virtual PC
- Método GetFloppyDiskFiles Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método GetFloppyDiskFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9759a3b909bb4f4ac179c166635185a701a8a16e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645135"
---
# <a name="ivmvirtualpcgetfloppydiskfiles-method"></a><span data-ttu-id="90956-106">Método IVMVirtualPC:: GetFloppyDiskFiles</span><span class="sxs-lookup"><span data-stu-id="90956-106">IVMVirtualPC::GetFloppyDiskFiles method</span></span>

<span data-ttu-id="90956-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="90956-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="90956-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="90956-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="90956-109">Recupera uma matriz de arquivos de disquete virtual conhecidos.</span><span class="sxs-lookup"><span data-stu-id="90956-109">Retrieves an array of known virtual floppy disk files.</span></span>

## <a name="syntax"></a><span data-ttu-id="90956-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90956-110">Syntax</span></span>


```C++
HRESULT GetFloppyDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outFloppyDiskFileList
);
```



## <a name="parameters"></a><span data-ttu-id="90956-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90956-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90956-112">*inAdditionalSearchPaths* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90956-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90956-113">Esses caminhos serão pesquisados juntamente com os caminhos definidos na propriedade [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) .</span><span class="sxs-lookup"><span data-stu-id="90956-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="90956-114">*outFloppyDiskFileList* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="90956-114">*outFloppyDiskFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="90956-115">Uma matriz de arquivos de disquete virtual encontrada nos caminhos de pesquisa especificados.</span><span class="sxs-lookup"><span data-stu-id="90956-115">An array of virtual floppy disk files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90956-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90956-116">Return value</span></span>

<span data-ttu-id="90956-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="90956-117">This method can return one of these values.</span></span>



| <span data-ttu-id="90956-118">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="90956-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="90956-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="90956-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="90956-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="90956-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="90956-121">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="90956-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="90956-122"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="90956-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="90956-123">O parâmetro *outFloppyDiskFileList* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="90956-123">The *outFloppyDiskFileList* parameter is **NULL**.</span></span><br/>                                   |
| <dl> <span data-ttu-id="90956-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="90956-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="90956-125">O parâmetro *inAdditionalSearchPaths* não é uma matriz de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="90956-125">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="90956-126"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="90956-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="90956-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="90956-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="90956-128"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="90956-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="90956-129">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="90956-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="90956-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="90956-130">Remarks</span></span>

<span data-ttu-id="90956-131">Os caminhos de pesquisa usados para recuperar a matriz de arquivos incluirão aqueles definidos anteriormente por [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) além daqueles especificados pelo parâmetro *inAdditionalSearchPaths* e o local do instalador para o módulo componentes de integração.</span><span class="sxs-lookup"><span data-stu-id="90956-131">The search paths used to retrieve the array of files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) in addition to those specified by the *inAdditionalSearchPaths* parameter and the installer location for the integration components module.</span></span>

## <a name="requirements"></a><span data-ttu-id="90956-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90956-132">Requirements</span></span>



| <span data-ttu-id="90956-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="90956-133">Requirement</span></span> | <span data-ttu-id="90956-134">Valor</span><span class="sxs-lookup"><span data-stu-id="90956-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="90956-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90956-135">Minimum supported client</span></span><br/> | <span data-ttu-id="90956-136">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="90956-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90956-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90956-137">Minimum supported server</span></span><br/> | <span data-ttu-id="90956-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="90956-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="90956-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="90956-139">End of client support</span></span><br/>    | <span data-ttu-id="90956-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="90956-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="90956-141">Produto</span><span class="sxs-lookup"><span data-stu-id="90956-141">Product</span></span><br/>                  | <span data-ttu-id="90956-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="90956-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="90956-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90956-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="90956-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="90956-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="90956-145">IID</span><span class="sxs-lookup"><span data-stu-id="90956-145">IID</span></span><br/>                      | <span data-ttu-id="90956-146">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="90956-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="90956-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="90956-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90956-148">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="90956-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

