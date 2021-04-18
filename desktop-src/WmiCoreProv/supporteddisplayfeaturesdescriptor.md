---
description: Representa os recursos de exibição com suporte do monitor.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: Classe SupportedDisplayFeaturesDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 30350d477533b7e51ba8b3130c5a24d81c12f10e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810913"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a><span data-ttu-id="c1584-103">Classe SupportedDisplayFeaturesDescriptor</span><span class="sxs-lookup"><span data-stu-id="c1584-103">SupportedDisplayFeaturesDescriptor class</span></span>

<span data-ttu-id="c1584-104">O **SupportedDisplayFeaturesDescriptor** representa os recursos de exibição com suporte do monitor.</span><span class="sxs-lookup"><span data-stu-id="c1584-104">The **SupportedDisplayFeaturesDescriptor** represents the supported display features of the monitor.</span></span> <span data-ttu-id="c1584-105">As informações nessa classe correspondem aos dados na definição de entrada de vídeo do padrão de dados de identificação de exibição estendida (E-EDID) avançado da VESA (Video Electronics Standard Association).</span><span class="sxs-lookup"><span data-stu-id="c1584-105">The information in this class corresponds to data in the Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1584-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1584-106">Syntax</span></span>

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a><span data-ttu-id="c1584-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c1584-107">Members</span></span>

<span data-ttu-id="c1584-108">A classe **SupportedDisplayFeaturesDescriptor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c1584-108">The **SupportedDisplayFeaturesDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="c1584-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1584-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1584-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1584-110">Properties</span></span>

<span data-ttu-id="c1584-111">A classe **SupportedDisplayFeaturesDescriptor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c1584-111">The **SupportedDisplayFeaturesDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c1584-112">**ActiveOffSupported**</span><span class="sxs-lookup"><span data-stu-id="c1584-112">**ActiveOffSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1584-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c1584-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1584-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1584-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1584-115">Suporte para ativo e energia muito baixa.</span><span class="sxs-lookup"><span data-stu-id="c1584-115">Support for active off and very low power.</span></span> <span data-ttu-id="c1584-116">A exibição consome menos energia quando recebe um sinal de intervalo que está fora do intervalo de operação do ativo declarado.</span><span class="sxs-lookup"><span data-stu-id="c1584-116">The display consumes less power when it receives a timing signal that is outside the declared active operating range.</span></span> <span data-ttu-id="c1584-117">A exibição será revertida para a operação normal se o sinal de intervalo retornar ao intervalo de operação normal.</span><span class="sxs-lookup"><span data-stu-id="c1584-117">The display will revert to normal operation if the timing signal returns to the normal operating range.</span></span> <span data-ttu-id="c1584-118">Exemplos de sinais de tempo fora do intervalo de operação normal não são sinais DE sincronização ou nenhum sinal DE.</span><span class="sxs-lookup"><span data-stu-id="c1584-118">Examples of timing signals outside the normal operating range are no sync signals or no DE signal.</span></span>

</dd> <dt>

<span data-ttu-id="c1584-119">**TipoDeExibição**</span><span class="sxs-lookup"><span data-stu-id="c1584-119">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1584-120">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="c1584-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c1584-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1584-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1584-122">Tipo de exibição do monitor.</span><span class="sxs-lookup"><span data-stu-id="c1584-122">Type of display for the monitor.</span></span> <span data-ttu-id="c1584-123">A tabela a seguir lista os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="c1584-123">The following table lists possible values.</span></span>



| <span data-ttu-id="c1584-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c1584-124">Value</span></span>                                                                              | <span data-ttu-id="c1584-125">Significado</span><span class="sxs-lookup"><span data-stu-id="c1584-125">Meaning</span></span>                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="c1584-126"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c1584-126"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c1584-127">Exibição monocromática/escala de cinza</span><span class="sxs-lookup"><span data-stu-id="c1584-127">Monochrome/grayscale display</span></span><br/> |
| <dl> <span data-ttu-id="c1584-128"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="c1584-128"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="c1584-129">Exibição de cor RGB</span><span class="sxs-lookup"><span data-stu-id="c1584-129">RGB color display</span></span><br/>            |
| <dl> <span data-ttu-id="c1584-130"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="c1584-130"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="c1584-131">Exibição de cores não RGB</span><span class="sxs-lookup"><span data-stu-id="c1584-131">Non-RGB multicolor display</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c1584-132">**GTFSupported**</span><span class="sxs-lookup"><span data-stu-id="c1584-132">**GTFSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1584-133">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c1584-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1584-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1584-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1584-135">Indica se a exibição tem suporte GTF.</span><span class="sxs-lookup"><span data-stu-id="c1584-135">Indicates whether the display has GTF support.</span></span> <span data-ttu-id="c1584-136">Se **for true**, a exibição dará suporte a intervalos com base no padrão GTF usando valores de parâmetro GTF padrão.</span><span class="sxs-lookup"><span data-stu-id="c1584-136">If **True**, the display supports timings based on the GTF standard using default GTF parameter values.</span></span>

