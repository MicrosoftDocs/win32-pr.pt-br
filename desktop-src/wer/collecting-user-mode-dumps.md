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
# <a name="collecting-user-mode-dumps"></a>Coletando despejos de User-Mode

A partir do Windows Server 2008 e do Windows Vista com Service Pack 1 (SP1), o Relatório de Erros do Windows (WER) pode ser configurado para que os despejos completos do modo de usuário sejam coletados e armazenados localmente após a falha de um aplicativo de modo de usuário. Os aplicativos que fazem seu próprio relatório de falhas personalizado, incluindo aplicativos .NET, não têm suporte nesse recurso.

Esse recurso não está habilitado por padrão. Habilitar o recurso requer privilégios de administrador. Para habilitar e configurar o recurso, use os seguintes valores de registro em **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ relatório de erros do Windows \\ LocalDumps** Key.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
<th>Type</th>
<th>Valor padrão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>DumpFolder</strong></td>
<td>O caminho onde os arquivos de despejo devem ser armazenados. Se você não usar o caminho padrão, certifique-se de que a pasta contém ACLs que permitem que o processo de falha grave dados na pasta. Para falhas de serviço, o despejo é gravado em pastas de perfil específicas de serviço, dependendo da conta de serviço usada. Por exemplo, a pasta de perfil para serviços do sistema é%WINDIR%\System32\Config\SystemProfile. Para serviços de rede e locais, a pasta é%WINDIR%\ServiceProfiles.<br/></td>
<td>REG_EXPAND_SZ</td>
<td>%LOCALAPPDATA%\CrashDumps</td>
</tr>
<tr class="even">
<td><strong>DumpCount</strong></td>
<td>O número máximo de arquivos de despejo na pasta. Quando o valor máximo for excedido, o arquivo de despejo mais antigo na pasta será substituído pelo novo arquivo de despejo.</td>
<td>REG_DWORD</td>
<td>10</td>
</tr>
<tr class="odd">
<td><strong>Dumptype</strong></td>
<td>Especifique um dos seguintes tipos de despejo:
<ul>
<li>0: despejo personalizado</li>
<li>1: mini Dump</li>
<li>2: despejo completo</li>
</ul></td>
<td>REG_DWORD</td>
<td>1</td>
</tr>
<tr class="even">
<td><strong>CustomDumpFlags</strong></td>
<td>As opções de despejo personalizado a serem usadas. Esse valor é usado somente quando <strong>dumptype</strong> é definido como 0.<br/> As opções são uma combinação de bits de bit de <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> valores de enumeração.<br/></td>
<td>REG_DWORD</td>
<td><code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData.</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> Um despejo de memória não é coletado quando você define a [depuração automática para falhas do **aplicativo**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes). 

Esses valores de registro representam as configurações globais. Você também pode fornecer configurações por aplicativo que substituem as configurações globais. Para criar uma configuração por aplicativo, crie uma nova chave para seu aplicativo em **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ relatório de erros do Windows \\ LocalDumps** (por exemplo, **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ relatório de erros do Windows \\ LocalDumps \\MyApplication.exe**). Adicione as configurações de despejo na chave de **MyApplication.exe** . Se o aplicativo falhar, o WER lerá primeiro as configurações globais e substituirá as configurações pelas configurações específicas do aplicativo.

Depois que um aplicativo falha e antes do encerramento, o sistema verificará as configurações do registro para determinar se um despejo local deve ser coletado. Após a conclusão da coleta de despejo, o aplicativo terá permissão para ser encerrado normalmente. Se o aplicativo der suporte à recuperação, o despejo local será coletado antes que o retorno de chamada de recuperação seja chamado.

Esses despejos são configurados e controlados independentemente do restante da infraestrutura do WER. Você pode fazer uso da coleção de despejo local mesmo se o WER estiver desabilitado ou se o usuário cancelar o relatório WER. O despejo local pode ser diferente do despejo enviado à Microsoft.

 

