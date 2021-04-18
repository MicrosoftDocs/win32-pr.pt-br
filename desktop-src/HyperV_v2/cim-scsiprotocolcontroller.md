---
description: Representa um controlador de protocolo que gerencia uma interface SCSI.
ms.assetid: 01ef85fc-2f05-4453-b524-7d63b647f6fb
title: Classe CIM_SCSIProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIProtocolController
- CIM_SCSIProtocolController.NameFormat
- CIM_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6479b405d3ca499615981d62744b1eaf25c7598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761718"
---
# <a name="cim_scsiprotocolcontroller-class"></a><span data-ttu-id="1b599-103">\_Classe CIM SCSIProtocolController</span><span class="sxs-lookup"><span data-stu-id="1b599-103">CIM\_SCSIProtocolController class</span></span>

<span data-ttu-id="1b599-104">Representa um controlador de protocolo que gerencia uma interface SCSI.</span><span class="sxs-lookup"><span data-stu-id="1b599-104">Represents a protocol controller that manages a SCSI interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b599-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b599-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_SCSIProtocolController : CIM_ProtocolController
{
  uint16 NameFormat;
  string OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="1b599-106">Membros</span><span class="sxs-lookup"><span data-stu-id="1b599-106">Members</span></span>

<span data-ttu-id="1b599-107">A classe **CIM \_ SCSIProtocolController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1b599-107">The **CIM\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="1b599-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1b599-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b599-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1b599-109">Properties</span></span>

<span data-ttu-id="1b599-110">A classe **CIM \_ SCSIProtocolController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1b599-110">The **CIM\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b599-111">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="1b599-111">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b599-112">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b599-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b599-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b599-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b599-114">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Name**","**CIM \_ SCSIProtocolController**.**OtherNameFormat**")</span><span class="sxs-lookup"><span data-stu-id="1b599-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="1b599-115">O formato da propriedade **Name** do **\_ SCSIProtocolController CIM**.</span><span class="sxs-lookup"><span data-stu-id="1b599-115">The format of the **Name** property of the **CIM\_SCSIProtocolController**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1b599-116">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1b599-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1b599-117">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1b599-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Port_WWN"></span><span id="fc_port_wwn"></span><span id="FC_PORT_WWN"></span>

<span data-ttu-id="1b599-118">**Porta FC WWN** (2)</span><span class="sxs-lookup"><span data-stu-id="1b599-118">**FC Port WWN** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_Name"></span><span id="iscsi_name"></span><span id="ISCSI_NAME"></span>

<span data-ttu-id="1b599-119">**nome iSCSI** (3)</span><span class="sxs-lookup"><span data-stu-id="1b599-119">**iSCSI Name** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1b599-120">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="1b599-120">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b599-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b599-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b599-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b599-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b599-123">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Name**","**CIM \_ SCSIProtocolController**.**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="1b599-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="1b599-124">Uma descrição da propriedade **NameFormat** quando **NameFormat** é definido como "1" (outro).</span><span class="sxs-lookup"><span data-stu-id="1b599-124">A description of the **NameFormat** property when **NameFormat** is set to "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b599-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b599-125">Requirements</span></span>



| <span data-ttu-id="1b599-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b599-126">Requirement</span></span> | <span data-ttu-id="1b599-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1b599-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b599-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b599-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1b599-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1b599-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1b599-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b599-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1b599-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1b599-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1b599-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b599-132">Namespace</span></span><br/>                | <span data-ttu-id="1b599-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1b599-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1b599-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1b599-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b599-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b599-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b599-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1b599-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b599-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1b599-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1b599-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b599-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b599-139">**\_PROTOCOLCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="1b599-139">**CIM\_ProtocolController**</span></span>](cim-protocolcontroller.md)
</dt> </dl>

 

