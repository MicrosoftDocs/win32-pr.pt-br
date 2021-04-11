---
title: Método FindLicenseServers da classe Win32_TerminalServiceSetting
description: Enumera todos os servidores de licença Área de Trabalho Remota e o método de descoberta.
ms.assetid: 0de2ee6f-6c56-4293-84da-131b433c6a9d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método FindLicenseServers
- Método FindLicenseServers Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método FindLicenseServers
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.FindLicenseServers
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83376876009a691fed233cf723f04dcc3bc3c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919046"
---
# <a name="findlicenseservers-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="c9100-106">Método FindLicenseServers da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="c9100-106">FindLicenseServers method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="c9100-107">Enumera todos os servidores de licença Área de Trabalho Remota e o método de descoberta.</span><span class="sxs-lookup"><span data-stu-id="c9100-107">Enumerates all of the Remote Desktop license servers, and the method of discovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9100-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9100-108">Syntax</span></span>


```mof
uint32 FindLicenseServers(
  [out] Win32_TSDiscoveredLicenseServer LicenseServersList[],
  [out] uint32                          Count
);
```



## <a name="parameters"></a><span data-ttu-id="c9100-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9100-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9100-110">*LicenseServersList* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c9100-110">*LicenseServersList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9100-111">A lista de [**objetos \_ TSDiscoveredLicenseServer do Win32**](win32-tsdiscoveredlicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="c9100-111">The list of [**Win32\_TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md) objects.</span></span> <span data-ttu-id="c9100-112">Cada objeto na lista de saída tem o nome do servidor de licença Área de Trabalho Remota e o método de descoberta.</span><span class="sxs-lookup"><span data-stu-id="c9100-112">Each object in the output list has the name of the Remote Desktop license server, and the method of discovery.</span></span>

</dd> <dt>

<span data-ttu-id="c9100-113">*Contagem* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="c9100-113">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9100-114">O número total de servidores de licença de Área de Trabalho Remota descobertos na lista de saída.</span><span class="sxs-lookup"><span data-stu-id="c9100-114">The total number of discovered Remote Desktop license servers in the output list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9100-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9100-115">Remarks</span></span>

<span data-ttu-id="c9100-116">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="c9100-116">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="c9100-117">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="c9100-117">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="c9100-118">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="c9100-118">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="c9100-119">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="c9100-119">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="c9100-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c9100-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c9100-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c9100-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c9100-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="c9100-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c9100-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c9100-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9100-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9100-124">Requirements</span></span>



| <span data-ttu-id="c9100-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9100-125">Requirement</span></span> | <span data-ttu-id="c9100-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c9100-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9100-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9100-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c9100-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9100-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c9100-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9100-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c9100-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9100-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c9100-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9100-131">Namespace</span></span><br/>                | <span data-ttu-id="c9100-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="c9100-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c9100-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c9100-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9100-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9100-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9100-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c9100-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9100-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9100-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9100-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9100-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9100-138">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="c9100-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

