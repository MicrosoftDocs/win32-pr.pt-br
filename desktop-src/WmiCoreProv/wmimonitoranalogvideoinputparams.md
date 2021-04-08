---
description: Representa os parâmetros de entrada de vídeo analógicos de um monitor de computador.
ms.assetid: 87d4260d-06c7-4a76-a3a1-8f6e51e23d92
title: Classe WmiMonitorAnalogVideoInputParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorAnalogVideoInputParams
- WmiMonitorAnalogVideoInputParams.Active
- WmiMonitorAnalogVideoInputParams.CompositeSyncSupported
- WmiMonitorAnalogVideoInputParams.InstanceName
- WmiMonitorAnalogVideoInputParams.SeparateSyncsSupported
- WmiMonitorAnalogVideoInputParams.SerrationOfVsyncRequired
- WmiMonitorAnalogVideoInputParams.SetupExpected
- WmiMonitorAnalogVideoInputParams.SignalLevelStandard
- WmiMonitorAnalogVideoInputParams.SyncOnGreenVideoSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 900bf4353de0c81acb5aa2c69578256b0212a2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922081"
---
# <a name="wmimonitoranalogvideoinputparams-class"></a><span data-ttu-id="c8031-103">Classe WmiMonitorAnalogVideoInputParams</span><span class="sxs-lookup"><span data-stu-id="c8031-103">WmiMonitorAnalogVideoInputParams class</span></span>

<span data-ttu-id="c8031-104">A classe WMI **WmiMonitorAnalogVideoInputParams** representa os parâmetros de entrada de vídeo analógicos de um monitor de computador.</span><span class="sxs-lookup"><span data-stu-id="c8031-104">The **WmiMonitorAnalogVideoInputParams** WMI class represents the analog video input parameters of a computer monitor.</span></span> <span data-ttu-id="c8031-105">Os dados nessa classe correspondem aos dados na definição de entrada de vídeo do padrão de dados de identificação de vídeo estendido (E-EDID) avançado de associação de vídeo de eletrônicos (VESA).</span><span class="sxs-lookup"><span data-stu-id="c8031-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="c8031-106">Uma instância dessa classe está disponível somente quando o valor da propriedade **VideoInputType** da classe [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) é "analógico".</span><span class="sxs-lookup"><span data-stu-id="c8031-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Analog".</span></span>

## <a name="syntax"></a><span data-ttu-id="c8031-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8031-107">Syntax</span></span>

``` syntax
class WmiMonitorAnalogVideoInputParams : MSMonitorClass
{
  boolean Active;
  uint8   CompositeSyncSupported;
  string  InstanceName;
  uint8   SeparateSyncsSupported;
  uint8   SerrationOfVsyncRequired;
  uint8   SetupExpected;
  uint8   SignalLevelStandard;
  uint8   SyncOnGreenVideoSupported;
};
```

## <a name="members"></a><span data-ttu-id="c8031-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c8031-108">Members</span></span>

<span data-ttu-id="c8031-109">A classe **WmiMonitorAnalogVideoInputParams** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c8031-109">The **WmiMonitorAnalogVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="c8031-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c8031-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8031-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c8031-111">Properties</span></span>

<span data-ttu-id="c8031-112">A classe **WmiMonitorAnalogVideoInputParams** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c8031-112">The **WmiMonitorAnalogVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8031-113">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="c8031-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8031-114">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c8031-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8031-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8031-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8031-116">Indica o monitor ativo.</span><span class="sxs-lookup"><span data-stu-id="c8031-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="c8031-117">**CompositeSyncSupported**</span><span class="sxs-lookup"><span data-stu-id="c8031-117">**CompositeSyncSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8031-118">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="c8031-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c8031-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8031-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8031-120">Indica se há suporte para a sincronização composta.</span><span class="sxs-lookup"><span data-stu-id="c8031-120">Indicates whether composite sync is supported.</span></span>



