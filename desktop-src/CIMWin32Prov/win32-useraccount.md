---
description: A \_ conta Win32 user&\# 32; A classe WMI contém informações sobre uma conta de usuário em um sistema de computador executando o Windows.
ms.assetid: 747b2ce2-ae38-47de-bf3a-97058df56a7a
ms.tgt_platform: multiple
title: Classe Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount
- Win32_UserAccount.AccountType
- Win32_UserAccount.Caption
- Win32_UserAccount.Description
- Win32_UserAccount.Disabled
- Win32_UserAccount.Domain
- Win32_UserAccount.FullName
- Win32_UserAccount.InstallDate
- Win32_UserAccount.LocalAccount
- Win32_UserAccount.Lockout
- Win32_UserAccount.Name
- Win32_UserAccount.PasswordChangeable
- Win32_UserAccount.PasswordExpires
- Win32_UserAccount.PasswordRequired
- Win32_UserAccount.SID
- Win32_UserAccount.SIDType
- Win32_UserAccount.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5af83f7a52e9f3db9dbaa4a959bfe01ae740746
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010133"
---
# <a name="win32_useraccount-class"></a><span data-ttu-id="3b79f-103">\_Classe USERACCOUNT do Win32</span><span class="sxs-lookup"><span data-stu-id="3b79f-103">Win32\_UserAccount class</span></span>

<span data-ttu-id="3b79f-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ USERACCOUNT do Win32** contém informações sobre uma conta de usuário em um sistema de computador que executa o Windows.</span><span class="sxs-lookup"><span data-stu-id="3b79f-104">The **Win32\_UserAccount** [WMI class](../wmisdk/retrieving-a-class.md) contains information about a user account on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="3b79f-105">Como o **nome** e o **domínio** são propriedades de chave, a enumeração da **\_ conta Win32** userem uma rede grande pode afetar negativamente o desempenho.</span><span class="sxs-lookup"><span data-stu-id="3b79f-105">Because both the **Name** and **Domain** are key properties, enumerating **Win32\_UserAccount** on a large network can negatively affect performance.</span></span> <span data-ttu-id="3b79f-106">Chamar **GetObject** ou consultas para uma instância específica tem menos impacto.</span><span class="sxs-lookup"><span data-stu-id="3b79f-106">Calling **GetObject** or querying for a specific instance has less impact.</span></span>

 

<span data-ttu-id="3b79f-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3b79f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3b79f-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="3b79f-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b79f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b79f-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserAccount : Win32_Account
{
  uint32   AccountType;
  string   Caption;
  string   Description;
  boolean  Disabled;
  string   Domain;
  string   FullName;
  datetime InstallDate;
  boolean  LocalAccount;
  boolean  Lockout;
  string   Name;
  boolean  PasswordChangeable;
  boolean  PasswordExpires;
  boolean  PasswordRequired;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="3b79f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="3b79f-110">Members</span></span>

<span data-ttu-id="3b79f-111">A **classe \_ USERACCOUNT do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3b79f-111">The **Win32\_UserAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="3b79f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3b79f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="3b79f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3b79f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3b79f-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="3b79f-114">Methods</span></span>

<span data-ttu-id="3b79f-115">A **classe \_ USERACCOUNT do Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3b79f-115">The **Win32\_UserAccount** class has these methods.</span></span>



| <span data-ttu-id="3b79f-116">Método</span><span class="sxs-lookup"><span data-stu-id="3b79f-116">Method</span></span>                                                     | <span data-ttu-id="3b79f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b79f-117">Description</span></span>                                             |
|:-----------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="3b79f-118">**Renomear**</span><span class="sxs-lookup"><span data-stu-id="3b79f-118">**Rename**</span></span>](rename-method-in-class-win32-useraccount.md) | <span data-ttu-id="3b79f-119">Permite a renomeação da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="3b79f-119">Allows for the renaming of the user account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3b79f-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3b79f-120">Properties</span></span>

