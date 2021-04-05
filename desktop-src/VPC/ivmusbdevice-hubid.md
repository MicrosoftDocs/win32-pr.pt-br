---
title: Propriedade IVMUSBDevice HubID (VPCCOMInterfaces. h)
description: Recupera o identificador do Hub no qual o dispositivo está conectado.
ms.assetid: 22e1d8fb-33f4-43a3-883f-174ddafa17c2
keywords:
- Propriedade HubID Virtual PC
- Propriedade HubID Virtual PC, interface IVMUSBDevice
- IVMUSBDevice interface virtual PC, Propriedade HubID
topic_type:
- apiref
api_name:
- IVMUSBDevice.HubID
- IVMUSBDevice.get_HubID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53faa79ee999022f993070767846ee4e4723c3a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009576"
---
# <a name="ivmusbdevicehubid-property"></a><span data-ttu-id="4612e-106">Propriedade IVMUSBDevice:: HubID</span><span class="sxs-lookup"><span data-stu-id="4612e-106">IVMUSBDevice::HubID property</span></span>

<span data-ttu-id="4612e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4612e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4612e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4612e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4612e-109">Recupera o identificador do Hub no qual o dispositivo está conectado.</span><span class="sxs-lookup"><span data-stu-id="4612e-109">Retrieves the identifier of the hub on which the device is connected.</span></span>

<span data-ttu-id="4612e-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="4612e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4612e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4612e-111">Syntax</span></span>


```C++
HRESULT get_HubID(
  [out, retval] long *hubID
);
```



## <a name="property-value"></a><span data-ttu-id="4612e-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4612e-112">Property value</span></span>

<span data-ttu-id="4612e-113">O identificador do Hub.</span><span class="sxs-lookup"><span data-stu-id="4612e-113">The hub identifier.</span></span> <span data-ttu-id="4612e-114">Esse valor é atribuído pelo driver do conector USB.</span><span class="sxs-lookup"><span data-stu-id="4612e-114">This value is assigned by the USB connector driver.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4612e-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4612e-115">Error codes</span></span>



| <span data-ttu-id="4612e-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="4612e-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="4612e-117">Significado</span><span class="sxs-lookup"><span data-stu-id="4612e-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="4612e-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4612e-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="4612e-119">O método foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="4612e-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="4612e-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="4612e-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="4612e-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4612e-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="4612e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4612e-122">Requirements</span></span>



| <span data-ttu-id="4612e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4612e-123">Requirement</span></span> | <span data-ttu-id="4612e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4612e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4612e-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4612e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4612e-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4612e-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4612e-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4612e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4612e-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4612e-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4612e-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4612e-129">End of client support</span></span><br/>    | <span data-ttu-id="4612e-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4612e-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4612e-131">Produto</span><span class="sxs-lookup"><span data-stu-id="4612e-131">Product</span></span><br/>                  | <span data-ttu-id="4612e-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4612e-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4612e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4612e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4612e-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4612e-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4612e-135">IID</span><span class="sxs-lookup"><span data-stu-id="4612e-135">IID</span></span><br/>                      | <span data-ttu-id="4612e-136">IID \_ IVMUSBDevice é definido como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="4612e-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4612e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="4612e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4612e-138">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="4612e-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

