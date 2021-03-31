---
title: Propriedade de porta IVMUSBDevice (VPCCOMInterfaces. h)
description: Recupera o identificador da porta na qual o dispositivo está conectado.
ms.assetid: 612c0eba-aa80-4539-a883-f05d32d13b41
keywords:
- Propriedade de porta Virtual PC
- Propriedade de porta Virtual PC, interface IVMUSBDevice
- Virtual PC interface IVMUSBDevice, Propriedade Port
topic_type:
- apiref
api_name:
- IVMUSBDevice.Port
- IVMUSBDevice.get_Port
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb821921d10b23fdb17256372708650d060e253b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645084"
---
# <a name="ivmusbdeviceport-property"></a><span data-ttu-id="61e80-106">IVMUSBDevice: Propriedade classificar de:P</span><span class="sxs-lookup"><span data-stu-id="61e80-106">IVMUSBDevice::Port property</span></span>

<span data-ttu-id="61e80-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="61e80-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="61e80-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="61e80-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="61e80-109">Recupera o identificador da porta na qual o dispositivo está conectado.</span><span class="sxs-lookup"><span data-stu-id="61e80-109">Retrieves the identifier of the port on which the device is connected.</span></span>

<span data-ttu-id="61e80-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="61e80-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="61e80-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61e80-111">Syntax</span></span>


```C++
HRESULT get_Port(
  [out, retval] long *port
);
```



## <a name="property-value"></a><span data-ttu-id="61e80-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="61e80-112">Property value</span></span>

<span data-ttu-id="61e80-113">O identificador de porta.</span><span class="sxs-lookup"><span data-stu-id="61e80-113">The port identifier.</span></span> <span data-ttu-id="61e80-114">Esse valor é atribuído pelo driver do conector USB.</span><span class="sxs-lookup"><span data-stu-id="61e80-114">This value is assigned by the USB connector driver.</span></span>

## <a name="error-codes"></a><span data-ttu-id="61e80-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="61e80-115">Error codes</span></span>



| <span data-ttu-id="61e80-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="61e80-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="61e80-117">Significado</span><span class="sxs-lookup"><span data-stu-id="61e80-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="61e80-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="61e80-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="61e80-119">O método foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="61e80-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="61e80-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="61e80-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="61e80-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="61e80-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="61e80-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61e80-122">Requirements</span></span>



| <span data-ttu-id="61e80-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="61e80-123">Requirement</span></span> | <span data-ttu-id="61e80-124">Valor</span><span class="sxs-lookup"><span data-stu-id="61e80-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="61e80-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61e80-125">Minimum supported client</span></span><br/> | <span data-ttu-id="61e80-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="61e80-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61e80-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61e80-127">Minimum supported server</span></span><br/> | <span data-ttu-id="61e80-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="61e80-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="61e80-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="61e80-129">End of client support</span></span><br/>    | <span data-ttu-id="61e80-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="61e80-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="61e80-131">Produto</span><span class="sxs-lookup"><span data-stu-id="61e80-131">Product</span></span><br/>                  | <span data-ttu-id="61e80-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="61e80-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="61e80-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61e80-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="61e80-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="61e80-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="61e80-135">IID</span><span class="sxs-lookup"><span data-stu-id="61e80-135">IID</span></span><br/>                      | <span data-ttu-id="61e80-136">IID \_ IVMUSBDevice é definido como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="61e80-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="61e80-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="61e80-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61e80-138">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="61e80-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

