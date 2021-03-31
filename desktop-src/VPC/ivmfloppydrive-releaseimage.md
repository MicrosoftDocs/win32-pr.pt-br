---
title: Método IVMFloppyDrive ReleaseImage (VPCCOMInterfaces. h)
description: Libera uma imagem de mídia de disquete no host da unidade de disquete.
ms.assetid: 12fc6dc4-8450-4122-b0f0-ed11cc10134c
keywords:
- ReleaseImage do método virtual PC
- Método ReleaseImage Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface virtual PC, método ReleaseImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece899bbb615fc2d54a3cbdc86193e743168ef23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644216"
---
# <a name="ivmfloppydrivereleaseimage-method"></a><span data-ttu-id="b8f14-106">Método IVMFloppyDrive:: ReleaseImage</span><span class="sxs-lookup"><span data-stu-id="b8f14-106">IVMFloppyDrive::ReleaseImage method</span></span>

<span data-ttu-id="b8f14-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b8f14-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b8f14-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b8f14-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b8f14-109">Libera uma imagem de mídia de disquete no host da unidade de disquete.</span><span class="sxs-lookup"><span data-stu-id="b8f14-109">Releases a floppy media image on the host from the floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f14-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8f14-110">Syntax</span></span>


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a><span data-ttu-id="b8f14-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8f14-111">Parameters</span></span>

<span data-ttu-id="b8f14-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b8f14-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8f14-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8f14-113">Return value</span></span>

<span data-ttu-id="b8f14-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b8f14-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b8f14-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b8f14-115">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="b8f14-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8f14-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8f14-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b8f14-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="b8f14-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b8f14-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b8f14-119"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b8f14-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>          | <span data-ttu-id="b8f14-120">A configuração desta máquina virtual não é válida ou não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="b8f14-120">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="b8f14-121"><dt>**VM \_ \_Mídia E \_ \_ tipo incorreto**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="b8f14-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl>  | <span data-ttu-id="b8f14-122">A mídia anexada a esta unidade de disquete não é uma imagem de disquete.</span><span class="sxs-lookup"><span data-stu-id="b8f14-122">The media attached to this floppy drive is not a floppy disk image.</span></span><br/>         |
| <dl> <span data-ttu-id="b8f14-123"><dt>**VM \_ E \_ nenhuma \_ mídia \_ capturada**</dt> <dt>0xA00400652</dt></span><span class="sxs-lookup"><span data-stu-id="b8f14-123"><dt>**VM\_E\_NO\_MEDIA\_CAPTURED**</dt> <dt>0xA00400652</dt></span></span> </dl> | <span data-ttu-id="b8f14-124">Não há mídia anexada a esta unidade de disquete.</span><span class="sxs-lookup"><span data-stu-id="b8f14-124">There is no media attached to this floppy drive.</span></span><br/>                            |
| <dl> <span data-ttu-id="b8f14-125"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="b8f14-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="b8f14-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="b8f14-126">An unexpected error has occurred.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="b8f14-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8f14-127">Requirements</span></span>



| <span data-ttu-id="b8f14-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8f14-128">Requirement</span></span> | <span data-ttu-id="b8f14-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b8f14-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f14-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8f14-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b8f14-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b8f14-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8f14-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8f14-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b8f14-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b8f14-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b8f14-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b8f14-134">End of client support</span></span><br/>    | <span data-ttu-id="b8f14-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b8f14-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b8f14-136">Produto</span><span class="sxs-lookup"><span data-stu-id="b8f14-136">Product</span></span><br/>                  | <span data-ttu-id="b8f14-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b8f14-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b8f14-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8f14-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8f14-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8f14-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b8f14-140">IID</span><span class="sxs-lookup"><span data-stu-id="b8f14-140">IID</span></span><br/>                      | <span data-ttu-id="b8f14-141">IID \_ IVMFloppyDrive é definido como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="b8f14-141">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="b8f14-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8f14-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f14-143">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="b8f14-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

