---
title: Coletando despejos de User-Mode
description: A partir do Windows Server 2008 e do Windows Vista com Service Pack 1 (SP1), o Relatório de Erros do Windows (WER) pode ser configurado para que os despejos completos do modo de usuário sejam coletados e armazenados localmente após a falha de um aplicativo de modo de usuário.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7b1e7850e84d9fa6c8d10953d23640b41b1bc6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823673"
---
# <a name="collecting-user-mode-dumps"></a><span data-ttu-id="7e9ec-103">Coletando despejos de User-Mode</span><span class="sxs-lookup"><span data-stu-id="7e9ec-103">Collecting User-Mode Dumps</span></span>

<span data-ttu-id="7e9ec-104">A partir do Windows Server 2008 e do Windows Vista com Service Pack 1 (SP1), o Relatório de Erros do Windows (WER) pode ser configurado para que os despejos completos do modo de usuário sejam coletados e armazenados localmente após a falha de um aplicativo de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-104">Starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1), Windows Error Reporting (WER) can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes.</span></span> <span data-ttu-id="7e9ec-105">Os aplicativos que fazem seu próprio relatório de falhas personalizado, incluindo aplicativos .NET, não têm suporte nesse recurso.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-105">Applications that do their own custom crash reporting, including .NET applications, are not supported by this feature.</span></span>