| <span data-ttu-id="c8031-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c8031-121">Value</span></span>                                                                              | <span data-ttu-id="c8031-122">Significado</span><span class="sxs-lookup"><span data-stu-id="c8031-122">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8031-123"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-123"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c8031-124">Há suporte para a sincronização composta na linha de sincronização horizontal.</span><span class="sxs-lookup"><span data-stu-id="c8031-124">Composite sync on horizontal sync line is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="c8031-125"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-125"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="c8031-126">Não há suporte para a sincronização composta na linha de sincronização horizontal.</span><span class="sxs-lookup"><span data-stu-id="c8031-126">Composite sync on horizontal sync line is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c8031-127">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="c8031-127">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8031-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8031-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8031-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8031-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8031-130">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="c8031-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c8031-131">Nome da instância de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="c8031-131">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="c8031-132">**SeparateSyncsSupported**</span><span class="sxs-lookup"><span data-stu-id="c8031-132">**SeparateSyncsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8031-133">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="c8031-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c8031-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8031-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8031-135">Indica se há suporte para sincronizações separadas.</span><span class="sxs-lookup"><span data-stu-id="c8031-135">Indicates whether separate syncs are supported.</span></span>



| <span data-ttu-id="c8031-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c8031-136">Value</span></span>                                                                              | <span data-ttu-id="c8031-137">Significado</span><span class="sxs-lookup"><span data-stu-id="c8031-137">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c8031-138"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-138"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c8031-139">Há suporte para sincronizações separadas.</span><span class="sxs-lookup"><span data-stu-id="c8031-139">Separate syncs are supported.</span></span><br/>     |
| <dl> <span data-ttu-id="c8031-140"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-140"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="c8031-141">Não há suporte para sincronizações separadas.</span><span class="sxs-lookup"><span data-stu-id="c8031-141">Separate syncs are not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c8031-142">**SerrationOfVsyncRequired**</span><span class="sxs-lookup"><span data-stu-id="c8031-142">**SerrationOfVsyncRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8031-143">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="c8031-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c8031-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8031-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8031-145">Indica se o pulso de sincronização vertical serration é necessário.</span><span class="sxs-lookup"><span data-stu-id="c8031-145">Indicates whether vertical sync pulse serration is required.</span></span>



| <span data-ttu-id="c8031-146">Valor</span><span class="sxs-lookup"><span data-stu-id="c8031-146">Value</span></span>                                                                              | <span data-ttu-id="c8031-147">Significado</span><span class="sxs-lookup"><span data-stu-id="c8031-147">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8031-148"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-148"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c8031-149">Serration do pulso de sincronização vertical é necessário quando a sincronização de composição ou o vídeo de sincronização em verde é usado.</span><span class="sxs-lookup"><span data-stu-id="c8031-149">Serration of the vertical sync pulse is required when composite sync or sync-on-green video is used.</span></span><br/>     |
| <dl> <span data-ttu-id="c8031-150"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-150"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="c8031-151">Serration do pulso de sincronização vertical não é necessário quando a sincronização de composição ou o vídeo de sincronização em verde é usado.</span><span class="sxs-lookup"><span data-stu-id="c8031-151">Serration of the vertical sync pulse is not required when composite sync or sync-on-green video is used.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c8031-152">**SetupExpected**</span><span class="sxs-lookup"><span data-stu-id="c8031-152">**SetupExpected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8031-153">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="c8031-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c8031-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8031-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8031-155">Indica se a configuração é esperada.</span><span class="sxs-lookup"><span data-stu-id="c8031-155">Indicates whether setup is expected.</span></span>



