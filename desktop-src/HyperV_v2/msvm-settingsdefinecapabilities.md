---
description: Fornece um link entre a instância de recursos e as configurações mínima, máxima, incremental e padrão para um recurso.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Classe Msvm_SettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineCapabilities
- Msvm_SettingsDefineCapabilities.SupportStatement
- Msvm_SettingsDefineCapabilities.GroupComponent
- Msvm_SettingsDefineCapabilities.PartComponent
- Msvm_SettingsDefineCapabilities.PropertyPolicy
- Msvm_SettingsDefineCapabilities.ValueRole
- Msvm_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7a312d3453b783c3d72f909ec6cb0b37d83feb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758797"
---
# <a name="msvm_settingsdefinecapabilities-class"></a><span data-ttu-id="c7ce3-103">\_Classe Msvm SettingsDefineCapabilities</span><span class="sxs-lookup"><span data-stu-id="c7ce3-103">Msvm\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="c7ce3-104">Fornece um link entre a instância de recursos e as configurações mínima, máxima, incremental e padrão para um recurso.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-104">Provides a link between the capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="c7ce3-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7ce3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7ce3-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  uint16               SupportStatement;
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="c7ce3-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c7ce3-107">Members</span></span>

<span data-ttu-id="c7ce3-108">A classe **Msvm \_ SettingsDefineCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c7ce3-108">The **Msvm\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="c7ce3-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7ce3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7ce3-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7ce3-110">Properties</span></span>

