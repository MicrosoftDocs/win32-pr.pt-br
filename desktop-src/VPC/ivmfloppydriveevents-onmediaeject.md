---
title: Método IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Recebe a notificação de que a mídia foi ejetada da unidade. | Método IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: 3e9c0b5d-8fec-4f34-93d2-c5975403798b
keywords:
- OnMediaEject do método virtual PC
- Método OnMediaEject Virtual PC, interface IVMFloppyDriveEvents
- IVMFloppyDriveEvents interface virtual PC, método OnMediaEject
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd640f7b8eb143eba4f3b19e984792f2b6779ad6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837907"
---
# <a name="ivmfloppydriveeventsonmediaeject-method"></a><span data-ttu-id="ffd7b-107">Método IVMFloppyDriveEvents:: OnMediaEject</span><span class="sxs-lookup"><span data-stu-id="ffd7b-107">IVMFloppyDriveEvents::OnMediaEject method</span></span>

<span data-ttu-id="ffd7b-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ffd7b-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ffd7b-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ffd7b-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ffd7b-110">Recebe a notificação de que a mídia foi ejetada da unidade.</span><span class="sxs-lookup"><span data-stu-id="ffd7b-110">Receives notification that media has been ejected from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffd7b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ffd7b-111">Syntax</span></span>


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="ffd7b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffd7b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffd7b-113">*mediaPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ffd7b-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd7b-114">A letra da unidade do host, ou caminho, para a imagem do disquete.</span><span class="sxs-lookup"><span data-stu-id="ffd7b-114">The host drive letter, or path, to floppy image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffd7b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ffd7b-115">Return value</span></span>

<span data-ttu-id="ffd7b-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ffd7b-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ffd7b-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ffd7b-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffd7b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ffd7b-118">Remarks</span></span>

<span data-ttu-id="ffd7b-119">Esse método é chamado quando a mídia (uma imagem de disquete ou um disquete em uma unidade de host) é ejetada.</span><span class="sxs-lookup"><span data-stu-id="ffd7b-119">This method is called when media (a floppy disk image or a floppy disk in a host drive) is ejected.</span></span> <span data-ttu-id="ffd7b-120">O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento vmFloppyDriveEvent OnMediaEject originado do [**IVMFloppyDrive**](ivmfloppydrive.md).</span><span class="sxs-lookup"><span data-stu-id="ffd7b-120">The client program must implement this interface method to receive notification of the vmFloppyDriveEvent\_OnMediaEject event originating from [**IVMFloppyDrive**](ivmfloppydrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffd7b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffd7b-121">Requirements</span></span>



| <span data-ttu-id="ffd7b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffd7b-122">Requirement</span></span> | <span data-ttu-id="ffd7b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ffd7b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd7b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffd7b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd7b-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ffd7b-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ffd7b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffd7b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd7b-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ffd7b-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ffd7b-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ffd7b-128">End of client support</span></span><br/>    | <span data-ttu-id="ffd7b-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ffd7b-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ffd7b-130">Produto</span><span class="sxs-lookup"><span data-stu-id="ffd7b-130">Product</span></span><br/>                  | <span data-ttu-id="ffd7b-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ffd7b-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ffd7b-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ffd7b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffd7b-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffd7b-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ffd7b-134">IID</span><span class="sxs-lookup"><span data-stu-id="ffd7b-134">IID</span></span><br/>                      | <span data-ttu-id="ffd7b-135">DIID \_ IVMFloppyDriveEvents é definido como a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="ffd7b-135">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="ffd7b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffd7b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffd7b-137">**IVMFloppyDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="ffd7b-137">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

