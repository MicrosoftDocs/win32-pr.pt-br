---
title: Método IVMVirtualMachineEvents OnEnhancedVideoModeChanged (VPCCOMInterfaces. h)
description: Recebe a notificação de que o suporte de uma máquina virtual para o modo de vídeo avançado foi alterado.
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- OnEnhancedVideoModeChanged do método virtual PC
- Método OnEnhancedVideoModeChanged Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnEnhancedVideoModeChanged
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnEnhancedVideoModeChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bbc67fe298c1a47d853072d8c58ab5b3ce1988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454583"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a><span data-ttu-id="f7059-106">Método IVMVirtualMachineEvents:: OnEnhancedVideoModeChanged</span><span class="sxs-lookup"><span data-stu-id="f7059-106">IVMVirtualMachineEvents::OnEnhancedVideoModeChanged method</span></span>

<span data-ttu-id="f7059-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f7059-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f7059-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f7059-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f7059-109">Recebe a notificação de que o suporte de uma máquina virtual para o modo de vídeo avançado foi alterado.</span><span class="sxs-lookup"><span data-stu-id="f7059-109">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7059-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7059-110">Syntax</span></span>


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a><span data-ttu-id="f7059-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7059-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7059-112">*enhancedVideoMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7059-112">*enhancedVideoMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7059-113">Indica se o modo de vídeo avançado está disponível.</span><span class="sxs-lookup"><span data-stu-id="f7059-113">Indicates whether enhanced video mode is available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7059-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7059-114">Return value</span></span>

<span data-ttu-id="f7059-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f7059-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f7059-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f7059-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7059-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7059-117">Requirements</span></span>



| <span data-ttu-id="f7059-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7059-118">Requirement</span></span> | <span data-ttu-id="f7059-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f7059-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7059-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7059-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f7059-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f7059-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7059-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7059-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f7059-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f7059-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f7059-124">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f7059-124">End of client support</span></span><br/>    | <span data-ttu-id="f7059-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f7059-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f7059-126">Produto</span><span class="sxs-lookup"><span data-stu-id="f7059-126">Product</span></span><br/>                  | <span data-ttu-id="f7059-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f7059-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f7059-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f7059-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7059-129"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7059-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f7059-130">IID</span><span class="sxs-lookup"><span data-stu-id="f7059-130">IID</span></span><br/>                      | <span data-ttu-id="f7059-131">DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="f7059-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="f7059-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7059-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7059-133">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="f7059-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

