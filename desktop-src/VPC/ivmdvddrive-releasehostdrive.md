---
title: Método IVMDVDDrive ReleaseHostDrive (VPCCOMInterfaces. h)
description: Libera uma unidade de host capturada da unidade de DVD.
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- ReleaseHostDrive do método virtual PC
- Método ReleaseHostDrive Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, método ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ed2c551ba619855743266b9b506a0c579f92a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369506"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a><span data-ttu-id="52ef2-106">Método IVMDVDDrive:: ReleaseHostDrive</span><span class="sxs-lookup"><span data-stu-id="52ef2-106">IVMDVDDrive::ReleaseHostDrive method</span></span>

<span data-ttu-id="52ef2-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="52ef2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="52ef2-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="52ef2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="52ef2-109">Libera uma unidade de host capturada da unidade de DVD.</span><span class="sxs-lookup"><span data-stu-id="52ef2-109">Releases a captured host drive from the DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="52ef2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52ef2-110">Syntax</span></span>


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a><span data-ttu-id="52ef2-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52ef2-111">Parameters</span></span>

<span data-ttu-id="52ef2-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="52ef2-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="52ef2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52ef2-113">Return value</span></span>

<span data-ttu-id="52ef2-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="52ef2-114">This method can return one of these values.</span></span>



| <span data-ttu-id="52ef2-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="52ef2-115">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="52ef2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="52ef2-116">Description</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="52ef2-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="52ef2-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="52ef2-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="52ef2-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="52ef2-119"><dt>**E \_ FALHA**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="52ef2-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="52ef2-120">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="52ef2-120">An unexpected error has occurred.</span></span><br/>                                  |
| <dl> <span data-ttu-id="52ef2-121"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="52ef2-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="52ef2-122">Não foi possível encontrar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="52ef2-122">The virtual machine could not be found.</span></span><br/>                            |
| <dl> <span data-ttu-id="52ef2-123"><dt>**VM \_ \_Mídia E \_ \_ tipo incorreto**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="52ef2-123"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="52ef2-124">A mídia capturada atualmente não é uma unidade de disco de host.</span><span class="sxs-lookup"><span data-stu-id="52ef2-124">The currently captured media is not a host disk drive.</span></span><br/>             |
| <dl> <span data-ttu-id="52ef2-125"><dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="52ef2-125"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="52ef2-126">A unidade não pôde ser inicializada devido a um local de barramento inválido.</span><span class="sxs-lookup"><span data-stu-id="52ef2-126">The drive could not be initialized due to an invalid bus location.</span></span><br/> |
| <dl> <span data-ttu-id="52ef2-127"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="52ef2-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="52ef2-128">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="52ef2-128">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="52ef2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52ef2-129">Requirements</span></span>



| <span data-ttu-id="52ef2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="52ef2-130">Requirement</span></span> | <span data-ttu-id="52ef2-131">Valor</span><span class="sxs-lookup"><span data-stu-id="52ef2-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="52ef2-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52ef2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="52ef2-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="52ef2-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52ef2-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52ef2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="52ef2-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="52ef2-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="52ef2-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="52ef2-136">End of client support</span></span><br/>    | <span data-ttu-id="52ef2-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52ef2-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="52ef2-138">Produto</span><span class="sxs-lookup"><span data-stu-id="52ef2-138">Product</span></span><br/>                  | <span data-ttu-id="52ef2-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="52ef2-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="52ef2-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52ef2-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="52ef2-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="52ef2-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="52ef2-142">IID</span><span class="sxs-lookup"><span data-stu-id="52ef2-142">IID</span></span><br/>                      | <span data-ttu-id="52ef2-143">IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="52ef2-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="52ef2-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="52ef2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52ef2-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="52ef2-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

