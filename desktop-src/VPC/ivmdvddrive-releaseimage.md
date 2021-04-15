---
title: Método IVMDVDDrive ReleaseImage (VPCCOMInterfaces. h)
description: Libera uma imagem ISO capturada da unidade de DVD.
ms.assetid: 7cc95cf3-9d25-495f-863c-8eddd4068835
keywords:
- ReleaseImage do método virtual PC
- Método ReleaseImage Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, método ReleaseImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a36a13b258d155760269399d9f25f5eda6f296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454723"
---
# <a name="ivmdvddrivereleaseimage-method"></a><span data-ttu-id="ce0c5-106">Método IVMDVDDrive:: ReleaseImage</span><span class="sxs-lookup"><span data-stu-id="ce0c5-106">IVMDVDDrive::ReleaseImage method</span></span>

<span data-ttu-id="ce0c5-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ce0c5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ce0c5-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ce0c5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ce0c5-109">Libera uma imagem ISO capturada da unidade de DVD.</span><span class="sxs-lookup"><span data-stu-id="ce0c5-109">Releases a captured ISO image from the DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce0c5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce0c5-110">Syntax</span></span>


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a><span data-ttu-id="ce0c5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce0c5-111">Parameters</span></span>

<span data-ttu-id="ce0c5-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ce0c5-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce0c5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce0c5-113">Return value</span></span>

<span data-ttu-id="ce0c5-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ce0c5-114">This method can return one of these values.</span></span>



| <span data-ttu-id="ce0c5-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ce0c5-115">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="ce0c5-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce0c5-116">Description</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ce0c5-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ce0c5-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="ce0c5-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ce0c5-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="ce0c5-119"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ce0c5-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="ce0c5-120">Não foi possível encontrar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ce0c5-120">The virtual machine could not be found.</span></span><br/>                            |
| <dl> <span data-ttu-id="ce0c5-121"><dt>**VM \_ \_Mídia E \_ \_ tipo incorreto**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="ce0c5-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="ce0c5-122">A mídia capturada atualmente não é uma unidade de disco de host.</span><span class="sxs-lookup"><span data-stu-id="ce0c5-122">The currently captured media is not a host disk drive.</span></span><br/>             |
| <dl> <span data-ttu-id="ce0c5-123"><dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ce0c5-123"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="ce0c5-124">A unidade não pôde ser inicializada devido a um local de barramento inválido.</span><span class="sxs-lookup"><span data-stu-id="ce0c5-124">The drive could not be initialized due to an invalid bus location.</span></span><br/> |
| <dl> <span data-ttu-id="ce0c5-125"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="ce0c5-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="ce0c5-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="ce0c5-126">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="ce0c5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce0c5-127">Requirements</span></span>



| <span data-ttu-id="ce0c5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce0c5-128">Requirement</span></span> | <span data-ttu-id="ce0c5-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ce0c5-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce0c5-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce0c5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ce0c5-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ce0c5-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ce0c5-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce0c5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ce0c5-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ce0c5-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ce0c5-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ce0c5-134">End of client support</span></span><br/>    | <span data-ttu-id="ce0c5-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ce0c5-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ce0c5-136">Produto</span><span class="sxs-lookup"><span data-stu-id="ce0c5-136">Product</span></span><br/>                  | <span data-ttu-id="ce0c5-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ce0c5-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ce0c5-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce0c5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce0c5-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce0c5-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ce0c5-140">IID</span><span class="sxs-lookup"><span data-stu-id="ce0c5-140">IID</span></span><br/>                      | <span data-ttu-id="ce0c5-141">IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="ce0c5-141">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="ce0c5-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce0c5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce0c5-143">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="ce0c5-143">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