<span data-ttu-id="3b79f-121">A **classe \_ USERACCOUNT do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3b79f-121">The **Win32\_UserAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b79f-122">**AccountType**</span><span class="sxs-lookup"><span data-stu-id="3b79f-122">**AccountType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-123">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3b79f-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b79f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-125">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| rede Management structures \| [**user \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| usri2 \_ flags")</span><span class="sxs-lookup"><span data-stu-id="3b79f-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|usri2\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-126">Sinalizadores que descrevem as características de uma conta de usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="3b79f-126">Flags that describe the characteristics of a Windows user account.</span></span>

<dt>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="3b79f-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Conta duplicada temporária** (256)</span><span class="sxs-lookup"><span data-stu-id="3b79f-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Temporary duplicate account** (256)</span></span>


</dt> <dd>

<span data-ttu-id="3b79f-128">**UF \_ \_ duplicado de \_ conta temporária**</span><span class="sxs-lookup"><span data-stu-id="3b79f-128">**UF\_TEMP\_DUPLICATE\_ACCOUNT**</span></span>

<span data-ttu-id="3b79f-129">Conta de usuário local para usuários que têm uma conta primária em outro domínio.</span><span class="sxs-lookup"><span data-stu-id="3b79f-129">Local user account for users who have a primary account in another domain.</span></span> <span data-ttu-id="3b79f-130">Essa conta fornece acesso de usuário somente a este domínio — não a nenhum domínio que confie nesse domínio.</span><span class="sxs-lookup"><span data-stu-id="3b79f-130">This account provides user access to this domain only—not to any domain that trusts this domain.</span></span>

</dd> <dt>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="3b79f-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Conta normal** (512)</span><span class="sxs-lookup"><span data-stu-id="3b79f-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Normal account** (512)</span></span>


</dt> <dd>

<span data-ttu-id="3b79f-132">**\_conta normal da UF \_**</span><span class="sxs-lookup"><span data-stu-id="3b79f-132">**UF\_NORMAL\_ACCOUNT**</span></span>

<span data-ttu-id="3b79f-133">Tipo de conta padrão que representa um usuário típico.</span><span class="sxs-lookup"><span data-stu-id="3b79f-133">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="3b79f-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Conta de confiança entre domínios** (2048)</span><span class="sxs-lookup"><span data-stu-id="3b79f-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Interdomain trust account** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="3b79f-135">**conta de confiança de domínio da UF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3b79f-135">**UF\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="3b79f-136">Conta para um domínio do sistema que confia em outros domínios.</span><span class="sxs-lookup"><span data-stu-id="3b79f-136">Account for a system domain that trusts other domains.</span></span>

</dd> <dt>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="3b79f-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Conta de confiança da estação de trabalho** (4096)</span><span class="sxs-lookup"><span data-stu-id="3b79f-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Workstation trust account** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="3b79f-138">**conta de confiança da UF \_ Workstation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3b79f-138">**UF\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="3b79f-139">Conta de computador para um sistema de computador que executa o Windows que é membro deste domínio.</span><span class="sxs-lookup"><span data-stu-id="3b79f-139">Computer account for a computer system running Windows that is a member of this domain.</span></span>

</dd> <dt>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="3b79f-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Conta de confiança do servidor** (8192)</span><span class="sxs-lookup"><span data-stu-id="3b79f-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Server trust account** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="3b79f-141">**\_conta de \_ confiança do servidor UF \_**</span><span class="sxs-lookup"><span data-stu-id="3b79f-141">**UF\_SERVER\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="3b79f-142">Conta para um controlador de domínio de backup do sistema que seja membro deste domínio.</span><span class="sxs-lookup"><span data-stu-id="3b79f-142">Account for a system backup domain controller that is a member of this domain.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3b79f-143">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="3b79f-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3b79f-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b79f-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-146">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3b79f-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-147">Domínio e nome de usuário da conta.</span><span class="sxs-lookup"><span data-stu-id="3b79f-147">Domain and username of the account.</span></span>

<span data-ttu-id="3b79f-148">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b79f-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b79f-149">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3b79f-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3b79f-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b79f-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-152">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="3b79f-152">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-153">Descrição da conta.</span><span class="sxs-lookup"><span data-stu-id="3b79f-153">Description of the account.</span></span>

<span data-ttu-id="3b79f-154">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b79f-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b79f-155">**Desabilitado**</span><span class="sxs-lookup"><span data-stu-id="3b79f-155">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-156">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3b79f-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b79f-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-158">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| user \_ info \| UF \_ ACCOUNTDISABLE")</span><span class="sxs-lookup"><span data-stu-id="3b79f-158">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|USER\_INFO\|UF\_ACCOUNTDISABLE")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-159">A conta de usuário do Windows está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="3b79f-159">Windows user account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="3b79f-160">**Domínio**</span><span class="sxs-lookup"><span data-stu-id="3b79f-160">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3b79f-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b79f-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-163">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management Functions \| nomedodomínio")</span><span class="sxs-lookup"><span data-stu-id="3b79f-163">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-164">Nome do domínio do Windows ao qual uma conta de usuário pertence, por exemplo: "NA-SALEs".</span><span class="sxs-lookup"><span data-stu-id="3b79f-164">Name of the Windows domain to which a user account belongs, for example: "NA-SALES".</span></span>

