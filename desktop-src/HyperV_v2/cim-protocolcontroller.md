---
description: Representa um grupo de controladores que controlam a operação e a função de dispositivos que iniciam protocolos.
ms.assetid: fb6b65d4-3a1a-47b1-afc7-9b10e8eeaa32
title: Classe CIM_ProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolController
- CIM_ProtocolController.MaxUnitsControlled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27372bc57ad36f37689d75b3963ec0c4b1106956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753476"
---
# <a name="cim_protocolcontroller-class"></a><span data-ttu-id="6e0e0-103">\_Classe CIM ProtocolController</span><span class="sxs-lookup"><span data-stu-id="6e0e0-103">CIM\_ProtocolController class</span></span>

<span data-ttu-id="6e0e0-104">Representa um grupo de controladores que controlam a operação e a função de dispositivos que iniciam protocolos.</span><span class="sxs-lookup"><span data-stu-id="6e0e0-104">Represents a group of controllers that control the operation and function of devices that initiate protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e0e0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e0e0-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolController : CIM_LogicalDevice
{
  uint32 MaxUnitsControlled;
};
```

## <a name="members"></a><span data-ttu-id="6e0e0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6e0e0-106">Members</span></span>

<span data-ttu-id="6e0e0-107">A classe **CIM \_ ProtocolController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6e0e0-107">The **CIM\_ProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="6e0e0-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6e0e0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e0e0-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6e0e0-109">Properties</span></span>

<span data-ttu-id="6e0e0-110">A classe **CIM \_ ProtocolController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6e0e0-110">The **CIM\_ProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e0e0-111">**MaxUnitsControlled**</span><span class="sxs-lookup"><span data-stu-id="6e0e0-111">**MaxUnitsControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0e0-112">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e0e0-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e0e0-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e0e0-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0e0-114">O número máximo de unidades que podem ser controladas pelo ou acessadas por meio do controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="6e0e0-114">The maximum number of units that can be controlled by or accessed through the protocol controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e0e0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e0e0-115">Requirements</span></span>



| <span data-ttu-id="6e0e0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e0e0-116">Requirement</span></span> | <span data-ttu-id="6e0e0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6e0e0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0e0-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e0e0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6e0e0-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e0e0-119">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6e0e0-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e0e0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6e0e0-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e0e0-121">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6e0e0-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e0e0-122">Namespace</span></span><br/>                | <span data-ttu-id="6e0e0-123">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6e0e0-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6e0e0-124">MOF</span><span class="sxs-lookup"><span data-stu-id="6e0e0-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e0e0-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e0e0-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e0e0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6e0e0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e0e0-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e0e0-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6e0e0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e0e0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e0e0-129">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="6e0e0-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




