---
description: Gerencia os dispositivos atribuíveis em um sistema de computador host.
ms.assetid: d958e978-682e-49eb-bd10-d31d9563fdbf
title: Classe Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8aff620e9227000b2c4a03069f8a5f900a5fc82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759875"
---
# <a name="msvm_assignabledeviceservice-class"></a><span data-ttu-id="0ce3f-103">\_Classe Msvm AssignableDeviceService</span><span class="sxs-lookup"><span data-stu-id="0ce3f-103">Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="0ce3f-104">Gerencia os dispositivos atribuíveis em um sistema de computador host.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-104">Manages the assignable devices on a host computer system.</span></span>

<span data-ttu-id="0ce3f-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce3f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ce3f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AssignableDeviceService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="0ce3f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="0ce3f-107">Members</span></span>

<span data-ttu-id="0ce3f-108">A classe **Msvm \_ AssignableDeviceService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0ce3f-108">The **Msvm\_AssignableDeviceService** class has these types of members:</span></span>

-   [<span data-ttu-id="0ce3f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="0ce3f-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0ce3f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="0ce3f-110">Methods</span></span>

<span data-ttu-id="0ce3f-111">A classe **Msvm \_ AssignableDeviceService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-111">The **Msvm\_AssignableDeviceService** class has these methods.</span></span>



| <span data-ttu-id="0ce3f-112">Método</span><span class="sxs-lookup"><span data-stu-id="0ce3f-112">Method</span></span>                                                                                    | <span data-ttu-id="0ce3f-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ce3f-113">Description</span></span>                                                                                    |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ce3f-114">**DismountAssignableDevice**</span><span class="sxs-lookup"><span data-stu-id="0ce3f-114">**DismountAssignableDevice**</span></span>](msvm-assignabledeviceservice-dismountassignabledevice.md) | <span data-ttu-id="0ce3f-115">Desmonta o dispositivo PCI especificado para que ele possa ser atribuído.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-115">Dismounts the specified PCI device so that it can be assigned.</span></span><br/>                      |
| [<span data-ttu-id="0ce3f-116">**MountAssignableDevice**</span><span class="sxs-lookup"><span data-stu-id="0ce3f-116">**MountAssignableDevice**</span></span>](msvm-assignabledeviceservice-mountassignabledevice.md)       | <span data-ttu-id="0ce3f-117">Monta o dispositivo PCI especificado para que ele possa ser usado pelo sistema de computador host.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-117">Mounts the specified PCI device so that it can be used by the host computer system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0ce3f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ce3f-118">Requirements</span></span>



| <span data-ttu-id="0ce3f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ce3f-119">Requirement</span></span> | <span data-ttu-id="0ce3f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0ce3f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce3f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ce3f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0ce3f-122">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="0ce3f-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0ce3f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ce3f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0ce3f-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0ce3f-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0ce3f-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ce3f-125">Namespace</span></span><br/>                | <span data-ttu-id="0ce3f-126">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0ce3f-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0ce3f-127">MOF</span><span class="sxs-lookup"><span data-stu-id="0ce3f-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ce3f-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ce3f-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ce3f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0ce3f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ce3f-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0ce3f-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0ce3f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ce3f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ce3f-132">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="0ce3f-132">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




