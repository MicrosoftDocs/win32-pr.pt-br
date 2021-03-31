---
title: Propriedade IVMVirtualPC DefaultVMConfigurationPath (VPCCOMInterfaces. h)
description: Diretório padrão a ser procurado por arquivos de configuração de máquina virtual disponíveis.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- Propriedade DefaultVMConfigurationPath Virtual PC
- Propriedade DefaultVMConfigurationPath Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, Propriedade DefaultVMConfigurationPath
topic_type:
- apiref
api_name:
- IVMVirtualPC.DefaultVMConfigurationPath
- IVMVirtualPC.get_DefaultVMConfigurationPath
- IVMVirtualPC.put_DefaultVMConfigurationPath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e13fc2323cb15bdbeb8c42e61810a376e49b3988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644957"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a><span data-ttu-id="a9613-106">IVMVirtualPC: Propriedade efaultVMConfigurationPath de:D</span><span class="sxs-lookup"><span data-stu-id="a9613-106">IVMVirtualPC::DefaultVMConfigurationPath property</span></span>

<span data-ttu-id="a9613-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a9613-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a9613-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a9613-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a9613-109">Recupera e define o diretório padrão a ser procurado por arquivos de configuração de máquina virtual disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a9613-109">Retrieves and sets the default directory to be searched for available virtual machine configuration files.</span></span>

<span data-ttu-id="a9613-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a9613-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9613-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9613-111">Syntax</span></span>


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a><span data-ttu-id="a9613-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a9613-112">Property value</span></span>

<span data-ttu-id="a9613-113">Especifica o caminho do diretório para os arquivos de configuração padrão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a9613-113">Specifies the directory path for the default virtual machine configuration files.</span></span> <span data-ttu-id="a9613-114">Na cadeia de caracteres de caminho, uma barra invertida ( \) pode aparecer imediatamente antes do caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="a9613-114">In the path string, a backslash (\) may appear immediately before the terminating null character.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a9613-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a9613-115">Error codes</span></span>



| <span data-ttu-id="a9613-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="a9613-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="a9613-117">Significado</span><span class="sxs-lookup"><span data-stu-id="a9613-117">Meaning</span></span>                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a9613-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a9613-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="a9613-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a9613-119">The operation was successful.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="a9613-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="a9613-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="a9613-121">O parâmetro *configurationPath* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a9613-121">The *configurationPath* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="a9613-122"><dt>HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="a9613-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="a9613-123">O sistema não pode localizar o diretório especificado pelo parâmetro *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="a9613-123">The system cannot find the directory specified by the *configurationPath* parameter.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="a9613-124"><dt>HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="a9613-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="a9613-125">O sistema não pode localizar o caminho especificado pelo parâmetro *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="a9613-125">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="a9613-126"><dt>HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="a9613-126"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="a9613-127">O parâmetro *configurationPath* contém um caractere inválido (um dos seguintes: " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="a9613-127">The *configurationPath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                   |
| <dl> <span data-ttu-id="a9613-128"><dt>HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="a9613-128"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="a9613-129">O parâmetro *configurationPath* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="a9613-129">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="a9613-130">Um caminho absoluto é necessário.</span><span class="sxs-lookup"><span data-stu-id="a9613-130">An absolute path is required.</span></span><br/>                                          |
| <dl> <span data-ttu-id="a9613-131"><dt>HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="a9613-131"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="a9613-132">O caminho especificado pelo parâmetro *configurationPath* é muito longo.</span><span class="sxs-lookup"><span data-stu-id="a9613-132">The path specified by the *configurationPath* parameter is too long.</span></span> <span data-ttu-id="a9613-133">O comprimento do caminho deve ser menor que o **\_ caminho máximo** (260) caracteres.</span><span class="sxs-lookup"><span data-stu-id="a9613-133">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="a9613-134"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="a9613-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="a9613-135">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="a9613-135">An unexpected error has occurred.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="a9613-136"><dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a9613-136"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="a9613-137">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="a9613-137">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                          |



## <a name="remarks"></a><span data-ttu-id="a9613-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9613-138">Remarks</span></span>

<span data-ttu-id="a9613-139">Por padrão, esse valor de propriedade é definido como o seguinte diretório: "% LocalAppData% \\ Microsoft \\ Windows Virtual PC \\ Virtual Machines \\ ".</span><span class="sxs-lookup"><span data-stu-id="a9613-139">By default, this property value is set to the following directory: "%LocalAppData%\\Microsoft\\Windows Virtual PC\\Virtual Machines\\".</span></span>

## <a name="requirements"></a><span data-ttu-id="a9613-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9613-140">Requirements</span></span>



| <span data-ttu-id="a9613-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9613-141">Requirement</span></span> | <span data-ttu-id="a9613-142">Valor</span><span class="sxs-lookup"><span data-stu-id="a9613-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9613-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9613-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a9613-144">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a9613-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9613-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9613-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a9613-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a9613-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a9613-147">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a9613-147">End of client support</span></span><br/>    | <span data-ttu-id="a9613-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9613-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a9613-149">Produto</span><span class="sxs-lookup"><span data-stu-id="a9613-149">Product</span></span><br/>                  | <span data-ttu-id="a9613-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a9613-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a9613-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9613-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9613-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9613-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a9613-153">IID</span><span class="sxs-lookup"><span data-stu-id="a9613-153">IID</span></span><br/>                      | <span data-ttu-id="a9613-154">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="a9613-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a9613-155">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a9613-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9613-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="a9613-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

