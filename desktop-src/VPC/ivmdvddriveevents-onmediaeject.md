---
title: Método IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Recebe a notificação de que a mídia foi ejetada da unidade. | Método IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- OnMediaEject do método virtual PC
- Método OnMediaEject Virtual PC, interface IVMDVDDriveEvents
- IVMDVDDriveEvents interface virtual PC, método OnMediaEject
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b66091dcc6cc5ee28ab6e0cb3d58e3e647e41cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837747"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a><span data-ttu-id="dfb52-107">Método IVMDVDDriveEvents:: OnMediaEject</span><span class="sxs-lookup"><span data-stu-id="dfb52-107">IVMDVDDriveEvents::OnMediaEject method</span></span>

<span data-ttu-id="dfb52-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dfb52-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dfb52-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dfb52-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dfb52-110">Recebe a notificação de que a mídia foi ejetada da unidade.</span><span class="sxs-lookup"><span data-stu-id="dfb52-110">Receives notification that media has been ejected from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb52-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfb52-111">Syntax</span></span>


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="dfb52-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfb52-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfb52-113">*mediaPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dfb52-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb52-114">A letra da unidade do host, ou caminho, para a imagem ISO.</span><span class="sxs-lookup"><span data-stu-id="dfb52-114">The host drive letter, or path, to the ISO image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfb52-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dfb52-115">Return value</span></span>

<span data-ttu-id="dfb52-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dfb52-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dfb52-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dfb52-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfb52-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfb52-118">Remarks</span></span>

<span data-ttu-id="dfb52-119">Esse método é chamado quando a mídia (uma imagem ISO ou um disco em uma unidade de host) é ejetada.</span><span class="sxs-lookup"><span data-stu-id="dfb52-119">This method is called when media (an ISO image or a disc in a host drive) is ejected.</span></span> <span data-ttu-id="dfb52-120">O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento Onejeção vmDVDDriveEvent originário de [**IVMDVDDrive**](ivmdvddrive.md).</span><span class="sxs-lookup"><span data-stu-id="dfb52-120">The client program must implement this interface method to receive notification of the vmDVDDriveEvent\_OnEject event originating from [**IVMDVDDrive**](ivmdvddrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb52-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfb52-121">Requirements</span></span>



| <span data-ttu-id="dfb52-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfb52-122">Requirement</span></span> | <span data-ttu-id="dfb52-123">Valor</span><span class="sxs-lookup"><span data-stu-id="dfb52-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb52-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfb52-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dfb52-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dfb52-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dfb52-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfb52-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dfb52-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dfb52-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dfb52-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="dfb52-128">End of client support</span></span><br/>    | <span data-ttu-id="dfb52-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfb52-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dfb52-130">Produto</span><span class="sxs-lookup"><span data-stu-id="dfb52-130">Product</span></span><br/>                  | <span data-ttu-id="dfb52-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dfb52-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dfb52-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfb52-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfb52-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfb52-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dfb52-134">IID</span><span class="sxs-lookup"><span data-stu-id="dfb52-134">IID</span></span><br/>                      | <span data-ttu-id="dfb52-135">DIID \_ IVMDVDDriveEvents é definido como c2a7d8e9-E76C-4eb8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="dfb52-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="dfb52-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfb52-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb52-137">**IVMDVDDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="dfb52-137">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

