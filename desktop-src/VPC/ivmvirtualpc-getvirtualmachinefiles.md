---
title: Método IVMVirtualPC GetVirtualMachineFiles (VPCCOMInterfaces. h)
description: Recupera uma matriz de arquivos de configuração de máquina virtual conhecidos.
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- GetVirtualMachineFiles do método virtual PC
- Método GetVirtualMachineFiles Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método GetVirtualMachineFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d1fe248b76756b39846d181341278f669d2f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295893"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a><span data-ttu-id="e7410-106">Método IVMVirtualPC:: GetVirtualMachineFiles</span><span class="sxs-lookup"><span data-stu-id="e7410-106">IVMVirtualPC::GetVirtualMachineFiles method</span></span>

<span data-ttu-id="e7410-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e7410-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e7410-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e7410-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e7410-109">Recupera uma matriz de arquivos de configuração de máquina virtual conhecidos.</span><span class="sxs-lookup"><span data-stu-id="e7410-109">Retrieves an array of known virtual machine configuration files.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7410-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7410-110">Syntax</span></span>


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a><span data-ttu-id="e7410-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7410-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7410-112">*inAdditionalSearchPaths* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7410-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7410-113">Esses caminhos serão pesquisados juntamente com os caminhos definidos nas propriedades [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) e [**IVMVirtualPC::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) .</span><span class="sxs-lookup"><span data-stu-id="e7410-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="e7410-114">*inExcludedRegisteredVMs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7410-114">*inExcludedRegisteredVMs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7410-115">**True** se as máquinas virtuais registradas devem ser excluídas do retorno da matriz no parâmetro *outVirtualMachineFileList* ; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="e7410-115">**TRUE** if registered virtual machines should be excluded from the array return in the *outVirtualMachineFileList* parameter and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="e7410-116">*outVirtualMachineFileList* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e7410-116">*outVirtualMachineFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e7410-117">Uma matriz de cadeias de caracteres de caminho para os arquivos de configuração de máquina virtual encontrados nos caminhos de pesquisa especificados.</span><span class="sxs-lookup"><span data-stu-id="e7410-117">An array of path strings for the virtual machine configuration files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7410-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7410-118">Return value</span></span>

<span data-ttu-id="e7410-119">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="e7410-119">This method can return one of these values.</span></span>



| <span data-ttu-id="e7410-120">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e7410-120">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="e7410-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7410-121">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e7410-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e7410-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="e7410-123">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e7410-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e7410-124"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="e7410-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="e7410-125">O parâmetro *outVirtualMachineFileList* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e7410-125">The *outVirtualMachineFileList* parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="e7410-126"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e7410-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="e7410-127">O parâmetro *inAdditionalSearchPaths* não é uma matriz de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e7410-127">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="e7410-128"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="e7410-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="e7410-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="e7410-129">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="e7410-130"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e7410-130"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="e7410-131">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="e7410-131">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e7410-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7410-132">Remarks</span></span>

<span data-ttu-id="e7410-133">Os caminhos de pesquisa usados para recuperar a matriz de arquivos de configuração incluirão aqueles definidos anteriormente por [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) e [**IVMVirtualPC::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) além daqueles especificados pelo parâmetro *inAdditionalSearchPaths* .</span><span class="sxs-lookup"><span data-stu-id="e7410-133">The search paths used to retrieve the array of configuration files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) in addition to those specified by the *inAdditionalSearchPaths* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7410-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7410-134">Requirements</span></span>



| <span data-ttu-id="e7410-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7410-135">Requirement</span></span> | <span data-ttu-id="e7410-136">Valor</span><span class="sxs-lookup"><span data-stu-id="e7410-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7410-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7410-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e7410-138">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e7410-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7410-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7410-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e7410-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e7410-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e7410-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e7410-141">End of client support</span></span><br/>    | <span data-ttu-id="e7410-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7410-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e7410-143">Produto</span><span class="sxs-lookup"><span data-stu-id="e7410-143">Product</span></span><br/>                  | <span data-ttu-id="e7410-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e7410-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e7410-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7410-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7410-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7410-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e7410-147">IID</span><span class="sxs-lookup"><span data-stu-id="e7410-147">IID</span></span><br/>                      | <span data-ttu-id="e7410-148">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="e7410-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e7410-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7410-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7410-150">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="e7410-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

