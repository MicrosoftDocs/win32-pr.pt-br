---
title: Método IVMHardDiskConnection SetBusLocation (VPCCOMInterfaces. h)
description: Define o local do barramento ao qual este disco rígido está anexado.
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- SetBusLocation do método virtual PC
- Método SetBusLocation Virtual PC, interface IVMHardDiskConnection
- IVMHardDiskConnection interface virtual PC, método SetBusLocation
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61de0f595bc06d497e7f5913da9173ccb3bf1ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294751"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a><span data-ttu-id="b0004-106">Método IVMHardDiskConnection:: SetBusLocation</span><span class="sxs-lookup"><span data-stu-id="b0004-106">IVMHardDiskConnection::SetBusLocation method</span></span>

<span data-ttu-id="b0004-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b0004-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b0004-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b0004-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b0004-109">Define o local do barramento ao qual este disco rígido está anexado.</span><span class="sxs-lookup"><span data-stu-id="b0004-109">Sets the bus location to which this hard disk is attached.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0004-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0004-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="b0004-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0004-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0004-112">*vmBusNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0004-112">*vmBusNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0004-113">O número do barramento a ser usado.</span><span class="sxs-lookup"><span data-stu-id="b0004-113">The bus number to be used.</span></span>

</dd> <dt>

<span data-ttu-id="b0004-114">*vmDeviceNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0004-114">*vmDeviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0004-115">O número do dispositivo a ser usado.</span><span class="sxs-lookup"><span data-stu-id="b0004-115">The device number to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0004-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0004-116">Return value</span></span>

<span data-ttu-id="b0004-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b0004-117">This method can return one of these values.</span></span>



| <span data-ttu-id="b0004-118">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0004-118">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="b0004-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0004-119">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0004-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b0004-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="b0004-121">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b0004-121">The operation was successful.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="b0004-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b0004-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="b0004-123">O local do barramento especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="b0004-123">The bus location specified is not valid.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="b0004-124"><dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="b0004-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="b0004-125">Não foi possível definir o local do barramento porque a máquina virtual está em um estado em execução ou salvo.</span><span class="sxs-lookup"><span data-stu-id="b0004-125">The bus location could not be set because the virtual machine is in a running or saved state.</span></span><br/>    |
| <dl> <span data-ttu-id="b0004-126"><dt>**VM \_ \_ \_ Barramento de unidade E \_ loc \_ in \_ usar**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="b0004-126"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="b0004-127">O local do barramento não pôde ser definido porque outro dispositivo está conectado no momento a este local.</span><span class="sxs-lookup"><span data-stu-id="b0004-127">The bus location could not be set because another device is currently attached to this location.</span></span><br/> |
| <dl> <span data-ttu-id="b0004-128"><dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b0004-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="b0004-129">A unidade atual não é válida.</span><span class="sxs-lookup"><span data-stu-id="b0004-129">The current drive is not valid.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="b0004-130"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b0004-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="b0004-131">A máquina virtual atual não é válida.</span><span class="sxs-lookup"><span data-stu-id="b0004-131">The current virtual machine is not valid.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b0004-132"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="b0004-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="b0004-133">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="b0004-133">An unexpected error has occurred.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="b0004-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0004-134">Requirements</span></span>



| <span data-ttu-id="b0004-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0004-135">Requirement</span></span> | <span data-ttu-id="b0004-136">Valor</span><span class="sxs-lookup"><span data-stu-id="b0004-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0004-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0004-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b0004-138">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b0004-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b0004-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0004-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b0004-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b0004-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b0004-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b0004-141">End of client support</span></span><br/>    | <span data-ttu-id="b0004-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b0004-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b0004-143">Produto</span><span class="sxs-lookup"><span data-stu-id="b0004-143">Product</span></span><br/>                  | <span data-ttu-id="b0004-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b0004-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b0004-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0004-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0004-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0004-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b0004-147">IID</span><span class="sxs-lookup"><span data-stu-id="b0004-147">IID</span></span><br/>                      | <span data-ttu-id="b0004-148">IID \_ IVMHardDiskconnection é definido como aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="b0004-148">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="b0004-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0004-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0004-150">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="b0004-150">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

