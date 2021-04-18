---
description: O Win32 \_ QuickFixEngineering&\# 8194; A classe WMI representa uma pequena atualização em todo o sistema, normalmente conhecida como atualização de QFE (Quick-Fix Engineering), aplicada ao sistema operacional atual.
ms.assetid: 84aed428-7620-4f7a-941f-f9d683020d8a
ms.tgt_platform: multiple
title: Classe Win32_QuickFixEngineering
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_QuickFixEngineering
- Win32_QuickFixEngineering.Caption
- Win32_QuickFixEngineering.Description
- Win32_QuickFixEngineering.InstallDate
- Win32_QuickFixEngineering.Name
- Win32_QuickFixEngineering.Status
- Win32_QuickFixEngineering.CSName
- Win32_QuickFixEngineering.FixComments
- Win32_QuickFixEngineering.HotFixID
- Win32_QuickFixEngineering.InstalledBy
- Win32_QuickFixEngineering.InstalledOn
- Win32_QuickFixEngineering.ServicePackInEffect
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9db31dd452161a31575b6f7184a34c35dea71e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751799"
---
# <a name="win32_quickfixengineering-class"></a><span data-ttu-id="2dbab-103">\_Classe Win32 QuickFixEngineering</span><span class="sxs-lookup"><span data-stu-id="2dbab-103">Win32\_QuickFixEngineering class</span></span>

