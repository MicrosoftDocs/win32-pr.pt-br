---
title: Método IVMFloppyDrive AttachHostDrive (VPCCOMInterfaces. h)
description: Anexa uma unidade física no host à unidade de disquete na máquina virtual.
ms.assetid: 9be84e06-e38a-419a-be50-dddd0cc6d2dd
keywords:
- AttachHostDrive do método virtual PC
- Método AttachHostDrive Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface virtual PC, método AttachHostDrive
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a21785e3e1e4ec77146f048ab4cce018de9d8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009503"
---
# <a name="ivmfloppydriveattachhostdrive-method"></a><span data-ttu-id="944b5-106">Método IVMFloppyDrive:: AttachHostDrive</span><span class="sxs-lookup"><span data-stu-id="944b5-106">IVMFloppyDrive::AttachHostDrive method</span></span>

<span data-ttu-id="944b5-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="944b5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="944b5-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="944b5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="944b5-109">Anexa uma unidade física no host à unidade de disquete na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="944b5-109">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="944b5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="944b5-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="944b5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="944b5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="944b5-112">*letra_da_unidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="944b5-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="944b5-113">A letra da unidade da unidade de disquete física no computador host deve ser conectada.</span><span class="sxs-lookup"><span data-stu-id="944b5-113">The drive letter of the physical floppy drive on the host machine to is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="944b5-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="944b5-114">Return value</span></span>

<span data-ttu-id="944b5-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="944b5-115">This method can return one of these values.</span></span>



| <span data-ttu-id="944b5-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="944b5-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="944b5-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="944b5-117">Description</span></span>                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="944b5-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="944b5-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="944b5-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="944b5-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="944b5-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="944b5-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="944b5-121">O parâmetro *driveLetter* é **nulo**, não é uma unidade de disquete válida ou o caminho fornecido está vazio.</span><span class="sxs-lookup"><span data-stu-id="944b5-121">The *driveLetter* parameter is **NULL**, is not a valid floppy drive, or the given path is empty.</span></span><br/> |
| <dl> <span data-ttu-id="944b5-122"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="944b5-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="944b5-123">A configuração desta máquina virtual não é válida ou não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="944b5-123">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                       |
| <dl> <span data-ttu-id="944b5-124"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="944b5-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="944b5-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="944b5-125">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="944b5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="944b5-126">Requirements</span></span>



| <span data-ttu-id="944b5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="944b5-127">Requirement</span></span> | <span data-ttu-id="944b5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="944b5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="944b5-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="944b5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="944b5-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="944b5-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="944b5-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="944b5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="944b5-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="944b5-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="944b5-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="944b5-133">End of client support</span></span><br/>    | <span data-ttu-id="944b5-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="944b5-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="944b5-135">Produto</span><span class="sxs-lookup"><span data-stu-id="944b5-135">Product</span></span><br/>                  | <span data-ttu-id="944b5-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="944b5-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="944b5-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="944b5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="944b5-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="944b5-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="944b5-139">IID</span><span class="sxs-lookup"><span data-stu-id="944b5-139">IID</span></span><br/>                      | <span data-ttu-id="944b5-140">IID \_ IVMFloppyDrive é definido como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="944b5-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="944b5-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="944b5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="944b5-142">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="944b5-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

