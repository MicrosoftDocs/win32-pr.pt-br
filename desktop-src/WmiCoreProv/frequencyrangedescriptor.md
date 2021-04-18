---
description: Representa um contêiner para características de um intervalo de frequência com suporte.
ms.assetid: eb07c10b-8d92-40bb-8a93-ebc5db46cfd3
title: Classe FrequencyRangeDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FrequencyRangeDescriptor
- FrequencyRangeDescriptor.Origin
- FrequencyRangeDescriptor.MinVSyncNumerator
- FrequencyRangeDescriptor.MinVSyncDenominator
- FrequencyRangeDescriptor.MaxVSyncNumerator
- FrequencyRangeDescriptor.MaxVSyncDenominator
- FrequencyRangeDescriptor.MinHSyncNumerator
- FrequencyRangeDescriptor.MinHSyncDenominator
- FrequencyRangeDescriptor.MaxHSyncNumerator
- FrequencyRangeDescriptor.MaxHSyncDenominator
- FrequencyRangeDescriptor.ConstraintType
- FrequencyRangeDescriptor.ActiveWidth
- FrequencyRangeDescriptor.ActiveHeight
- FrequencyRangeDescriptor.MaxPixelRate
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: d18bee8a69fd8663ea54973d6e4e8219f5f74e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794574"
---
# <a name="frequencyrangedescriptor-class"></a><span data-ttu-id="5c50d-103">Classe FrequencyRangeDescriptor</span><span class="sxs-lookup"><span data-stu-id="5c50d-103">FrequencyRangeDescriptor class</span></span>