<span data-ttu-id="2dbab-104">A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ QuickFixEngineering do Win32** representa uma pequena atualização de todo o sistema, normalmente conhecida como atualização de QFE (rápida correção de engenharia), aplicada ao sistema operacional atual.</span><span class="sxs-lookup"><span data-stu-id="2dbab-104">The **Win32\_QuickFixEngineering** [WMI class](../wmisdk/retrieving-a-class.md) represents a small system-wide update, commonly referred to as a quick-fix engineering (QFE) update, applied to the current operating system.</span></span> <span data-ttu-id="2dbab-105">Essa classe retorna apenas as atualizações fornecidas pela CBS (serviço baseado em componente).</span><span class="sxs-lookup"><span data-stu-id="2dbab-105">This class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="2dbab-106">Essas atualizações não estão listadas no registro.</span><span class="sxs-lookup"><span data-stu-id="2dbab-106">These updates are not listed in the registry.</span></span> <span data-ttu-id="2dbab-107">As atualizações fornecidas pelo Microsoft Windows Installer (MSI) ou pelo site do Windows Update ( [https://update.microsoft.com](https://update.microsoft.com/) ) não são retornadas pelo **Win32 \_ QuickFixEngineering**.</span><span class="sxs-lookup"><span data-stu-id="2dbab-107">Updates supplied by Microsoft Windows Installer (MSI) or the Windows update site ([https://update.microsoft.com](https://update.microsoft.com/)) are not returned by **Win32\_QuickFixEngineering**.</span></span>

<span data-ttu-id="2dbab-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2dbab-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2dbab-109">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="2dbab-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dbab-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2dbab-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A1}"), AMENDMENT]
class Win32_QuickFixEngineering : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CSName;
  string   FixComments;
  string   HotFixID;
  string   InstalledBy;
  string   InstalledOn;
  string   ServicePackInEffect;
};
```

## <a name="members"></a><span data-ttu-id="2dbab-111">Membros</span><span class="sxs-lookup"><span data-stu-id="2dbab-111">Members</span></span>

<span data-ttu-id="2dbab-112">A classe **Win32 \_ QuickFixEngineering** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2dbab-112">The **Win32\_QuickFixEngineering** class has these types of members:</span></span>

-   [<span data-ttu-id="2dbab-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2dbab-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2dbab-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2dbab-114">Properties</span></span>

<span data-ttu-id="2dbab-115">A classe **Win32 \_ QuickFixEngineering** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2dbab-115">The **Win32\_QuickFixEngineering** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2dbab-116">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="2dbab-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dbab-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2dbab-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2dbab-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-119">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2dbab-119">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2dbab-120">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="2dbab-120">A short textual description of the object.</span></span>

<span data-ttu-id="2dbab-121">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2dbab-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dbab-122">**CSName**</span><span class="sxs-lookup"><span data-stu-id="2dbab-122">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dbab-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2dbab-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2dbab-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-125">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**propagado**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de ComputerSystem do CIM**](cim-computersystem.md).**Name**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" WMI ")</span><span class="sxs-lookup"><span data-stu-id="2dbab-125">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2dbab-126">Nome local do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="2dbab-126">Local name of the computer system.</span></span> <span data-ttu-id="2dbab-127">O valor dessa propriedade é proveniente da classe [**de \_ sistema CIM**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="2dbab-127">The value for this property comes from the [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="2dbab-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2dbab-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dbab-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2dbab-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2dbab-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-131">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="2dbab-131">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2dbab-132">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="2dbab-132">A textual description of the object.</span></span>

<span data-ttu-id="2dbab-133">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2dbab-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dbab-134">**FixComments**</span><span class="sxs-lookup"><span data-stu-id="2dbab-134">**FixComments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dbab-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2dbab-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2dbab-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-137">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software WIN32REGISTRY \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="2dbab-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="2dbab-138">Comentários adicionais relacionados à atualização.</span><span class="sxs-lookup"><span data-stu-id="2dbab-138">Additional comments that relate to the update.</span></span>

</dd> <dt>

<span data-ttu-id="2dbab-139">**HotFixID**</span><span class="sxs-lookup"><span data-stu-id="2dbab-139">**HotFixID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dbab-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2dbab-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2dbab-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-142">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="2dbab-142">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="2dbab-143">Identificador exclusivo associado a uma atualização específica.</span><span class="sxs-lookup"><span data-stu-id="2dbab-143">Unique identifier associated with a particular update.</span></span>

</dd> <dt>

<span data-ttu-id="2dbab-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2dbab-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dbab-145">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2dbab-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2dbab-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-147">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="2dbab-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2dbab-148">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="2dbab-148">Indicates when the object was installed.</span></span> <span data-ttu-id="2dbab-149">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="2dbab-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2dbab-150">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2dbab-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dbab-151">**InstalledBy**</span><span class="sxs-lookup"><span data-stu-id="2dbab-151">**InstalledBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dbab-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2dbab-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2dbab-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-154">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software WIN32REGISTRY \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="2dbab-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="2dbab-155">Pessoa que instalou a atualização.</span><span class="sxs-lookup"><span data-stu-id="2dbab-155">Person who installed the update.</span></span> <span data-ttu-id="2dbab-156">Se esse valor for desconhecido, a propriedade estará vazia.</span><span class="sxs-lookup"><span data-stu-id="2dbab-156">If this value is unknown, the property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="2dbab-157">**Dever**</span><span class="sxs-lookup"><span data-stu-id="2dbab-157">**InstalledOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dbab-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2dbab-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2dbab-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-160">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software WIN32REGISTRY \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="2dbab-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="2dbab-161">Data em que a atualização foi instalada.</span><span class="sxs-lookup"><span data-stu-id="2dbab-161">Date that the update was installed.</span></span> <span data-ttu-id="2dbab-162">Se esse valor for desconhecido, a propriedade estará vazia.</span><span class="sxs-lookup"><span data-stu-id="2dbab-162">If this value is unknown, the property is empty.</span></span>

> [!Note]  
> <span data-ttu-id="2dbab-163">Essa propriedade pode usar formatos diferentes, dependendo de quando o QuickFix foi instalado.</span><span class="sxs-lookup"><span data-stu-id="2dbab-163">This property may use different formats, depending on when the QuickFix was installed.</span></span> <span data-ttu-id="2dbab-164">A maioria dos sistemas usa um formato de data padrão, como "23-10-2013".</span><span class="sxs-lookup"><span data-stu-id="2dbab-164">Most systems use a standard date format, such as "23-10-2013".</span></span> <span data-ttu-id="2dbab-165">No entanto, alguns sistemas podem retornar um valor hexadecimal de 64 bits no formato [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) do Win32.</span><span class="sxs-lookup"><span data-stu-id="2dbab-165">However, some systems may return a 64-bit hexidecimal value in the Win32 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

 

</dd> <dt>

<span data-ttu-id="2dbab-166">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2dbab-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dbab-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2dbab-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2dbab-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-169">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2dbab-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2dbab-170">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="2dbab-170">Label by which the object is known.</span></span> <span data-ttu-id="2dbab-171">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="2dbab-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2dbab-172">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2dbab-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dbab-173">**ServicePackInEffect**</span><span class="sxs-lookup"><span data-stu-id="2dbab-173">**ServicePackInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dbab-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2dbab-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2dbab-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-176">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="2dbab-176">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="2dbab-177">Service Pack em vigor quando a atualização foi aplicada.</span><span class="sxs-lookup"><span data-stu-id="2dbab-177">Service pack in effect when the update was applied.</span></span> <span data-ttu-id="2dbab-178">Se nenhum service pack tiver sido aplicado, a propriedade terá o valor SP0.</span><span class="sxs-lookup"><span data-stu-id="2dbab-178">If no service pack has been applied, the property takes on the value SP0.</span></span> <span data-ttu-id="2dbab-179">Se não for possível determinar qual service pack estava em vigor, essa propriedade será **nula**.</span><span class="sxs-lookup"><span data-stu-id="2dbab-179">If it cannot be determined what service pack was in effect, this property is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2dbab-180">**Status**</span><span class="sxs-lookup"><span data-stu-id="2dbab-180">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dbab-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2dbab-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2dbab-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dbab-183">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="2dbab-183">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2dbab-184">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="2dbab-184">String that indicates the current status of the object.</span></span> <span data-ttu-id="2dbab-185">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="2dbab-185">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2dbab-186">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="2dbab-186">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2dbab-187">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="2dbab-187">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2dbab-188">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="2dbab-188">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2dbab-189">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="2dbab-189">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2dbab-190">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="2dbab-190">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2dbab-191">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2dbab-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2dbab-192">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2dbab-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2dbab-193">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2dbab-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2dbab-194">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="2dbab-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2dbab-195">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="2dbab-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2dbab-196">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="2dbab-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2dbab-197">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="2dbab-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2dbab-198">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="2dbab-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2dbab-199">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="2dbab-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2dbab-200">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="2dbab-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2dbab-201">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="2dbab-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2dbab-202">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="2dbab-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2dbab-203">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="2dbab-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2dbab-204">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="2dbab-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="2dbab-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2dbab-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="2dbab-206">Comentários</span><span class="sxs-lookup"><span data-stu-id="2dbab-206">Remarks</span></span>

<span data-ttu-id="2dbab-207">A classe **Win32 \_ QuickFixEngineering** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2dbab-207">The **Win32\_QuickFixEngineering** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="2dbab-208">Como as atualizações são armazenadas em dois locais, uma enumeração dessa classe pode resultar em duplicatas.</span><span class="sxs-lookup"><span data-stu-id="2dbab-208">Because updates are stored in two places, an enumeration of this class can result in duplicates.</span></span>

<span data-ttu-id="2dbab-209">Um Hot Fix é um patch de sistema operacional temporário produzido pelo grupo de engenharia de correção rápida na Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2dbab-209">A hot fix is a temporary operating system patch produced by the Quick Fix Engineering group at Microsoft.</span></span> <span data-ttu-id="2dbab-210">Assim como os service packs, os hot fixes representam as alterações feitas em uma versão do Windows após o lançamento do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2dbab-210">Like service packs, hot fixes represent changes that have been made to a version of Windows after the operating system has been released.</span></span>

<span data-ttu-id="2dbab-211">Ao contrário dos Service Packs, os hot fixes não se destinam à instalação em aberto em todos os computadores.</span><span class="sxs-lookup"><span data-stu-id="2dbab-211">Unlike service packs, hot fixes are not intended for blanket installation on all computers.</span></span> <span data-ttu-id="2dbab-212">Em vez disso, eles são desenvolvidos para resolver problemas muito específicos, geralmente para configurações de computador específicas.</span><span class="sxs-lookup"><span data-stu-id="2dbab-212">Instead, they are developed to address very specific problems, often for specific computer configurations.</span></span>

<span data-ttu-id="2dbab-213">Além disso, hot fixes representam instalações independentes que não dependem de outros hotfixes liberados.</span><span class="sxs-lookup"><span data-stu-id="2dbab-213">In addition, hot fixes represent independent installations that do not depend on other released hot fixes.</span></span> <span data-ttu-id="2dbab-214">Por exemplo, um Hot Fix 4 hipotético não incluiria as correções de bug e a funcionalidade incluídas em hot fixes 1, 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="2dbab-214">For example, a hypothetical hot fix 4 would not include the bug fixes and functionality included in hot fixes 1, 2, and 3.</span></span> <span data-ttu-id="2dbab-215">Na maioria dos casos, também não haverá nenhum requisito para instalar hot fixes 1, 2 e 3 antes de instalar o Hot Fix 4.</span><span class="sxs-lookup"><span data-stu-id="2dbab-215">In most cases, there would also be no requirement that you install hot fixes 1, 2, and 3 before installing hot fix 4.</span></span> <span data-ttu-id="2dbab-216">Isso faz com que a enumeração de hot fixes individuais seja uma tarefa administrativa importante: para saber a configuração exata de um computador, você precisa saber não apenas quais Service Packs foram instalados, mas também quais hot fixes individuais foram instalados.</span><span class="sxs-lookup"><span data-stu-id="2dbab-216">This makes enumeration of individual hot fixes an important administrative task: to know the exact configuration of a computer, you need to know not only which service packs have been installed but also which individual hot fixes have been installed.</span></span>

<span data-ttu-id="2dbab-217">A classe **Win32 \_ QuickFixEngineering** permite que você Enumere todos os hot fixes que foram instalados em um computador</span><span class="sxs-lookup"><span data-stu-id="2dbab-217">The **Win32\_QuickFixEngineering** class enables you to enumerate all the hot fixes that have been installed on a computer</span></span>

## <a name="examples"></a><span data-ttu-id="2dbab-218">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2dbab-218">Examples</span></span>

<span data-ttu-id="2dbab-219">O exemplo do PowerShell [obter programas instalados](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) retorna uma lista completa dos programas instalados.</span><span class="sxs-lookup"><span data-stu-id="2dbab-219">The [Get Installed Programs](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) PowerShell example returns a full list of installed programs.</span></span>

<span data-ttu-id="2dbab-220">O exemplo de VBScript a seguir enumera os hot fixes instalados em um computador</span><span class="sxs-lookup"><span data-stu-id="2dbab-220">The following VBScript sample enumerates the installed hot fixes on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colQuickFixes = objWMIService.ExecQuery("SELECT * FROM Win32_QuickFixEngineering")
For Each objQuickFix in colQuickFixes
 Wscript.Echo "Computer: " & objQuickFix.CSName
 Wscript.Echo "Description: " & objQuickFix.Description
 Wscript.Echo "Hot Fix ID: " & objQuickFix.HotFixID
 Wscript.Echo "Installation Date: " & objQuickFix.InstallDate
 Wscript.Echo "Installed By: " & objQuickFix.InstalledBy
Next
```



