---
description: Contém informações sobre contas de usuário e contas de grupo conhecidas pelo sistema de computador que executa o Windows.
ms.assetid: c0916f20-05be-4282-9642-28cec606bfd7
ms.tgt_platform: multiple
title: Classe Win32_Account
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Account
- Win32_Account.Caption
- Win32_Account.Description
- Win32_Account.Domain
- Win32_Account.InstallDate
- Win32_Account.LocalAccount
- Win32_Account.Name
- Win32_Account.SID
- Win32_Account.SIDType
- Win32_Account.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2af601799095192d7af4ffedce0c8e0cd28bff21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089543"
---
# <a name="win32_account-class"></a><span data-ttu-id="536f6-103">\_Classe de conta Win32</span><span class="sxs-lookup"><span data-stu-id="536f6-103">Win32\_Account class</span></span>

<span data-ttu-id="536f6-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstrata da **\_ conta do Win32** contém informações sobre contas de usuário e contas de grupo conhecidas pelo sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="536f6-104">The **Win32\_Account** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) contains information about user accounts and group accounts known to the computer system running Windows.</span></span> <span data-ttu-id="536f6-105">Os nomes de usuário ou grupo reconhecidos por um domínio do Windows são descendentes (ou membros) dessa classe.</span><span class="sxs-lookup"><span data-stu-id="536f6-105">User or group names recognized by a Windows domain are descendants (or members) of this class.</span></span>

<span data-ttu-id="536f6-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="536f6-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="536f6-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="536f6-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="536f6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="536f6-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4C9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Account : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   Domain;
  datetime InstallDate;
  boolean  LocalAccount;
  string   Name;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="536f6-109">Membros</span><span class="sxs-lookup"><span data-stu-id="536f6-109">Members</span></span>

<span data-ttu-id="536f6-110">A classe de **\_ conta Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="536f6-110">The **Win32\_Account** class has these types of members:</span></span>

-   [<span data-ttu-id="536f6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="536f6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="536f6-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="536f6-112">Properties</span></span>

<span data-ttu-id="536f6-113">A classe de **\_ conta Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="536f6-113">The **Win32\_Account** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="536f6-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="536f6-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="536f6-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="536f6-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="536f6-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="536f6-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="536f6-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="536f6-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="536f6-118">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="536f6-118">Short description of the object.</span></span>

<span data-ttu-id="536f6-119">Essa propriedade é herdada da classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="536f6-119">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="536f6-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="536f6-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="536f6-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="536f6-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="536f6-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="536f6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="536f6-123">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="536f6-123">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="536f6-124">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="536f6-124">Description of the object.</span></span>

<span data-ttu-id="536f6-125">Essa propriedade é herdada da classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="536f6-125">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="536f6-126">**Domínio**</span><span class="sxs-lookup"><span data-stu-id="536f6-126">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="536f6-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="536f6-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="536f6-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="536f6-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="536f6-129">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| domínio de funções de gerenciamento de rede win32api \| ")</span><span class="sxs-lookup"><span data-stu-id="536f6-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="536f6-130">Nome do domínio do Windows ao qual pertence um grupo ou usuário.</span><span class="sxs-lookup"><span data-stu-id="536f6-130">Name of the Windows domain to which a group or user belongs.</span></span>

<span data-ttu-id="536f6-131">Exemplo: "NA-SALEs"</span><span class="sxs-lookup"><span data-stu-id="536f6-131">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="536f6-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="536f6-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="536f6-133">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="536f6-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="536f6-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="536f6-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="536f6-135">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="536f6-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="536f6-136">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="536f6-136">Date and time that the object was installed.</span></span> <span data-ttu-id="536f6-137">Essa propriedade não requer um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="536f6-137">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="536f6-138">Essa propriedade é herdada da classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="536f6-138">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="536f6-139">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="536f6-139">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="536f6-140">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="536f6-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="536f6-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="536f6-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="536f6-142">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="536f6-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="536f6-143">Se for **true**, a conta será definida no computador local.</span><span class="sxs-lookup"><span data-stu-id="536f6-143">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="536f6-144">Para recuperar apenas as contas definidas no computador local, crie uma consulta que inclua a condição "LocalAccount =**true**".</span><span class="sxs-lookup"><span data-stu-id="536f6-144">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

</dd> <dt>

<span data-ttu-id="536f6-145">**Nome**</span><span class="sxs-lookup"><span data-stu-id="536f6-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="536f6-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="536f6-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="536f6-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="536f6-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="536f6-148">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management estruturas \| name")</span><span class="sxs-lookup"><span data-stu-id="536f6-148">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="536f6-149">Nome da conta do sistema Windows no domínio especificado pela propriedade de **domínio** dessa classe.</span><span class="sxs-lookup"><span data-stu-id="536f6-149">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span> <span data-ttu-id="536f6-150">Essa propriedade substitui a propriedade **Name** herdada de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="536f6-150">This property overrides the **Name** property inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="536f6-151">**SID**</span><span class="sxs-lookup"><span data-stu-id="536f6-151">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="536f6-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="536f6-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="536f6-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="536f6-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="536f6-154">Qualificadores: [**fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| identificadores de segurança do win32api (SIDs)")</span><span class="sxs-lookup"><span data-stu-id="536f6-154">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="536f6-155">SID (identificador de segurança) desta conta.</span><span class="sxs-lookup"><span data-stu-id="536f6-155">Security identifier (SID) for this account.</span></span> <span data-ttu-id="536f6-156">Um SID é um valor de cadeia de caracteres de comprimento variável usado para identificar um confiável.</span><span class="sxs-lookup"><span data-stu-id="536f6-156">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="536f6-157">Cada conta tem um SID exclusivo emitido por uma autoridade (como um domínio do Windows), armazenado em um banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="536f6-157">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="536f6-158">Quando um usuário faz logon, o sistema recupera o SID do usuário do banco de dados e o coloca no token de acesso do usuário.</span><span class="sxs-lookup"><span data-stu-id="536f6-158">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="536f6-159">O sistema usa o SID no token de acesso do usuário para identificar o usuário em todas as interações subsequentes com a segurança do Windows.</span><span class="sxs-lookup"><span data-stu-id="536f6-159">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="536f6-160">Quando um SID é usado como o identificador exclusivo para um usuário ou grupo, ele não pode ser usado novamente para identificar outro usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="536f6-160">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

</dd> <dt>

<span data-ttu-id="536f6-161">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="536f6-161">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="536f6-162">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="536f6-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="536f6-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="536f6-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="536f6-164">Qualificadores: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| tipos de enumeração de controle de acesso do \| \_ nome SID \_ use")</span><span class="sxs-lookup"><span data-stu-id="536f6-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="536f6-165">Valores enumerados que especificam o tipo de SID (identificador de segurança).</span><span class="sxs-lookup"><span data-stu-id="536f6-165">Enumerated values that specify the type of security identifier (SID).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="536f6-166">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="536f6-166">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="536f6-167">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="536f6-167">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="536f6-168">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="536f6-168">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="536f6-169">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="536f6-169">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="536f6-170">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="536f6-170">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="536f6-171">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="536f6-171">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="536f6-172">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="536f6-172">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="536f6-173">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="536f6-173">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="536f6-174">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="536f6-174">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="536f6-175">**Status**</span><span class="sxs-lookup"><span data-stu-id="536f6-175">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="536f6-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="536f6-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="536f6-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="536f6-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="536f6-178">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="536f6-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="536f6-179">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="536f6-179">Current status of the object.</span></span> <span data-ttu-id="536f6-180">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="536f6-180">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="536f6-181">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevê uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="536f6-181">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicts a failure in the near future).</span></span> <span data-ttu-id="536f6-182">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="536f6-182">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="536f6-183">O último, "serviço", pode ser aplicado durante o espelhamento de espelho de um disco, recarregamento de uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="536f6-183">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="536f6-184">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="536f6-184">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="536f6-185">Essa propriedade é herdada da classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="536f6-185">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

