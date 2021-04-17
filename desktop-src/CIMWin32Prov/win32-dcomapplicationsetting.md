---
description: O Win32 \_ DCOMApplicationSetting&\# 8194; A classe WMI representa as configurações de um aplicativo DCOM.
ms.assetid: afa23faa-bf4d-4f54-9ee9-227956ff3292
ms.tgt_platform: multiple
title: Classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting
- Win32_DCOMApplicationSetting.Caption
- Win32_DCOMApplicationSetting.Description
- Win32_DCOMApplicationSetting.SettingID
- Win32_DCOMApplicationSetting.AppID
- Win32_DCOMApplicationSetting.AuthenticationLevel
- Win32_DCOMApplicationSetting.CustomSurrogate
- Win32_DCOMApplicationSetting.EnableAtStorageActivation
- Win32_DCOMApplicationSetting.LocalService
- Win32_DCOMApplicationSetting.RemoteServerName
- Win32_DCOMApplicationSetting.RunAsUser
- Win32_DCOMApplicationSetting.ServiceParameters
- Win32_DCOMApplicationSetting.UseSurrogate
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 085304c5319811ba87979124613c7d8e83fd7479
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755662"
---
# <a name="win32_dcomapplicationsetting-class"></a><span data-ttu-id="fc6e6-103">\_Classe Win32 DCOMApplicationSetting</span><span class="sxs-lookup"><span data-stu-id="fc6e6-103">Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="fc6e6-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DCOMApplicationSetting do Win32** representa as configurações de um aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-104">The **Win32\_DCOMApplicationSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a DCOM application.</span></span> <span data-ttu-id="fc6e6-105">Ele contém opções de configuração do DCOM associadas à chave **AppID** no registro.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-105">It contains DCOM configuration options associated with the **AppID** key in the registry.</span></span> <span data-ttu-id="fc6e6-106">Essas opções são válidas nos componentes agrupados logicamente sob a classe de aplicativo fornecida.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-106">These options are valid on the components logically grouped under the given application class.</span></span>

