---
description: Descreve a sessão de logon ou as sessões associadas a um usuário conectado a um sistema de computador executando o Windows.
ms.assetid: d09a115b-95a3-47c7-a04d-c810d044ccc8
ms.tgt_platform: multiple
title: Classe Win32_LogonSession
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSession
- Win32_LogonSession.Caption
- Win32_LogonSession.Description
- Win32_LogonSession.InstallDate
- Win32_LogonSession.Name
- Win32_LogonSession.Status
- Win32_LogonSession.StartTime
- Win32_LogonSession.AuthenticationPackage
- Win32_LogonSession.LogonId
- Win32_LogonSession.LogonType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78e14bbd41c2fd8bb0c10a7bfeeda0dc9d426b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646270"
---
# <a name="win32_logonsession-class"></a><span data-ttu-id="9bf47-103">\_Classe Win32 LogonSession</span><span class="sxs-lookup"><span data-stu-id="9bf47-103">Win32\_LogonSession class</span></span>

<span data-ttu-id="9bf47-104">A classe WMI **\_ LogonSession do Win32** (consulte [recuperando uma classe WMI](/windows/desktop/wmisdk/retrieving-a-class)) descreve a sessão de logon ou as sessões associadas a um usuário conectado a um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="9bf47-104">The **Win32\_LogonSession** WMI class (see [Retrieving a WMI class](/windows/desktop/wmisdk/retrieving-a-class)) describes the logon session or sessions associated with a user logged on to a computer system running Windows.</span></span>

