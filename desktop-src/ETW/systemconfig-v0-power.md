---
description: Classe SystemConfig_V0_Power-essa classe é a classe de tipo de evento para eventos de configuração de energia. A sintaxe a seguir é simplificada do código MOF.
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
ms.openlocfilehash: ab268e719374906e149dc9c1b733487f986e8308
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105934"
---
# <a name="systemconfig_v0_power-class"></a><span data-ttu-id="5cca8-104">\_Classe de \_ energia SystemConfig V0</span><span class="sxs-lookup"><span data-stu-id="5cca8-104">SystemConfig\_V0\_Power class</span></span>

<span data-ttu-id="5cca8-105">Essa classe é a classe de tipo de evento para eventos de configuração de energia.</span><span class="sxs-lookup"><span data-stu-id="5cca8-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="5cca8-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="5cca8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cca8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5cca8-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="5cca8-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5cca8-108">Members</span></span>

<span data-ttu-id="5cca8-109">A classe de **\_ \_ energia SystemConfig V0** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5cca8-109">The **SystemConfig\_V0\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="5cca8-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5cca8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5cca8-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5cca8-111">Properties</span></span>

<span data-ttu-id="5cca8-112">A classe de **\_ \_ energia SystemConfig V0** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5cca8-112">The **SystemConfig\_V0\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5cca8-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="5cca8-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cca8-114">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="5cca8-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5cca8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-116">Qualificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="5cca8-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="5cca8-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5cca8-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5cca8-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="5cca8-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cca8-119">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="5cca8-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5cca8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-121">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="5cca8-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="5cca8-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5cca8-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5cca8-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="5cca8-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cca8-124">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="5cca8-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5cca8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-126">Qualificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="5cca8-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="5cca8-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5cca8-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5cca8-128">s1</span><span class="sxs-lookup"><span data-stu-id="5cca8-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cca8-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5cca8-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5cca8-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-131">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="5cca8-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="5cca8-132">Verdadeiro indica que o sistema dá suporte ao estado de suspensão S1.</span><span class="sxs-lookup"><span data-stu-id="5cca8-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="5cca8-133">S2</span><span class="sxs-lookup"><span data-stu-id="5cca8-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cca8-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5cca8-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5cca8-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-136">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="5cca8-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="5cca8-137">Verdadeiro indica que o sistema dá suporte ao estado de suspensão S2.</span><span class="sxs-lookup"><span data-stu-id="5cca8-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="5cca8-138">s3</span><span class="sxs-lookup"><span data-stu-id="5cca8-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cca8-139">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5cca8-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5cca8-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-141">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="5cca8-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="5cca8-142">Verdadeiro indica que o sistema dá suporte ao estado de suspensão S3.</span><span class="sxs-lookup"><span data-stu-id="5cca8-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="5cca8-143">S4</span><span class="sxs-lookup"><span data-stu-id="5cca8-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cca8-144">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5cca8-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5cca8-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-146">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="5cca8-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="5cca8-147">Verdadeiro indica que o sistema dá suporte ao estado de suspensão S4.</span><span class="sxs-lookup"><span data-stu-id="5cca8-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="5cca8-148">S5</span><span class="sxs-lookup"><span data-stu-id="5cca8-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cca8-149">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5cca8-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5cca8-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cca8-151">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="5cca8-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="5cca8-152">Verdadeiro indica que o sistema dá suporte ao estado de suspensão s5.</span><span class="sxs-lookup"><span data-stu-id="5cca8-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5cca8-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cca8-153">Requirements</span></span>



| <span data-ttu-id="5cca8-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cca8-154">Requirement</span></span> | <span data-ttu-id="5cca8-155">Valor</span><span class="sxs-lookup"><span data-stu-id="5cca8-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5cca8-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cca8-156">Minimum supported client</span></span><br/> | <span data-ttu-id="5cca8-157">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5cca8-157">None supported</span></span><br/>                            |
| <span data-ttu-id="5cca8-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cca8-158">Minimum supported server</span></span><br/> | <span data-ttu-id="5cca8-159">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5cca8-159">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cca8-160">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5cca8-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cca8-161">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="5cca8-161">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




