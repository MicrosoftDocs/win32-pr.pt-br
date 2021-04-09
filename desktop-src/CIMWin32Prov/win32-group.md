---
description: Representa dados sobre uma conta de grupo.
ms.assetid: a53d1276-3dc9-419a-bbb8-5dd07794a971
ms.tgt_platform: multiple
title: Classe Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group
- Win32_Group.Caption
- Win32_Group.Description
- Win32_Group.InstallDate
- Win32_Group.Status
- Win32_Group.LocalAccount
- Win32_Group.SID
- Win32_Group.SIDType
- Win32_Group.Domain
- Win32_Group.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8849ba149e0de570150682d3afbad3a4ee33f36
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089461"
---
# <a name="win32_group-class"></a><span data-ttu-id="11552-103">\_Classe de grupo Win32</span><span class="sxs-lookup"><span data-stu-id="11552-103">Win32\_Group class</span></span>

<span data-ttu-id="11552-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ grupo Win32** representa dados sobre uma conta de grupo.</span><span class="sxs-lookup"><span data-stu-id="11552-104">The **Win32\_Group** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents data about a group account.</span></span> <span data-ttu-id="11552-105">Uma conta de grupo permite que os privilégios de acesso sejam alterados para uma lista de usuários.</span><span class="sxs-lookup"><span data-stu-id="11552-105">A group account allows access privileges to be changed for a list of users.</span></span> <span data-ttu-id="11552-106">Exemplo: Marketing2.</span><span class="sxs-lookup"><span data-stu-id="11552-106">Example: Marketing2.</span></span>

<span data-ttu-id="11552-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="11552-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="11552-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="11552-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="11552-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11552-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Group : Win32_Account
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  LocalAccount;
  string   SID;
  uint8    SIDType;
  string   Domain;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="11552-110">Membros</span><span class="sxs-lookup"><span data-stu-id="11552-110">Members</span></span>

<span data-ttu-id="11552-111">A classe de **\_ grupo Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="11552-111">The **Win32\_Group** class has these types of members:</span></span>

