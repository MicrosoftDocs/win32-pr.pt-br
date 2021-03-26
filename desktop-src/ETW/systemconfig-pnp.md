---
description: Essa classe é a classe de tipo de evento para eventos PnP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 01e9a8bb-3f54-4e20-b4db-1b4bba745d4f
title: Classe SystemConfig_PnP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PnP
- SystemConfig_PnP.IDLength
- SystemConfig_PnP.DescriptionLength
- SystemConfig_PnP.FriendlyNameLength
- SystemConfig_PnP.DeviceID
- SystemConfig_PnP.DeviceDescription
- SystemConfig_PnP.FriendlyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2bd4cdbbec5c61f453a0ef6fae3fef0bd494edac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461046"
---
# <a name="systemconfig_pnp-class"></a><span data-ttu-id="50c1d-104">\_Classe PNP SystemConfig</span><span class="sxs-lookup"><span data-stu-id="50c1d-104">SystemConfig\_PnP class</span></span>

<span data-ttu-id="50c1d-105">Essa classe é a classe de tipo de evento para eventos PnP.</span><span class="sxs-lookup"><span data-stu-id="50c1d-105">This class is the event type class for PnP events.</span></span>

<span data-ttu-id="50c1d-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="50c1d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="50c1d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50c1d-107">Syntax</span></span>

``` syntax
[EventType(22), EventTypeName("PnP")]
class SystemConfig_PnP : SystemConfig
{
  uint32 IDLength;
  uint32 DescriptionLength;
  uint32 FriendlyNameLength;
  string DeviceID;
  string DeviceDescription;
  string FriendlyName;
};
```

## <a name="members"></a><span data-ttu-id="50c1d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="50c1d-108">Members</span></span>

<span data-ttu-id="50c1d-109">A **classe \_ PNP SystemConfig** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="50c1d-109">The **SystemConfig\_PnP** class has these types of members:</span></span>

-   [<span data-ttu-id="50c1d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="50c1d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50c1d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="50c1d-111">Properties</span></span>

<span data-ttu-id="50c1d-112">A **classe \_ PNP SystemConfig** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="50c1d-112">The **SystemConfig\_PnP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50c1d-113">**DescriptionLength**</span><span class="sxs-lookup"><span data-stu-id="50c1d-113">**DescriptionLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50c1d-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50c1d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50c1d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50c1d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50c1d-116">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="50c1d-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="50c1d-117">Comprimento, em caracteres, da cadeia de caracteres DeviceDescription.</span><span class="sxs-lookup"><span data-stu-id="50c1d-117">Length, in characters, of the DeviceDescription string.</span></span>

</dd> <dt>

<span data-ttu-id="50c1d-118">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="50c1d-118">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50c1d-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50c1d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50c1d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50c1d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50c1d-121">Qualificadores: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="50c1d-121">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="50c1d-122">Descrição do dispositivo PnP.</span><span class="sxs-lookup"><span data-stu-id="50c1d-122">Description of the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="50c1d-123">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="50c1d-123">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50c1d-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50c1d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50c1d-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50c1d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50c1d-126">Qualificadores: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="50c1d-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="50c1d-127">Identifica o dispositivo PnP.</span><span class="sxs-lookup"><span data-stu-id="50c1d-127">Identifies the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="50c1d-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="50c1d-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50c1d-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="50c1d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50c1d-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50c1d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50c1d-131">Qualificadores: WmiDataId (6), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="50c1d-131">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="50c1d-132">Nome do dispositivo PnP a ser usado em uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="50c1d-132">Name of the PnP device to use in a user interface.</span></span>

</dd> <dt>

<span data-ttu-id="50c1d-133">**FriendlyNameLength**</span><span class="sxs-lookup"><span data-stu-id="50c1d-133">**FriendlyNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50c1d-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50c1d-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50c1d-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50c1d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50c1d-136">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="50c1d-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="50c1d-137">Comprimento, em caracteres, da cadeia de caracteres amigável.</span><span class="sxs-lookup"><span data-stu-id="50c1d-137">Length, in characters, of the FriendlyName string.</span></span>

</dd> <dt>

<span data-ttu-id="50c1d-138">**IDLength**</span><span class="sxs-lookup"><span data-stu-id="50c1d-138">**IDLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50c1d-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50c1d-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50c1d-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="50c1d-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50c1d-141">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="50c1d-141">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="50c1d-142">Comprimento, em caracteres, da cadeia de caracteres DeviceID.</span><span class="sxs-lookup"><span data-stu-id="50c1d-142">Length, in characters, of the DeviceID string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50c1d-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50c1d-143">Requirements</span></span>



| <span data-ttu-id="50c1d-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="50c1d-144">Requirement</span></span> | <span data-ttu-id="50c1d-145">Valor</span><span class="sxs-lookup"><span data-stu-id="50c1d-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="50c1d-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50c1d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="50c1d-147">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50c1d-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="50c1d-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50c1d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="50c1d-149">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="50c1d-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50c1d-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="50c1d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50c1d-151">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="50c1d-151">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