</dd> <dt>

<span data-ttu-id="3b79f-165">**FullName**</span><span class="sxs-lookup"><span data-stu-id="3b79f-165">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3b79f-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-167">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b79f-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-168">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| rede Management structures \| [**user \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **usri2 \_ Full \_ Name**")</span><span class="sxs-lookup"><span data-stu-id="3b79f-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**usri2\_full\_name**")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-169">Nome completo de um usuário local, por exemplo: "Dan Wilson".</span><span class="sxs-lookup"><span data-stu-id="3b79f-169">Full name of a local user, for example: "Dan Wilson".</span></span>

</dd> <dt>

<span data-ttu-id="3b79f-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3b79f-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-171">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3b79f-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b79f-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-173">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="3b79f-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-174">Data em que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="3b79f-174">Date the object is installed.</span></span> <span data-ttu-id="3b79f-175">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="3b79f-175">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3b79f-176">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b79f-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b79f-177">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="3b79f-177">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-178">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3b79f-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b79f-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-180">Qualificadores: [ **fixos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="3b79f-180">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-181">Se for **true**, a conta será definida no computador local.</span><span class="sxs-lookup"><span data-stu-id="3b79f-181">If **true**, the account is defined on the local computer.</span></span>

<span data-ttu-id="3b79f-182">Essa propriedade é herdada [**da \_ conta Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="3b79f-182">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b79f-183">**Bloquear**</span><span class="sxs-lookup"><span data-stu-id="3b79f-183">**Lockout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-184">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3b79f-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-185">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b79f-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-186">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| Gerenciamento de rede de estruturas de \| [**usuário \_ \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\ \| **\_ bloqueio da UF**")</span><span class="sxs-lookup"><span data-stu-id="3b79f-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_LOCKOUT**")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-187">Se for **true**, a conta de usuário será bloqueada no sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="3b79f-187">If **true**, the user account is locked out of the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="3b79f-188">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3b79f-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3b79f-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b79f-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-191">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| name")</span><span class="sxs-lookup"><span data-stu-id="3b79f-191">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-192">Nome da conta de usuário do Windows no domínio que a propriedade de **domínio** dessa classe especifica.</span><span class="sxs-lookup"><span data-stu-id="3b79f-192">Name of the Windows user account on the domain that the **Domain** property of this class specifies.</span></span>

<span data-ttu-id="3b79f-193">Exemplo: "danwilson".</span><span class="sxs-lookup"><span data-stu-id="3b79f-193">Example: "danwilson".</span></span>

<span data-ttu-id="3b79f-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b79f-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b79f-195">**PasswordChangeable**</span><span class="sxs-lookup"><span data-stu-id="3b79f-195">**PasswordChangeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-196">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3b79f-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-197">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b79f-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-198">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ passwd \_ não \_ Change**")</span><span class="sxs-lookup"><span data-stu-id="3b79f-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_CANT\_CHANGE**")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-199">Se **for true**, a senha nessa conta de usuário poderá ser alterada.</span><span class="sxs-lookup"><span data-stu-id="3b79f-199">If **true**, the password on this user account can be changed.</span></span>

