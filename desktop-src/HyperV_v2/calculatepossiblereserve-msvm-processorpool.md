---
description: Esse método é usado para localizar a reserva real com o parâmetro de entrada sendo o número de processadores de máquina virtual para os quais a reserva é calculada.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Método CalculatePossibleReserve da classe Msvm_ProcessorPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool.CalculatePossibleReserve
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7f88bcf3295b1792fca6be88ae0c9282b72646e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662196"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a><span data-ttu-id="45233-103">Método CalculatePossibleReserve da \_ classe ProcessorPool Msvm</span><span class="sxs-lookup"><span data-stu-id="45233-103">CalculatePossibleReserve method of the Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="45233-104">Esse método é usado para localizar a reserva real com o parâmetro de entrada sendo o número de processadores de máquina virtual para os quais a reserva é calculada.</span><span class="sxs-lookup"><span data-stu-id="45233-104">This method is used to find the actual reserve with the input parameter being the number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="45233-105">Esse método é necessário porque a reserva de recursos do processador é altamente dependente do número de processadores que devem ser agendados em paralelo.</span><span class="sxs-lookup"><span data-stu-id="45233-105">This method is necessary because the reservation of processor resources is highly dependent on the number of processors which must be scheduled in parallel.</span></span>

## <a name="syntax"></a><span data-ttu-id="45233-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45233-106">Syntax</span></span>


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a><span data-ttu-id="45233-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45233-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45233-108">*ProcessorCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45233-108">*ProcessorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45233-109">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45233-109">Type: **uint16**</span></span>

<span data-ttu-id="45233-110">O número de processadores de máquina virtual para os quais a reserva é calculada.</span><span class="sxs-lookup"><span data-stu-id="45233-110">The number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="45233-111">O valor máximo dessa propriedade é a contagem de processadores lógicos para o computador host.</span><span class="sxs-lookup"><span data-stu-id="45233-111">The maximum value for this property is the logical processor count for the host computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45233-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45233-112">Return value</span></span>

<span data-ttu-id="45233-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45233-113">Type: **uint32**</span></span>

<span data-ttu-id="45233-114">A quantidade de recursos de CPU que podem ser reservados para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="45233-114">The amount of CPU resources that may be reserved for a virtual machine.</span></span>

## <a name="remarks"></a><span data-ttu-id="45233-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="45233-115">Remarks</span></span>

<span data-ttu-id="45233-116">O acesso à classe [**Msvm \_ ProcessorPool**](msvm-processorpool.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="45233-116">Access to the [**Msvm\_ProcessorPool**](msvm-processorpool.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="45233-117">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="45233-117">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="45233-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45233-118">Requirements</span></span>



| <span data-ttu-id="45233-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="45233-119">Requirement</span></span> | <span data-ttu-id="45233-120">Valor</span><span class="sxs-lookup"><span data-stu-id="45233-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45233-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45233-121">Minimum supported client</span></span><br/> | <span data-ttu-id="45233-122">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="45233-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="45233-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45233-123">Minimum supported server</span></span><br/> | <span data-ttu-id="45233-124">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="45233-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45233-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="45233-125">Namespace</span></span><br/>                | <span data-ttu-id="45233-126">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="45233-126">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="45233-127">MOF</span><span class="sxs-lookup"><span data-stu-id="45233-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45233-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45233-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45233-129">DLL</span><span class="sxs-lookup"><span data-stu-id="45233-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45233-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45233-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="45233-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="45233-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45233-132">**Msvm \_ ProcessorPool**</span><span class="sxs-lookup"><span data-stu-id="45233-132">**Msvm\_ProcessorPool**</span></span>](msvm-processorpool.md)
</dt> </dl>

 