<span data-ttu-id="5c50d-104">A classe WMI **FrequencyRangeDescriptor** representa um contêiner para características de um intervalo de frequência com suporte.</span><span class="sxs-lookup"><span data-stu-id="5c50d-104">The **FrequencyRangeDescriptor** WMI class represents a container for characteristics of a supported frequency range.</span></span> <span data-ttu-id="5c50d-105">As instâncias dessa classe são elementos da matriz **MonitorFreqRanges** em [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md).</span><span class="sxs-lookup"><span data-stu-id="5c50d-105">Instances of this class are elements of the **MonitorFreqRanges** array in [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5c50d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c50d-106">Syntax</span></span>

``` syntax
class FrequencyRangeDescriptor
{
  uint8  Origin;
  uint32 MinVSyncNumerator;
  uint32 MinVSyncDenominator;
  uint32 MaxVSyncNumerator;
  uint32 MaxVSyncDenominator;
  uint32 MinHSyncNumerator;
  uint32 MinHSyncDenominator;
  uint32 MaxHSyncNumerator;
  uint32 MaxHSyncDenominator;
  uint32 ConstraintType;
  uint32 ActiveWidth;
  uint32 ActiveHeight;
  uint32 MaxPixelRate;
};
```

## <a name="members"></a><span data-ttu-id="5c50d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5c50d-107">Members</span></span>

<span data-ttu-id="5c50d-108">A classe **FrequencyRangeDescriptor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5c50d-108">The **FrequencyRangeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="5c50d-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5c50d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c50d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5c50d-110">Properties</span></span>

<span data-ttu-id="5c50d-111">A classe **FrequencyRangeDescriptor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5c50d-111">The **FrequencyRangeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c50d-112">**ActiveHeight**</span><span class="sxs-lookup"><span data-stu-id="5c50d-112">**ActiveHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c50d-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c50d-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c50d-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c50d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c50d-115">Altura, em pixels, da imagem ativa.</span><span class="sxs-lookup"><span data-stu-id="5c50d-115">Height, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="5c50d-116">**ActiveWidth**</span><span class="sxs-lookup"><span data-stu-id="5c50d-116">**ActiveWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c50d-117">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c50d-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c50d-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c50d-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c50d-119">Largura, em pixels, da imagem ativa.</span><span class="sxs-lookup"><span data-stu-id="5c50d-119">Width, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="5c50d-120">**ConstraintType**</span><span class="sxs-lookup"><span data-stu-id="5c50d-120">**ConstraintType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c50d-121">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c50d-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c50d-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c50d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c50d-123">Tipo de restrição para o intervalo de frequência.</span><span class="sxs-lookup"><span data-stu-id="5c50d-123">Constraint type for the frequency range.</span></span>

</dd> <dt>

<span data-ttu-id="5c50d-124">**MaxHSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="5c50d-124">**MaxHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c50d-125">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c50d-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c50d-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c50d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c50d-127">Denominador de sincronização horizontal máximo.</span><span class="sxs-lookup"><span data-stu-id="5c50d-127">Maximum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="5c50d-128">**MaxHSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="5c50d-128">**MaxHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c50d-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c50d-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c50d-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c50d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c50d-131">Numerador de sincronização horizontal máximo em kilohertz (KHz).</span><span class="sxs-lookup"><span data-stu-id="5c50d-131">Maximum horizontal sync numerator in kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="5c50d-132">**MaxPixelRate**</span><span class="sxs-lookup"><span data-stu-id="5c50d-132">**MaxPixelRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c50d-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c50d-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c50d-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c50d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c50d-135">Taxa máxima de pixels em Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="5c50d-135">Maximum pixel rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="5c50d-136">**MaxVSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="5c50d-136">**MaxVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c50d-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c50d-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c50d-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c50d-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c50d-139">Denominador de sincronização vertical máximo.</span><span class="sxs-lookup"><span data-stu-id="5c50d-139">Maximum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="5c50d-140">**MaxVSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="5c50d-140">**MaxVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c50d-141">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c50d-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c50d-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c50d-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c50d-143">Numerador de sincronização vertical máximo, em Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="5c50d-143">Maximum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="5c50d-144">**MinHSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="5c50d-144">**MinHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c50d-145">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c50d-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c50d-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c50d-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c50d-147">Denominador de sincronização horizontal mínimo.</span><span class="sxs-lookup"><span data-stu-id="5c50d-147">Minimum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="5c50d-148">**MinHSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="5c50d-148">**MinHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c50d-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c50d-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c50d-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c50d-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c50d-151">Numerador de sincronização horizontal mínimo em, kilohertz (KHz).</span><span class="sxs-lookup"><span data-stu-id="5c50d-151">Minimum horizontal sync numerator in, kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="5c50d-152">**MinVSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="5c50d-152">**MinVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c50d-153">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c50d-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c50d-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c50d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c50d-155">Denominador de sincronização vertical mínimo.</span><span class="sxs-lookup"><span data-stu-id="5c50d-155">Minimum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="5c50d-156">**MinVSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="5c50d-156">**MinVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c50d-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c50d-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c50d-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c50d-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c50d-159">Numerador de sincronização vertical mínimo, em Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="5c50d-159">Minimum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="5c50d-160">**Ter**</span><span class="sxs-lookup"><span data-stu-id="5c50d-160">**Origin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c50d-161">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="5c50d-161">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5c50d-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c50d-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c50d-163">Ter.</span><span class="sxs-lookup"><span data-stu-id="5c50d-163">Origin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c50d-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c50d-164">Requirements</span></span>



| <span data-ttu-id="5c50d-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c50d-165">Requirement</span></span> | <span data-ttu-id="5c50d-166">Valor</span><span class="sxs-lookup"><span data-stu-id="5c50d-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c50d-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c50d-167">Minimum supported client</span></span><br/> | <span data-ttu-id="5c50d-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c50d-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5c50d-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c50d-169">Minimum supported server</span></span><br/> | <span data-ttu-id="5c50d-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c50d-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5c50d-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c50d-171">Namespace</span></span><br/>                | <span data-ttu-id="5c50d-172">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="5c50d-172">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="5c50d-173">MOF</span><span class="sxs-lookup"><span data-stu-id="5c50d-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c50d-174"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c50d-174"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c50d-175">DLL</span><span class="sxs-lookup"><span data-stu-id="5c50d-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c50d-176"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c50d-176"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c50d-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c50d-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c50d-178">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="5c50d-178">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




