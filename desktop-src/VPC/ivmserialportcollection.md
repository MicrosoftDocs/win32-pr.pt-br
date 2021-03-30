---
title: Interface IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Define a coleção de portas seriais na máquina virtual. Para obter um objeto IVMSerialPortCollection, use a propriedade SerialPorts IVMVirtualMachine.
ms.assetid: c0ee9799-f3f7-477e-b33b-52f424752aad
keywords:
- Virtual PC de interface IVMSerialPortCollection
- Virtual PC de interface IVMSerialPortCollection, descrito
topic_type:
- apiref
api_name:
- IVMSerialPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d2ec37789423b5f9446d667da69eca346a2286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644709"
---
# <a name="ivmserialportcollection-interface"></a><span data-ttu-id="10466-106">Interface IVMSerialPortCollection</span><span class="sxs-lookup"><span data-stu-id="10466-106">IVMSerialPortCollection interface</span></span>

<span data-ttu-id="10466-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="10466-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="10466-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="10466-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="10466-109">Define a coleção de portas seriais na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="10466-109">Defines the collection of serial ports within the virtual machine.</span></span> <span data-ttu-id="10466-110">Para obter um objeto **IVMSerialPortCollection** , use a propriedade [**IVMVirtualMachine:: SerialPorts**](ivmvirtualmachine-serialports.md) .</span><span class="sxs-lookup"><span data-stu-id="10466-110">To obtain an **IVMSerialPortCollection** object, use the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="10466-111">Membros</span><span class="sxs-lookup"><span data-stu-id="10466-111">Members</span></span>

<span data-ttu-id="10466-112">A interface **IVMSerialPortCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="10466-112">The **IVMSerialPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="10466-113">**IVMSerialPortCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="10466-113">**IVMSerialPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="10466-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10466-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10466-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10466-115">Properties</span></span>

<span data-ttu-id="10466-116">A interface **IVMSerialPortCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="10466-116">The **IVMSerialPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="10466-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="10466-117">Property</span></span>                                                         | <span data-ttu-id="10466-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="10466-118">Access type</span></span>          | <span data-ttu-id="10466-119">Description</span><span class="sxs-lookup"><span data-stu-id="10466-119">Description</span></span>                                                                |
|:-----------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="10466-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="10466-120">**\_NewEnum**</span></span>](ivmserialportcollection--newenum.md)<br/> | <span data-ttu-id="10466-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10466-121">Read-only</span></span><br/> | <span data-ttu-id="10466-122">Um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="10466-122">An enumerator for the collection.</span></span><br/>                               |
| [<span data-ttu-id="10466-123">**Contar**</span><span class="sxs-lookup"><span data-stu-id="10466-123">**Count**</span></span>](ivmserialportcollection-count.md)<br/>        | <span data-ttu-id="10466-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10466-124">Read-only</span></span><br/> | <span data-ttu-id="10466-125">O número de portas seriais nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="10466-125">The number of serial ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="10466-126">**Item**</span><span class="sxs-lookup"><span data-stu-id="10466-126">**Item**</span></span>](ivmserialportcollection-item.md)<br/>          | <span data-ttu-id="10466-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10466-127">Read-only</span></span><br/> | <span data-ttu-id="10466-128">O objeto de porta serial que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="10466-128">The serial port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="10466-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10466-129">Requirements</span></span>



| <span data-ttu-id="10466-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="10466-130">Requirement</span></span> | <span data-ttu-id="10466-131">Valor</span><span class="sxs-lookup"><span data-stu-id="10466-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="10466-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10466-132">Minimum supported client</span></span><br/> | <span data-ttu-id="10466-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="10466-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="10466-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10466-134">Minimum supported server</span></span><br/> | <span data-ttu-id="10466-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="10466-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="10466-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="10466-136">End of client support</span></span><br/>    | <span data-ttu-id="10466-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="10466-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="10466-138">Produto</span><span class="sxs-lookup"><span data-stu-id="10466-138">Product</span></span><br/>                  | <span data-ttu-id="10466-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="10466-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="10466-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10466-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="10466-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="10466-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="10466-142">IID</span><span class="sxs-lookup"><span data-stu-id="10466-142">IID</span></span><br/>                      | <span data-ttu-id="10466-143">IID \_ IVMSerialPortCollection é definido como dd3c6175-1f04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="10466-143">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="10466-144">Consulte também</span><span class="sxs-lookup"><span data-stu-id="10466-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10466-145">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="10466-145">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> <dt>

[<span data-ttu-id="10466-146">**IVMVirtualMachine:: SerialPorts**</span><span class="sxs-lookup"><span data-stu-id="10466-146">**IVMVirtualMachine::SerialPorts**</span></span>](ivmvirtualmachine-serialports.md)
</dt> </dl>

 

