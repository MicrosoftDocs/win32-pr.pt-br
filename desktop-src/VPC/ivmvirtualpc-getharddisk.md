---
title: Método IVMVirtualPC GetHardDisk (VPCCOMInterfaces. h)
description: Recupera um objeto correspondente a um arquivo de imagem de disco existente.
ms.assetid: 648a3f8a-5114-4c14-b9a9-f175941333ab
keywords:
- GetHardDisk do método virtual PC
- Método GetHardDisk Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método GetHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 558d098b6745718830c63dd700c14febf4f6bed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918931"
---
# <a name="ivmvirtualpcgetharddisk-method"></a><span data-ttu-id="bd2cf-106">Método IVMVirtualPC:: GetHardDisk</span><span class="sxs-lookup"><span data-stu-id="bd2cf-106">IVMVirtualPC::GetHardDisk method</span></span>

<span data-ttu-id="bd2cf-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bd2cf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bd2cf-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bd2cf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bd2cf-109">Recupera um objeto correspondente a um arquivo de imagem de disco existente.</span><span class="sxs-lookup"><span data-stu-id="bd2cf-109">Retrieves an object corresponding to an existing disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd2cf-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd2cf-110">Syntax</span></span>


```C++
HRESULT GetHardDisk(
  [in]          BSTR        imagePath,
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="parameters"></a><span data-ttu-id="bd2cf-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd2cf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd2cf-112">*imagePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bd2cf-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd2cf-113">O caminho completo para um arquivo de imagem de disco existente.</span><span class="sxs-lookup"><span data-stu-id="bd2cf-113">The full path to an existing disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="bd2cf-114">*HD* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bd2cf-114">*hardDisk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bd2cf-115">Um objeto [**IVMHardDisk**](ivmharddisk.md) correspondente a esta imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="bd2cf-115">An [**IVMHardDisk**](ivmharddisk.md) object corresponding to this disk image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd2cf-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bd2cf-116">Return value</span></span>

<span data-ttu-id="bd2cf-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="bd2cf-117">This method can return one of these values.</span></span>



| <span data-ttu-id="bd2cf-118">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bd2cf-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="bd2cf-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd2cf-119">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd2cf-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bd2cf-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="bd2cf-121">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bd2cf-121">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="bd2cf-122"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="bd2cf-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="bd2cf-123">O parâmetro *imagePath* ou *HD* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bd2cf-123">The *imagePath* or *hardDisk* parameter is **NULL**.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="bd2cf-124"><dt>**HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="bd2cf-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="bd2cf-125">O sistema não pode localizar o arquivo especificado pelo parâmetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="bd2cf-125">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="bd2cf-126"><dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="bd2cf-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="bd2cf-127">O sistema não pode localizar o caminho especificado pelo parâmetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="bd2cf-127">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="bd2cf-128"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="bd2cf-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="bd2cf-129">O parâmetro *imagePath* contém um caractere inválido (um de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="bd2cf-129">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="bd2cf-130"><dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="bd2cf-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="bd2cf-131">O parâmetro *imagePath* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="bd2cf-131">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="bd2cf-132">Um caminho absoluto é necessário.</span><span class="sxs-lookup"><span data-stu-id="bd2cf-132">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="bd2cf-133"><dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="bd2cf-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="bd2cf-134">O caminho especificado pelo parâmetro *imagePath* é muito longo.</span><span class="sxs-lookup"><span data-stu-id="bd2cf-134">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="bd2cf-135">O comprimento do caminho deve ter menos de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="bd2cf-135">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="bd2cf-136"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="bd2cf-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="bd2cf-137">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="bd2cf-137">An unexpected error has occurred.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="bd2cf-138"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bd2cf-138"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="bd2cf-139">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="bd2cf-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="bd2cf-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd2cf-140">Requirements</span></span>



| <span data-ttu-id="bd2cf-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd2cf-141">Requirement</span></span> | <span data-ttu-id="bd2cf-142">Valor</span><span class="sxs-lookup"><span data-stu-id="bd2cf-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd2cf-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd2cf-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bd2cf-144">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bd2cf-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bd2cf-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd2cf-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bd2cf-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bd2cf-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bd2cf-147">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="bd2cf-147">End of client support</span></span><br/>    | <span data-ttu-id="bd2cf-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bd2cf-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bd2cf-149">Produto</span><span class="sxs-lookup"><span data-stu-id="bd2cf-149">Product</span></span><br/>                  | <span data-ttu-id="bd2cf-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bd2cf-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bd2cf-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd2cf-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd2cf-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd2cf-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bd2cf-153">IID</span><span class="sxs-lookup"><span data-stu-id="bd2cf-153">IID</span></span><br/>                      | <span data-ttu-id="bd2cf-154">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="bd2cf-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="bd2cf-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd2cf-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd2cf-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="bd2cf-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