<span data-ttu-id="c7ce3-111">A classe **Msvm \_ SettingsDefineCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-111">The **Msvm\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7ce3-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7ce3-113">Tipo de dados: **[ **\_ recursos CIM**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="c7ce3-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7ce3-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7ce3-115">A instância de recursos.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-115">The capabilities instance.</span></span> <span data-ttu-id="c7ce3-116">Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7ce3-116">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7ce3-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7ce3-118">Tipo de dados: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-118">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="c7ce3-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7ce3-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7ce3-120">Uma configuração usada para definir a instância de recursos associados.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-120">A setting used to define the associated capabilities instance.</span></span> <span data-ttu-id="c7ce3-121">Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7ce3-121">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7ce3-122">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-122">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7ce3-123">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7ce3-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7ce3-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7ce3-125">Indica se as propriedades não nulas e não-chave da instância de dados de configuração associada são tratadas de forma independente ou como um conjunto correlacionado.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-125">Indicates whether the non-null, non-key properties of the associated setting data instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="c7ce3-126">Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) e é sempre definida como 0 (independente).</span><span class="sxs-lookup"><span data-stu-id="c7ce3-126">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) and it is always set to 0 (Independent).</span></span>

</dd> <dt>

<span data-ttu-id="c7ce3-127">**SupportStatement**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-127">**SupportStatement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7ce3-128">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7ce3-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7ce3-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7ce3-130">Identifica a instrução de suporte.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-130">Identifies the support statement.</span></span>

> [!Note]  
> <span data-ttu-id="c7ce3-131">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-131">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span data-ttu-id="c7ce3-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Produção** (0)</span><span class="sxs-lookup"><span data-stu-id="c7ce3-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Production** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span data-ttu-id="c7ce3-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Pré-lançamento** (1)</span><span class="sxs-lookup"><span data-stu-id="c7ce3-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Prerelease** (1)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c7ce3-134">Was não **produto** no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-134">Was **NonProduction** in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="c7ce3-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c7ce3-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7ce3-136">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-136">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7ce3-137">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7ce3-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7ce3-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7ce3-139">Qualquer semântica adicional na interpretação de todas as propriedades não nulas e não chave dos dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-139">Any further semantics on the interpretation of all non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="c7ce3-140">Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7ce3-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7ce3-141">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7ce3-142">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7ce3-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7ce3-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7ce3-144">Qualquer semântica adicional na interpretação das propriedades não nulas e não chave dos dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-144">Any further semantics on the interpretation of the non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="c7ce3-145">Essa propriedade é herdada do [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7ce3-145">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7ce3-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7ce3-146">Remarks</span></span>

<span data-ttu-id="c7ce3-147">Os valores para as propriedades **ValueRole** e **ValueRange** são usados nos seguintes pares:</span><span class="sxs-lookup"><span data-stu-id="c7ce3-147">The values for the **ValueRole** and **ValueRange** properties are used in the following pairs:</span></span>

-   <span data-ttu-id="c7ce3-148">Ponto/padrão (0/0)</span><span class="sxs-lookup"><span data-stu-id="c7ce3-148">Point/Default (0/0)</span></span>
-   <span data-ttu-id="c7ce3-149">Mínimos/com suporte (1/3)</span><span class="sxs-lookup"><span data-stu-id="c7ce3-149">Minimums/Supported (1/3)</span></span>
-   <span data-ttu-id="c7ce3-150">Máximos/com suporte (2/3)</span><span class="sxs-lookup"><span data-stu-id="c7ce3-150">Maximums/Supported (2/3)</span></span>
-   <span data-ttu-id="c7ce3-151">Incrementos/com suporte (3/3).</span><span class="sxs-lookup"><span data-stu-id="c7ce3-151">Increments/Supported (3/3).</span></span>

<span data-ttu-id="c7ce3-152">"Point" significa que cada uma das propriedades no objeto **PartComponent** representa o padrão da plataforma.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-152">"Point" means that each of the properties on the **PartComponent** object represents the platform default.</span></span>

<span data-ttu-id="c7ce3-153">"Mínimos" e "máximos" significam que cada uma das propriedades no objeto **PartComponent** representa os menores e os maiores valores possíveis para essas propriedades com suporte da plataforma com base na configuração atual do computador.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-153">"Minimums" and "Maximums" mean that each of the properties on the **PartComponent** object represent the smallest and largest possible values for these properties that are supported by the platform based on your current machine configuration.</span></span>

<span data-ttu-id="c7ce3-154">"Incrementos" indica a granularidade na qual você pode aumentar ou diminuir as configurações.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-154">"Increments" indicates the granularity at which you can increase or decrease the settings.</span></span>

<span data-ttu-id="c7ce3-155">O acesso à classe **Msvm \_ SettingsDefineCapabilities** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="c7ce3-155">Access to the **Msvm\_SettingsDefineCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c7ce3-156">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c7ce3-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7ce3-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7ce3-157">Requirements</span></span>



| <span data-ttu-id="c7ce3-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7ce3-158">Requirement</span></span> | <span data-ttu-id="c7ce3-159">Valor</span><span class="sxs-lookup"><span data-stu-id="c7ce3-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ce3-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7ce3-160">Minimum supported client</span></span><br/> | <span data-ttu-id="c7ce3-161">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c7ce3-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c7ce3-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7ce3-162">Minimum supported server</span></span><br/> | <span data-ttu-id="c7ce3-163">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c7ce3-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7ce3-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7ce3-164">Namespace</span></span><br/>                | <span data-ttu-id="c7ce3-165">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c7ce3-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c7ce3-166">MOF</span><span class="sxs-lookup"><span data-stu-id="c7ce3-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7ce3-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7ce3-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7ce3-168">DLL</span><span class="sxs-lookup"><span data-stu-id="c7ce3-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7ce3-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7ce3-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c7ce3-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7ce3-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7ce3-171">**\_SETTINGSDEFINECAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-171">**CIM\_SettingsDefineCapabilities**</span></span>](cim-settingsdefinecapabilities.md)
</dt> <dt>

<span data-ttu-id="c7ce3-172">[**\_SETTINGSDEFINECAPABILITIES CIM**](/previous-versions//cc136913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7ce3-172">[**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c7ce3-173">**Msvm \_ SettingsDefineCapabilities (v1)**</span><span class="sxs-lookup"><span data-stu-id="c7ce3-173">**Msvm\_SettingsDefineCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[<span data-ttu-id="c7ce3-174">Classes de gerenciamento de recursos</span><span class="sxs-lookup"><span data-stu-id="c7ce3-174">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

