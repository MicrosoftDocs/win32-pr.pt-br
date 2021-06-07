---
title: Redirecionador do sistema de arquivos
description: O \\ diretório windir system32 é reservado para aplicativos de 64 bits no Windows de 64 bits.
ms.assetid: b4d36fe8-8bbb-469b-8ad1-650d559a4c75
keywords:
- Programação do Windows de redirecionador de sistema de arquivos de 64 bits
- Guia de programação do Windows de 64 bits, programação do Windows de 64 bits, redirecionador do sistema de arquivos
- Programação WOW64 de 64 bits do Windows, redirecionador de sistema de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568ddde85d18f90b951051251774c3509081dfdd
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443627"
---
# <a name="file-system-redirector"></a>Redirecionador do sistema de arquivos

O diretório% windir% \\ System32 é reservado para aplicativos de 64 bits em janelas de 64 bits. A maioria dos nomes de arquivo DLL não foi alterada quando as versões de 64 bits das DLLs foram criadas, portanto, as versões de 32 bits das DLLs são armazenadas em um diretório diferente. O WOW64 oculta essa diferença usando um *redirecionador de sistema de arquivos*.

Na maioria dos casos, sempre que um aplicativo de 32 bits tenta acessar% windir% \\ System32,% windir% \\ LastGood \\ System32 ou% windir% \\regedit.exe, o acesso é redirecionado para um caminho específico da arquitetura.

> [!Note]  
> Esses caminhos são fornecidos apenas para referência. Para compatibilidade, os aplicativos não devem usar esses caminhos diretamente. Em vez disso, eles devem chamar as APIs descritas abaixo.

 



| Caminho Original                | Caminho Redirecionado para processos x86 de 32 bits | Caminho Redirecionado para processos ARM de 32 bits |
|------------------------------|------------------------------------------|------------------------------------------|
| % WINDIR% \\ System32           | % WINDIR% \\ SysWOW64                       | % WINDIR% \\ SysArm32                       |
| % WINDIR% \\ LastGood \\ System32 | % WINDIR% \\ LastGood \\ SysWOW64             | % WINDIR% \\ LastGood \\ SysArm32             |
| % WINDIR% \\regedit.exe        | % WINDIR% \\ SysWOW64 \\regedit.exe          | % WINDIR% \\ SysArm32 \\regedit.exe         |



 

Se o acesso fizer com que o sistema exiba o prompt do UAC, o redirecionamento não ocorrerá. Em vez disso, a versão de 64 bits do arquivo solicitado é iniciada. Para evitar esse problema, especifique o diretório SysWOW64 para evitar o redirecionamento e garanta o acesso à versão de 32 bits do arquivo ou execute o aplicativo de 32 bits com privilégios de administrador para que o prompt do UAC não seja exibido.

* * Não há suporte para o Windows Server 2003 e o Windows XP: * * UAC.

Determinados subdiretórios são isentos do redirecionamento. O acesso a esses subdiretórios não é redirecionado para% WINDIR% \\ SysWOW64: <dl> % WINDIR% \\ System32 \\ Catroot  
% WINDIR% \\ System32 \\ Catroot2  
% WINDIR% \\ System32 \\ DriverStore  
% WINDIR% \\ System32 \\ drivers \\ etc  
% WINDIR% \\ System32 \\ LogFiles  
% WINDIR% \\ System32 \\ spool  
</dl>

* * Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP: * *% WINDIR% \\ System32 \\ DriverStore é redirecionado.

Para recuperar o nome do diretório do sistema de 32 bits, os aplicativos de 64 bits devem usar a função [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) (Windows 10, versão 1511) ou a função [**GetSystemWow64Directory**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .

Os aplicativos devem usar a função [**SHGetKnownFolderPath**](https://www.bing.com/search?q=**SHGetKnownFolderPath**) para determinar o nome do diretório% ProgramFiles%.

**Windows Server 2003 e Windows XP:** Os aplicativos devem usar a função [**SHGetSpecialFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) para determinar o nome do diretório% ProgramFiles%.

Os aplicativos podem controlar o redirecionador do sistema de arquivos do WOW64 usando as funções [**Wow64DisableWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection), [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)e [**Wow64RevertWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection) . Desabilitar o redirecionamento do sistema de arquivos afeta todas as operações de arquivo executadas pelo thread de chamada, portanto, ele deve ser desabilitado somente quando necessário para uma única chamada [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e reabilitado imediatamente após a função retornar. Desabilitar o redirecionamento do sistema de arquivos por períodos mais longos pode impedir que aplicativos de 32 bits carreguem DLLs do sistema, fazendo com que os aplicativos falhem.

os aplicativos de 32 bits podem acessar o diretório nativo do sistema substituindo% windir% \\ SysNative para% WINDIR% \\ System32. O WOW64 reconhece SysNative como um alias especial usado para indicar que o sistema de arquivos não deve redirecionar o acesso. Esse mecanismo é flexível e fácil de usar, portanto, é o mecanismo recomendado para ignorar o redirecionamento do sistema de arquivos. Observe que os aplicativos de 64 bits não podem usar o alias SysNative, pois ele é um diretório virtual, não um real.

**Windows Server 2003 e Windows XP:** O alias SysNative foi adicionado a partir do Windows Vista.

 

 