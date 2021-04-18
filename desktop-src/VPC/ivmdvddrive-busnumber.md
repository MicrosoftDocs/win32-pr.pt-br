---
title: Propriedade IVMDVDDrive BusNumber (VPCCOMInterfaces. h)
description: Recupera o número do barramento ao qual este dispositivo está anexado.
ms.assetid: 8edc94da-22bc-4141-a6c7-1b18cca754fc
keywords:
- Propriedade BusNumber Virtual PC
- Propriedade BusNumber Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, Propriedade BusNumber
topic_type:
- apiref
api_name:
- IVMDVDDrive.BusNumber
- IVMDVDDrive.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056770b7eb11518645f3c28a6d45685795c7107a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789729"
---
# <a name="ivmdvddrivebusnumber-property"></a><span data-ttu-id="db602-106">Propriedade IVMDVDDrive:: BusNumber</span><span class="sxs-lookup"><span data-stu-id="db602-106">IVMDVDDrive::BusNumber property</span></span>

<span data-ttu-id="db602-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="db602-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="db602-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="db602-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="db602-109">Recupera o número do barramento ao qual este dispositivo está anexado.</span><span class="sxs-lookup"><span data-stu-id="db602-109">Retrieves the bus number to which this device is attached.</span></span>

<span data-ttu-id="db602-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="db602-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="db602-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db602-111">Syntax</span></span>


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a><span data-ttu-id="db602-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="db602-112">Property value</span></span>

<span data-ttu-id="db602-113">O número do barramento.</span><span class="sxs-lookup"><span data-stu-id="db602-113">The bus number.</span></span> <span data-ttu-id="db602-114">Por exemplo, em um barramento IDE, esse valor representaria o local primário ou secundário.</span><span class="sxs-lookup"><span data-stu-id="db602-114">For example, on an IDE bus, this value would represent either the primary or secondary location.</span></span>

## <a name="error-codes"></a><span data-ttu-id="db602-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="db602-115">Error codes</span></span>



| <span data-ttu-id="db602-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="db602-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="db602-117">Significado</span><span class="sxs-lookup"><span data-stu-id="db602-117">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db602-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="db602-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="db602-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="db602-119">The operation was successful.</span></span><br/>                                          |
| <dl> <span data-ttu-id="db602-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="db602-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="db602-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="db602-121">The parameter is **NULL**.</span></span><br/>                                             |
| <dl> <span data-ttu-id="db602-122"><dt>VM \_ Unidade E 0xA0040502 \_ \_ inválidas</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="db602-122"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="db602-123">O local do barramento desta unidade de DVD não foi inicializado corretamente.</span><span class="sxs-lookup"><span data-stu-id="db602-123">The bus location for this DVD drive has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="db602-124"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="db602-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="db602-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="db602-125">An unexpected error has occurred.</span></span><br/>                                      |



## <a name="requirements"></a><span data-ttu-id="db602-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db602-126">Requirements</span></span>



| <span data-ttu-id="db602-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="db602-127">Requirement</span></span> | <span data-ttu-id="db602-128">Valor</span><span class="sxs-lookup"><span data-stu-id="db602-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="db602-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db602-129">Minimum supported client</span></span><br/> | <span data-ttu-id="db602-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="db602-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db602-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db602-131">Minimum supported server</span></span><br/> | <span data-ttu-id="db602-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="db602-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="db602-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="db602-133">End of client support</span></span><br/>    | <span data-ttu-id="db602-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="db602-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="db602-135">Produto</span><span class="sxs-lookup"><span data-stu-id="db602-135">Product</span></span><br/>                  | <span data-ttu-id="db602-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="db602-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="db602-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db602-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="db602-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="db602-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="db602-139">IID</span><span class="sxs-lookup"><span data-stu-id="db602-139">IID</span></span><br/>                      | <span data-ttu-id="db602-140">IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="db602-140">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="db602-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="db602-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db602-142">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="db602-142">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

