---
title: Propriedade IVMVirtualPC USBDeviceCollection (VPCCOMInterfaces. h)
description: Uma coleção enumerável de todos os dispositivos USB conectados ao host.
ms.assetid: 80844912-15b1-44d1-8d07-dca90c579927
keywords:
- Propriedade USBDeviceCollection Virtual PC
- Propriedade USBDeviceCollection Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, Propriedade USBDeviceCollection
topic_type:
- apiref
api_name:
- IVMVirtualPC.USBDeviceCollection
- IVMVirtualPC.get_USBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0428862cdd53ef6e657624d5dbd3e15c2445042f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644784"
---
# <a name="ivmvirtualpcusbdevicecollection-property"></a><span data-ttu-id="f4a89-106">Propriedade IVMVirtualPC:: USBDeviceCollection</span><span class="sxs-lookup"><span data-stu-id="f4a89-106">IVMVirtualPC::USBDeviceCollection property</span></span>

<span data-ttu-id="f4a89-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f4a89-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f4a89-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f4a89-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f4a89-109">Recupera uma coleção enumerável de todos os dispositivos USB conectados ao host.</span><span class="sxs-lookup"><span data-stu-id="f4a89-109">Retrieves an enumerable collection of all USB devices connected to the host.</span></span>

<span data-ttu-id="f4a89-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f4a89-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4a89-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4a89-111">Syntax</span></span>


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="f4a89-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f4a89-112">Property value</span></span>

<span data-ttu-id="f4a89-113">Uma referência a um ponteiro [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md) que representa uma coleção de objetos [**IVMUSBDevice**](ivmusbdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="f4a89-113">A reference to an [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md) pointer that represents a collection of [**IVMUSBDevice**](ivmusbdevice.md) objects.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f4a89-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f4a89-114">Error codes</span></span>



| <span data-ttu-id="f4a89-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="f4a89-115">Name/value</span></span>                                                                                                                                                                                | <span data-ttu-id="f4a89-116">Significado</span><span class="sxs-lookup"><span data-stu-id="f4a89-116">Meaning</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f4a89-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f4a89-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                   | <span data-ttu-id="f4a89-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f4a89-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f4a89-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="f4a89-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                     | <span data-ttu-id="f4a89-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f4a89-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="f4a89-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="f4a89-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                             | <span data-ttu-id="f4a89-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="f4a89-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="f4a89-123"><dt>VM \_ \_Falha de enumeração de USB E \_ \_ \_ mais \_ dispositivos</dt> <dt>0xA0040930</dt></span><span class="sxs-lookup"><span data-stu-id="f4a89-123"><dt>VM\_E\_USB\_ENUMERATION\_FAILED\_MORE\_DEVICES</dt> <dt>0xA0040930</dt></span></span> </dl> | <span data-ttu-id="f4a89-124">Mais de 16 dispositivos USB estão conectados ao host.</span><span class="sxs-lookup"><span data-stu-id="f4a89-124">More than 16 USB devices are connected to the host.</span></span><br/>                                  |
| <dl> <span data-ttu-id="f4a89-125"><dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f4a89-125"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>      | <span data-ttu-id="f4a89-126">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="f4a89-126">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f4a89-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4a89-127">Requirements</span></span>



| <span data-ttu-id="f4a89-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4a89-128">Requirement</span></span> | <span data-ttu-id="f4a89-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f4a89-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a89-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4a89-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f4a89-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f4a89-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f4a89-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4a89-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f4a89-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f4a89-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f4a89-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f4a89-134">End of client support</span></span><br/>    | <span data-ttu-id="f4a89-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f4a89-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f4a89-136">Produto</span><span class="sxs-lookup"><span data-stu-id="f4a89-136">Product</span></span><br/>                  | <span data-ttu-id="f4a89-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f4a89-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f4a89-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4a89-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4a89-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4a89-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f4a89-140">IID</span><span class="sxs-lookup"><span data-stu-id="f4a89-140">IID</span></span><br/>                      | <span data-ttu-id="f4a89-141">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="f4a89-141">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f4a89-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f4a89-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4a89-143">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="f4a89-143">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

