---
title: Classe Win32_RemoteAppChangeEvent
description: Representa uma alteração nas configurações do RemoteApp do Windows Server 2008 R2 no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 3434ee4e-283e-4147-a73b-c131e8af6c57
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RemoteAppChangeEvent Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RemoteAppChangeEvent classe, descrita
topic_type:
- apiref
api_name:
- Win32_RemoteAppChangeEvent
- Win32_RemoteAppChangeEvent.SECURITY_DESCRIPTOR
- Win32_RemoteAppChangeEvent.TIME_CREATED
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5355d057038e97e9f381646134ff6487541f67f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085554"
---
# <a name="win32_remoteappchangeevent-class"></a><span data-ttu-id="5e5c4-105">\_Classe Win32 RemoteAppChangeEvent</span><span class="sxs-lookup"><span data-stu-id="5e5c4-105">Win32\_RemoteAppChangeEvent class</span></span>

<span data-ttu-id="5e5c4-106">Representa uma alteração nas configurações do RemoteApp do Windows Server 2008 R2 no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="5e5c4-106">Represents a change to Windows Server 2008 R2 RemoteApp settings on the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e5c4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e5c4-107">Syntax</span></span>

``` syntax
class Win32_RemoteAppChangeEvent : ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="5e5c4-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5e5c4-108">Members</span></span>

<span data-ttu-id="5e5c4-109">A classe **Win32 \_ RemoteAppChangeEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5e5c4-109">The **Win32\_RemoteAppChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="5e5c4-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5e5c4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e5c4-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5e5c4-111">Properties</span></span>

<span data-ttu-id="5e5c4-112">A classe **Win32 \_ RemoteAppChangeEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5e5c4-112">The **Win32\_RemoteAppChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e5c4-113">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="5e5c4-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c4-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="5e5c4-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5e5c4-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e5c4-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e5c4-116">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="5e5c4-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="5e5c4-117">Esta propriedade é herdada do [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="5e5c4-117">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="5e5c4-118">Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="5e5c4-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="5e5c4-119">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="5e5c4-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c4-120">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5e5c4-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c4-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e5c4-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e5c4-122">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="5e5c4-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="5e5c4-123">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="5e5c4-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="5e5c4-124">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="5e5c4-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="5e5c4-125">Esta propriedade é herdada do [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="5e5c4-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="5e5c4-126">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5e5c4-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e5c4-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e5c4-127">Remarks</span></span>

<span data-ttu-id="5e5c4-128">Para se conectar ao namespace " \\ \\ terminal cimv2" raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="5e5c4-128">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="5e5c4-129">Para chamadas C/C++, esse é um nível de autenticação **de \_ \_ privacidade do \_ PCT no \_ nível \_** de autenticado RPC C, que pode ser definido usando a função com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="5e5c4-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="5e5c4-130">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="5e5c4-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="5e5c4-131">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="5e5c4-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="5e5c4-132">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5e5c4-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5e5c4-133">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5e5c4-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5e5c4-134">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="5e5c4-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5e5c4-135">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5e5c4-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e5c4-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e5c4-136">Requirements</span></span>



| <span data-ttu-id="5e5c4-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e5c4-137">Requirement</span></span> | <span data-ttu-id="5e5c4-138">Valor</span><span class="sxs-lookup"><span data-stu-id="5e5c4-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5c4-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e5c4-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5c4-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5e5c4-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5e5c4-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e5c4-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5c4-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e5c4-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e5c4-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e5c4-143">Namespace</span></span><br/>                | <span data-ttu-id="5e5c4-144">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="5e5c4-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5e5c4-145">MOF</span><span class="sxs-lookup"><span data-stu-id="5e5c4-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e5c4-146"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e5c4-146"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="5e5c4-147">DLL</span><span class="sxs-lookup"><span data-stu-id="5e5c4-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e5c4-148"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e5c4-148"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