| <span data-ttu-id="c8031-156">Valor</span><span class="sxs-lookup"><span data-stu-id="c8031-156">Value</span></span>                                                                              | <span data-ttu-id="c8031-157">Significado</span><span class="sxs-lookup"><span data-stu-id="c8031-157">Meaning</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8031-158"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-158"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c8031-159">O monitor espera uma instalação em branco ou pedestal por padrão de nível de sinal apropriado.</span><span class="sxs-lookup"><span data-stu-id="c8031-159">Monitor expects a blank-to-blank setup or pedestal per appropriate Signal Level Standard.</span></span><br/>                      |
| <dl> <span data-ttu-id="c8031-160"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-160"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="c8031-161">O monitor não espera uma instalação em branco ou pedestal de acordo com o padrão de nível de sinal apropriado.</span><span class="sxs-lookup"><span data-stu-id="c8031-161">Monitor does not expect a blank-to-blank setup or pedestal according to the appropriate signal level standard.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c8031-162">**SignalLevelStandard**</span><span class="sxs-lookup"><span data-stu-id="c8031-162">**SignalLevelStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8031-163">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="c8031-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c8031-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8031-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8031-165">Padrão de nível de sinal para conexões EVC (conector de vídeo avançado).</span><span class="sxs-lookup"><span data-stu-id="c8031-165">Signal level standard for Enhanced video connector (EVC) connections.</span></span>



| <span data-ttu-id="c8031-166">Valor</span><span class="sxs-lookup"><span data-stu-id="c8031-166">Value</span></span>                                                                              | <span data-ttu-id="c8031-167">Significado</span><span class="sxs-lookup"><span data-stu-id="c8031-167">Meaning</span></span>                     |
|------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="c8031-168"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-168"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c8031-169">0,7, 0,3 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="c8031-169">0.7,0.3\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="c8031-170"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-170"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="c8031-171">0.714, 0.286 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="c8031-171">0.714,0.286\[V\]</span></span><br/> |
| <dl> <span data-ttu-id="c8031-172"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-172"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="c8031-173">1.0, 0.4 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="c8031-173">1.0,0.4\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="c8031-174"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-174"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="c8031-175">0,7, 0,0 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="c8031-175">0.7,0.0\[V\]</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="c8031-176">**SyncOnGreenVideoSupported**</span><span class="sxs-lookup"><span data-stu-id="c8031-176">**SyncOnGreenVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8031-177">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="c8031-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c8031-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8031-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8031-179">Indica se há suporte para sincronização em verde.</span><span class="sxs-lookup"><span data-stu-id="c8031-179">Indicates whether sync on green is supported.</span></span>



| <span data-ttu-id="c8031-180">Valor</span><span class="sxs-lookup"><span data-stu-id="c8031-180">Value</span></span>                                                                              | <span data-ttu-id="c8031-181">Significado</span><span class="sxs-lookup"><span data-stu-id="c8031-181">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="c8031-182"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c8031-183">Há suporte para sincronização em vídeo verde.</span><span class="sxs-lookup"><span data-stu-id="c8031-183">Sync on green video is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="c8031-184"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="c8031-185">Não há suporte para sincronização em vídeo verde.</span><span class="sxs-lookup"><span data-stu-id="c8031-185">Sync on green video is not supported.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8031-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8031-186">Requirements</span></span>



| <span data-ttu-id="c8031-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8031-187">Requirement</span></span> | <span data-ttu-id="c8031-188">Valor</span><span class="sxs-lookup"><span data-stu-id="c8031-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8031-189">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8031-189">Minimum supported client</span></span><br/> | <span data-ttu-id="c8031-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8031-190">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c8031-191">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8031-191">Minimum supported server</span></span><br/> | <span data-ttu-id="c8031-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8031-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c8031-193">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8031-193">Namespace</span></span><br/>                | <span data-ttu-id="c8031-194">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="c8031-194">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="c8031-195">MOF</span><span class="sxs-lookup"><span data-stu-id="c8031-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8031-196"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-196"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8031-197">DLL</span><span class="sxs-lookup"><span data-stu-id="c8031-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8031-198"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8031-198"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8031-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8031-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8031-200">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="c8031-200">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




