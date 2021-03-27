---
description: Essa classe é a classe de tipo de evento para eventos de configuração de energia. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: Classe SystemConfig_V0_Power
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Power
- SystemConfig_V0_Power.s1
- SystemConfig_V0_Power.s2
- SystemConfig_V0_Power.s3
- SystemConfig_V0_Power.s4
- SystemConfig_V0_Power.s5
- SystemConfig_V0_Power.Pad1
- SystemConfig_V0_Power.Pad2
- SystemConfig_V0_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2e42af68ad12857d65d776b7a73794d2d13b2b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967379"
---
# <a name="systemconfig_v0_power-class"></a><span data-ttu-id="06eee-104">\_Classe de \_ energia SystemConfig V0</span><span class="sxs-lookup"><span data-stu-id="06eee-104">SystemConfig\_V0\_Power class</span></span>

<span data-ttu-id="06eee-105">Essa classe é a classe de tipo de evento para eventos de configuração de energia.</span><span class="sxs-lookup"><span data-stu-id="06eee-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="06eee-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="06eee-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="06eee-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06eee-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_V0_Power : SystemConfig_V0
{
  boolean s1;
  boolean s2;
  boolean s3;
  boolean s4;
  boolean s5;
  uint8   Pad1;
  uint8   Pad2;
  uint8   Pad3;
};
```

## <a name="members"></a><span data-ttu-id="06eee-108">Membros</span><span class="sxs-lookup"><span data-stu-id="06eee-108">Members</span></span>

<span data-ttu-id="06eee-109">A classe de **\_ \_ energia SystemConfig V0** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="06eee-109">The **SystemConfig\_V0\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="06eee-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="06eee-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06eee-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="06eee-111">Properties</span></span>

<span data-ttu-id="06eee-112">A classe de **\_ \_ energia SystemConfig V0** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="06eee-112">The **SystemConfig\_V0\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06eee-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="06eee-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06eee-114">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="06eee-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="06eee-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06eee-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06eee-116">Qualificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="06eee-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="06eee-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="06eee-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="06eee-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="06eee-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06eee-119">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="06eee-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="06eee-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06eee-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06eee-121">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="06eee-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="06eee-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="06eee-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="06eee-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="06eee-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06eee-124">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="06eee-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="06eee-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06eee-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06eee-126">Qualificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="06eee-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="06eee-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="06eee-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="06eee-128">s1</span><span class="sxs-lookup"><span data-stu-id="06eee-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06eee-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="06eee-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06eee-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06eee-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06eee-131">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="06eee-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="06eee-132">Verdadeiro indica que o sistema dá suporte ao estado de suspensão S1.</span><span class="sxs-lookup"><span data-stu-id="06eee-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="06eee-133">S2</span><span class="sxs-lookup"><span data-stu-id="06eee-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06eee-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="06eee-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06eee-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06eee-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06eee-136">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="06eee-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="06eee-137">Verdadeiro indica que o sistema dá suporte ao estado de suspensão S2.</span><span class="sxs-lookup"><span data-stu-id="06eee-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="06eee-138">s3</span><span class="sxs-lookup"><span data-stu-id="06eee-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06eee-139">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="06eee-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06eee-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06eee-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06eee-141">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="06eee-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="06eee-142">Verdadeiro indica que o sistema dá suporte ao estado de suspensão S3.</span><span class="sxs-lookup"><span data-stu-id="06eee-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="06eee-143">S4</span><span class="sxs-lookup"><span data-stu-id="06eee-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06eee-144">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="06eee-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06eee-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06eee-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06eee-146">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="06eee-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="06eee-147">Verdadeiro indica que o sistema dá suporte ao estado de suspensão S4.</span><span class="sxs-lookup"><span data-stu-id="06eee-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="06eee-148">S5</span><span class="sxs-lookup"><span data-stu-id="06eee-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06eee-149">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="06eee-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06eee-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06eee-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06eee-151">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="06eee-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="06eee-152">Verdadeiro indica que o sistema dá suporte ao estado de suspensão s5.</span><span class="sxs-lookup"><span data-stu-id="06eee-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06eee-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06eee-153">Requirements</span></span>



| <span data-ttu-id="06eee-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="06eee-154">Requirement</span></span> | <span data-ttu-id="06eee-155">Valor</span><span class="sxs-lookup"><span data-stu-id="06eee-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="06eee-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06eee-156">Minimum supported client</span></span><br/> | <span data-ttu-id="06eee-157">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="06eee-157">None supported</span></span><br/>                            |
| <span data-ttu-id="06eee-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06eee-158">Minimum supported server</span></span><br/> | <span data-ttu-id="06eee-159">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="06eee-159">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06eee-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="06eee-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06eee-161">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="06eee-161">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