## <a name="requirements"></a><span data-ttu-id="2dbab-221">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dbab-221">Requirements</span></span>



| <span data-ttu-id="2dbab-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dbab-222">Requirement</span></span> | <span data-ttu-id="2dbab-223">Valor</span><span class="sxs-lookup"><span data-stu-id="2dbab-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dbab-224">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dbab-224">Minimum supported client</span></span><br/> | <span data-ttu-id="2dbab-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2dbab-225">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2dbab-226">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dbab-226">Minimum supported server</span></span><br/> | <span data-ttu-id="2dbab-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2dbab-227">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2dbab-228">Namespace</span><span class="sxs-lookup"><span data-stu-id="2dbab-228">Namespace</span></span><br/>                | <span data-ttu-id="2dbab-229">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2dbab-229">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2dbab-230">MOF</span><span class="sxs-lookup"><span data-stu-id="2dbab-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2dbab-231"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2dbab-231"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2dbab-232">DLL</span><span class="sxs-lookup"><span data-stu-id="2dbab-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dbab-233"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dbab-233"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dbab-234">Confira também</span><span class="sxs-lookup"><span data-stu-id="2dbab-234">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dbab-235">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="2dbab-235">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="2dbab-236">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="2dbab-236">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="2dbab-237">Tarefas do WMI: sistemas operacionais</span><span class="sxs-lookup"><span data-stu-id="2dbab-237">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> </dl>

 

 
