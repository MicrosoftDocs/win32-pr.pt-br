---
title: Interface IVMSerialPort (VPCCOMInterfaces. h)
description: Define uma porta serial dentro de uma máquina virtual.
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- Virtual PC de interface IVMSerialPort
- Virtual PC de interface IVMSerialPort, descrito
topic_type:
- apiref
api_name:
- IVMSerialPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6edc758ffecca9a0d4788e5586c902cf0b21dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499580"
---
# <a name="ivmserialport-interface"></a><span data-ttu-id="61ed5-105">Interface IVMSerialPort</span><span class="sxs-lookup"><span data-stu-id="61ed5-105">IVMSerialPort interface</span></span>

<span data-ttu-id="61ed5-106">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="61ed5-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="61ed5-107">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="61ed5-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="61ed5-108">Define uma porta serial dentro de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="61ed5-108">Defines a serial port inside a virtual machine.</span></span> <span data-ttu-id="61ed5-109">Essa interface permite que você configure portas seriais dentro de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="61ed5-109">This interface allows you to configure serial ports inside a virtual machine.</span></span> <span data-ttu-id="61ed5-110">Você pode recuperar um objeto **IVMSerialPort** do objeto [**IVMSerialPortCollection**](ivmserialportcollection.md) retornado da propriedade [**IVMVirtualMachine:: SerialPorts**](ivmvirtualmachine-serialports.md) .</span><span class="sxs-lookup"><span data-stu-id="61ed5-110">You can retrieve an **IVMSerialPort** object from the [**IVMSerialPortCollection**](ivmserialportcollection.md) object returned from the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="61ed5-111">Membros</span><span class="sxs-lookup"><span data-stu-id="61ed5-111">Members</span></span>

<span data-ttu-id="61ed5-112">A interface **IVMSerialPort** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="61ed5-112">The **IVMSerialPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="61ed5-113">**IVMSerialPort** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="61ed5-113">**IVMSerialPort** also has these types of members:</span></span>

-   [<span data-ttu-id="61ed5-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="61ed5-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="61ed5-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61ed5-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="61ed5-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="61ed5-116">Methods</span></span>

<span data-ttu-id="61ed5-117">A interface **IVMSerialPort** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="61ed5-117">The **IVMSerialPort** interface has these methods.</span></span>



| <span data-ttu-id="61ed5-118">Método</span><span class="sxs-lookup"><span data-stu-id="61ed5-118">Method</span></span>                                       | <span data-ttu-id="61ed5-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="61ed5-119">Description</span></span>                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="61ed5-120">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="61ed5-120">**\_ID**</span></span>](ivmserialport--id.md)            | <span data-ttu-id="61ed5-121">Recupera o identificador interno da porta serial.</span><span class="sxs-lookup"><span data-stu-id="61ed5-121">Retrieves the internal identifier of the serial port.</span></span><br/> |
| [<span data-ttu-id="61ed5-122">**Configurar**</span><span class="sxs-lookup"><span data-stu-id="61ed5-122">**Configure**</span></span>](ivmserialport-configure.md) | <span data-ttu-id="61ed5-123">Configura a porta serial.</span><span class="sxs-lookup"><span data-stu-id="61ed5-123">Configures the serial port.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="61ed5-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61ed5-124">Properties</span></span>

<span data-ttu-id="61ed5-125">A interface **IVMSerialPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="61ed5-125">The **IVMSerialPort** interface has these properties.</span></span>



| <span data-ttu-id="61ed5-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="61ed5-126">Property</span></span>                                                                  | <span data-ttu-id="61ed5-127">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="61ed5-127">Access type</span></span>          | <span data-ttu-id="61ed5-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="61ed5-128">Description</span></span>                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61ed5-129">**ConnectImmediately**</span><span class="sxs-lookup"><span data-stu-id="61ed5-129">**ConnectImmediately**</span></span>](ivmserialport-connectimmediately.md)<br/> | <span data-ttu-id="61ed5-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61ed5-130">Read-only</span></span><br/> | <span data-ttu-id="61ed5-131">Indica se a porta serial deve ser aberta sem aguardar a recepção de um comando de modem.</span><span class="sxs-lookup"><span data-stu-id="61ed5-131">Indicates whether the serial port should be opened without waiting for a modem command to be received.</span></span><br/> |
| [<span data-ttu-id="61ed5-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="61ed5-132">**Name**</span></span>](ivmserialport-name.md)<br/>                             | <span data-ttu-id="61ed5-133">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61ed5-133">Read-only</span></span><br/> | <span data-ttu-id="61ed5-134">O nome da porta serial.</span><span class="sxs-lookup"><span data-stu-id="61ed5-134">The name of the serial port.</span></span><br/>                                                                           |
| [<span data-ttu-id="61ed5-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="61ed5-135">**Type**</span></span>](ivmserialport-type.md)<br/>                             | <span data-ttu-id="61ed5-136">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61ed5-136">Read-only</span></span><br/> | <span data-ttu-id="61ed5-137">O tipo da porta serial.</span><span class="sxs-lookup"><span data-stu-id="61ed5-137">The type of the serial port.</span></span><br/>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="61ed5-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61ed5-138">Requirements</span></span>



| <span data-ttu-id="61ed5-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="61ed5-139">Requirement</span></span> | <span data-ttu-id="61ed5-140">Valor</span><span class="sxs-lookup"><span data-stu-id="61ed5-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ed5-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61ed5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="61ed5-142">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="61ed5-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61ed5-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61ed5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="61ed5-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="61ed5-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="61ed5-145">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="61ed5-145">End of client support</span></span><br/>    | <span data-ttu-id="61ed5-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="61ed5-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="61ed5-147">Produto</span><span class="sxs-lookup"><span data-stu-id="61ed5-147">Product</span></span><br/>                  | <span data-ttu-id="61ed5-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="61ed5-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="61ed5-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61ed5-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="61ed5-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="61ed5-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="61ed5-151">IID</span><span class="sxs-lookup"><span data-stu-id="61ed5-151">IID</span></span><br/>                      | <span data-ttu-id="61ed5-152">IID \_ IVMSerialPort é definido como 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="61ed5-152">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



 

