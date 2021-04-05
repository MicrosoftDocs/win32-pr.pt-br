---
title: Propriedade Manufacturerstring do IVMUSBDevice (VPCCOMInterfaces. h)
description: Recupera o nome do fabricante do dispositivo USB.
ms.assetid: 0d815887-96bf-4795-a4eb-32fb2f35c57e
keywords:
- Propriedade manufacturerstring Virtual PC
- Propriedade manufacturerstring Virtual PC, interface IVMUSBDevice
- IVMUSBDevice interface virtual PC, Propriedade Manufacturerstring
topic_type:
- apiref
api_name:
- IVMUSBDevice.ManufacturerString
- IVMUSBDevice.get_ManufacturerString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8d74cbe737c59e10daf2cf3ee93e4b1f14983f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085966"
---
# <a name="ivmusbdevicemanufacturerstring-property"></a><span data-ttu-id="549a6-106">Propriedade IVMUSBDevice:: Manufacturerstring</span><span class="sxs-lookup"><span data-stu-id="549a6-106">IVMUSBDevice::ManufacturerString property</span></span>

<span data-ttu-id="549a6-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="549a6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="549a6-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="549a6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="549a6-109">Recupera o nome do fabricante do dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="549a6-109">Retrieves the name of the USB device manufacturer.</span></span>

<span data-ttu-id="549a6-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="549a6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="549a6-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="549a6-111">Syntax</span></span>


```C++
HRESULT get_ManufacturerString(
  [out, retval] BSTR *manufacturerName
);
```



## <a name="property-value"></a><span data-ttu-id="549a6-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="549a6-112">Property value</span></span>

<span data-ttu-id="549a6-113">O nome do fabricante do dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="549a6-113">The name of the USB device manufacturer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="549a6-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="549a6-114">Error codes</span></span>



| <span data-ttu-id="549a6-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="549a6-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="549a6-116">Significado</span><span class="sxs-lookup"><span data-stu-id="549a6-116">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="549a6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="549a6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="549a6-118">O método foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="549a6-118">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="549a6-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="549a6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="549a6-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="549a6-120">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="549a6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="549a6-121">Requirements</span></span>



| <span data-ttu-id="549a6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="549a6-122">Requirement</span></span> | <span data-ttu-id="549a6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="549a6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="549a6-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="549a6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="549a6-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="549a6-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="549a6-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="549a6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="549a6-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="549a6-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="549a6-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="549a6-128">End of client support</span></span><br/>    | <span data-ttu-id="549a6-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="549a6-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="549a6-130">Produto</span><span class="sxs-lookup"><span data-stu-id="549a6-130">Product</span></span><br/>                  | <span data-ttu-id="549a6-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="549a6-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="549a6-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="549a6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="549a6-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="549a6-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="549a6-134">IID</span><span class="sxs-lookup"><span data-stu-id="549a6-134">IID</span></span><br/>                      | <span data-ttu-id="549a6-135">IID \_ IVMUSBDevice é definido como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="549a6-135">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="549a6-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="549a6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="549a6-137">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="549a6-137">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

