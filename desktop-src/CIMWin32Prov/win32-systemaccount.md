---
description: O Win32 \_ SystemAccount&\# 8194; A classe WMI representa uma conta do sistema.
ms.assetid: 0f745d93-cbac-428e-bf27-56f6e97d529f
ms.tgt_platform: multiple
title: Classe Win32_SystemAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemAccount
- Win32_SystemAccount.Caption
- Win32_SystemAccount.Description
- Win32_SystemAccount.InstallDate
- Win32_SystemAccount.Status
- Win32_SystemAccount.LocalAccount
- Win32_SystemAccount.SID
- Win32_SystemAccount.SIDType
- Win32_SystemAccount.Domain
- Win32_SystemAccount.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ef246a0ee372c5755aeb30980095e7f2f6ca1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754384"
---
# <a name="win32_systemaccount-class"></a><span data-ttu-id="24d60-103">\_Classe Win32 SystemAccount</span><span class="sxs-lookup"><span data-stu-id="24d60-103">Win32\_SystemAccount class</span></span>

<span data-ttu-id="24d60-104">A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemAccount do Win32** representa uma conta do sistema.</span><span class="sxs-lookup"><span data-stu-id="24d60-104">The **Win32\_SystemAccount** [WMI class](../wmisdk/retrieving-a-class.md) represents a system account.</span></span> <span data-ttu-id="24d60-105">A conta do sistema é usada pelo sistema operacional e serviços.</span><span class="sxs-lookup"><span data-stu-id="24d60-105">The system account is used by the operating system and services.</span></span> <span data-ttu-id="24d60-106">Há muitos serviços e processos no Windows que precisam da capacidade de fazer logon internamente, por exemplo, durante uma instalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="24d60-106">There are many services and processes within Windows that need the capability to logon internally, for example, during a Windows installation.</span></span> <span data-ttu-id="24d60-107">A conta do sistema foi projetada para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="24d60-107">The system account was designed for that purpose.</span></span>

<span data-ttu-id="24d60-108">A conta do sistema é uma conta interna que não aparece no Gerenciador de usuários, não pode ser adicionada a nenhum grupo e não pode ter direitos de usuário atribuídos a ela.</span><span class="sxs-lookup"><span data-stu-id="24d60-108">The system account is an internal account that does not show up in User Manager, cannot be added to any groups, and cannot have user rights assigned to it.</span></span> <span data-ttu-id="24d60-109">No entanto, a conta do sistema aparece em um volume do sistema de arquivos NTFS no Gerenciador de arquivos, localizado na seção permissões do menu segurança.</span><span class="sxs-lookup"><span data-stu-id="24d60-109">However, the system account does show up on an NTFS file system volume in file manager, which is located in the Permissions section of the Security menu.</span></span> <span data-ttu-id="24d60-110">Por padrão, a conta System recebe controle total para todos os arquivos em um volume do sistema de arquivos NTFS, o que significa que a conta System tem os mesmos privilégios funcionais que a conta de administrador.</span><span class="sxs-lookup"><span data-stu-id="24d60-110">By default, the system account is granted full control to all files on an NTFS file system volume, which means that the system account has the same functional privileges as the administrator account.</span></span>

<span data-ttu-id="24d60-111">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="24d60-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="24d60-112">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="24d60-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="24d60-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24d60-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemAccount : Win32_Account
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

## <a name="members"></a><span data-ttu-id="24d60-114">Membros</span><span class="sxs-lookup"><span data-stu-id="24d60-114">Members</span></span>

<span data-ttu-id="24d60-115">A classe **Win32 \_ SystemAccount** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="24d60-115">The **Win32\_SystemAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="24d60-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="24d60-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24d60-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="24d60-117">Properties</span></span>

<span data-ttu-id="24d60-118">A classe **Win32 \_ SystemAccount** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="24d60-118">The **Win32\_SystemAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24d60-119">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="24d60-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24d60-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="24d60-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24d60-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="24d60-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24d60-122">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="24d60-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="24d60-123">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="24d60-123">A short textual description of the object.</span></span>

<span data-ttu-id="24d60-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="24d60-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24d60-125">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="24d60-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24d60-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="24d60-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24d60-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="24d60-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24d60-128">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="24d60-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="24d60-129">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="24d60-129">A textual description of the object.</span></span>

<span data-ttu-id="24d60-130">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="24d60-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24d60-131">**Domínio**</span><span class="sxs-lookup"><span data-stu-id="24d60-131">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24d60-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="24d60-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24d60-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="24d60-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24d60-134">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management Functions \| nomedodomínio")</span><span class="sxs-lookup"><span data-stu-id="24d60-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="24d60-135">Nome do domínio do Windows ao qual a conta do sistema pertence.</span><span class="sxs-lookup"><span data-stu-id="24d60-135">Name of the Windows domain to which the system account belongs.</span></span>