-   [<span data-ttu-id="11552-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="11552-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="11552-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="11552-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="11552-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="11552-114">Methods</span></span>

<span data-ttu-id="11552-115">A classe de **\_ grupo Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="11552-115">The **Win32\_Group** class has these methods.</span></span>



| <span data-ttu-id="11552-116">Método</span><span class="sxs-lookup"><span data-stu-id="11552-116">Method</span></span>                                               | <span data-ttu-id="11552-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="11552-117">Description</span></span>                        |
|:-----------------------------------------------------|:-----------------------------------|
| [<span data-ttu-id="11552-118">**Renomear**</span><span class="sxs-lookup"><span data-stu-id="11552-118">**Rename**</span></span>](rename-method-in-class-win32-group.md) | <span data-ttu-id="11552-119">Altera o nome do grupo.</span><span class="sxs-lookup"><span data-stu-id="11552-119">Changes the group name.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="11552-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="11552-120">Properties</span></span>

<span data-ttu-id="11552-121">A classe do **\_ grupo Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="11552-121">The **Win32\_Group** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11552-122">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="11552-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11552-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11552-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11552-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11552-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11552-125">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="11552-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="11552-126">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="11552-126">A short textual description of the object.</span></span>

<span data-ttu-id="11552-127">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11552-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="11552-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="11552-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11552-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11552-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11552-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11552-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11552-131">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="11552-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="11552-132">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="11552-132">A textual description of the object.</span></span>

<span data-ttu-id="11552-133">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11552-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="11552-134">**Domínio**</span><span class="sxs-lookup"><span data-stu-id="11552-134">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11552-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11552-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11552-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11552-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11552-137">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Domain"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management Functions \| nomedodomínio")</span><span class="sxs-lookup"><span data-stu-id="11552-137">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Domain"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="11552-138">Nome do domínio do Windows ao qual a conta do grupo pertence.</span><span class="sxs-lookup"><span data-stu-id="11552-138">Name of the Windows domain to which the group account belongs.</span></span>

<span data-ttu-id="11552-139">Exemplo: "NA-SALEs"</span><span class="sxs-lookup"><span data-stu-id="11552-139">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="11552-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="11552-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11552-141">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="11552-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="11552-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11552-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11552-143">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="11552-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="11552-144">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="11552-144">Indicates when the object was installed.</span></span> <span data-ttu-id="11552-145">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="11552-145">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="11552-146">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11552-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="11552-147">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="11552-147">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11552-148">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="11552-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11552-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11552-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11552-150">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11552-150">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11552-151">Se for **true**, a conta será definida no computador local.</span><span class="sxs-lookup"><span data-stu-id="11552-151">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="11552-152">Para recuperar apenas as contas definidas no computador local, crie uma consulta que inclua a condição "LocalAccount =**true**".</span><span class="sxs-lookup"><span data-stu-id="11552-152">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="11552-153">Essa propriedade é herdada [**da \_ conta Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="11552-153">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="11552-154">**Nome**</span><span class="sxs-lookup"><span data-stu-id="11552-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11552-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11552-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11552-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11552-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11552-157">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management estruturas \| name")</span><span class="sxs-lookup"><span data-stu-id="11552-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="11552-158">Nome da conta de grupo do Windows no domínio especificado pela propriedade de **domínio** dessa classe.</span><span class="sxs-lookup"><span data-stu-id="11552-158">Name of the Windows group account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="11552-159">**SID**</span><span class="sxs-lookup"><span data-stu-id="11552-159">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11552-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11552-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11552-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11552-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11552-162">Qualificadores: [**fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| identificadores de segurança do win32api (SIDs)")</span><span class="sxs-lookup"><span data-stu-id="11552-162">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="11552-163">SID (identificador de segurança) desta conta.</span><span class="sxs-lookup"><span data-stu-id="11552-163">Security identifier (SID) for this account.</span></span> <span data-ttu-id="11552-164">Um SID é um valor de cadeia de caracteres de comprimento variável usado para identificar um confiável.</span><span class="sxs-lookup"><span data-stu-id="11552-164">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="11552-165">Cada conta tem um SID exclusivo emitido por uma autoridade (como um domínio do Windows), armazenado em um banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="11552-165">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="11552-166">Quando um usuário faz logon, o sistema recupera o SID do usuário do banco de dados e o coloca no token de acesso do usuário.</span><span class="sxs-lookup"><span data-stu-id="11552-166">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="11552-167">O sistema usa o SID no token de acesso do usuário para identificar o usuário em todas as interações subsequentes com a segurança do Windows.</span><span class="sxs-lookup"><span data-stu-id="11552-167">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="11552-168">Quando um SID é usado como o identificador exclusivo para um usuário ou grupo, ele não pode ser usado novamente para identificar outro usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="11552-168">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="11552-169">Essa propriedade é herdada [**da \_ conta Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="11552-169">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="11552-170">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="11552-170">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11552-171">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="11552-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="11552-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11552-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11552-173">Qualificadores: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| tipos de enumeração de controle de acesso do \| \_ nome SID \_ use")</span><span class="sxs-lookup"><span data-stu-id="11552-173">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="11552-174">Valores enumerados que especificam o tipo de SID (identificador de segurança).</span><span class="sxs-lookup"><span data-stu-id="11552-174">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="11552-175">Essa propriedade é herdada [**da \_ conta Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="11552-175">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="11552-176">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="11552-176">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="11552-177">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="11552-177">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="11552-178">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="11552-178">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="11552-179">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="11552-179">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="11552-180">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="11552-180">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="11552-181">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="11552-181">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="11552-182">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="11552-182">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="11552-183">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="11552-183">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="11552-184">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="11552-184">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="11552-185">**Status**</span><span class="sxs-lookup"><span data-stu-id="11552-185">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11552-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11552-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11552-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11552-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11552-188">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="11552-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="11552-189">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="11552-189">String that indicates the current status of the object.</span></span> <span data-ttu-id="11552-190">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="11552-190">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="11552-191">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="11552-191">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="11552-192">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="11552-192">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="11552-193">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="11552-193">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="11552-194">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="11552-194">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="11552-195">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="11552-195">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="11552-196">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11552-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="11552-197">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="11552-197">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="11552-198">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="11552-198">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="11552-199">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="11552-199">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="11552-200">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="11552-200">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11552-201">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="11552-201">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="11552-202">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="11552-202">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="11552-203">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="11552-203">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="11552-204">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="11552-204">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="11552-205">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="11552-205">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="11552-206">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="11552-206">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="11552-207">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="11552-207">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="11552-208">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="11552-208">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="11552-209">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="11552-209">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="11552-210"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="11552-210"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="11552-211">Comentários</span><span class="sxs-lookup"><span data-stu-id="11552-211">Remarks</span></span>

<span data-ttu-id="11552-212">A classe do **\_ grupo Win32** é derivada [**da \_ conta Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="11552-212">The **Win32\_Group** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="examples"></a><span data-ttu-id="11552-213">Exemplos</span><span class="sxs-lookup"><span data-stu-id="11552-213">Examples</span></span>

<span data-ttu-id="11552-214">O código a seguir, extraído da [lista de grupos locais usando](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) o exemplo de código do WMI VBScript na galeria do TechNet, usa o **\_ grupo Win32** para retornar informações sobre os grupos locais encontrados em um computador.</span><span class="sxs-lookup"><span data-stu-id="11552-214">The following code, taken from the [List Local Groups Using WMI](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) VBScript code example on TechNet Gallery, uses **Win32\_Group** to return information about the local groups found on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_Group  Where LocalAccount = True") 
 
For Each objItem in colItems 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Domain: " & objItem.Domain 
    Wscript.Echo "Local Account: " & objItem.LocalAccount 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "SID: " & objItem.SID 
    Wscript.Echo "SID Type: " & objItem.SIDType 
    Wscript.Echo "Status: " & objItem.Status 
    Wscript.Echo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="11552-215">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11552-215">Requirements</span></span>



| <span data-ttu-id="11552-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="11552-216">Requirement</span></span> | <span data-ttu-id="11552-217">Valor</span><span class="sxs-lookup"><span data-stu-id="11552-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11552-218">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11552-218">Minimum supported client</span></span><br/> | <span data-ttu-id="11552-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11552-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="11552-220">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11552-220">Minimum supported server</span></span><br/> | <span data-ttu-id="11552-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11552-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="11552-222">Namespace</span><span class="sxs-lookup"><span data-stu-id="11552-222">Namespace</span></span><br/>                | <span data-ttu-id="11552-223">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="11552-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="11552-224">MOF</span><span class="sxs-lookup"><span data-stu-id="11552-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11552-225"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11552-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="11552-226">DLL</span><span class="sxs-lookup"><span data-stu-id="11552-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11552-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11552-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11552-228">Confira também</span><span class="sxs-lookup"><span data-stu-id="11552-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11552-229">**\_Conta Win32**</span><span class="sxs-lookup"><span data-stu-id="11552-229">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

<span data-ttu-id="11552-230">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="11552-230">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

