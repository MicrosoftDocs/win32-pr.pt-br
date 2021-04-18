---
title: Método GetWinstationDriverNames da classe Win32_TerminalServiceSetting
description: Recupera uma lista de nomes de driver WinStation.
ms.assetid: 578c2a07-17e7-4bd6-b520-942cd48ee40f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetWinstationDriverNames
- Método GetWinstationDriverNames Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método GetWinstationDriverNames
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetWinstationDriverNames
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41bc0157f368edf129f578765c1b8d73f6f48a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105800007"
---
# <a name="getwinstationdrivernames-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="9b790-106">Método GetWinstationDriverNames da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="9b790-106">GetWinstationDriverNames method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="9b790-107">Recupera uma lista de nomes de driver WinStation.</span><span class="sxs-lookup"><span data-stu-id="9b790-107">Retrieves a list of Winstation driver names.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b790-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b790-108">Syntax</span></span>


```mof
uint32 GetWinstationDriverNames(
  [out] string WinstaDriverNames[]
);
```



## <a name="parameters"></a><span data-ttu-id="9b790-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b790-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b790-110">*WinstaDriverNames* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9b790-110">*WinstaDriverNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b790-111">A lista de nomes de driver WinStation.</span><span class="sxs-lookup"><span data-stu-id="9b790-111">The list of Winstation driver names.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b790-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b790-112">Remarks</span></span>

<span data-ttu-id="9b790-113">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="9b790-113">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="9b790-114">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="9b790-114">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="9b790-115">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="9b790-115">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="9b790-116">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="9b790-116">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="9b790-117">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9b790-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9b790-118">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9b790-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9b790-119">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="9b790-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9b790-120">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9b790-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b790-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b790-121">Requirements</span></span>



| <span data-ttu-id="9b790-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b790-122">Requirement</span></span> | <span data-ttu-id="9b790-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9b790-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b790-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b790-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9b790-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b790-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b790-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b790-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9b790-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b790-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b790-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b790-128">Namespace</span></span><br/>                | <span data-ttu-id="9b790-129">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="9b790-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9b790-130">MOF</span><span class="sxs-lookup"><span data-stu-id="9b790-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b790-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b790-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b790-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9b790-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b790-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b790-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b790-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b790-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b790-135">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="9b790-135">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

