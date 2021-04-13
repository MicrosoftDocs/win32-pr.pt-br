---
title: Método IVMDVDDrive AttachImage (VPCCOMInterfaces. h)
description: Anexa uma imagem ISO à unidade de DVD na VM.
ms.assetid: 08947898-ca3f-41b6-97a3-52dc6977fc6d
keywords:
- AttachImage do método virtual PC
- Método AttachImage Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, método AttachImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58204545e21bd7dbf48d21acbc232b9fc5d1e3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369862"
---
# <a name="ivmdvddriveattachimage-method"></a><span data-ttu-id="bb29b-106">Método IVMDVDDrive:: AttachImage</span><span class="sxs-lookup"><span data-stu-id="bb29b-106">IVMDVDDrive::AttachImage method</span></span>

<span data-ttu-id="bb29b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bb29b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bb29b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bb29b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bb29b-109">Anexa uma imagem ISO à unidade de DVD na VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="bb29b-109">Attaches an ISO image to the DVD drive within the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="bb29b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb29b-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR imagePath
);
```



## <a name="parameters"></a><span data-ttu-id="bb29b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb29b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb29b-112">*imagePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bb29b-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb29b-113">O caminho completo para a imagem ISO que deve ser anexada.</span><span class="sxs-lookup"><span data-stu-id="bb29b-113">The full path to the ISO image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb29b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb29b-114">Return value</span></span>

<span data-ttu-id="bb29b-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="bb29b-115">This method can return one of these values.</span></span>



| <span data-ttu-id="bb29b-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bb29b-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="bb29b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb29b-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb29b-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bb29b-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="bb29b-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bb29b-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="bb29b-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="bb29b-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="bb29b-121">O parâmetro *imagePath* é um diretório.</span><span class="sxs-lookup"><span data-stu-id="bb29b-121">The *imagePath* parameter is a directory.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="bb29b-122"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="bb29b-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="bb29b-123">O parâmetro *imagePath* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bb29b-123">The *imagePath* parameter is **NULL**.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="bb29b-124"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bb29b-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="bb29b-125">Não foi possível encontrar a VM.</span><span class="sxs-lookup"><span data-stu-id="bb29b-125">The VM could not be found.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="bb29b-126"><dt>**VM \_ \_Unidade E \_ em \_ uso**</dt> <dt>0xA0040727</dt></span><span class="sxs-lookup"><span data-stu-id="bb29b-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="bb29b-127">Uma unidade de DVD de host ou imagem ISO já está conectada a esta unidade.</span><span class="sxs-lookup"><span data-stu-id="bb29b-127">A host DVD drive or ISO image is already attached to this drive.</span></span><br/>                                  |
| <dl> <span data-ttu-id="bb29b-128"><dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bb29b-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="bb29b-129">O local do barramento desta unidade é inválido ou a unidade não parece ser uma unidade de DVD válida.</span><span class="sxs-lookup"><span data-stu-id="bb29b-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/> |
| <dl> <span data-ttu-id="bb29b-130"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="bb29b-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="bb29b-131">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="bb29b-131">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="bb29b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb29b-132">Requirements</span></span>



| <span data-ttu-id="bb29b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb29b-133">Requirement</span></span> | <span data-ttu-id="bb29b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="bb29b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb29b-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb29b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bb29b-136">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bb29b-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb29b-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb29b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bb29b-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bb29b-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bb29b-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="bb29b-139">End of client support</span></span><br/>    | <span data-ttu-id="bb29b-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb29b-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bb29b-141">Produto</span><span class="sxs-lookup"><span data-stu-id="bb29b-141">Product</span></span><br/>                  | <span data-ttu-id="bb29b-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bb29b-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bb29b-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb29b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb29b-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb29b-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bb29b-145">IID</span><span class="sxs-lookup"><span data-stu-id="bb29b-145">IID</span></span><br/>                      | <span data-ttu-id="bb29b-146">IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="bb29b-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="bb29b-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb29b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb29b-148">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="bb29b-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

