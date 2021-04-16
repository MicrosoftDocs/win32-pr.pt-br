---
description: Representa as configurações para o serviço de métrica. As propriedades desta classe não podem ser modificadas diretamente. O cliente deve chamar o método ModifyServiceSettings para modificar qualquer uma dessas propriedades.
ms.assetid: 578ddda7-4c8e-498e-8612-29c392390b73
title: Classe Msvm_MetricServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceSettingData
- Msvm_MetricServiceSettingData.InstanceID
- Msvm_MetricServiceSettingData.Caption
- Msvm_MetricServiceSettingData.Description
- Msvm_MetricServiceSettingData.ElementName
- Msvm_MetricServiceSettingData.MetricsFlushInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a1211b19692761dd8b92de69cf42e4ad55246f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761711"
---
# <a name="msvm_metricservicesettingdata-class"></a><span data-ttu-id="b8cbc-105">\_Classe Msvm MetricServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="b8cbc-105">Msvm\_MetricServiceSettingData class</span></span>

<span data-ttu-id="b8cbc-106">Representa as configurações para o serviço de métrica.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-106">Represents the settings for the metric service.</span></span> <span data-ttu-id="b8cbc-107">As propriedades desta classe não podem ser modificadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="b8cbc-108">O cliente deve chamar o método [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) para modificar qualquer uma dessas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-108">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="b8cbc-109">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8cbc-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8cbc-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service Settings";
  string   Description = "Defines Hyper-V Metric Service Settings";
  string   ElementName = "Hyper-V Metric Service Settings";
  datetime MetricsFlushInterval;
};
```

## <a name="members"></a><span data-ttu-id="b8cbc-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b8cbc-111">Members</span></span>

<span data-ttu-id="b8cbc-112">A classe **Msvm \_ MetricServiceSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b8cbc-112">The **Msvm\_MetricServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b8cbc-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b8cbc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8cbc-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b8cbc-114">Properties</span></span>

<span data-ttu-id="b8cbc-115">A classe **Msvm \_ MetricServiceSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-115">The **Msvm\_MetricServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8cbc-116">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cbc-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8cbc-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8cbc-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8cbc-119">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-119">A short description of the object.</span></span> <span data-ttu-id="b8cbc-120">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações do serviço de métrica do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="b8cbc-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="b8cbc-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cbc-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8cbc-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8cbc-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8cbc-124">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="b8cbc-124">A description of the object.</span></span> <span data-ttu-id="b8cbc-125">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "define as configurações do serviço de métrica do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="b8cbc-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="b8cbc-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cbc-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8cbc-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8cbc-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8cbc-129">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-129">A display name for the object.</span></span> <span data-ttu-id="b8cbc-130">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações do serviço de métrica do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="b8cbc-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="b8cbc-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cbc-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8cbc-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8cbc-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8cbc-134">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b8cbc-135">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b8cbc-136">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b8cbc-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8cbc-137">**MetricsFlushInterval**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-137">**MetricsFlushInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8cbc-138">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8cbc-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8cbc-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8cbc-140">Define o intervalo no qual as métricas devem ser liberadas para o disco.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-140">Defines the interval at which metrics should be flushed to disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8cbc-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8cbc-141">Requirements</span></span>



| <span data-ttu-id="b8cbc-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8cbc-142">Requirement</span></span> | <span data-ttu-id="b8cbc-143">Valor</span><span class="sxs-lookup"><span data-stu-id="b8cbc-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8cbc-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8cbc-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b8cbc-145">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b8cbc-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b8cbc-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8cbc-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b8cbc-147">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b8cbc-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8cbc-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8cbc-148">Namespace</span></span><br/>                | <span data-ttu-id="b8cbc-149">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b8cbc-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b8cbc-150">MOF</span><span class="sxs-lookup"><span data-stu-id="b8cbc-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8cbc-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8cbc-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8cbc-152">DLL</span><span class="sxs-lookup"><span data-stu-id="b8cbc-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8cbc-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8cbc-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b8cbc-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8cbc-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8cbc-155">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="b8cbc-156">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="b8cbc-156">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md)
</dt> </dl>

 

