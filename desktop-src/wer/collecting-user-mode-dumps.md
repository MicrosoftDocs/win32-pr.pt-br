---
title: Coletando despejos de User-Mode
description: a partir do Windows Server 2008 e Windows Vista com Service Pack 1 (SP1), Relatório de Erros do Windows (WER) podem ser configurados para que os despejos completos do modo de usuário sejam coletados e armazenados localmente após a falha de um aplicativo de modo de usuário.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6291d3ad8dfeb641582a93f6789ca7844594ad
ms.sourcegitcommit: 892997f4126d44df413286074e08a9c6065313ec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2021
ms.locfileid: "114300181"
---
# <a name="collecting-user-mode-dumps"></a><span data-ttu-id="20d75-103">Coletando despejos de User-Mode</span><span class="sxs-lookup"><span data-stu-id="20d75-103">Collecting User-Mode Dumps</span></span>

<span data-ttu-id="20d75-104">a partir do Windows Server 2008 e Windows Vista com Service Pack 1 (SP1), Relatório de Erros do Windows (WER) podem ser configurados para que os despejos completos do modo de usuário sejam coletados e armazenados localmente após a falha de um aplicativo de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="20d75-104">Starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1), Windows Error Reporting (WER) can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes.</span></span> <span data-ttu-id="20d75-105">Os aplicativos que fazem seu próprio relatório de falhas personalizado, incluindo aplicativos .NET, não têm suporte nesse recurso.</span><span class="sxs-lookup"><span data-stu-id="20d75-105">Applications that do their own custom crash reporting, including .NET applications, are not supported by this feature.</span></span>

<span data-ttu-id="20d75-106">Esse recurso não está habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="20d75-106">This feature is not enabled by default.</span></span> <span data-ttu-id="20d75-107">Habilitar o recurso requer privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="20d75-107">Enabling the feature requires administrator privileges.</span></span> <span data-ttu-id="20d75-108">para habilitar e configurar o recurso, use os seguintes valores de registro em **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows \\ Relatório de Erros do Windows chave \\ LocalDumps** .</span><span class="sxs-lookup"><span data-stu-id="20d75-108">To enable and configure the feature, use the following registry values under the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** key.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20d75-109">Valor</span><span class="sxs-lookup"><span data-stu-id="20d75-109">Value</span></span></th>
<th><span data-ttu-id="20d75-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="20d75-110">Description</span></span></th>
<th><span data-ttu-id="20d75-111">Type</span><span class="sxs-lookup"><span data-stu-id="20d75-111">Type</span></span></th>
<th><span data-ttu-id="20d75-112">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="20d75-112">Default value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20d75-113"><strong>DumpFolder</strong></span><span class="sxs-lookup"><span data-stu-id="20d75-113"><strong>DumpFolder</strong></span></span></td>
<td><span data-ttu-id="20d75-114">O caminho onde os arquivos de despejo devem ser armazenados.</span><span class="sxs-lookup"><span data-stu-id="20d75-114">The path where the dump files are to be stored.</span></span> <span data-ttu-id="20d75-115">Se você não usar o caminho padrão, certifique-se de que a pasta contém ACLs que permitem que o processo de falha grave dados na pasta.</span><span class="sxs-lookup"><span data-stu-id="20d75-115">If you do not use the default path, then make sure that the folder contains ACLs that allow the crashing process to write data to the folder.</span></span> <span data-ttu-id="20d75-116">Para falhas de serviço, o despejo é gravado em pastas de perfil específicas de serviço, dependendo da conta de serviço usada.</span><span class="sxs-lookup"><span data-stu-id="20d75-116">For service crashes, the dump is written to service specific profile folders depending on the service account used.</span></span> <span data-ttu-id="20d75-117">Por exemplo, a pasta de perfil para serviços do sistema é%WINDIR%\System32\Config\SystemProfile.</span><span class="sxs-lookup"><span data-stu-id="20d75-117">For example, the profile folder for System services is %WINDIR%\System32\Config\SystemProfile.</span></span> <span data-ttu-id="20d75-118">Para serviços de rede e locais, a pasta é%WINDIR%\ServiceProfiles.</span><span class="sxs-lookup"><span data-stu-id="20d75-118">For Network and Local Services, the folder is %WINDIR%\ServiceProfiles.</span></span><br/></td>
<td><span data-ttu-id="20d75-119">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="20d75-119">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="20d75-120">%LOCALAPPDATA%\CrashDumps</span><span class="sxs-lookup"><span data-stu-id="20d75-120">%LOCALAPPDATA%\CrashDumps</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20d75-121"><strong>DumpCount</strong></span><span class="sxs-lookup"><span data-stu-id="20d75-121"><strong>DumpCount</strong></span></span></td>
<td><span data-ttu-id="20d75-122">O número máximo de arquivos de despejo na pasta.</span><span class="sxs-lookup"><span data-stu-id="20d75-122">The maximum number of dump files in the folder.</span></span> <span data-ttu-id="20d75-123">Quando o valor máximo for excedido, o arquivo de despejo mais antigo na pasta será substituído pelo novo arquivo de despejo.</span><span class="sxs-lookup"><span data-stu-id="20d75-123">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span></td>
<td><span data-ttu-id="20d75-124">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="20d75-124">REG_DWORD</span></span></td>
<td><span data-ttu-id="20d75-125">10</span><span class="sxs-lookup"><span data-stu-id="20d75-125">10</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20d75-126"><strong>Dumptype</strong></span><span class="sxs-lookup"><span data-stu-id="20d75-126"><strong>DumpType</strong></span></span></td>
<td><span data-ttu-id="20d75-127">Especifique um dos seguintes tipos de despejo:</span><span class="sxs-lookup"><span data-stu-id="20d75-127">Specify one of the following dump types:</span></span>
<ul>
<li><span data-ttu-id="20d75-128">0: despejo personalizado</span><span class="sxs-lookup"><span data-stu-id="20d75-128">0: Custom dump</span></span></li>
<li><span data-ttu-id="20d75-129">1: mini Dump</span><span class="sxs-lookup"><span data-stu-id="20d75-129">1: Mini dump</span></span></li>
<li><span data-ttu-id="20d75-130">2: despejo completo</span><span class="sxs-lookup"><span data-stu-id="20d75-130">2: Full dump</span></span></li>
</ul></td>
<td><span data-ttu-id="20d75-131">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="20d75-131">REG_DWORD</span></span></td>
<td><span data-ttu-id="20d75-132">1</span><span class="sxs-lookup"><span data-stu-id="20d75-132">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20d75-133"><strong>CustomDumpFlags</strong></span><span class="sxs-lookup"><span data-stu-id="20d75-133"><strong>CustomDumpFlags</strong></span></span></td>
<td><span data-ttu-id="20d75-134">As opções de despejo personalizado a serem usadas.</span><span class="sxs-lookup"><span data-stu-id="20d75-134">The custom dump options to be used.</span></span> <span data-ttu-id="20d75-135">Esse valor é usado somente quando <strong>dumptype</strong> é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="20d75-135">This value is used only when <strong>DumpType</strong> is set to 0.</span></span><br/> <span data-ttu-id="20d75-136">As opções são uma combinação de bits de bit de <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="20d75-136">The options are a bitwise combination of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeration values.</span></span><br/></td>
<td><span data-ttu-id="20d75-137">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="20d75-137">REG_DWORD</span></span></td>
 <td><span data-ttu-id="20d75-138"><code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code></span><span class="sxs-lookup"><span data-stu-id="20d75-138"><code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code></span></span></td>
