---
title: Propriedade IVMUSBDevice AttachedToVM (VPCCOMInterfaces. h)
description: Recupera o nome da máquina virtual à qual o dispositivo USB está anexado.
ms.assetid: 214ed891-1fca-4311-945a-0ce3d05d604e
keywords:
- Propriedade AttachedToVM Virtual PC
- Propriedade AttachedToVM Virtual PC, interface IVMUSBDevice
- IVMUSBDevice interface virtual PC, Propriedade AttachedToVM
topic_type:
- apiref
api_name:
- IVMUSBDevice.AttachedToVM
- IVMUSBDevice.get_AttachedToVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c64e265cba81858bc887cbf595426bffd1b604aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009436"
---
# <a name="ivmusbdeviceattachedtovm-property"></a><span data-ttu-id="8618b-106">Propriedade IVMUSBDevice:: AttachedToVM</span><span class="sxs-lookup"><span data-stu-id="8618b-106">IVMUSBDevice::AttachedToVM property</span></span>

<span data-ttu-id="8618b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8618b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8618b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8618b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8618b-109">Recupera o nome da máquina virtual à qual o dispositivo USB está anexado.</span><span class="sxs-lookup"><span data-stu-id="8618b-109">Retrieves the name of the virtual machine to which the USB Device is attached.</span></span>

<span data-ttu-id="8618b-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="8618b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8618b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8618b-111">Syntax</span></span>


```C++
HRESULT get_AttachedToVM(
  [out, retval] BSTR *ConfigName
);
```



## <a name="property-value"></a><span data-ttu-id="8618b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8618b-112">Property value</span></span>

<span data-ttu-id="8618b-113">O nome da VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="8618b-113">The name of the virtual machine (VM).</span></span>

## <a name="error-codes"></a><span data-ttu-id="8618b-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8618b-114">Error codes</span></span>



| <span data-ttu-id="8618b-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="8618b-115">Name/value</span></span>                                                                                                                                                           | <span data-ttu-id="8618b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8618b-116">Meaning</span></span>                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8618b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8618b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="8618b-118">O dispositivo é anexado à VM e seu nome é retornado.</span><span class="sxs-lookup"><span data-stu-id="8618b-118">The device is attached to the VM, and its name is returned.</span></span><br/> |
| <dl> <span data-ttu-id="8618b-119"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8618b-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                           | <span data-ttu-id="8618b-120">O dispositivo está conectado ao host.</span><span class="sxs-lookup"><span data-stu-id="8618b-120">The device is attached to the host.</span></span><br/>                         |
| <dl> <span data-ttu-id="8618b-121"><dt>VM \_ 0xA00400929 \_ \_ \_ VM externa USB</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8618b-121"><dt>VM\_E\_USB\_EXTERNAL\_VM</dt> <dt>0xA00400929</dt></span></span> </dl> | <span data-ttu-id="8618b-122">O dispositivo está anexado a uma VM em outra sessão de usuário.</span><span class="sxs-lookup"><span data-stu-id="8618b-122">The device is attached to a VM in another user session.</span></span><br/>     |
| <dl> <span data-ttu-id="8618b-123"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="8618b-123"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                | <span data-ttu-id="8618b-124">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8618b-124">The parameter is **NULL**.</span></span><br/>                                  |



## <a name="requirements"></a><span data-ttu-id="8618b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8618b-125">Requirements</span></span>



| <span data-ttu-id="8618b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8618b-126">Requirement</span></span> | <span data-ttu-id="8618b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8618b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8618b-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8618b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8618b-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8618b-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8618b-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8618b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8618b-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8618b-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8618b-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8618b-132">End of client support</span></span><br/>    | <span data-ttu-id="8618b-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8618b-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8618b-134">Produto</span><span class="sxs-lookup"><span data-stu-id="8618b-134">Product</span></span><br/>                  | <span data-ttu-id="8618b-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8618b-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8618b-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8618b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8618b-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8618b-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8618b-138">IID</span><span class="sxs-lookup"><span data-stu-id="8618b-138">IID</span></span><br/>                      | <span data-ttu-id="8618b-139">IID \_ IVMUSBDevice é definido como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="8618b-139">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8618b-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="8618b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8618b-141">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="8618b-141">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

