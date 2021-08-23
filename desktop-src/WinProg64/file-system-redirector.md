---
title: Redirecionador do sistema de arquivos
description: O diretório windir System32 é reservado para aplicativos \\ de 64 bits em 64 bits Windows.
ms.assetid: b4d36fe8-8bbb-469b-8ad1-650d559a4c75
keywords:
- programação do Windows de 64 bits do sistema de arquivos
- Guia de programação Windows de 64 bits Windows de 64 bits, redirecionador do sistema de arquivos
- Wow64 64 bits Windows programação , redirecionador do sistema de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318a04d85309ca6c97c87ae2d6a580a85f1a4ee224e162a008034e731a1ff557
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569966"
---
# <a name="file-system-redirector"></a>Redirecionador do sistema de arquivos

O diretório %windir% System32 é reservado para aplicativos \\ de 64 bits em Windows. A maioria dos nomes de arquivo DLL não foi alterada quando versões de 64 bits das DLLs foram criadas, portanto, as versões de 32 bits das DLLs são armazenadas em um diretório diferente. O WOW64 oculta essa diferença usando um *redirecionador do sistema de arquivos*.

Na maioria dos casos, sempre que um aplicativo de 32 bits tenta acessar %windir% \\ System32, %windir% \\ last last \\ ltda system32 ou %windir%regedit.exe, o acesso é redirecionado para um caminho específico da \\ arquitetura.

> [!Note]  
> Esses caminhos são fornecidos apenas para referência. Para compatibilidade, os aplicativos não devem usar esses caminhos diretamente. Em vez disso, eles devem chamar as APIs descritas abaixo.

 



| Caminho Original                | Caminho redirecionado para processos x86 de 32 bits | Caminho redirecionado para processos arm de 32 bits |
|------------------------------|------------------------------------------|------------------------------------------|
| %windir% \\ System32           | %windir% \\ SysWOW64                       | %windir% \\ SysArm32                       |
| %windir% \\ last o \\ sistema32 | %windir% \\ lastow \\ SysWOW64             | %windir% \\ last últimos \\ SysArm32             |
| %windir% \\regedit.exe        | %windir% \\ SysWOW64 \\regedit.exe          | %windir% \\ SysArm32 \\regedit.exe         |



 

Se o acesso fizer o sistema exibir o prompt do UAC, o redirecionamento não ocorrerá. Em vez disso, a versão de 64 bits do arquivo solicitado é lançada. Para evitar esse problema, especifique o diretório SysWOW64 para evitar o redirecionamento e garantir o acesso à versão de 32 bits do arquivo ou execute o aplicativo de 32 bits com privilégios de administrador para que o prompt do UAC não seja exibido.

**Windows Server 2003 e Windows XP: ** Não há suporte para UAC.

Determinados subdireários são isentos do redirecionamento. O acesso a esses subdireários não é redirecionado para %windir% \\ SysWOW64: <dl> %windir% \\ system32 \\ catroot  
%windir% \\ system32 \\ catroot2  
%windir% \\ system32 \\ driverstore  
%windir% \\ drivers system32 \\ \\ etc  
%windir% \\ system32 \\ logfiles  
%windir% \\ spool system32 \\  
</dl>

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP: **%windir% \\ system32 driverstore é \\ redirecionado.

Para recuperar o nome do diretório do sistema de 32 bits, os aplicativos de 64 bits devem usar a função [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) (Windows 10, versão 1511) ou a [**função GetSystemWow64Directory.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)

Os aplicativos devem usar [**a função SHGetKnownFolderPath**](https://www.bing.com/search?q=**SHGetKnownFolderPath**) para determinar o nome do diretório %ProgramFiles%.

**Windows Server 2003 e Windows XP:** Os aplicativos devem usar [**a função SHGetSpecialFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) para determinar o nome do diretório %ProgramFiles%.

Os aplicativos podem controlar o redirecionador do sistema de arquivos WOW64 usando as funções [**Wow64DisableWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection), [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)e [**Wow64RevertWow64FsRedirection.**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection) Desabilitar o redirecionamento do sistema de arquivos afeta todas as operações de arquivo executadas pelo thread de chamada, portanto, ele deve ser desabilitado somente quando necessário para uma única chamada [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e reabilitar novamente imediatamente após o retorno da função. Desabilitar o redirecionamento do sistema de arquivos por períodos mais longos pode impedir que aplicativos de 32 bits carregam DLLs do sistema, fazendo com que os aplicativos falhem.

Aplicativos de 32 bits podem acessar o diretório do sistema nativo substituindo %windir% \\ Sysnative por %windir% \\ System32. O WOW64 reconhece o Sysnative como um alias especial usado para indicar que o sistema de arquivos não deve redirecionar o acesso. Esse mecanismo é flexível e fácil de usar, portanto, é o mecanismo recomendado para ignorar o redirecionamento do sistema de arquivos. Observe que os aplicativos de 64 bits não podem usar o alias Sysnative, pois é um diretório virtual que não é real.

**Windows Server 2003 e Windows XP:** O alias Sysnative foi adicionado a partir do Windows Vista.

 

 