</tr>
</tbody>
</table>

>[!NOTE]
> <span data-ttu-id="20d75-139">Um despejo de memória não é coletado quando você define a [depuração automática para falhas do **aplicativo**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span><span class="sxs-lookup"><span data-stu-id="20d75-139">A crash dump is not collected when you set [automatic debugging for **application** crashes](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span></span> 

<span data-ttu-id="20d75-140">Esses valores de registro representam as configurações globais.</span><span class="sxs-lookup"><span data-stu-id="20d75-140">These registry values represent the global settings.</span></span> <span data-ttu-id="20d75-141">Você também pode fornecer configurações por aplicativo que substituem as configurações globais.</span><span class="sxs-lookup"><span data-stu-id="20d75-141">You can also provide per-application settings that override the global settings.</span></span> <span data-ttu-id="20d75-142">para criar uma configuração por aplicativo, crie uma nova chave para seu aplicativo em **hkey \_ local \_ machine \\ software \\ microsoft \\ Windows \\ Relatório de Erros do Windows \\ LocalDumps** (por exemplo, **hkey \_ local \_ machine \\ software \\ microsoft \\ Windows \\ Relatório de Erros do Windows \\ LocalDumps \\MyApplication.exe**).</span><span class="sxs-lookup"><span data-stu-id="20d75-142">To create a per-application setting, create a new key for your application under **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** (for example, **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps\\MyApplication.exe**).</span></span> <span data-ttu-id="20d75-143">Adicione as configurações de despejo na chave de **MyApplication.exe** .</span><span class="sxs-lookup"><span data-stu-id="20d75-143">Add your dump settings under the **MyApplication.exe** key.</span></span> <span data-ttu-id="20d75-144">Se o aplicativo falhar, o WER lerá primeiro as configurações globais e substituirá as configurações pelas configurações específicas do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="20d75-144">If your application crashes, WER will first read the global settings, and then will override any of the settings with your application-specific settings.</span></span>

<span data-ttu-id="20d75-145">Depois que um aplicativo falha e antes do encerramento, o sistema verificará as configurações do registro para determinar se um despejo local deve ser coletado.</span><span class="sxs-lookup"><span data-stu-id="20d75-145">After an application crashes and prior to its termination, the system will check the registry settings to determine whether a local dump is to be collected.</span></span> <span data-ttu-id="20d75-146">Após a conclusão da coleta de despejo, o aplicativo terá permissão para ser encerrado normalmente.</span><span class="sxs-lookup"><span data-stu-id="20d75-146">After the dump collection has completed, the application will be allowed to terminate normally.</span></span> <span data-ttu-id="20d75-147">Se o aplicativo der suporte à recuperação, o despejo local será coletado antes que o retorno de chamada de recuperação seja chamado.</span><span class="sxs-lookup"><span data-stu-id="20d75-147">If the application supports recovery, the local dump is collected before the recovery callback is called.</span></span>

<span data-ttu-id="20d75-148">Esses despejos são configurados e controlados independentemente do restante da infraestrutura do WER.</span><span class="sxs-lookup"><span data-stu-id="20d75-148">These dumps are configured and controlled independently of the rest of the WER infrastructure.</span></span> <span data-ttu-id="20d75-149">Você pode fazer uso da coleção de despejo local mesmo se o WER estiver desabilitado ou se o usuário cancelar o relatório WER.</span><span class="sxs-lookup"><span data-stu-id="20d75-149">You can make use of the local dump collection even if WER is disabled or if the user cancels WER reporting.</span></span> <span data-ttu-id="20d75-150">O despejo local pode ser diferente do despejo enviado à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20d75-150">The local dump can be different than the dump sent to Microsoft.</span></span>

 

