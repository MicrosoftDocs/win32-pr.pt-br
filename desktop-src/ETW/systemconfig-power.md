---
description: Classe SystemConfig_Power-essa classe é a classe de tipo de evento para eventos de configuração de energia. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 7065b0b0-9a1d-4fce-a494-5762d5efb239
title: Classe SystemConfig_Power
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Power
- SystemConfig_Power.s1
- SystemConfig_Power.s2
- SystemConfig_Power.s3
- SystemConfig_Power.s4
- SystemConfig_Power.s5
- SystemConfig_Power.Pad1
- SystemConfig_Power.Pad2
- SystemConfig_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: d7338faad8c313847ad7db7aaac5d4000abba5be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106064"
---
# <a name="systemconfig_power-class"></a><span data-ttu-id="e2a3a-104">\_Classe de energia SystemConfig</span><span class="sxs-lookup"><span data-stu-id="e2a3a-104">SystemConfig\_Power class</span></span>

<span data-ttu-id="e2a3a-105">Essa classe é a classe de tipo de evento para eventos de configuração de energia.</span><span class="sxs-lookup"><span data-stu-id="e2a3a-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="e2a3a-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="e2a3a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2a3a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2a3a-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_Power : SystemConfig
{
  uint8 s1;
  uint8 s2;
  uint8 s3;
  uint8 s4;
  uint8 s5;
  uint8 Pad1;
  uint8 Pad2;
  uint8 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="e2a3a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e2a3a-108">Members</span></span>

<span data-ttu-id="e2a3a-109">A classe de **\_ energia SystemConfig** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e2a3a-109">The **SystemConfig\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="e2a3a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e2a3a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2a3a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e2a3a-111">Properties</span></span>

<span data-ttu-id="e2a3a-112">A classe de **\_ energia SystemConfig** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e2a3a-112">The **SystemConfig\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2a3a-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="e2a3a-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a3a-114">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="e2a3a-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2a3a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-116">Qualificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="e2a3a-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="e2a3a-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="e2a3a-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2a3a-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="e2a3a-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a3a-119">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="e2a3a-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2a3a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-121">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="e2a3a-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="e2a3a-122">Não usado.</span><span class="sxs-lookup"><span data-stu-id="e2a3a-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2a3a-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="e2a3a-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a3a-124">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="e2a3a-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2a3a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-126">Qualificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="e2a3a-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="e2a3a-127">Não usado.</span><span class="sxs-lookup"><span data-stu-id="e2a3a-127">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2a3a-128">s1</span><span class="sxs-lookup"><span data-stu-id="e2a3a-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a3a-129">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="e2a3a-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2a3a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-131">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="e2a3a-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="e2a3a-132">Verdadeiro indica que o sistema dá suporte ao estado de suspensão S1.</span><span class="sxs-lookup"><span data-stu-id="e2a3a-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="e2a3a-133">S2</span><span class="sxs-lookup"><span data-stu-id="e2a3a-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a3a-134">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="e2a3a-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2a3a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-136">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="e2a3a-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="e2a3a-137">Verdadeiro indica que o sistema dá suporte ao estado de suspensão S2.</span><span class="sxs-lookup"><span data-stu-id="e2a3a-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="e2a3a-138">s3</span><span class="sxs-lookup"><span data-stu-id="e2a3a-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a3a-139">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="e2a3a-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2a3a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-141">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="e2a3a-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e2a3a-142">Verdadeiro indica que o sistema dá suporte ao estado de suspensão S3.</span><span class="sxs-lookup"><span data-stu-id="e2a3a-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="e2a3a-143">S4</span><span class="sxs-lookup"><span data-stu-id="e2a3a-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a3a-144">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="e2a3a-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2a3a-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-146">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="e2a3a-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="e2a3a-147">Verdadeiro indica que o sistema dá suporte ao estado de suspensão S4.</span><span class="sxs-lookup"><span data-stu-id="e2a3a-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="e2a3a-148">S5</span><span class="sxs-lookup"><span data-stu-id="e2a3a-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a3a-149">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="e2a3a-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2a3a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a3a-151">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="e2a3a-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="e2a3a-152">Verdadeiro indica que o sistema dá suporte ao estado de suspensão s5.</span><span class="sxs-lookup"><span data-stu-id="e2a3a-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2a3a-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2a3a-153">Requirements</span></span>



| <span data-ttu-id="e2a3a-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2a3a-154">Requirement</span></span> | <span data-ttu-id="e2a3a-155">Valor</span><span class="sxs-lookup"><span data-stu-id="e2a3a-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2a3a-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2a3a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="e2a3a-157">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2a3a-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e2a3a-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2a3a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="e2a3a-159">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2a3a-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2a3a-160">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e2a3a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a3a-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="e2a3a-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




