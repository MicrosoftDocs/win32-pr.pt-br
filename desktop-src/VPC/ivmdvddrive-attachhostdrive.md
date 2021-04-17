---
title: Método IVMDVDDrive AttachHostDrive (VPCCOMInterfaces. h)
description: Anexa uma unidade de host à unidade de DVD na máquina virtual.
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- AttachHostDrive do método virtual PC
- Método AttachHostDrive Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, método AttachHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012afcdc0b88aa5b77f1d85cc5becff1e70853f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105747726"
---
# <a name="ivmdvddriveattachhostdrive-method"></a><span data-ttu-id="4c3eb-106">Método IVMDVDDrive:: AttachHostDrive</span><span class="sxs-lookup"><span data-stu-id="4c3eb-106">IVMDVDDrive::AttachHostDrive method</span></span>

<span data-ttu-id="4c3eb-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4c3eb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4c3eb-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4c3eb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4c3eb-109">Anexa uma unidade de host à unidade de DVD na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4c3eb-109">Attaches a host drive to the DVD drive within the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c3eb-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c3eb-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="4c3eb-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c3eb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c3eb-112">*letra_da_unidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4c3eb-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c3eb-113">A letra da unidade do host a ser anexada.</span><span class="sxs-lookup"><span data-stu-id="4c3eb-113">The letter of the host drive that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c3eb-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c3eb-114">Return value</span></span>

<span data-ttu-id="4c3eb-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="4c3eb-115">This method can return one of these values.</span></span>



| <span data-ttu-id="4c3eb-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4c3eb-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="4c3eb-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c3eb-117">Description</span></span>                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c3eb-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4c3eb-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="4c3eb-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4c3eb-119">The operation was successful.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="4c3eb-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="4c3eb-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="4c3eb-121">Nenhuma letra de unidade foi especificada ou a letra da unidade especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="4c3eb-121">No drive letter was specified, or the specified drive letter is invalid.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="4c3eb-122"><dt>**E \_ FALHA**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="4c3eb-122"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>               | <span data-ttu-id="4c3eb-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="4c3eb-123">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="4c3eb-124"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4c3eb-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="4c3eb-125">Não foi possível encontrar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4c3eb-125">The virtual machine could not be found.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="4c3eb-126"><dt>**VM \_ \_Unidade E \_ em \_ uso**</dt> <dt>0xA0040727</dt></span><span class="sxs-lookup"><span data-stu-id="4c3eb-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="4c3eb-127">Uma unidade de DVD de host ou imagem ISO já está conectada a esta unidade na máquina virtual ou a unidade host especificada já está em uso em outra máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4c3eb-127">A host DVD drive or ISO image is already attached to this drive within the virtual machine, or the specified host drive is already in use within another virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="4c3eb-128"><dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4c3eb-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="4c3eb-129">O local do barramento desta unidade é inválido ou a unidade não parece ser uma unidade de DVD válida.</span><span class="sxs-lookup"><span data-stu-id="4c3eb-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="4c3eb-130"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="4c3eb-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="4c3eb-131">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="4c3eb-131">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="4c3eb-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c3eb-132">Requirements</span></span>



| <span data-ttu-id="4c3eb-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c3eb-133">Requirement</span></span> | <span data-ttu-id="4c3eb-134">Valor</span><span class="sxs-lookup"><span data-stu-id="4c3eb-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c3eb-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c3eb-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4c3eb-136">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4c3eb-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c3eb-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c3eb-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4c3eb-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4c3eb-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4c3eb-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4c3eb-139">End of client support</span></span><br/>    | <span data-ttu-id="4c3eb-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c3eb-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4c3eb-141">Produto</span><span class="sxs-lookup"><span data-stu-id="4c3eb-141">Product</span></span><br/>                  | <span data-ttu-id="4c3eb-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4c3eb-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4c3eb-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c3eb-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c3eb-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c3eb-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4c3eb-145">IID</span><span class="sxs-lookup"><span data-stu-id="4c3eb-145">IID</span></span><br/>                      | <span data-ttu-id="4c3eb-146">IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="4c3eb-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="4c3eb-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c3eb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c3eb-148">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="4c3eb-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