</dd> <dt>

<span data-ttu-id="3b79f-200">**PasswordExpires**</span><span class="sxs-lookup"><span data-stu-id="3b79f-200">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-201">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3b79f-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-202">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b79f-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-203">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| rede de estruturas de gerenciamento de redes \| [**usuário \_ \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF não \_ \_ expirar \_ passwd**")</span><span class="sxs-lookup"><span data-stu-id="3b79f-203">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_DONT\_EXPIRE\_PASSWD**")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-204">Se **for true**, a senha nessa conta de usuário expirará.</span><span class="sxs-lookup"><span data-stu-id="3b79f-204">If **true**, the password on this user account expires.</span></span>

</dd> <dt>

<span data-ttu-id="3b79f-205">**PasswordRequired**</span><span class="sxs-lookup"><span data-stu-id="3b79f-205">**PasswordRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-206">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3b79f-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-207">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b79f-207">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-208">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ passwd \_ NOTREQD**")</span><span class="sxs-lookup"><span data-stu-id="3b79f-208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_NOTREQD**")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-209">Se for **true**, uma senha será necessária em uma conta de usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="3b79f-209">If **true**, a password is required on a Windows user account.</span></span> <span data-ttu-id="3b79f-210">Se **for false**, essa conta não exigirá uma senha.</span><span class="sxs-lookup"><span data-stu-id="3b79f-210">If **false**, this account does not require a password.</span></span>

</dd> <dt>