<span data-ttu-id="7e9ec-106">Esse recurso não está habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-106">This feature is not enabled by default.</span></span> <span data-ttu-id="7e9ec-107">Habilitar o recurso requer privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-107">Enabling the feature requires administrator privileges.</span></span> <span data-ttu-id="7e9ec-108">Para habilitar e configurar o recurso, use os seguintes valores de registro em **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ relatório de erros do Windows \\ LocalDumps** Key.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-108">To enable and configure the feature, use the following registry values under the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** key.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e9ec-109">Valor</span><span class="sxs-lookup"><span data-stu-id="7e9ec-109">Value</span></span></th>
<th><span data-ttu-id="7e9ec-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e9ec-110">Description</span></span></th>
<th><span data-ttu-id="7e9ec-111">Type</span><span class="sxs-lookup"><span data-stu-id="7e9ec-111">Type</span></span></th>
<th><span data-ttu-id="7e9ec-112">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="7e9ec-112">Default value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e9ec-113"><strong>DumpFolder</strong></span><span class="sxs-lookup"><span data-stu-id="7e9ec-113"><strong>DumpFolder</strong></span></span></td>
<td><span data-ttu-id="7e9ec-114">O caminho onde os arquivos de despejo devem ser armazenados.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-114">The path where the dump files are to be stored.</span></span> <span data-ttu-id="7e9ec-115">Se você não usar o caminho padrão, certifique-se de que a pasta contém ACLs que permitem que o processo de falha grave dados na pasta.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-115">If you do not use the default path, then make sure that the folder contains ACLs that allow the crashing process to write data to the folder.</span></span> <span data-ttu-id="7e9ec-116">Para falhas de serviço, o despejo é gravado em pastas de perfil específicas de serviço, dependendo da conta de serviço usada.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-116">For service crashes, the dump is written to service specific profile folders depending on the service account used.</span></span> <span data-ttu-id="7e9ec-117">Por exemplo, a pasta de perfil para serviços do sistema é%WINDIR%\System32\Config\SystemProfile.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-117">For example, the profile folder for System services is %WINDIR%\System32\Config\SystemProfile.</span></span> <span data-ttu-id="7e9ec-118">Para serviços de rede e locais, a pasta é%WINDIR%\ServiceProfiles.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-118">For Network and Local Services, the folder is %WINDIR%\ServiceProfiles.</span></span><br/></td>
<td><span data-ttu-id="7e9ec-119">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="7e9ec-119">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="7e9ec-120">%LOCALAPPDATA%\CrashDumps</span><span class="sxs-lookup"><span data-stu-id="7e9ec-120">%LOCALAPPDATA%\CrashDumps</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e9ec-121"><strong>DumpCount</strong></span><span class="sxs-lookup"><span data-stu-id="7e9ec-121"><strong>DumpCount</strong></span></span></td>
<td><span data-ttu-id="7e9ec-122">O número máximo de arquivos de despejo na pasta.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-122">The maximum number of dump files in the folder.</span></span> <span data-ttu-id="7e9ec-123">Quando o valor máximo for excedido, o arquivo de despejo mais antigo na pasta será substituído pelo novo arquivo de despejo.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-123">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span></td>
<td><span data-ttu-id="7e9ec-124">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7e9ec-124">REG_DWORD</span></span></td>
<td><span data-ttu-id="7e9ec-125">10</span><span class="sxs-lookup"><span data-stu-id="7e9ec-125">10</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e9ec-126"><strong>Dumptype</strong></span><span class="sxs-lookup"><span data-stu-id="7e9ec-126"><strong>DumpType</strong></span></span></td>
<td><span data-ttu-id="7e9ec-127">Especifique um dos seguintes tipos de despejo:</span><span class="sxs-lookup"><span data-stu-id="7e9ec-127">Specify one of the following dump types:</span></span>
<ul>
<li><span data-ttu-id="7e9ec-128">0: despejo personalizado</span><span class="sxs-lookup"><span data-stu-id="7e9ec-128">0: Custom dump</span></span></li>
<li><span data-ttu-id="7e9ec-129">1: mini Dump</span><span class="sxs-lookup"><span data-stu-id="7e9ec-129">1: Mini dump</span></span></li>
<li><span data-ttu-id="7e9ec-130">2: despejo completo</span><span class="sxs-lookup"><span data-stu-id="7e9ec-130">2: Full dump</span></span></li>
</ul></td>
<td><span data-ttu-id="7e9ec-131">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7e9ec-131">REG_DWORD</span></span></td>
<td><span data-ttu-id="7e9ec-132">1</span><span class="sxs-lookup"><span data-stu-id="7e9ec-132">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e9ec-133"><strong>CustomDumpFlags</strong></span><span class="sxs-lookup"><span data-stu-id="7e9ec-133"><strong>CustomDumpFlags</strong></span></span></td>
<td><span data-ttu-id="7e9ec-134">As opções de despejo personalizado a serem usadas.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-134">The custom dump options to be used.</span></span> <span data-ttu-id="7e9ec-135">Esse valor é usado somente quando <strong>dumptype</strong> é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-135">This value is used only when <strong>DumpType</strong> is set to 0.</span></span><br/> <span data-ttu-id="7e9ec-136">As opções são uma combinação de bits de bit de <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-136">The options are a bitwise combination of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeration values.</span></span><br/></td>
<td><span data-ttu-id="7e9ec-137">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7e9ec-137">REG_DWORD</span></span></td>
<td><code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData.</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> <span data-ttu-id="7e9ec-138">Um despejo de memória não é coletado quando você define a [depuração automática para falhas do **aplicativo**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span><span class="sxs-lookup"><span data-stu-id="7e9ec-138">A crash dump is not collected when you set [automatic debugging for **application** crashes](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span></span> 

<span data-ttu-id="7e9ec-139">Esses valores de registro representam as configurações globais.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-139">These registry values represent the global settings.</span></span> <span data-ttu-id="7e9ec-140">Você também pode fornecer configurações por aplicativo que substituem as configurações globais.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-140">You can also provide per-application settings that override the global settings.</span></span> <span data-ttu-id="7e9ec-141">Para criar uma configuração por aplicativo, crie uma nova chave para seu aplicativo em **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ relatório de erros do Windows \\ LocalDumps** (por exemplo, **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ relatório de erros do Windows \\ LocalDumps \\MyApplication.exe**).</span><span class="sxs-lookup"><span data-stu-id="7e9ec-141">To create a per-application setting, create a new key for your application under **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** (for example, **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps\\MyApplication.exe**).</span></span> <span data-ttu-id="7e9ec-142">Adicione as configurações de despejo na chave de **MyApplication.exe** .</span><span class="sxs-lookup"><span data-stu-id="7e9ec-142">Add your dump settings under the **MyApplication.exe** key.</span></span> <span data-ttu-id="7e9ec-143">Se o aplicativo falhar, o WER lerá primeiro as configurações globais e substituirá as configurações pelas configurações específicas do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-143">If your application crashes, WER will first read the global settings, and then will override any of the settings with your application-specific settings.</span></span>

<span data-ttu-id="7e9ec-144">Depois que um aplicativo falha e antes do encerramento, o sistema verificará as configurações do registro para determinar se um despejo local deve ser coletado.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-144">After an application crashes and prior to its termination, the system will check the registry settings to determine whether a local dump is to be collected.</span></span> <span data-ttu-id="7e9ec-145">Após a conclusão da coleta de despejo, o aplicativo terá permissão para ser encerrado normalmente.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-145">After the dump collection has completed, the application will be allowed to terminate normally.</span></span> <span data-ttu-id="7e9ec-146">Se o aplicativo der suporte à recuperação, o despejo local será coletado antes que o retorno de chamada de recuperação seja chamado.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-146">If the application supports recovery, the local dump is collected before the recovery callback is called.</span></span>

<span data-ttu-id="7e9ec-147">Esses despejos são configurados e controlados independentemente do restante da infraestrutura do WER.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-147">These dumps are configured and controlled independently of the rest of the WER infrastructure.</span></span> <span data-ttu-id="7e9ec-148">Você pode fazer uso da coleção de despejo local mesmo se o WER estiver desabilitado ou se o usuário cancelar o relatório WER.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-148">You can make use of the local dump collection even if WER is disabled or if the user cancels WER reporting.</span></span> <span data-ttu-id="7e9ec-149">O despejo local pode ser diferente do despejo enviado à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7e9ec-149">The local dump can be different than the dump sent to Microsoft.</span></span>

 

