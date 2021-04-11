---
title: Método GetGracePeriodDays da classe Win32_TerminalServiceSetting
description: Recupera o número de dias restantes no período de carência de licenciamento Serviços de Área de Trabalho Remota para um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Um valor zero indica que o período de carência está acima.
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetGracePeriodDays
- Método GetGracePeriodDays Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método GetGracePeriodDays
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetGracePeriodDays
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0faaf525bb74a8ac4b0164c181e5a20cfb215d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294779"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="dc2e9-107">Método GetGracePeriodDays da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="dc2e9-107">GetGracePeriodDays method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="dc2e9-108">Recupera o número de dias restantes no período de carência de licenciamento Serviços de Área de Trabalho Remota para um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="dc2e9-108">Retrieves the number of days that are remaining in the Remote Desktop Services licensing grace period for a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="dc2e9-109">Um valor zero indica que o período de carência está acima.</span><span class="sxs-lookup"><span data-stu-id="dc2e9-109">A zero value indicates that the grace period is over.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc2e9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc2e9-110">Syntax</span></span>


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a><span data-ttu-id="dc2e9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc2e9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc2e9-112">*DaysLeft* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dc2e9-112">*DaysLeft* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc2e9-113">O número de dias restantes no período de carência.</span><span class="sxs-lookup"><span data-stu-id="dc2e9-113">The number of days that are remaining in the grace period.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc2e9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc2e9-114">Remarks</span></span>

<span data-ttu-id="dc2e9-115">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="dc2e9-115">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="dc2e9-116">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="dc2e9-116">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="dc2e9-117">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="dc2e9-117">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="dc2e9-118">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="dc2e9-118">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="dc2e9-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="dc2e9-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dc2e9-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="dc2e9-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="dc2e9-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="dc2e9-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dc2e9-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="dc2e9-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc2e9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc2e9-123">Requirements</span></span>



| <span data-ttu-id="dc2e9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc2e9-124">Requirement</span></span> | <span data-ttu-id="dc2e9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="dc2e9-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2e9-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc2e9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dc2e9-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc2e9-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc2e9-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc2e9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dc2e9-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc2e9-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc2e9-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc2e9-130">Namespace</span></span><br/>                | <span data-ttu-id="dc2e9-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="dc2e9-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="dc2e9-132">MOF</span><span class="sxs-lookup"><span data-stu-id="dc2e9-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc2e9-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc2e9-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc2e9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="dc2e9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc2e9-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc2e9-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc2e9-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc2e9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc2e9-137">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="dc2e9-137">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