<span data-ttu-id="3b79f-211">**SID**</span><span class="sxs-lookup"><span data-stu-id="3b79f-211">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-212">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3b79f-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b79f-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-214">Qualificadores: [**fixos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| identificadores de segurança do win32api (SIDs)")</span><span class="sxs-lookup"><span data-stu-id="3b79f-214">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-215">SID (identificador de segurança) desta conta.</span><span class="sxs-lookup"><span data-stu-id="3b79f-215">Security identifier (SID) for this account.</span></span> <span data-ttu-id="3b79f-216">Um SID é um valor de cadeia de caracteres de comprimento variável que é usado para identificar um confiável.</span><span class="sxs-lookup"><span data-stu-id="3b79f-216">A SID is a string value of variable length that is used to identify a trustee.</span></span> <span data-ttu-id="3b79f-217">Cada conta tem um SID exclusivo que uma autoridade, como um domínio do Windows, emite problemas.</span><span class="sxs-lookup"><span data-stu-id="3b79f-217">Each account has a unique SID that an authority, such as a Windows domain, issues.</span></span> <span data-ttu-id="3b79f-218">O SID é armazenado no banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="3b79f-218">The SID is stored in the security database.</span></span> <span data-ttu-id="3b79f-219">Quando um usuário faz logon, o sistema recupera o SID do usuário do banco de dados, coloca o SID no token de acesso do usuário e, em seguida, usa o SID no token de acesso do usuário para identificar o usuário em todas as interações subsequentes com a segurança do Windows.</span><span class="sxs-lookup"><span data-stu-id="3b79f-219">When a user logs on, the system retrieves the user SID from the database, places the SID in the user access token, and then uses the SID in the user access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="3b79f-220">Cada SID é um identificador exclusivo para um usuário ou grupo, e um usuário ou grupo diferente não pode ter o mesmo SID.</span><span class="sxs-lookup"><span data-stu-id="3b79f-220">Each SID is a unique identifier for a user or group, and a different user or group cannot have the same SID.</span></span>

<span data-ttu-id="3b79f-221">Essa propriedade é herdada [**da \_ conta Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="3b79f-221">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b79f-222">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="3b79f-222">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-223">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="3b79f-223">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b79f-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-225">Qualificadores: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| tipos de enumeração de controle de acesso do \| [**\_ nome SID \_ use**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")</span><span class="sxs-lookup"><span data-stu-id="3b79f-225">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|[**SID\_NAME\_USE**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-226">Valor enumerado que especifica o tipo de SID.</span><span class="sxs-lookup"><span data-stu-id="3b79f-226">Enumerated value that specifies the type of SID.</span></span>

<span data-ttu-id="3b79f-227">Essa propriedade é herdada [**da \_ conta Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="3b79f-227">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="3b79f-228">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="3b79f-228">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="3b79f-229">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="3b79f-229">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="3b79f-230">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="3b79f-230">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="3b79f-231">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="3b79f-231">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="3b79f-232">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="3b79f-232">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="3b79f-233">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="3b79f-233">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="3b79f-234">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="3b79f-234">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="3b79f-235">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="3b79f-235">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="3b79f-236">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="3b79f-236">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3b79f-237">**Status**</span><span class="sxs-lookup"><span data-stu-id="3b79f-237">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b79f-238">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3b79f-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b79f-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b79f-240">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="3b79f-240">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3b79f-241">Status atual de um objeto.</span><span class="sxs-lookup"><span data-stu-id="3b79f-241">Current status of an object.</span></span> <span data-ttu-id="3b79f-242">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="3b79f-242">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3b79f-243">Os status operacionais incluem: "OK", "degradado" e "Pred falha", que é um elemento como uma unidade de disco rígido habilitada para inteligente que pode estar funcionando corretamente, mas prevê uma falha em um futuro próximo.</span><span class="sxs-lookup"><span data-stu-id="3b79f-243">Operational statuses include: "OK", "Degraded", and "Pred Fail", which is an element such as a SMART-enabled hard disk drive that may be functioning properly, but predicts a failure in the near future.</span></span> <span data-ttu-id="3b79f-244">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço", que pode ser aplicado durante o reprateação de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="3b79f-244">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service", which can apply during mirror resilvering of a disk, reloading a user permissions list, or other administrative work.</span></span>

<span data-ttu-id="3b79f-245">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b79f-245">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3b79f-246">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3b79f-246">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3b79f-247">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="3b79f-247">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3b79f-248">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="3b79f-248">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3b79f-249">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="3b79f-249">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b79f-250">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="3b79f-250">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3b79f-251">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="3b79f-251">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3b79f-252">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="3b79f-252">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3b79f-253">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="3b79f-253">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3b79f-254">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="3b79f-254">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3b79f-255">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="3b79f-255">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3b79f-256">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="3b79f-256">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3b79f-257">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="3b79f-257">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3b79f-258">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="3b79f-258">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="3b79f-259"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3b79f-259"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="3b79f-260">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b79f-260">Remarks</span></span>

<span data-ttu-id="3b79f-261">A **classe \_ USERACCOUNT do Win32** é derivada [**da \_ conta Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="3b79f-261">The **Win32\_UserAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

> [!Note]  
> <span data-ttu-id="3b79f-262">Um erro não é retornado para uma tentativa de gravar em uma propriedade somente leitura, e o valor da propriedade permanece inalterado.</span><span class="sxs-lookup"><span data-stu-id="3b79f-262">An error is not returned for an attempt to write to a read-only property, and the value of the property remains unchanged.</span></span>

 

## <a name="examples"></a><span data-ttu-id="3b79f-263">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3b79f-263">Examples</span></span>

<span data-ttu-id="3b79f-264">A [lista de contas de usuário locais usando](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) o exemplo de código do WMI VBScript na galeria do TechNet usa a **\_ conta Win32** Userpara retornar informações sobre as contas de usuário local encontradas em um computador.</span><span class="sxs-lookup"><span data-stu-id="3b79f-264">The [List Local User Accounts Using WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript code sample on TechNet Gallery uses **Win32\_UserAccount** to Returns information about the local user accounts found on a computer.</span></span>

<span data-ttu-id="3b79f-265">[O Sid de conversão para conta de usuário e conta de usuário para Sid](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) O exemplo de código do PowerShell na galeria do TechNet usa a **\_ conta Win32** Userpara converter um SID na conta de usuário e/ou uma conta de usuário em Sid.</span><span class="sxs-lookup"><span data-stu-id="3b79f-265">[The Translate SID to User Account and User Account to SID](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) PowerShell code sample on TechNet Gallery uses **Win32\_UserAccount** to translate a SID to User Account and/or a User Account to SID.</span></span>

<span data-ttu-id="3b79f-266">O exemplo de código VBScript a seguir mostra como obter o nome completo de um usuário em um computador local.</span><span class="sxs-lookup"><span data-stu-id="3b79f-266">The following VBScript code example shows you how to get the full name of a user on a local computer.</span></span> <span data-ttu-id="3b79f-267">O nome completo é o nome do idioma humano, por exemplo, uma pessoa pode ter o nome de usuário "kensanchez" e o nome completo pode ser "Ken Sanchez"; Portanto, substitua o nome de domínio real e o nome de usuário por "mydomainname" e "myusername".</span><span class="sxs-lookup"><span data-stu-id="3b79f-267">The full name is the human language name, for example, a person may have the user name of "kensanchez" and the full name may be "Ken Sanchez", so you substitute the real domain name and user name for "MyDomainName" and "MyUserName".</span></span> <span data-ttu-id="3b79f-268">Para uma consulta eficiente, você deve especificar as propriedades de domínio e nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="3b79f-268">For an efficient query, you must specify both the domain and user name properties.</span></span>

<span data-ttu-id="3b79f-269">Se você for um administrador em um computador remoto, poderá atribuir o nome do computador remoto para strComputer (em vez de ".") e, em seguida, usar o seguinte tipo de script para obter o nome completo de uma conta de usuário em um computador local — de um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="3b79f-269">If you are an administrator on a remote computer, you can assign the name of the remote computer for strComputer (instead of "."), and then use the following type of script to get the full name of a user account on a local computer—from a remote computer.</span></span>


```VB
On Error Resume Next
strComputer = "."

Set objUserAccount = GetObject("winmgmts{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_UserAccount.Domain='MyDomainName',Name='MyUserName' ")

If Err = 0 Then
    WScript.Echo objUserAccount.FullName
Else
    WScript.Echo "No object found" & Err.Number
End If
```




```CSharp
using System.Management;

{
     ManagementScope mgmtScope = new ManagementScope("\\\\.\\Root\\CIMv2");
     ObjectQuery oQuery = new ObjectQuery("SELECT * FROM Win32_UserAccount Where Name=\"myUserName\"");
     ManagementObjectSearcher mgmtSearch = new ManagementObjectSearcher(mgmtScope, oQuery);
     ManagementObjectCollection objCollection = mgmtSearch.Get();
     foreach (ManagementObject mgmtObject in objCollection)
     {
          Console.WriteLine("Full Name : {0}", mgmtObject["FullName"]);
     }
}
```



## <a name="requirements"></a><span data-ttu-id="3b79f-270">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b79f-270">Requirements</span></span>



| <span data-ttu-id="3b79f-271">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b79f-271">Requirement</span></span> | <span data-ttu-id="3b79f-272">Valor</span><span class="sxs-lookup"><span data-stu-id="3b79f-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b79f-273">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b79f-273">Minimum supported client</span></span><br/> | <span data-ttu-id="3b79f-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b79f-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b79f-275">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b79f-275">Minimum supported server</span></span><br/> | <span data-ttu-id="3b79f-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b79f-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b79f-277">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b79f-277">Namespace</span></span><br/>                | <span data-ttu-id="3b79f-278">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3b79f-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b79f-279">MOF</span><span class="sxs-lookup"><span data-stu-id="3b79f-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b79f-280"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b79f-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b79f-281">DLL</span><span class="sxs-lookup"><span data-stu-id="3b79f-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b79f-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b79f-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b79f-283">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b79f-283">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b79f-284">**\_Conta Win32**</span><span class="sxs-lookup"><span data-stu-id="3b79f-284">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="3b79f-285">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="3b79f-285">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
