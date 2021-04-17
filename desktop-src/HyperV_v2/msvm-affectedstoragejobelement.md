---
description: Representa a associação entre um trabalho e os elementos gerenciados que podem ser afetados pela sua execução.
ms.assetid: 81849DE4-9039-426F-B7B1-45BB31A9132C
title: Classe Msvm_AffectedStorageJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedStorageJobElement
- Msvm_AffectedStorageJobElement.AffectedElement
- Msvm_AffectedStorageJobElement.AffectingElement
- Msvm_AffectedStorageJobElement.ElementEffects
- Msvm_AffectedStorageJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d900f42e5022301a08ebeee0036400be3a2f1bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755107"
---
# <a name="msvm_affectedstoragejobelement-class"></a><span data-ttu-id="17a07-103">\_Classe Msvm AffectedStorageJobElement</span><span class="sxs-lookup"><span data-stu-id="17a07-103">Msvm\_AffectedStorageJobElement class</span></span>

<span data-ttu-id="17a07-104">Representa a associação entre um trabalho e os elementos gerenciados que podem ser afetados pela sua execução.</span><span class="sxs-lookup"><span data-stu-id="17a07-104">Represents the association between a job and the managed elements that may be affected by its execution.</span></span>

<span data-ttu-id="17a07-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="17a07-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="17a07-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17a07-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedStorageJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_StorageJob    REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="17a07-107">Membros</span><span class="sxs-lookup"><span data-stu-id="17a07-107">Members</span></span>

<span data-ttu-id="17a07-108">A classe **Msvm \_ AffectedStorageJobElement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="17a07-108">The **Msvm\_AffectedStorageJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="17a07-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="17a07-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17a07-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="17a07-110">Properties</span></span>

<span data-ttu-id="17a07-111">A classe **Msvm \_ AffectedStorageJobElement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="17a07-111">The **Msvm\_AffectedStorageJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17a07-112">**Afetadoselement**</span><span class="sxs-lookup"><span data-stu-id="17a07-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a07-113">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="17a07-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="17a07-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="17a07-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17a07-115">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="17a07-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="17a07-116">O elemento gerenciado afetado pela execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="17a07-116">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="17a07-117">Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="17a07-117">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="17a07-118">**Afetando**</span><span class="sxs-lookup"><span data-stu-id="17a07-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a07-119">Tipo de dados: **[ **Msvm \_ StorageJob**](msvm-storagejob.md)**</span><span class="sxs-lookup"><span data-stu-id="17a07-119">Data type: **[**Msvm\_StorageJob**](msvm-storagejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="17a07-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="17a07-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17a07-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ AffectedJobElement. influenciaelement")</span><span class="sxs-lookup"><span data-stu-id="17a07-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_AffectedJobElement.AffectingElement")</span></span>
</dt> </dl>

<span data-ttu-id="17a07-122">O trabalho que está afetando o elemento afetado.</span><span class="sxs-lookup"><span data-stu-id="17a07-122">The job that is affecting the affected element.</span></span> <span data-ttu-id="17a07-123">Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="17a07-123">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="17a07-124">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="17a07-124">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a07-125">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17a07-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="17a07-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="17a07-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17a07-127">Uma enumeração que descreve o efeito sobre o elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="17a07-127">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="17a07-128">Essa matriz corresponde à matriz da propriedade **OtherElementEffectsDescriptions** , em que o último fornece detalhes relacionados aos efeitos de alto nível enumerados por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="17a07-128">This array corresponds to the **OtherElementEffectsDescriptions** property array, where the latter provides details related to the high-level effects enumerated by this property.</span></span> <span data-ttu-id="17a07-129">Detalhes adicionais serão necessários se a matriz da propriedade **ElementEffects** contiver o valor 1, (outro).</span><span class="sxs-lookup"><span data-stu-id="17a07-129">Additional detail is required if the **ElementEffects** property array contains the value 1, (Other).</span></span> <span data-ttu-id="17a07-130">Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="17a07-130">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="17a07-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="17a07-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="17a07-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="17a07-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="17a07-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Uso exclusivo** (2)</span><span class="sxs-lookup"><span data-stu-id="17a07-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Exclusive Use** (2)</span></span>
</dt> <dt>

<span data-ttu-id="17a07-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Impacto no desempenho** (3)</span><span class="sxs-lookup"><span data-stu-id="17a07-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Performance Impact** (3)</span></span>
</dt> <dt>

<span data-ttu-id="17a07-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Integridade do elemento** (4)</span><span class="sxs-lookup"><span data-stu-id="17a07-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Element Integrity** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="17a07-136">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="17a07-136">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a07-137">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="17a07-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="17a07-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="17a07-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17a07-139">Fornece detalhes para o efeito na posição da matriz correspondente na matriz da propriedade **ElementEffects** .</span><span class="sxs-lookup"><span data-stu-id="17a07-139">Provides details for the effect at the corresponding array position in the **ElementEffects** property array.</span></span> <span data-ttu-id="17a07-140">Essas informações são necessárias sempre que o elemento correspondente na matriz da propriedade **ElementEffects** contiver o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="17a07-140">This information is required whenever the corresponding element in the **ElementEffects** property array contains the value 1 (Other).</span></span> <span data-ttu-id="17a07-141">Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="17a07-141">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17a07-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="17a07-142">Remarks</span></span>

<span data-ttu-id="17a07-143">O acesso à classe **Msvm \_ AffectedStorageJobElement** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="17a07-143">Access to the **Msvm\_AffectedStorageJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="17a07-144">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="17a07-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="17a07-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17a07-145">Requirements</span></span>



| <span data-ttu-id="17a07-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="17a07-146">Requirement</span></span> | <span data-ttu-id="17a07-147">Valor</span><span class="sxs-lookup"><span data-stu-id="17a07-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17a07-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17a07-148">Minimum supported client</span></span><br/> | <span data-ttu-id="17a07-149">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="17a07-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="17a07-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17a07-150">Minimum supported server</span></span><br/> | <span data-ttu-id="17a07-151">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="17a07-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17a07-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="17a07-152">Namespace</span></span><br/>                | <span data-ttu-id="17a07-153">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="17a07-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="17a07-154">MOF</span><span class="sxs-lookup"><span data-stu-id="17a07-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17a07-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17a07-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="17a07-156">DLL</span><span class="sxs-lookup"><span data-stu-id="17a07-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17a07-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="17a07-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="17a07-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="17a07-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a07-159">**\_AFFECTEDJOBELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="17a07-159">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="17a07-160">[**\_AFFECTEDJOBELEMENT CIM**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17a07-160">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="17a07-161">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="17a07-161">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

