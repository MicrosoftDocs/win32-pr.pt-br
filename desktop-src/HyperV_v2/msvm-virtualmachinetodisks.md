---
description: Definindo dados a serem passados como uma matriz para a \_ classe Msvm CollectionReferencePointExportSettingData.
ms.assetid: f127880f-f917-4069-a283-a6f9427c5e07
title: Classe Msvm_VirtualMachineToDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualMachineToDisks
- Msvm_VirtualMachineToDisks.VirtualMachineId
- Msvm_VirtualMachineToDisks.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cad5de9389b9cb1d5e7db0573f3a4e3fc271ba31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826863"
---
# <a name="msvm_virtualmachinetodisks-class"></a><span data-ttu-id="bff9f-103">\_Classe Msvm VirtualMachineToDisks</span><span class="sxs-lookup"><span data-stu-id="bff9f-103">Msvm\_VirtualMachineToDisks class</span></span>

<span data-ttu-id="bff9f-104">Definindo dados a serem passados como uma matriz para a classe [**Msvm \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="bff9f-104">Setting data to be passed as an array to the [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) class.</span></span>

<span data-ttu-id="bff9f-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bff9f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bff9f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bff9f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualMachineToDisks
{
  string VirtualMachineId;
  string DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="bff9f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="bff9f-107">Members</span></span>

<span data-ttu-id="bff9f-108">A classe **Msvm \_ VirtualMachineToDisks** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bff9f-108">The **Msvm\_VirtualMachineToDisks** class has these types of members:</span></span>

-   [<span data-ttu-id="bff9f-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bff9f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bff9f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bff9f-110">Properties</span></span>

<span data-ttu-id="bff9f-111">A classe **Msvm \_ VirtualMachineToDisks** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bff9f-111">The **Msvm\_VirtualMachineToDisks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bff9f-112">**DisksToExport**</span><span class="sxs-lookup"><span data-stu-id="bff9f-112">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bff9f-113">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bff9f-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bff9f-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bff9f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bff9f-115">As IDs da instância do WMI dos discos que pertencem a uma determinada ID da máquina virtual para a qual os dados precisam ser exportados.</span><span class="sxs-lookup"><span data-stu-id="bff9f-115">The WMI instance IDs of the disks those belong to given Virtual Machine ID for which data needs to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="bff9f-116">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="bff9f-116">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bff9f-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bff9f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bff9f-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bff9f-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bff9f-119">Uma ID da máquina virtual à qual os discos virtuais estão associados.</span><span class="sxs-lookup"><span data-stu-id="bff9f-119">A Virtual Machine ID that virtual disks are associated with.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bff9f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bff9f-120">Requirements</span></span>



| <span data-ttu-id="bff9f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bff9f-121">Requirement</span></span> | <span data-ttu-id="bff9f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bff9f-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bff9f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bff9f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bff9f-124">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bff9f-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bff9f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bff9f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bff9f-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bff9f-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bff9f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="bff9f-127">Namespace</span></span><br/>                | <span data-ttu-id="bff9f-128">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="bff9f-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bff9f-129">MOF</span><span class="sxs-lookup"><span data-stu-id="bff9f-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bff9f-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bff9f-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bff9f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bff9f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bff9f-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bff9f-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




