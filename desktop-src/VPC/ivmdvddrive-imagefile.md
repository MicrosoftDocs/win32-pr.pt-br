---
title: Propriedade ImageFile de IVMDVDDrive (VPCCOMInterfaces. h)
description: Recupera o caminho completo do conjunto de arquivos de imagem para este dispositivo.
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- Propriedade ImageFile Virtual PC
- Propriedade ImageFile Virtual PC, interface IVMDVDDrive
- IVMDVDDrive da interface virtual PC, propriedade ImageFile
topic_type:
- apiref
api_name:
- IVMDVDDrive.ImageFile
- IVMDVDDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c71ed5328e41a72c9896147c6dcd824b2bd2ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824724"
---
# <a name="ivmdvddriveimagefile-property"></a><span data-ttu-id="89a7f-106">Propriedade IVMDVDDrive:: ImageFile</span><span class="sxs-lookup"><span data-stu-id="89a7f-106">IVMDVDDrive::ImageFile property</span></span>

<span data-ttu-id="89a7f-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="89a7f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="89a7f-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="89a7f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="89a7f-109">Recupera o caminho completo do conjunto de arquivos de imagem para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89a7f-109">Retrieves the full path of the image file set for this device.</span></span>

<span data-ttu-id="89a7f-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="89a7f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="89a7f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89a7f-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imagePath
);
```



## <a name="property-value"></a><span data-ttu-id="89a7f-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="89a7f-112">Property value</span></span>

<span data-ttu-id="89a7f-113">O caminho completo para o arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="89a7f-113">The full path to the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="89a7f-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="89a7f-114">Error codes</span></span>



| <span data-ttu-id="89a7f-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="89a7f-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="89a7f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="89a7f-116">Meaning</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89a7f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="89a7f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="89a7f-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="89a7f-118">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="89a7f-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="89a7f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="89a7f-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="89a7f-120">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="89a7f-121"><dt>E \_ FALHA</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="89a7f-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="89a7f-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="89a7f-122">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="89a7f-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="89a7f-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="89a7f-124">Não foi possível encontrar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="89a7f-124">The virtual machine could not be found.</span></span><br/>                        |
| <dl> <span data-ttu-id="89a7f-125"><dt>VM \_ Unidade E 0xA0040502 \_ \_ inválidas</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="89a7f-125"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="89a7f-126">O local do barramento desta unidade não é válido.</span><span class="sxs-lookup"><span data-stu-id="89a7f-126">The bus location for this drive is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="89a7f-127"><dt>VM \_ \_Mídia E \_ \_ tipo incorreto</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="89a7f-127"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="89a7f-128">A mídia capturada por esta unidade de DVD não é um arquivo de imagem ISO.</span><span class="sxs-lookup"><span data-stu-id="89a7f-128">The media captured by this DVD drive is not an ISO image file.</span></span><br/> |
| <dl> <span data-ttu-id="89a7f-129"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="89a7f-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="89a7f-130">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="89a7f-130">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="89a7f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89a7f-131">Requirements</span></span>



| <span data-ttu-id="89a7f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="89a7f-132">Requirement</span></span> | <span data-ttu-id="89a7f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="89a7f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a7f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89a7f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="89a7f-135">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="89a7f-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89a7f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89a7f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="89a7f-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="89a7f-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="89a7f-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="89a7f-138">End of client support</span></span><br/>    | <span data-ttu-id="89a7f-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="89a7f-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="89a7f-140">Produto</span><span class="sxs-lookup"><span data-stu-id="89a7f-140">Product</span></span><br/>                  | <span data-ttu-id="89a7f-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="89a7f-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="89a7f-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89a7f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="89a7f-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="89a7f-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="89a7f-144">IID</span><span class="sxs-lookup"><span data-stu-id="89a7f-144">IID</span></span><br/>                      | <span data-ttu-id="89a7f-145">IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="89a7f-145">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="89a7f-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="89a7f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a7f-147">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="89a7f-147">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

