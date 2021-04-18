---
title: Método IVMVirtualMachine AddDVDROMDrive (VPCCOMInterfaces. h)
description: Adiciona uma nova unidade de CD ou DVD à máquina virtual.
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- AddDVDROMDrive do método virtual PC
- Método AddDVDROMDrive Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método AddDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7acbe70f6b338b3490c12ab67bcdfdc997d90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781125"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a><span data-ttu-id="4401d-106">Método IVMVirtualMachine:: AddDVDROMDrive</span><span class="sxs-lookup"><span data-stu-id="4401d-106">IVMVirtualMachine::AddDVDROMDrive method</span></span>

<span data-ttu-id="4401d-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4401d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4401d-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4401d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4401d-109">Adiciona uma nova unidade de CD ou DVD à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4401d-109">Adds a new CD or DVD drive to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="4401d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4401d-110">Syntax</span></span>


```C++
HRESULT AddDVDROMDrive(
  [in]          long        busNumber,
  [in]          long        deviceNumber,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="4401d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4401d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4401d-112">*busNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4401d-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4401d-113">O barramento ao qual a unidade será anexada.</span><span class="sxs-lookup"><span data-stu-id="4401d-113">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="4401d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="4401d-114">Value</span></span>                                                                        | <span data-ttu-id="4401d-115">Significado</span><span class="sxs-lookup"><span data-stu-id="4401d-115">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="4401d-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4401d-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="4401d-117">A unidade será anexada ao primeiro barramento.</span><span class="sxs-lookup"><span data-stu-id="4401d-117">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="4401d-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4401d-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="4401d-119">A unidade será anexada ao segundo barramento.</span><span class="sxs-lookup"><span data-stu-id="4401d-119">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4401d-120">*deviceNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4401d-120">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4401d-121">O dispositivo ao qual a unidade será anexada.</span><span class="sxs-lookup"><span data-stu-id="4401d-121">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="4401d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4401d-122">Value</span></span>                                                                        | <span data-ttu-id="4401d-123">Significado</span><span class="sxs-lookup"><span data-stu-id="4401d-123">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4401d-124"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4401d-124"><dt>0</dt></span></span> </dl> | <span data-ttu-id="4401d-125">A unidade será anexada ao primeiro dispositivo no barramento.</span><span class="sxs-lookup"><span data-stu-id="4401d-125">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="4401d-126"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4401d-126"><dt>1</dt></span></span> </dl> | <span data-ttu-id="4401d-127">A unidade será anexada ao segundo dispositivo no barramento.</span><span class="sxs-lookup"><span data-stu-id="4401d-127">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4401d-128">*dvdDrive* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4401d-128">*dvdDrive* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4401d-129">Um objeto [**IVMDVDDrive**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="4401d-129">An [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4401d-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4401d-130">Return value</span></span>

<span data-ttu-id="4401d-131">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="4401d-131">This method can return one of these values.</span></span>



| <span data-ttu-id="4401d-132">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4401d-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="4401d-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="4401d-133">Description</span></span>                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="4401d-134"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4401d-134"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="4401d-135">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4401d-135">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="4401d-136"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="4401d-136"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                       | <span data-ttu-id="4401d-137">O parâmetro *dvdDrive* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4401d-137">The *dvdDrive* parameter is **NULL**.</span></span><br/>               |
| <dl> <span data-ttu-id="4401d-138"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="4401d-138"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="4401d-139">Um parâmetro não é válido.</span><span class="sxs-lookup"><span data-stu-id="4401d-139">A parameter is not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="4401d-140"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4401d-140"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="4401d-141">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="4401d-141">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="4401d-142"><dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="4401d-142"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="4401d-143">A máquina virtual está em um estado em execução ou salvo.</span><span class="sxs-lookup"><span data-stu-id="4401d-143">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="4401d-144"><dt>**VM \_ \_ \_ Barramento de unidade E \_ loc \_ in \_ usar**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="4401d-144"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="4401d-145">O local do barramento especificado está em uso.</span><span class="sxs-lookup"><span data-stu-id="4401d-145">The specified bus location is in use.</span></span><br/>               |
| <dl> <span data-ttu-id="4401d-146"><dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4401d-146"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="4401d-147">A unidade especificada não é válida.</span><span class="sxs-lookup"><span data-stu-id="4401d-147">The drive specified is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="4401d-148"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="4401d-148"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="4401d-149">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="4401d-149">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="4401d-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="4401d-150">Remarks</span></span>

<span data-ttu-id="4401d-151">Você só pode adicionar uma nova unidade de CD ou DVD a uma máquina virtual parada.</span><span class="sxs-lookup"><span data-stu-id="4401d-151">You can only add a new CD or DVD drive to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="4401d-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4401d-152">Requirements</span></span>



| <span data-ttu-id="4401d-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="4401d-153">Requirement</span></span> | <span data-ttu-id="4401d-154">Valor</span><span class="sxs-lookup"><span data-stu-id="4401d-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4401d-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4401d-155">Minimum supported client</span></span><br/> | <span data-ttu-id="4401d-156">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4401d-156">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4401d-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4401d-157">Minimum supported server</span></span><br/> | <span data-ttu-id="4401d-158">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4401d-158">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4401d-159">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4401d-159">End of client support</span></span><br/>    | <span data-ttu-id="4401d-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4401d-160">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4401d-161">Produto</span><span class="sxs-lookup"><span data-stu-id="4401d-161">Product</span></span><br/>                  | <span data-ttu-id="4401d-162">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4401d-162">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4401d-163">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4401d-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="4401d-164"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4401d-164"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4401d-165">IID</span><span class="sxs-lookup"><span data-stu-id="4401d-165">IID</span></span><br/>                      | <span data-ttu-id="4401d-166">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="4401d-166">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4401d-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="4401d-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4401d-168">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="4401d-168">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

