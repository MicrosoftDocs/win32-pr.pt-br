---
title: Método IVMFloppyDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
description: Recebe a notificação de que a mídia foi inserida na unidade. | Método IVMFloppyDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- OnMediaInsert do método virtual PC
- Método OnMediaInsert Virtual PC, interface IVMFloppyDriveEvents
- IVMFloppyDriveEvents interface virtual PC, método OnMediaInsert
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d607a2f63836ca1cb151e602b2d3b2021f4e3913
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105781128"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a><span data-ttu-id="c31da-107">Método IVMFloppyDriveEvents:: OnMediaInsert</span><span class="sxs-lookup"><span data-stu-id="c31da-107">IVMFloppyDriveEvents::OnMediaInsert method</span></span>

<span data-ttu-id="c31da-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c31da-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c31da-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c31da-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c31da-110">Recebe a notificação de que a mídia foi inserida na unidade.</span><span class="sxs-lookup"><span data-stu-id="c31da-110">Receives notification that media has been inserted into the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="c31da-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c31da-111">Syntax</span></span>


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="c31da-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c31da-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c31da-113">*mediaPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c31da-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c31da-114">A letra da unidade do host, ou caminho, para a imagem do disquete.</span><span class="sxs-lookup"><span data-stu-id="c31da-114">The host drive letter, or path, to floppy image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c31da-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c31da-115">Return value</span></span>

<span data-ttu-id="c31da-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c31da-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c31da-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c31da-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c31da-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c31da-118">Remarks</span></span>

<span data-ttu-id="c31da-119">Esse método é chamado quando a mídia (uma imagem de disquete ou um disquete em uma unidade de host) é inserida.</span><span class="sxs-lookup"><span data-stu-id="c31da-119">This method is called when media (a floppy disk image or a floppy disk in a host drive) is inserted.</span></span> <span data-ttu-id="c31da-120">O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento vmFloppyDriveEvent OnMediaInsert originado do [**IVMFloppyDrive**](ivmfloppydrive.md).</span><span class="sxs-lookup"><span data-stu-id="c31da-120">The client program must implement this interface method to receive notification of the vmFloppyDriveEvent\_OnMediaInsert event originating from [**IVMFloppyDrive**](ivmfloppydrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c31da-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c31da-121">Requirements</span></span>



| <span data-ttu-id="c31da-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c31da-122">Requirement</span></span> | <span data-ttu-id="c31da-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c31da-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c31da-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c31da-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c31da-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c31da-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c31da-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c31da-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c31da-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c31da-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c31da-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c31da-128">End of client support</span></span><br/>    | <span data-ttu-id="c31da-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c31da-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c31da-130">Produto</span><span class="sxs-lookup"><span data-stu-id="c31da-130">Product</span></span><br/>                  | <span data-ttu-id="c31da-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c31da-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c31da-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c31da-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c31da-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c31da-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c31da-134">IID</span><span class="sxs-lookup"><span data-stu-id="c31da-134">IID</span></span><br/>                      | <span data-ttu-id="c31da-135">DIID \_ IVMFloppyDriveEvents é definido como a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="c31da-135">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="c31da-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="c31da-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c31da-137">**IVMFloppyDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="c31da-137">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

