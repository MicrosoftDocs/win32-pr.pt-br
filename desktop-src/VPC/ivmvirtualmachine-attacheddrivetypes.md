---
title: Propriedade IVMVirtualMachine AttachedDriveTypes (VPCCOMInterfaces. h)
description: Uma matriz que indica o tipo de unidade anexado a cada local na VM.
ms.assetid: 6896c9cd-5448-4fbb-8c8e-eef306a5cea1
keywords:
- Propriedade AttachedDriveTypes Virtual PC
- Propriedade AttachedDriveTypes Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade AttachedDriveTypes
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachedDriveTypes
- IVMVirtualMachine.get_AttachedDriveTypes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5f01802b7fa7e3a4f1ccbfc1b5c4bf70e06614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086214"
---
# <a name="ivmvirtualmachineattacheddrivetypes-property"></a><span data-ttu-id="c7ec2-106">Propriedade IVMVirtualMachine:: AttachedDriveTypes</span><span class="sxs-lookup"><span data-stu-id="c7ec2-106">IVMVirtualMachine::AttachedDriveTypes property</span></span>

<span data-ttu-id="c7ec2-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c7ec2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c7ec2-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c7ec2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c7ec2-109">Recupera uma matriz que indica o tipo de unidade anexado a cada local na VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="c7ec2-109">Retrieves an array indicating the type of drive attached to each location in the virtual machine (VM).</span></span>

<span data-ttu-id="c7ec2-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="c7ec2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7ec2-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7ec2-111">Syntax</span></span>


```C++
HRESULT get_AttachedDriveTypes(
  [out, retval] VARIANT *driveTypes
);
```



## <a name="property-value"></a><span data-ttu-id="c7ec2-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c7ec2-112">Property value</span></span>

<span data-ttu-id="c7ec2-113">Uma variante do tipo **VT \_** \| **\_ variante** de matriz VT que contém entradas do tipo **VT \_ UI1**.</span><span class="sxs-lookup"><span data-stu-id="c7ec2-113">A variant of type **VT\_ARRAY** \| **VT\_VARIANT** containing entries of type **VT\_UI1**.</span></span> <span data-ttu-id="c7ec2-114">A matriz contém o valor [**VMDriveType**](vmdrivetype.md) de cada dispositivo conectado a cada local de barramento.</span><span class="sxs-lookup"><span data-stu-id="c7ec2-114">The array contains the [**VMDriveType**](vmdrivetype.md) value of each device connected to every bus location.</span></span> <span data-ttu-id="c7ec2-115">A matriz é ordenada por \[ *busNumber* \] \[ *DeviceID* \] .</span><span class="sxs-lookup"><span data-stu-id="c7ec2-115">The array is ordered by \[*busNumber*\]\[*deviceID*\].</span></span>

## <a name="error-codes"></a><span data-ttu-id="c7ec2-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="c7ec2-116">Error codes</span></span>



| <span data-ttu-id="c7ec2-117">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="c7ec2-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c7ec2-118">Significado</span><span class="sxs-lookup"><span data-stu-id="c7ec2-118">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c7ec2-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c7ec2-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c7ec2-120">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c7ec2-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c7ec2-121"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="c7ec2-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c7ec2-122">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c7ec2-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c7ec2-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c7ec2-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c7ec2-124">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="c7ec2-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="c7ec2-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="c7ec2-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c7ec2-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="c7ec2-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c7ec2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7ec2-127">Requirements</span></span>



| <span data-ttu-id="c7ec2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7ec2-128">Requirement</span></span> | <span data-ttu-id="c7ec2-129">Valor</span><span class="sxs-lookup"><span data-stu-id="c7ec2-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ec2-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7ec2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c7ec2-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c7ec2-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7ec2-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7ec2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c7ec2-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c7ec2-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c7ec2-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c7ec2-134">End of client support</span></span><br/>    | <span data-ttu-id="c7ec2-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c7ec2-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c7ec2-136">Produto</span><span class="sxs-lookup"><span data-stu-id="c7ec2-136">Product</span></span><br/>                  | <span data-ttu-id="c7ec2-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c7ec2-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c7ec2-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7ec2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7ec2-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7ec2-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c7ec2-140">IID</span><span class="sxs-lookup"><span data-stu-id="c7ec2-140">IID</span></span><br/>                      | <span data-ttu-id="c7ec2-141">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="c7ec2-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c7ec2-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7ec2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7ec2-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="c7ec2-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

