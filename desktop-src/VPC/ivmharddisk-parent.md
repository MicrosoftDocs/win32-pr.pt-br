---
title: Propriedade pai IVMHardDisk (VPCCOMInterfaces. h)
description: Pai do disco rígido virtual diferencial.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Propriedade pai Virtual PC
- Propriedade pai Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, Propriedade Parent
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9487750b67fc133f4b15f15050a74638f3d0f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917956"
---
# <a name="ivmharddiskparent-property"></a><span data-ttu-id="b484a-106">IVMHardDisk: Propriedade porcentagem de:P</span><span class="sxs-lookup"><span data-stu-id="b484a-106">IVMHardDisk::Parent property</span></span>

<span data-ttu-id="b484a-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b484a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b484a-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b484a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b484a-109">Recupera e define o pai do disco rígido virtual diferencial.</span><span class="sxs-lookup"><span data-stu-id="b484a-109">Retrieves and sets the parent of the differencing virtual hard disk.</span></span>

<span data-ttu-id="b484a-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b484a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b484a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b484a-111">Syntax</span></span>


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a><span data-ttu-id="b484a-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b484a-112">Property value</span></span>

<span data-ttu-id="b484a-113">Define o objeto [**IVMHardDisk**](ivmharddisk.md) associado à imagem do disco rígido pai.</span><span class="sxs-lookup"><span data-stu-id="b484a-113">Sets the [**IVMHardDisk**](ivmharddisk.md) object associated with the parent hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b484a-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b484a-114">Error codes</span></span>



| <span data-ttu-id="b484a-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="b484a-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="b484a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b484a-116">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b484a-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b484a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="b484a-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b484a-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="b484a-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="b484a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="b484a-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b484a-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="b484a-121"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b484a-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="b484a-122">Esse não é um disco rígido diferencial, portanto, ele não tem nenhum pai.</span><span class="sxs-lookup"><span data-stu-id="b484a-122">This is not a differencing hard disk, so it has no parent.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="b484a-123"><dt>HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="b484a-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="b484a-124">O sistema não pôde localizar o arquivo de disco rígido virtual pai.</span><span class="sxs-lookup"><span data-stu-id="b484a-124">The system could not find the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="b484a-125"><dt>HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="b484a-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="b484a-126">O sistema não pôde localizar o caminho para o arquivo de disco rígido virtual pai.</span><span class="sxs-lookup"><span data-stu-id="b484a-126">The system could not find the path to the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="b484a-127"><dt>VM \_ 0xA004067C \_ de \_ \_ \_ falha de abertura de imagem de HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b484a-127"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="b484a-128">Ocorreu um erro ao tentar abrir o arquivo de imagem de disco rígido atual.</span><span class="sxs-lookup"><span data-stu-id="b484a-128">An error occurred while attempting to open the current hard disk image file.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="b484a-129"><dt>VM \_ E & 0xA0040681 de \_ \_ \_ acesso de imagem de HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b484a-129"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="b484a-130">Ocorreu um erro ao tentar acessar o arquivo de imagem de disco rígido atual.</span><span class="sxs-lookup"><span data-stu-id="b484a-130">An error occurred while attempting to access the current hard disk image file.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="b484a-131"><dt>VM \_ Não \_ há \_ \_ \_ incompatibilidade de ID de filho pai do E</dt> <dt>0xA0040685</dt></span><span class="sxs-lookup"><span data-stu-id="b484a-131"><dt>VM\_E\_PARENT\_CHILD\_ID\_MISMATCH</dt> <dt>0xA0040685</dt></span></span> </dl>            | <span data-ttu-id="b484a-132">A imagem do disco rígido virtual localizado pelo parâmetro *pai* não tem a mesma ID da imagem do disco filho.</span><span class="sxs-lookup"><span data-stu-id="b484a-132">The virtual hard disk image located by the *parent* parameter does not have the same ID as the child disk image.</span></span> <span data-ttu-id="b484a-133">Verifique se a imagem do disco rígido virtual pai localizado pelo parâmetro *pai* é a mesma imagem usada para criar a imagem de disco rígido virtual diferencial.</span><span class="sxs-lookup"><span data-stu-id="b484a-133">Make sure the parent virtual hard disk image located by the *parent* parameter is the same image used to create the differencing virtual hard disk image.</span></span><br/> |
| <dl> <span data-ttu-id="b484a-134"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="b484a-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="b484a-135">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="b484a-135">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="b484a-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="b484a-136">Remarks</span></span>

<span data-ttu-id="b484a-137">Essa propriedade só é válida com imagens de disco rígido diferencial.</span><span class="sxs-lookup"><span data-stu-id="b484a-137">This property is only valid with differencing hard disk images.</span></span>

## <a name="requirements"></a><span data-ttu-id="b484a-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b484a-138">Requirements</span></span>



| <span data-ttu-id="b484a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b484a-139">Requirement</span></span> | <span data-ttu-id="b484a-140">Valor</span><span class="sxs-lookup"><span data-stu-id="b484a-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b484a-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b484a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b484a-142">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b484a-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b484a-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b484a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b484a-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b484a-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b484a-145">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b484a-145">End of client support</span></span><br/>    | <span data-ttu-id="b484a-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b484a-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b484a-147">Produto</span><span class="sxs-lookup"><span data-stu-id="b484a-147">Product</span></span><br/>                  | <span data-ttu-id="b484a-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b484a-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b484a-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b484a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="b484a-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b484a-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b484a-151">IID</span><span class="sxs-lookup"><span data-stu-id="b484a-151">IID</span></span><br/>                      | <span data-ttu-id="b484a-152">IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="b484a-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b484a-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="b484a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b484a-154">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="b484a-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