</dd> <dt>

<span data-ttu-id="c1584-137">**HasPreferredTimingMode**</span><span class="sxs-lookup"><span data-stu-id="c1584-137">**HasPreferredTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1584-138">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c1584-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1584-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1584-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1584-140">Indica se a exibição tem um modo de temporizador preferencial.</span><span class="sxs-lookup"><span data-stu-id="c1584-140">Indicates whether the display has has a preferred timing mode.</span></span> <span data-ttu-id="c1584-141">Se **for true**, o primeiro bloco de tempo detalhado conterá o modo de temporização preferencial do monitor.</span><span class="sxs-lookup"><span data-stu-id="c1584-141">If **True**, the first detailed timing block contains the preferred timing mode of the monitor.</span></span> <span data-ttu-id="c1584-142">O uso do modo de temporização preferencial é exigido pelo EDID v. 1.3 e superior.</span><span class="sxs-lookup"><span data-stu-id="c1584-142">Use of preferred timing mode is required by EDID v.1.3 and higher.</span></span>

</dd> <dt>

<span data-ttu-id="c1584-143">**sRGBSupported**</span><span class="sxs-lookup"><span data-stu-id="c1584-143">**sRGBSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1584-144">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c1584-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1584-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1584-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1584-146">Se **for true**, a exibição dará suporte a sRGB.</span><span class="sxs-lookup"><span data-stu-id="c1584-146">If **True**, the display supports sRGB.</span></span>

</dd> <dt>

<span data-ttu-id="c1584-147">**StandbySupported**</span><span class="sxs-lookup"><span data-stu-id="c1584-147">**StandbySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1584-148">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c1584-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1584-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1584-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1584-150">Indica se a exibição dá suporte à espera de DPMS (sinalização de gerenciamento de energia de vídeo VESA).</span><span class="sxs-lookup"><span data-stu-id="c1584-150">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) standby.</span></span> <span data-ttu-id="c1584-151">Se for **true**, o DPMS standby terá suporte.</span><span class="sxs-lookup"><span data-stu-id="c1584-151">If **True**, DPMS standby is supported.</span></span>

</dd> <dt>

<span data-ttu-id="c1584-152">**SuspendSupported**</span><span class="sxs-lookup"><span data-stu-id="c1584-152">**SuspendSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1584-153">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c1584-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1584-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1584-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1584-155">Indica se a exibição dá suporte à suspensão de sinalização de gerenciamento de energia de vídeo VESA (DPMS).</span><span class="sxs-lookup"><span data-stu-id="c1584-155">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) suspend.</span></span> <span data-ttu-id="c1584-156">Se for **true**, haverá suporte para a suspensão de DPMS.</span><span class="sxs-lookup"><span data-stu-id="c1584-156">If **True**, DPMS suspend is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1584-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1584-157">Requirements</span></span>



| <span data-ttu-id="c1584-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1584-158">Requirement</span></span> | <span data-ttu-id="c1584-159">Valor</span><span class="sxs-lookup"><span data-stu-id="c1584-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1584-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1584-160">Minimum supported client</span></span><br/> | <span data-ttu-id="c1584-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1584-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c1584-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1584-162">Minimum supported server</span></span><br/> | <span data-ttu-id="c1584-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1584-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c1584-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1584-164">Namespace</span></span><br/>                | <span data-ttu-id="c1584-165">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="c1584-165">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="c1584-166">MOF</span><span class="sxs-lookup"><span data-stu-id="c1584-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1584-167"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1584-167"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1584-168">DLL</span><span class="sxs-lookup"><span data-stu-id="c1584-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1584-169"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1584-169"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1584-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1584-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1584-171">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="c1584-171">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




