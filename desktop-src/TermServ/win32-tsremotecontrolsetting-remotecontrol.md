---
title: Método RemoteControl da classe Win32_TSRemoteControlSetting
description: O método RemoteControl define a propriedade LevelOfControl.
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoteControl
- Método RemoteControl Serviços de Área de Trabalho Remota, classe Win32_TSRemoteControlSetting
- Classe Win32_TSRemoteControlSetting Serviços de Área de Trabalho Remota, método RemoteControl
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting.RemoteControl
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476269c2f619b7ea46bc6546f106d7ccd2a486e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295774"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a><span data-ttu-id="fac28-106">Método RemoteControl da classe Win32 \_ TSRemoteControlSetting</span><span class="sxs-lookup"><span data-stu-id="fac28-106">RemoteControl method of the Win32\_TSRemoteControlSetting class</span></span>

<span data-ttu-id="fac28-107">O método **RemoteControl** define a propriedade **LevelOfControl** .</span><span class="sxs-lookup"><span data-stu-id="fac28-107">The **RemoteControl** method sets the **LevelOfControl** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac28-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fac28-108">Syntax</span></span>


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a><span data-ttu-id="fac28-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fac28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac28-110">*LevelOfControl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fac28-110">*LevelOfControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fac28-111">Novo valor para a propriedade **LevelOfControl** , que especifica se a sessão será exibida apenas pelo usuário remoto ou exibida e controlada por meio de um teclado e mouse.</span><span class="sxs-lookup"><span data-stu-id="fac28-111">New value for the **LevelOfControl** property, which specifies whether the session will only be viewed by the remote user, or viewed and controlled through a keyboard and mouse.</span></span> <span data-ttu-id="fac28-112">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="fac28-112">For more information, see the Remarks section.</span></span> <span data-ttu-id="fac28-113">Os valores a seguir têm suporte.</span><span class="sxs-lookup"><span data-stu-id="fac28-113">The following values are supported.</span></span>

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="fac28-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Desabilitar** (0)</span><span class="sxs-lookup"><span data-stu-id="fac28-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fac28-115">O controle remoto está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="fac28-115">Remote control is disabled.</span></span>

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span data-ttu-id="fac28-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span><span class="sxs-lookup"><span data-stu-id="fac28-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fac28-117">O usuário do controle remoto tem controle total da sessão do usuário, com a permissão do usuário.</span><span class="sxs-lookup"><span data-stu-id="fac28-117">The user of remote control has full control of the user's session, with the user's permission.</span></span>

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span data-ttu-id="fac28-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span><span class="sxs-lookup"><span data-stu-id="fac28-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fac28-119">O usuário do controle remoto tem controle total da sessão do usuário; a permissão do usuário não é necessária.</span><span class="sxs-lookup"><span data-stu-id="fac28-119">The user of remote control has full control of the user's session; the user's permission is not required.</span></span>

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span data-ttu-id="fac28-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span><span class="sxs-lookup"><span data-stu-id="fac28-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fac28-121">O usuário do controle remoto pode exibir a sessão remotamente, com a permissão do usuário; o usuário remoto não pode controlar ativamente a sessão.</span><span class="sxs-lookup"><span data-stu-id="fac28-121">The user of remote control can view the session remotely, with the user's permission; the remote user cannot actively control the session.</span></span>

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span data-ttu-id="fac28-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span><span class="sxs-lookup"><span data-stu-id="fac28-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fac28-123">O usuário do controle remoto pode exibir a sessão remotamente, mas não controlar ativamente a sessão; a permissão do usuário não é necessária.</span><span class="sxs-lookup"><span data-stu-id="fac28-123">The user of remote control can view the session remotely, but not actively control the session; the user's permission is not required.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac28-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fac28-124">Return value</span></span>

<span data-ttu-id="fac28-125">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="fac28-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="fac28-126">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="fac28-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="fac28-127">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="fac28-127">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="fac28-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="fac28-128">Remarks</span></span>

<span data-ttu-id="fac28-129">O controle total de uma sessão significa que o usuário remoto pode controlar ativamente a sessão do usuário com um teclado e um mouse.</span><span class="sxs-lookup"><span data-stu-id="fac28-129">Full control of a session means that the remote user can actively control the user's session with a keyboard and mouse.</span></span>

<span data-ttu-id="fac28-130">Quando um usuário tenta estabelecer uma conexão de controle remoto, o sistema exibe uma mensagem para o cliente remoto, solicitando permissão para exibir ou participar ativamente na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="fac28-130">When a user attempts to establish a remote-control connection, the system displays a message to the remote client, requesting permission to either view or participate actively in the remote session.</span></span>

<span data-ttu-id="fac28-131">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fac28-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fac28-132">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fac28-132">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fac28-133">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="fac28-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fac28-134">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fac28-134">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fac28-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fac28-135">Requirements</span></span>



| <span data-ttu-id="fac28-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="fac28-136">Requirement</span></span> | <span data-ttu-id="fac28-137">Valor</span><span class="sxs-lookup"><span data-stu-id="fac28-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fac28-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fac28-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fac28-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fac28-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fac28-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fac28-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fac28-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fac28-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fac28-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="fac28-142">Namespace</span></span><br/>                | <span data-ttu-id="fac28-143">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="fac28-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fac28-144">MOF</span><span class="sxs-lookup"><span data-stu-id="fac28-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fac28-145"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fac28-145"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fac28-146">DLL</span><span class="sxs-lookup"><span data-stu-id="fac28-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fac28-147"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fac28-147"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac28-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="fac28-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac28-149">**\_TSRemoteControlSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="fac28-149">**Win32\_TSRemoteControlSetting**</span></span>](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

