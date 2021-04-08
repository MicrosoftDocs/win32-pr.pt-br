---
description: Representa um dispositivo lógico que permite que um usuário insira, exiba ou Ouça dados no sistema de computador.
ms.assetid: 95f88a63-3a2a-4b8c-9849-564dac254933
title: Classe CIM_UserDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.IsLocked
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8776c0b5e9ddf1653747b82e94040197e4c56f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827885"
---
# <a name="cim_userdevice-class-hyper-v-management"></a><span data-ttu-id="2de6d-103">Classe CIM_UserDevice (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="2de6d-103">CIM_UserDevice class (Hyper-V management)</span></span>

<span data-ttu-id="2de6d-104">Representa um dispositivo lógico que permite que um usuário insira, exiba ou Ouça dados no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="2de6d-104">Represents a logical device that allows a user to input, view or hear data on the computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de6d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2de6d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
{
  boolean IsLocked;
};
```

## <a name="members"></a><span data-ttu-id="2de6d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="2de6d-106">Members</span></span>

<span data-ttu-id="2de6d-107">A classe de **\_ userdevice do CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2de6d-107">The **CIM\_UserDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="2de6d-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2de6d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2de6d-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2de6d-109">Properties</span></span>

<span data-ttu-id="2de6d-110">A classe **CIM \_ userdevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2de6d-110">The **CIM\_UserDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2de6d-111">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="2de6d-111">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2de6d-112">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2de6d-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2de6d-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2de6d-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2de6d-114">**true** se o dispositivo estiver bloqueado, impedindo a entrada ou saída do usuário; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="2de6d-114">**true** if the device is locked, preventing user input or output; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2de6d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2de6d-115">Requirements</span></span>



| <span data-ttu-id="2de6d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2de6d-116">Requirement</span></span> | <span data-ttu-id="2de6d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2de6d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2de6d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2de6d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2de6d-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2de6d-119">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2de6d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2de6d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2de6d-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2de6d-121">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2de6d-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="2de6d-122">Namespace</span></span><br/>                | <span data-ttu-id="2de6d-123">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2de6d-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2de6d-124">MOF</span><span class="sxs-lookup"><span data-stu-id="2de6d-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2de6d-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2de6d-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2de6d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2de6d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2de6d-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2de6d-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2de6d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2de6d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de6d-129">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2de6d-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




