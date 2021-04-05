---
title: Propriedade ImageFile de IVMFloppyDrive (VPCCOMInterfaces. h)
description: Recupera o caminho completo do arquivo de imagem ao qual a unidade de disquete está anexada.
ms.assetid: fc87e438-e5d4-494d-8ac2-27a4312ee81d
keywords:
- Propriedade ImageFile Virtual PC
- Propriedade ImageFile Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive da interface virtual PC, propriedade ImageFile
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ImageFile
- IVMFloppyDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa18c4a1da3137613e0106f828f59805e5615384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009580"
---
# <a name="ivmfloppydriveimagefile-property"></a><span data-ttu-id="68d69-106">Propriedade IVMFloppyDrive:: ImageFile</span><span class="sxs-lookup"><span data-stu-id="68d69-106">IVMFloppyDrive::ImageFile property</span></span>

<span data-ttu-id="68d69-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="68d69-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="68d69-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="68d69-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="68d69-109">Recupera o caminho completo do arquivo de imagem ao qual a unidade de disquete está anexada.</span><span class="sxs-lookup"><span data-stu-id="68d69-109">Retrieves the full path of the image file to which the floppy drive is attached.</span></span>

<span data-ttu-id="68d69-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="68d69-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="68d69-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68d69-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imageFile
);
```



## <a name="property-value"></a><span data-ttu-id="68d69-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="68d69-112">Property value</span></span>

<span data-ttu-id="68d69-113">O caminho completo do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="68d69-113">The full path of the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="68d69-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="68d69-114">Error codes</span></span>



| <span data-ttu-id="68d69-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="68d69-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="68d69-116">Significado</span><span class="sxs-lookup"><span data-stu-id="68d69-116">Meaning</span></span>                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68d69-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="68d69-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="68d69-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="68d69-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="68d69-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="68d69-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="68d69-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="68d69-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="68d69-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="68d69-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="68d69-122">A configuração desta máquina virtual não é válida ou não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="68d69-122">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="68d69-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="68d69-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="68d69-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="68d69-124">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="requirements"></a><span data-ttu-id="68d69-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68d69-125">Requirements</span></span>



| <span data-ttu-id="68d69-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="68d69-126">Requirement</span></span> | <span data-ttu-id="68d69-127">Valor</span><span class="sxs-lookup"><span data-stu-id="68d69-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="68d69-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68d69-128">Minimum supported client</span></span><br/> | <span data-ttu-id="68d69-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="68d69-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68d69-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68d69-130">Minimum supported server</span></span><br/> | <span data-ttu-id="68d69-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="68d69-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="68d69-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="68d69-132">End of client support</span></span><br/>    | <span data-ttu-id="68d69-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="68d69-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="68d69-134">Produto</span><span class="sxs-lookup"><span data-stu-id="68d69-134">Product</span></span><br/>                  | <span data-ttu-id="68d69-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="68d69-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="68d69-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68d69-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="68d69-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="68d69-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="68d69-138">IID</span><span class="sxs-lookup"><span data-stu-id="68d69-138">IID</span></span><br/>                      | <span data-ttu-id="68d69-139">IID \_ IVMFloppyDrive é definido como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="68d69-139">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="68d69-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="68d69-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68d69-141">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="68d69-141">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

