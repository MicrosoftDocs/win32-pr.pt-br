---
title: Coletando despejos User-Mode dados
description: A partir do Windows Server 2008 e do Windows Vista com Service Pack 1 (SP1), o Relatório de Erros do Windows (WER) pode ser configurado para que os despejos completos do modo de usuário sejam coletados e armazenados localmente após uma falha de um aplicativo no modo de usuário.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4597c4bf1fd583b647e7ad74b7f1cb2cd41be9c0118226d502932c61f481cedd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442360"
---
# <a name="collecting-user-mode-dumps"></a>Coletando despejos User-Mode dados

A partir do Windows Server 2008 e do Windows Vista com Service Pack 1 (SP1), o Relatório de Erros do Windows (WER) pode ser configurado para que os despejos completos do modo de usuário sejam coletados e armazenados localmente após uma falha de um aplicativo no modo de usuário. Não há suporte para aplicativos que fazem seus próprios relatórios de falhas personalizados, incluindo aplicativos .NET.

Esse recurso não está habilitado por padrão. A habilitação do recurso requer privilégios de administrador. Para habilitar e configurar o recurso, use os seguintes valores de Registro na chave **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows Relatório de Erros do Windows \_ \\ \\ \\ \\ \\ LocalDumps.**

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
<td>O caminho em que os arquivos de despejo devem ser armazenados. Se você não usar o caminho padrão, certifique-se de que a pasta contém ACLs que permitem que o processo de falha escreva dados na pasta. Para falhas de serviço, o despejo é gravado em pastas de perfil específicas do serviço, dependendo da conta de serviço usada. Por exemplo, a pasta de perfil para serviços do sistema é %WINDIR%\System32\Config\SystemProfile. Para Serviços Locais e de Rede, a pasta é %WINDIR%\ServiceProfiles.<br/></td>
<td>Reg_expand_sz</td>
<td>%LOCALAPPDATA%\CrashDumps</td>
</tr>
<tr class="even">
<td><strong>DumpCount</strong></td>
<td>O número máximo de arquivos de despejo na pasta. Quando o valor máximo for excedido, o arquivo de despejo mais antigo na pasta será substituído pelo novo arquivo de despejo.</td>
<td>REG_DWORD</td>
<td>10</td>
</tr>
<tr class="odd">
<td><strong>DumpType</strong></td>
<td>Especifique um dos seguintes tipos de despejo:
<ul>
<li>0: Despejo personalizado</li>
<li>1: Mini despejo</li>
<li>2: Despejo completo</li>
</ul></td>
<td>REG_DWORD</td>
<td>1</td>
</tr>
<tr class="even">
<td><strong>CustomDumpFlags</strong></td>
<td>As opções de despejo personalizadas a serem usadas. Esse valor é usado somente quando <strong>DumpType</strong> é definido como 0.<br/> As opções são uma combinação bit a bit dos <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> de enumeração.<br/></td>
<td>REG_DWORD</td>
 <td><code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> Um despejo de falha não é coletado quando você configura [a depuração automática para **falhas** de aplicativo.](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes) 

Esses valores do Registro representam as configurações globais. Você também pode fornecer configurações por aplicativo que substituem as configurações globais. Para criar uma configuração por aplicativo, crie uma nova chave para seu aplicativo em **HKEY \_ LOCAL MACHINE Software Microsoft Windows Relatório de Erros do Windows \_ \\ \\ \\ \\ \\ LocalDumps** (por exemplo, **HKEY LOCAL MACHINE Software \_ Microsoft Windows Relatório de Erros do Windows \_ \\ \\ \\ \\ \\ LocalDumps \\MyApplication.exe**). Adicione as configurações de despejo sob a **MyApplication.exe** chave. Se o aplicativo falhar, o WER lerá primeiro as configurações globais e, em seguida, substituirá qualquer uma das configurações com as configurações específicas do aplicativo.

Depois que um aplicativo falhar e antes de seu encerramento, o sistema verificará as configurações do Registro para determinar se um despejo local deve ser coletado. Depois que a coleta de despejo tiver sido concluída, o aplicativo terá permissão para terminar normalmente. Se o aplicativo dá suporte à recuperação, o despejo local é coletado antes que o retorno de chamada de recuperação seja chamado.

Esses despejos são configurados e controlados independentemente do restante da infraestrutura wer. Você pode usar a coleção de despejo local mesmo se o WER estiver desabilitado ou se o usuário cancelar o relatório wer. O despejo local pode ser diferente do despejo enviado à Microsoft.

 