<span data-ttu-id="fc6e6-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fc6e6-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc6e6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc6e6-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A561-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplicationSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  uint32  AuthenticationLevel;
  string  CustomSurrogate;
  boolean EnableAtStorageActivation;
  string  LocalService;
  string  RemoteServerName;
  string  RunAsUser;
  string  ServiceParameters;
  boolean UseSurrogate;
};
```

## <a name="members"></a><span data-ttu-id="fc6e6-110">Membros</span><span class="sxs-lookup"><span data-stu-id="fc6e6-110">Members</span></span>

<span data-ttu-id="fc6e6-111">A classe **Win32 \_ DCOMApplicationSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fc6e6-111">The **Win32\_DCOMApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="fc6e6-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc6e6-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="fc6e6-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fc6e6-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fc6e6-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc6e6-114">Methods</span></span>

<span data-ttu-id="fc6e6-115">A classe **Win32 \_ DCOMApplicationSetting** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-115">The **Win32\_DCOMApplicationSetting** class has these methods.</span></span>



| <span data-ttu-id="fc6e6-116">Método</span><span class="sxs-lookup"><span data-stu-id="fc6e6-116">Method</span></span>                                                                                                                        | <span data-ttu-id="fc6e6-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc6e6-117">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc6e6-118">**GetAccessSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-118">**GetAccessSecurityDescriptor**</span></span>](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="fc6e6-119">Obtém o descritor de segurança que controla quem tem permissão para acessar um aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-119">Gets the security descriptor that controls who is allowed to access a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="fc6e6-120">**GetConfigurationSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-120">**GetConfigurationSecurityDescriptor**</span></span>](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="fc6e6-121">Obtém o descritor de segurança que controla quem tem permissão para configurar um aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-121">Gets the security descriptor that controls who is allowed to configure a DCOM application.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="fc6e6-122">**GetLaunchSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-122">**GetLaunchSecurityDescriptor**</span></span>](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | <span data-ttu-id="fc6e6-123">Obtém o descritor de segurança que controla quem tem permissão para iniciar um aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-123">Gets the security descriptor that controls who is allowed to launch a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="fc6e6-124">**SetAccessSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-124">**SetAccessSecurityDescriptor**</span></span>](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="fc6e6-125">Atualiza o descritor de segurança de acesso do aplicativo DCOM com um novo descritor de segurança que é definido por uma instância da classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="fc6e6-125">Updates the access security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |
| [<span data-ttu-id="fc6e6-126">**SetConfigurationSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-126">**SetConfigurationSecurityDescriptor**</span></span>](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="fc6e6-127">Atualiza o descritor de segurança de configuração do aplicativo DCOM com um novo descritor de segurança que é definido por uma instância da classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="fc6e6-127">Updates the configuration security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/> |
| [<span data-ttu-id="fc6e6-128">**SetLaunchSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-128">**SetLaunchSecurityDescriptor**</span></span>](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="fc6e6-129">Atualiza o descritor de segurança de inicialização do aplicativo DCOM com um novo descritor de segurança que é definido por uma instância da classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="fc6e6-129">Updates the launch security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="fc6e6-130">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fc6e6-130">Properties</span></span>

<span data-ttu-id="fc6e6-131">A classe **Win32 \_ DCOMApplicationSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-131">The **Win32\_DCOMApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc6e6-132">**AppID**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-132">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc6e6-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc6e6-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-135">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="fc6e6-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="fc6e6-136">GUID (identificador global exclusivo) para este aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-136">Globally unique identifier (GUID) for this DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="fc6e6-137">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-137">**AuthenticationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc6e6-138">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fc6e6-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-140">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ AuthenticationLevel \] ")</span><span class="sxs-lookup"><span data-stu-id="fc6e6-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[AuthenticationLevel\]")</span></span>
</dt> </dl>

<span data-ttu-id="fc6e6-141">Nível mínimo de autenticação do cliente exigido por este servidor COM.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-141">Minimum client authentication level required by this COM server.</span></span> <span data-ttu-id="fc6e6-142">Se for **NULL**, os valores padrão serão usados.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-142">If **NULL**, the default values are used.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="fc6e6-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nenhum** (1)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fc6e6-144">Nenhum (nenhuma autenticação é executada)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-144">None (no authentication is performed)</span></span>

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span data-ttu-id="fc6e6-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Conectar** (2)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Connect** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fc6e6-146">Conectar (a autenticação é executada somente quando o cliente estabelece uma relação com o aplicativo)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-146">Connect (authentication is performed only when the client establishes a relationship with the application)</span></span>

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span data-ttu-id="fc6e6-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**Chamada** (3)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**Call** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fc6e6-148">Chamada (a autenticação é executada somente no início de cada chamada quando o aplicativo recebe a solicitação)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-148">Call (authentication is performed only at the beginning of each call when the application receives the request)</span></span>

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span data-ttu-id="fc6e6-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Pacote** (4)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Packet** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fc6e6-150">Pacote (a autenticação é executada em todos os dados recebidos do cliente)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-150">Packet (authentication is performed on all of the data received from the client)</span></span>

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span data-ttu-id="fc6e6-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fc6e6-152">PacketIntegrity (todos os dados transferidos entre o cliente e o aplicativo são autenticados e verificados)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-152">PacketIntegrity (all of the data transferred between the client and the application is authenticated and verified)</span></span>

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span data-ttu-id="fc6e6-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fc6e6-154">PacketPrivacy (as propriedades dos outros níveis de autenticação são usadas e todos os dados são criptografados)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-154">PacketPrivacy (the properties of the other authentication levels are used and all of the data is encrypted)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc6e6-155">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-155">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc6e6-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc6e6-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-158">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="fc6e6-159">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-159">Short textual description of the current object.</span></span>

<span data-ttu-id="fc6e6-160">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="fc6e6-160">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc6e6-161">**CustomSurrogate**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-161">**CustomSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc6e6-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc6e6-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-164">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")</span><span class="sxs-lookup"><span data-stu-id="fc6e6-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="fc6e6-165">Nome do substituto personalizado no qual o aplicativo DCOM em processo é ativado.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-165">Name of the custom surrogate in which the in-process DCOM application is activated.</span></span> <span data-ttu-id="fc6e6-166">Se esse valor for **nulo** e a chave **UseSurrogate** for **true**, o sistema fornecerá um processo substituto.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-166">If this value is **NULL** and the **UseSurrogate** key is **TRUE**, then the system provides a surrogate process.</span></span>

</dd> <dt>

<span data-ttu-id="fc6e6-167">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc6e6-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc6e6-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc6e6-170">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-170">Textual description of the current object.</span></span>

<span data-ttu-id="fc6e6-171">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="fc6e6-171">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc6e6-172">**EnableAtStorageActivation**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-172">**EnableAtStorageActivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc6e6-173">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc6e6-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-175">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ ActivateAtStorage \] ")</span><span class="sxs-lookup"><span data-stu-id="fc6e6-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ActivateAtStorage\]")</span></span>
</dt> </dl>

<span data-ttu-id="fc6e6-176">O aplicativo DCOM recupera o estado salvo do aplicativo ou começa com o estado em que o aplicativo é inicializado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-176">DCOM application retrieves the saved state of the application or begins from the state in which the application is first initialized.</span></span>

</dd> <dt>

<span data-ttu-id="fc6e6-177">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-177">**LocalService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc6e6-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc6e6-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-180">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ LocalService \] ")</span><span class="sxs-lookup"><span data-stu-id="fc6e6-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[LocalService\]")</span></span>
</dt> </dl>

<span data-ttu-id="fc6e6-181">Nome dos serviços fornecidos pelo aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-181">Name for the services provided by the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="fc6e6-182">**RemoteServerName**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-182">**RemoteServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc6e6-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fc6e6-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-185">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ RemoteServerName \] ")</span><span class="sxs-lookup"><span data-stu-id="fc6e6-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RemoteServerName\]")</span></span>
</dt> </dl>

<span data-ttu-id="fc6e6-186">Nome do servidor remoto onde o aplicativo é ativado.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-186">Name of the remote server where the application is activated.</span></span>

</dd> <dt>

<span data-ttu-id="fc6e6-187">**RunAsUser**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-187">**RunAsUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc6e6-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc6e6-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-190">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ runas \] ")</span><span class="sxs-lookup"><span data-stu-id="fc6e6-190">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RunAs\]")</span></span>
</dt> </dl>

<span data-ttu-id="fc6e6-191">Conta de usuário específica sob a qual o aplicativo deve ser executado na ativação.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-191">Specific user account under which the application is to be run on activation.</span></span>

</dd> <dt>

<span data-ttu-id="fc6e6-192">**Serviceparameters**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-192">**ServiceParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc6e6-193">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc6e6-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-195">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ serviceparameters \] ")</span><span class="sxs-lookup"><span data-stu-id="fc6e6-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ServiceParameters\]")</span></span>
</dt> </dl>

<span data-ttu-id="fc6e6-196">Parâmetros de linha de comando passados para o aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-196">Command-line parameters passed to the DCOM application.</span></span> <span data-ttu-id="fc6e6-197">Isso será válido somente se o aplicativo for escrito como um serviço baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-197">This is valid only if the application is written as a Windows-based service.</span></span>

</dd> <dt>

<span data-ttu-id="fc6e6-198">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-198">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc6e6-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc6e6-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-201">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="fc6e6-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fc6e6-202">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-202">Identifier by which the current object is known.</span></span>

<span data-ttu-id="fc6e6-203">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="fc6e6-203">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc6e6-204">**UseSurrogate**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-204">**UseSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc6e6-205">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-206">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fc6e6-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc6e6-207">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")</span><span class="sxs-lookup"><span data-stu-id="fc6e6-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="fc6e6-208">O aplicativo DCOM pode ser ativado como um servidor fora do processo pelo uso de um arquivo executável substituto.</span><span class="sxs-lookup"><span data-stu-id="fc6e6-208">DCOM application can be activated as an out-of-process server by use of a surrogate executable file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc6e6-209">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc6e6-209">Remarks</span></span>

<span data-ttu-id="fc6e6-210">A classe **Win32 \_ DCOMApplicationSetting** é derivada da [**\_ configuração do Win32**](win32-comsetting.md).</span><span class="sxs-lookup"><span data-stu-id="fc6e6-210">The **Win32\_DCOMApplicationSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc6e6-211">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc6e6-211">Requirements</span></span>



| <span data-ttu-id="fc6e6-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc6e6-212">Requirement</span></span> | <span data-ttu-id="fc6e6-213">Valor</span><span class="sxs-lookup"><span data-stu-id="fc6e6-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc6e6-214">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc6e6-214">Minimum supported client</span></span><br/> | <span data-ttu-id="fc6e6-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc6e6-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fc6e6-216">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc6e6-216">Minimum supported server</span></span><br/> | <span data-ttu-id="fc6e6-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc6e6-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc6e6-218">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc6e6-218">Namespace</span></span><br/>                | <span data-ttu-id="fc6e6-219">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fc6e6-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fc6e6-220">MOF</span><span class="sxs-lookup"><span data-stu-id="fc6e6-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc6e6-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc6e6-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc6e6-222">DLL</span><span class="sxs-lookup"><span data-stu-id="fc6e6-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc6e6-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc6e6-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc6e6-224">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc6e6-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc6e6-225">**Configuração do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-225">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="fc6e6-226">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc6e6-226">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fc6e6-227">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="fc6e6-227">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="fc6e6-228">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="fc6e6-228">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="fc6e6-229">Alterando a segurança de acesso em objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="fc6e6-229">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

