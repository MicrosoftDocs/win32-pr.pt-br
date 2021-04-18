---
description: Representa os recursos e o gerenciamento de uma unidade de fita.
ms.assetid: 8140fd9a-8a12-43b4-bc61-ec143e5d754c
title: Classe CIM_TapeDrive (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.Padding
- CIM_TapeDrive.MaxRewindTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b92360388b71abcb0b67d30fddea9b4f5ed7920f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778762"
---
# <a name="cim_tapedrive-class-hyper-v-management"></a><span data-ttu-id="ca858-103">Classe CIM_TapeDrive (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="ca858-103">CIM_TapeDrive class (Hyper-V management)</span></span>

<span data-ttu-id="ca858-104">Representa os recursos e o gerenciamento de uma unidade de fita.</span><span class="sxs-lookup"><span data-stu-id="ca858-104">Represents the capabilities and management of a tape drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca858-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca858-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices")]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint32 EOTWarningZoneSize;
  uint32 MaxPartitionCount;
  uint32 Padding;
  uint64 MaxRewindTime;
};
```

## <a name="members"></a><span data-ttu-id="ca858-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ca858-106">Members</span></span>

<span data-ttu-id="ca858-107">A classe **CIM \_ TapeDrive** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ca858-107">The **CIM\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="ca858-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ca858-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca858-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ca858-109">Properties</span></span>

<span data-ttu-id="ca858-110">A classe **CIM \_ TapeDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ca858-110">The **CIM\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca858-111">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="ca858-111">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca858-112">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca858-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca858-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca858-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca858-114">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **PUnit** ("byte")</span><span class="sxs-lookup"><span data-stu-id="ca858-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="ca858-115">O tamanho, em bytes, da área designada como "fim da fita".</span><span class="sxs-lookup"><span data-stu-id="ca858-115">The size, in bytes, of the area designated as "end of tape".</span></span> <span data-ttu-id="ca858-116">O acesso nessa área gera um aviso de "fim da fita".</span><span class="sxs-lookup"><span data-stu-id="ca858-116">Access in this area generates an "end of tape" warning.</span></span>

</dd> <dt>

<span data-ttu-id="ca858-117">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="ca858-117">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca858-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca858-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca858-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca858-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca858-120">A contagem máxima de partições para a unidade de fita.</span><span class="sxs-lookup"><span data-stu-id="ca858-120">The maximum partition count for the tape drive.</span></span>

</dd> <dt>

<span data-ttu-id="ca858-121">**MaxRewindTime**</span><span class="sxs-lookup"><span data-stu-id="ca858-121">**MaxRewindTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca858-122">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ca858-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ca858-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca858-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca858-124">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos"), **PUnit** ("segundo \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="ca858-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="ca858-125">O tempo, em milissegundos, para mover do ponto mais distante fisicamente na fita até o início.</span><span class="sxs-lookup"><span data-stu-id="ca858-125">The time, in milliseconds, to move from the most physically distant point on the tape to the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="ca858-126">**Preenchimento**</span><span class="sxs-lookup"><span data-stu-id="ca858-126">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca858-127">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca858-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca858-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca858-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca858-129">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **PUnit** ("byte")</span><span class="sxs-lookup"><span data-stu-id="ca858-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="ca858-130">O número de bytes inseridos entre os blocos na mídia de fita.</span><span class="sxs-lookup"><span data-stu-id="ca858-130">The number of bytes inserted between blocks on tape media.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca858-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca858-131">Requirements</span></span>



| <span data-ttu-id="ca858-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca858-132">Requirement</span></span> | <span data-ttu-id="ca858-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ca858-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca858-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca858-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ca858-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ca858-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ca858-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca858-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ca858-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ca858-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ca858-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca858-138">Namespace</span></span><br/>                | <span data-ttu-id="ca858-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ca858-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ca858-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ca858-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca858-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca858-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca858-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ca858-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca858-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca858-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ca858-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca858-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca858-145">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ca858-145">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

