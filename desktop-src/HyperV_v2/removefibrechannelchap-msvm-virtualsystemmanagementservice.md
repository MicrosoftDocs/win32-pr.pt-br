---
description: Remove os parâmetros DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) de uma porta de Fibre Channel sintética em uma máquina virtual.
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Método RemoveFibreChannelChap da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06e944c3c592b0b61ace8a72b5d42a801ab0f5df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757404"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="99f5b-103">Método RemoveFibreChannelChap da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="99f5b-103">RemoveFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="99f5b-104">Remove os parâmetros DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) de uma porta de Fibre Channel sintética em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99f5b-104">Removes DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters from a synthetic Fibre Channel port in a virtual machine.</span></span> <span data-ttu-id="99f5b-105">Esse método falhará se a máquina virtual estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="99f5b-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="99f5b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99f5b-106">Syntax</span></span>


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a><span data-ttu-id="99f5b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99f5b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99f5b-108">*FcPortSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99f5b-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99f5b-109">Uma matriz de cadeias de caracteres que contém uma instância inserida da classe [**Msvm \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) que define as portas de Fibre Channel sintéticas das quais os parâmetros DH-CHAP são removidos.</span><span class="sxs-lookup"><span data-stu-id="99f5b-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that define the synthetic Fibre Channel ports to remove the DH-CHAP parameters from.</span></span> <span data-ttu-id="99f5b-110">A propriedade **InstanceId** de cada uma dessas instâncias identifica os elementos a serem modificados.</span><span class="sxs-lookup"><span data-stu-id="99f5b-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99f5b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99f5b-111">Return value</span></span>

<span data-ttu-id="99f5b-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="99f5b-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="99f5b-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="99f5b-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="99f5b-114">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="99f5b-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="99f5b-115">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="99f5b-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="99f5b-116">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="99f5b-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="99f5b-117">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="99f5b-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="99f5b-118">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="99f5b-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="99f5b-119">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="99f5b-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="99f5b-120">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="99f5b-120">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="99f5b-121">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="99f5b-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="99f5b-122">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="99f5b-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="99f5b-123">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="99f5b-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="99f5b-124">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="99f5b-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="99f5b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99f5b-125">Requirements</span></span>



| <span data-ttu-id="99f5b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="99f5b-126">Requirement</span></span> | <span data-ttu-id="99f5b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="99f5b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99f5b-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99f5b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="99f5b-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="99f5b-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="99f5b-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99f5b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="99f5b-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="99f5b-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="99f5b-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="99f5b-132">Namespace</span></span><br/>                | <span data-ttu-id="99f5b-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="99f5b-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="99f5b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="99f5b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99f5b-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99f5b-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="99f5b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="99f5b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99f5b-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="99f5b-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="99f5b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="99f5b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99f5b-139">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="99f5b-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