<span data-ttu-id="536f6-186">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="536f6-186">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="536f6-187">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="536f6-187">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="536f6-188">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="536f6-188">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="536f6-189">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="536f6-189">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="536f6-190">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="536f6-190">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="536f6-191">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="536f6-191">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="536f6-192">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="536f6-192">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="536f6-193">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="536f6-193">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="536f6-194">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="536f6-194">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="536f6-195">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="536f6-195">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="536f6-196">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="536f6-196">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="536f6-197">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="536f6-197">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="536f6-198">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="536f6-198">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="536f6-199"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="536f6-199"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="536f6-200">Comentários</span><span class="sxs-lookup"><span data-stu-id="536f6-200">Remarks</span></span>

<span data-ttu-id="536f6-201">A classe de **\_ conta Win32** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="536f6-201">The **Win32\_Account** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="536f6-202">Exemplos</span><span class="sxs-lookup"><span data-stu-id="536f6-202">Examples</span></span>

<span data-ttu-id="536f6-203">O código do PowerShell a seguir recupera as contas locais.</span><span class="sxs-lookup"><span data-stu-id="536f6-203">The following PowerShell code retrieves the local accounts.</span></span>


```PowerShell
Get-WmiObject Win32_Account -Filter "Domain='$Env:ComputerName'"
```



<span data-ttu-id="536f6-204">O código do PowerShell a seguir recupera as contas de domínio.</span><span class="sxs-lookup"><span data-stu-id="536f6-204">The following PowerShell code retrieves the domain accounts.</span></span>


```PowerShell
 Get-WmiObject Win32_Account -Filter "Domain='$Env:UserDomain'" 
```



## <a name="requirements"></a><span data-ttu-id="536f6-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="536f6-205">Requirements</span></span>



| <span data-ttu-id="536f6-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="536f6-206">Requirement</span></span> | <span data-ttu-id="536f6-207">Valor</span><span class="sxs-lookup"><span data-stu-id="536f6-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="536f6-208">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="536f6-208">Minimum supported client</span></span><br/> | <span data-ttu-id="536f6-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="536f6-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="536f6-210">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="536f6-210">Minimum supported server</span></span><br/> | <span data-ttu-id="536f6-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="536f6-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="536f6-212">Namespace</span><span class="sxs-lookup"><span data-stu-id="536f6-212">Namespace</span></span><br/>                | <span data-ttu-id="536f6-213">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="536f6-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="536f6-214">MOF</span><span class="sxs-lookup"><span data-stu-id="536f6-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="536f6-215"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="536f6-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="536f6-216">DLL</span><span class="sxs-lookup"><span data-stu-id="536f6-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="536f6-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="536f6-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="536f6-218">Confira também</span><span class="sxs-lookup"><span data-stu-id="536f6-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="536f6-219">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="536f6-219">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="536f6-220">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="536f6-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