<span data-ttu-id="24d60-136">Exemplo: "NA-SALEs"</span><span class="sxs-lookup"><span data-stu-id="24d60-136">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="24d60-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="24d60-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24d60-138">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="24d60-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="24d60-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="24d60-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24d60-140">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="24d60-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="24d60-141">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="24d60-141">Indicates when the object was installed.</span></span> <span data-ttu-id="24d60-142">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="24d60-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="24d60-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="24d60-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24d60-144">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="24d60-144">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24d60-145">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="24d60-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24d60-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="24d60-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24d60-147">Qualificadores: [ **fixos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="24d60-147">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="24d60-148">Se for **true**, a conta será definida no computador local.</span><span class="sxs-lookup"><span data-stu-id="24d60-148">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="24d60-149">Para recuperar apenas as contas definidas no computador local, crie uma consulta que inclua a condição "LocalAccount =**true**".</span><span class="sxs-lookup"><span data-stu-id="24d60-149">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="24d60-150">Essa propriedade é herdada [**da \_ conta Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="24d60-150">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="24d60-151">**Nome**</span><span class="sxs-lookup"><span data-stu-id="24d60-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24d60-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="24d60-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24d60-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="24d60-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24d60-154">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| name")</span><span class="sxs-lookup"><span data-stu-id="24d60-154">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="24d60-155">Nome da conta do sistema Windows no domínio especificado pela propriedade de **domínio** dessa classe.</span><span class="sxs-lookup"><span data-stu-id="24d60-155">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="24d60-156">**SID**</span><span class="sxs-lookup"><span data-stu-id="24d60-156">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24d60-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="24d60-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24d60-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="24d60-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24d60-159">Qualificadores: [**fixos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| identificadores de segurança do win32api (SIDs)")</span><span class="sxs-lookup"><span data-stu-id="24d60-159">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="24d60-160">SID (identificador de segurança) desta conta.</span><span class="sxs-lookup"><span data-stu-id="24d60-160">Security identifier (SID) for this account.</span></span> <span data-ttu-id="24d60-161">Um SID é um valor de cadeia de caracteres de comprimento variável usado para identificar um confiável.</span><span class="sxs-lookup"><span data-stu-id="24d60-161">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="24d60-162">Cada conta tem um SID exclusivo emitido por uma autoridade (como um domínio do Windows), armazenado em um banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="24d60-162">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="24d60-163">Quando um usuário faz logon, o sistema recupera o SID do usuário do banco de dados e o coloca no token de acesso do usuário.</span><span class="sxs-lookup"><span data-stu-id="24d60-163">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="24d60-164">O sistema usa o SID no token de acesso do usuário para identificar o usuário em todas as interações subsequentes com a segurança do Windows.</span><span class="sxs-lookup"><span data-stu-id="24d60-164">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="24d60-165">Quando um SID é usado como o identificador exclusivo para um usuário ou grupo, ele não pode ser usado novamente para identificar outro usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="24d60-165">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="24d60-166">Essa propriedade é herdada [**da \_ conta Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="24d60-166">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="24d60-167">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="24d60-167">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24d60-168">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="24d60-168">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="24d60-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="24d60-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24d60-170">Qualificadores: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| tipos de enumeração de controle de acesso do \| \_ nome SID \_ use")</span><span class="sxs-lookup"><span data-stu-id="24d60-170">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="24d60-171">Valores enumerados que especificam o tipo de SID (identificador de segurança).</span><span class="sxs-lookup"><span data-stu-id="24d60-171">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="24d60-172">Essa propriedade é herdada [**da \_ conta Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="24d60-172">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="24d60-173">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="24d60-173">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="24d60-174">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="24d60-174">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="24d60-175">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="24d60-175">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="24d60-176">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="24d60-176">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="24d60-177">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="24d60-177">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="24d60-178">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="24d60-178">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="24d60-179">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="24d60-179">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="24d60-180">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="24d60-180">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="24d60-181">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="24d60-181">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24d60-182">**Status**</span><span class="sxs-lookup"><span data-stu-id="24d60-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24d60-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="24d60-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24d60-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="24d60-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24d60-185">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="24d60-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="24d60-186">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="24d60-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="24d60-187">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="24d60-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="24d60-188">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="24d60-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="24d60-189">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="24d60-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="24d60-190">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="24d60-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="24d60-191">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="24d60-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="24d60-192">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="24d60-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="24d60-193">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="24d60-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="24d60-194">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="24d60-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="24d60-195">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="24d60-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="24d60-196">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="24d60-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="24d60-197">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="24d60-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24d60-198">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="24d60-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="24d60-199">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="24d60-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="24d60-200">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="24d60-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="24d60-201">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="24d60-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="24d60-202">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="24d60-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="24d60-203">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="24d60-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="24d60-204">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="24d60-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="24d60-205">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="24d60-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="24d60-206">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="24d60-206">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="24d60-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="24d60-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="24d60-208">Comentários</span><span class="sxs-lookup"><span data-stu-id="24d60-208">Remarks</span></span>

<span data-ttu-id="24d60-209">A classe **Win32 \_ SystemAccount** é derivada da [**\_ conta Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="24d60-209">The **Win32\_SystemAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24d60-210">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24d60-210">Requirements</span></span>



| <span data-ttu-id="24d60-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="24d60-211">Requirement</span></span> | <span data-ttu-id="24d60-212">Valor</span><span class="sxs-lookup"><span data-stu-id="24d60-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24d60-213">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24d60-213">Minimum supported client</span></span><br/> | <span data-ttu-id="24d60-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24d60-214">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24d60-215">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24d60-215">Minimum supported server</span></span><br/> | <span data-ttu-id="24d60-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24d60-216">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24d60-217">Namespace</span><span class="sxs-lookup"><span data-stu-id="24d60-217">Namespace</span></span><br/>                | <span data-ttu-id="24d60-218">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="24d60-218">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="24d60-219">MOF</span><span class="sxs-lookup"><span data-stu-id="24d60-219">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24d60-220"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24d60-220"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="24d60-221">DLL</span><span class="sxs-lookup"><span data-stu-id="24d60-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24d60-222"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24d60-222"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24d60-223">Confira também</span><span class="sxs-lookup"><span data-stu-id="24d60-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24d60-224">**\_Conta Win32**</span><span class="sxs-lookup"><span data-stu-id="24d60-224">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="24d60-225">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="24d60-225">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
