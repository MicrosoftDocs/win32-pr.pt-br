---
title: Propriedade IVMDVDDrive HostDriveLetter (VPCCOMInterfaces. h)
description: A letra da unidade do host definida para este dispositivo.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- Propriedade HostDriveLetter Virtual PC
- Propriedade HostDriveLetter Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, Propriedade HostDriveLetter
topic_type:
- apiref
api_name:
- IVMDVDDrive.HostDriveLetter
- IVMDVDDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60d2599b8fb73e727100111dc37d29a9d13c5d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644548"
---
# <a name="ivmdvddrivehostdriveletter-property"></a><span data-ttu-id="726df-106">Propriedade IVMDVDDrive:: HostDriveLetter</span><span class="sxs-lookup"><span data-stu-id="726df-106">IVMDVDDrive::HostDriveLetter property</span></span>

<span data-ttu-id="726df-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="726df-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="726df-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="726df-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="726df-109">Recupera a letra do conjunto de unidades do host para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="726df-109">Retrieves the letter of the host drive set for this device.</span></span>

<span data-ttu-id="726df-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="726df-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="726df-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="726df-111">Syntax</span></span>


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a><span data-ttu-id="726df-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="726df-112">Property value</span></span>

<span data-ttu-id="726df-113">A letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="726df-113">The drive letter.</span></span>

## <a name="error-codes"></a><span data-ttu-id="726df-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="726df-114">Error codes</span></span>



| <span data-ttu-id="726df-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="726df-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="726df-116">Significado</span><span class="sxs-lookup"><span data-stu-id="726df-116">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="726df-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="726df-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="726df-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="726df-118">The operation was successful.</span></span><br/>                             |
| <dl> <span data-ttu-id="726df-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="726df-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="726df-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="726df-120">The parameter is **NULL**.</span></span><br/>                                |
| <dl> <span data-ttu-id="726df-121"><dt>E \_ FALHA</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="726df-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="726df-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="726df-122">An unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="726df-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="726df-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="726df-124">Não foi possível encontrar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="726df-124">The virtual machine could not be found.</span></span><br/>                   |
| <dl> <span data-ttu-id="726df-125"><dt>VM \_ \_Mídia E \_ \_ tipo incorreto</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="726df-125"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="726df-126">A mídia capturada por esta unidade de DVD não é uma unidade host.</span><span class="sxs-lookup"><span data-stu-id="726df-126">The media captured by this DVD drive is not a host drive.</span></span><br/> |
| <dl> <span data-ttu-id="726df-127"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="726df-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="726df-128">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="726df-128">An unexpected error has occurred.</span></span><br/>                         |



## <a name="requirements"></a><span data-ttu-id="726df-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="726df-129">Requirements</span></span>



| <span data-ttu-id="726df-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="726df-130">Requirement</span></span> | <span data-ttu-id="726df-131">Valor</span><span class="sxs-lookup"><span data-stu-id="726df-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="726df-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="726df-132">Minimum supported client</span></span><br/> | <span data-ttu-id="726df-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="726df-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="726df-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="726df-134">Minimum supported server</span></span><br/> | <span data-ttu-id="726df-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="726df-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="726df-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="726df-136">End of client support</span></span><br/>    | <span data-ttu-id="726df-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="726df-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="726df-138">Produto</span><span class="sxs-lookup"><span data-stu-id="726df-138">Product</span></span><br/>                  | <span data-ttu-id="726df-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="726df-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="726df-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="726df-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="726df-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="726df-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="726df-142">IID</span><span class="sxs-lookup"><span data-stu-id="726df-142">IID</span></span><br/>                      | <span data-ttu-id="726df-143">IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="726df-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="726df-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="726df-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="726df-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="726df-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

