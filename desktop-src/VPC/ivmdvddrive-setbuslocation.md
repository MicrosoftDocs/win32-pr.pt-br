---
title: Método IVMDVDDrive SetBusLocation (VPCCOMInterfaces. h)
description: Anexa a unidade de DVD ao local do barramento especificado na máquina virtual.
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- SetBusLocation do método virtual PC
- Método SetBusLocation Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, método SetBusLocation
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db6091493a56c020f57300e65328fee0eb65a69e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758568"
---
# <a name="ivmdvddrivesetbuslocation-method"></a><span data-ttu-id="f874e-106">Método IVMDVDDrive:: SetBusLocation</span><span class="sxs-lookup"><span data-stu-id="f874e-106">IVMDVDDrive::SetBusLocation method</span></span>

<span data-ttu-id="f874e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f874e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f874e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f874e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f874e-109">Anexa a unidade de DVD ao local do barramento especificado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f874e-109">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="f874e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f874e-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="f874e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f874e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f874e-112">*busNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f874e-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f874e-113">O número do barramento ao qual esta unidade deve ser anexada.</span><span class="sxs-lookup"><span data-stu-id="f874e-113">The bus number to which this drive is to be attached.</span></span> <span data-ttu-id="f874e-114">Por exemplo, em um barramento IDE, esse número representaria se o número de barramento primário ou secundário deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="f874e-114">For example, on an IDE bus, this number would represent whether to use the primary or secondary bus number.</span></span>

</dd> <dt>

<span data-ttu-id="f874e-115">*deviceNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f874e-115">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f874e-116">O número do dispositivo ao qual esta unidade deve ser anexada.</span><span class="sxs-lookup"><span data-stu-id="f874e-116">The device number to which this drive is to be attached.</span></span> <span data-ttu-id="f874e-117">Por exemplo, em um barramento IDE, esse número representaria se o local do dispositivo primário ou secundário deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="f874e-117">For example, on an IDE bus, this number would represent whether to use the primary or secondary device location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f874e-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f874e-118">Return value</span></span>

<span data-ttu-id="f874e-119">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="f874e-119">This method can return one of these values.</span></span>



| <span data-ttu-id="f874e-120">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f874e-120">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="f874e-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="f874e-121">Description</span></span>                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f874e-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f874e-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="f874e-123">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f874e-123">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="f874e-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="f874e-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="f874e-125">O local do barramento especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="f874e-125">The bus location specified is not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="f874e-126"><dt>**E \_ FALHA**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="f874e-126"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                       | <span data-ttu-id="f874e-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="f874e-127">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="f874e-128"><dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="f874e-128"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="f874e-129">O local do barramento não pode ser definido enquanto a máquina virtual está em execução ou está em um estado salvo.</span><span class="sxs-lookup"><span data-stu-id="f874e-129">The bus location cannot be set while the virtual machine is running or in a saved state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f874e-130"><dt>**\_E/ \_ s \_ de barramento da VM \_ em \_ uso**</dt></span><span class="sxs-lookup"><span data-stu-id="f874e-130"><dt>**VM\_E\_BUS\_LOC\_IN\_USE**</dt></span></span> </dl>                                                                      | <span data-ttu-id="f874e-131">Outro dispositivo já está conectado ao local do barramento especificado.</span><span class="sxs-lookup"><span data-stu-id="f874e-131">Another device is already attached to the specified bus location.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="f874e-132"><dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f874e-132"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="f874e-133">A unidade atual não pôde ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="f874e-133">The current drive could not be initialized.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="f874e-134"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f874e-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="f874e-135">Não foi possível gravar as alterações no arquivo de preferências porque a máquina virtual desta unidade não pôde ser determinada.</span><span class="sxs-lookup"><span data-stu-id="f874e-135">The changes could not be written to the preferences file because the virtual machine for this drive could not be determined.</span></span><br/> |
| <dl> <span data-ttu-id="f874e-136"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="f874e-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="f874e-137">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="f874e-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="f874e-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f874e-138">Requirements</span></span>



| <span data-ttu-id="f874e-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f874e-139">Requirement</span></span> | <span data-ttu-id="f874e-140">Valor</span><span class="sxs-lookup"><span data-stu-id="f874e-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f874e-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f874e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f874e-142">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f874e-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f874e-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f874e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f874e-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f874e-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f874e-145">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f874e-145">End of client support</span></span><br/>    | <span data-ttu-id="f874e-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f874e-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f874e-147">Produto</span><span class="sxs-lookup"><span data-stu-id="f874e-147">Product</span></span><br/>                  | <span data-ttu-id="f874e-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f874e-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f874e-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f874e-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="f874e-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f874e-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f874e-151">IID</span><span class="sxs-lookup"><span data-stu-id="f874e-151">IID</span></span><br/>                      | <span data-ttu-id="f874e-152">IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="f874e-152">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f874e-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="f874e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f874e-154">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="f874e-154">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