<span data-ttu-id="9bf47-105">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9bf47-105">The following syntax is simplified from Managed Object Format (MOF) code, and includes all of the inherited properties.</span></span> <span data-ttu-id="9bf47-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="9bf47-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf47-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bf47-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{9083C21E-7D58-4e0e-BC30-0BC8922AFB8B}"), AMENDMENT]
class Win32_LogonSession : Win32_Session
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
  string   AuthenticationPackage;
  string   LogonId;
  uint32   LogonType;
};
```

## <a name="members"></a><span data-ttu-id="9bf47-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9bf47-108">Members</span></span>

<span data-ttu-id="9bf47-109">A classe **Win32 \_ LogonSession** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9bf47-109">The **Win32\_LogonSession** class has these types of members:</span></span>

-   [<span data-ttu-id="9bf47-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9bf47-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9bf47-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9bf47-111">Properties</span></span>

<span data-ttu-id="9bf47-112">A classe **Win32 \_ LogonSession** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9bf47-112">The **Win32\_LogonSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9bf47-113">**AuthenticationPackage**</span><span class="sxs-lookup"><span data-stu-id="9bf47-113">**AuthenticationPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bf47-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bf47-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9bf47-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bf47-116">Nome do subsistema usado para autenticar a sessão de logon.</span><span class="sxs-lookup"><span data-stu-id="9bf47-116">Name of the subsystem used to authenticate the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="9bf47-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="9bf47-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bf47-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bf47-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9bf47-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-120">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9bf47-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9bf47-121">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9bf47-121">A short textual description of the object.</span></span>

<span data-ttu-id="9bf47-122">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9bf47-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bf47-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9bf47-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bf47-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bf47-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9bf47-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-126">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="9bf47-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9bf47-127">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9bf47-127">A textual description of the object.</span></span>

<span data-ttu-id="9bf47-128">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9bf47-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bf47-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9bf47-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bf47-130">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9bf47-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9bf47-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-132">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="9bf47-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9bf47-133">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="9bf47-133">Indicates when the object was installed.</span></span> <span data-ttu-id="9bf47-134">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="9bf47-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9bf47-135">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9bf47-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bf47-136">**LogonId**</span><span class="sxs-lookup"><span data-stu-id="9bf47-136">**LogonId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bf47-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bf47-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9bf47-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-139">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9bf47-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9bf47-140">ID atribuída à sessão de logon.</span><span class="sxs-lookup"><span data-stu-id="9bf47-140">ID assigned to the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="9bf47-141">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="9bf47-141">**LogonType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bf47-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9bf47-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9bf47-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bf47-144">Valor numérico que indica o tipo de sessão de logon.</span><span class="sxs-lookup"><span data-stu-id="9bf47-144">Numeric value that indicates the type of logon session.</span></span>

<dt>

<span data-ttu-id="9bf47-145">0</span><span class="sxs-lookup"><span data-stu-id="9bf47-145">0</span></span>
</dt> <dd>

<span data-ttu-id="9bf47-146">Usado somente pela conta do sistema.</span><span class="sxs-lookup"><span data-stu-id="9bf47-146">Used only by the System account.</span></span>

</dd> <dt>

<span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>

<span data-ttu-id="9bf47-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interativo** (2)</span><span class="sxs-lookup"><span data-stu-id="9bf47-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interactive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9bf47-148">Destinado a usuários que estão usando a máquina interativamente, como um usuário conectado por um servidor de terminal, Remote Shell ou processo semelhante.</span><span class="sxs-lookup"><span data-stu-id="9bf47-148">Intended for users who are interactively using the machine, such as a user being logged on by a terminal server, remote shell, or similar process.</span></span>

</dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="9bf47-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Rede** (3)</span><span class="sxs-lookup"><span data-stu-id="9bf47-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Network** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9bf47-150">Destinado a servidores de alto desempenho para autenticar senhas de texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="9bf47-150">Intended for high-performance servers to authenticate clear text passwords.</span></span> <span data-ttu-id="9bf47-151">LogonUser não armazena em cache as credenciais para esse tipo de logon.</span><span class="sxs-lookup"><span data-stu-id="9bf47-151">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>

<span data-ttu-id="9bf47-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Lote** (4)</span><span class="sxs-lookup"><span data-stu-id="9bf47-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Batch** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9bf47-153">Destinado a servidores de lote, em que processos podem ser executados em nome de um usuário sem sua intervenção direta; ou para servidores de desempenho mais alto que processam muitas tentativas de autenticação de texto não criptografado por vez, como email ou servidores Web.</span><span class="sxs-lookup"><span data-stu-id="9bf47-153">Intended for batch servers, where processes can be executed on behalf of a user without their direct intervention; or for higher performance servers that process many clear-text authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="9bf47-154">LogonUser não armazena em cache as credenciais para esse tipo de logon.</span><span class="sxs-lookup"><span data-stu-id="9bf47-154">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9bf47-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço** (5)</span><span class="sxs-lookup"><span data-stu-id="9bf47-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9bf47-156">Indica um logon de tipo de serviço.</span><span class="sxs-lookup"><span data-stu-id="9bf47-156">Indicates a service-type logon.</span></span> <span data-ttu-id="9bf47-157">A conta fornecida deve ter o privilégio de serviço habilitado.</span><span class="sxs-lookup"><span data-stu-id="9bf47-157">The account provided must have the service privilege enabled.</span></span>

</dd> <dt>

<span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>

<span data-ttu-id="9bf47-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)</span><span class="sxs-lookup"><span data-stu-id="9bf47-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9bf47-159">Indica um logon do tipo proxy.</span><span class="sxs-lookup"><span data-stu-id="9bf47-159">Indicates a proxy-type logon.</span></span>

</dd> <dt>

<span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>

<span data-ttu-id="9bf47-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Desbloquear** (7)</span><span class="sxs-lookup"><span data-stu-id="9bf47-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Unlock** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9bf47-161">Esse tipo de logon destina-se a logs de DLLs GINAs em usuários que estão interativamente usando o computador.</span><span class="sxs-lookup"><span data-stu-id="9bf47-161">This logon type is intended for GINA DLLs logging on users who are interactively using the machine.</span></span> <span data-ttu-id="9bf47-162">Esse tipo de logon permite que um registro de auditoria exclusivo seja gerado, mostrando quando a estação de trabalho foi desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="9bf47-162">This logon type allows a unique audit record to be generated that shows when the workstation was unlocked.</span></span>

</dd> <dt>

<span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>

<span data-ttu-id="9bf47-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8)</span><span class="sxs-lookup"><span data-stu-id="9bf47-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9bf47-164">Preserva o nome e a senha nos pacotes de autenticação, permitindo que o servidor faça conexões com outros servidores de rede, ao mesmo tempo que representa o cliente.</span><span class="sxs-lookup"><span data-stu-id="9bf47-164">Preserves the name and password in the authentication packages, allowing the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="9bf47-165">Isso permite que um servidor aceite credenciais de texto não criptografado de um cliente, chame LogonUser, verifique se o usuário pode acessar o sistema pela rede e ainda se comunica com outros servidores.</span><span class="sxs-lookup"><span data-stu-id="9bf47-165">This allows a server to accept clear text credentials from a client, call LogonUser, verify that the user can access the system across the network, and still communicate with other servers.</span></span>

</dd> <dt>

<span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>

<span data-ttu-id="9bf47-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9)</span><span class="sxs-lookup"><span data-stu-id="9bf47-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9)</span></span>


</dt> <dd>

<span data-ttu-id="9bf47-167">Permite que o chamador clone seu token atual e especifique novas credenciais para conexões de saída.</span><span class="sxs-lookup"><span data-stu-id="9bf47-167">Allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="9bf47-168">A nova sessão de logon tem a mesma identificação local, mas usa credenciais diferentes para outras conexões de rede.</span><span class="sxs-lookup"><span data-stu-id="9bf47-168">The new logon session has the same local identify, but uses different credentials for other network connections.</span></span>

</dd> <dt>

<span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>

<span data-ttu-id="9bf47-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10)</span><span class="sxs-lookup"><span data-stu-id="9bf47-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10)</span></span>


</dt> <dd>

<span data-ttu-id="9bf47-170">Sessão de serviços de terminal que é remota e interativa.</span><span class="sxs-lookup"><span data-stu-id="9bf47-170">Terminal Services session that is both remote and interactive.</span></span>

</dd> <dt>

<span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>

<span data-ttu-id="9bf47-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11)</span><span class="sxs-lookup"><span data-stu-id="9bf47-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11)</span></span>


</dt> <dd>

<span data-ttu-id="9bf47-172">Tente credenciais em cache sem acessar a rede.</span><span class="sxs-lookup"><span data-stu-id="9bf47-172">Attempt cached credentials without accessing the network.</span></span>

</dd> <dt>

<span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>

<span data-ttu-id="9bf47-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12)</span><span class="sxs-lookup"><span data-stu-id="9bf47-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12)</span></span>


</dt> <dd>

<span data-ttu-id="9bf47-174">O mesmo que RemoteInteractive.</span><span class="sxs-lookup"><span data-stu-id="9bf47-174">Same as RemoteInteractive.</span></span> <span data-ttu-id="9bf47-175">Isso é usado para auditoria interna.</span><span class="sxs-lookup"><span data-stu-id="9bf47-175">This is used for internal auditing.</span></span>

</dd> <dt>

<span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>

<span data-ttu-id="9bf47-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13)</span><span class="sxs-lookup"><span data-stu-id="9bf47-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9bf47-177">Logon na estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9bf47-177">Workstation logon.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9bf47-178">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9bf47-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bf47-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bf47-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9bf47-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-181">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9bf47-181">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9bf47-182">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="9bf47-182">Label by which the object is known.</span></span> <span data-ttu-id="9bf47-183">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="9bf47-183">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9bf47-184">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9bf47-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bf47-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="9bf47-185">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bf47-186">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9bf47-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9bf47-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bf47-188">Hora em que a sessão foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="9bf47-188">Time at which the session started.</span></span>

<span data-ttu-id="9bf47-189">Esta propriedade é herdada [**da \_ sessão Win32**](win32-session.md).</span><span class="sxs-lookup"><span data-stu-id="9bf47-189">This property is inherited from [**Win32\_Session**](win32-session.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bf47-190">**Status**</span><span class="sxs-lookup"><span data-stu-id="9bf47-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bf47-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bf47-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9bf47-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bf47-193">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9bf47-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9bf47-194">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9bf47-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="9bf47-195">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="9bf47-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="9bf47-196">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="9bf47-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="9bf47-197">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="9bf47-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="9bf47-198">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="9bf47-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9bf47-199">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="9bf47-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9bf47-200">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="9bf47-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9bf47-201">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9bf47-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9bf47-202">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9bf47-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9bf47-203">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9bf47-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9bf47-204">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="9bf47-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9bf47-205">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="9bf47-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9bf47-206">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="9bf47-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9bf47-207">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="9bf47-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9bf47-208">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="9bf47-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9bf47-209">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="9bf47-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9bf47-210">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="9bf47-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9bf47-211">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="9bf47-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9bf47-212">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="9bf47-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9bf47-213">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="9bf47-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9bf47-214">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="9bf47-214">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="9bf47-215"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9bf47-215"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="examples"></a><span data-ttu-id="9bf47-216">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9bf47-216">Examples</span></span>

<span data-ttu-id="9bf47-217">O exemplo do PowerShell [listar informações da sessão de logon](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) retorna informações sobre sessões de logon associadas ao usuário conectado no momento a um computador.</span><span class="sxs-lookup"><span data-stu-id="9bf47-217">The [List Logon Session Information](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) PowerShell sample returns information about logon sessions associated with the user currently logged on to a computer.</span></span>

<span data-ttu-id="9bf47-218">O exemplo do PowerShell a seguir verifica se a sessão remota está aberta para um usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="9bf47-218">The following PowerShell example checks for remote session open for a specified user.</span></span>


```PowerShell
$user = "<user name>"
$servers = gci servers.txt 

     foreach ($server in $servers){
     $logons = gwmi win32_loggedonuser -computername $server

          foreach ($logon in $logons){
               if ($logon.antecedent -match $user){
               $logonid = $logon.dependent.split("=")[1] 
               $session =gwmi win32_logonsession |? {$_.logonid -match $logonid}
               if ($session.logontype -eq "10"){
               Write-host "You have an active Terminal Server session on server $($server)"
                }
          }
```



## <a name="requirements"></a><span data-ttu-id="9bf47-219">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bf47-219">Requirements</span></span>



| <span data-ttu-id="9bf47-220">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bf47-220">Requirement</span></span> | <span data-ttu-id="9bf47-221">Valor</span><span class="sxs-lookup"><span data-stu-id="9bf47-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf47-222">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bf47-222">Minimum supported client</span></span><br/> | <span data-ttu-id="9bf47-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9bf47-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9bf47-224">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bf47-224">Minimum supported server</span></span><br/> | <span data-ttu-id="9bf47-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9bf47-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9bf47-226">Namespace</span><span class="sxs-lookup"><span data-stu-id="9bf47-226">Namespace</span></span><br/>                | <span data-ttu-id="9bf47-227">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9bf47-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9bf47-228">MOF</span><span class="sxs-lookup"><span data-stu-id="9bf47-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bf47-229"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bf47-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9bf47-230">DLL</span><span class="sxs-lookup"><span data-stu-id="9bf47-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bf47-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bf47-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bf47-232">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bf47-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bf47-233">**Sessão do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="9bf47-233">**Win32\_Session**</span></span>](win32-session.md)
</dt> <dt>

<span data-ttu-id="9bf47-234">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9bf47-234">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

