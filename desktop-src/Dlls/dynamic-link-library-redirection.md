---
description: Os aplicativos podem depender de uma versão específica de uma DLL compartilhada e começar a falhar se outro aplicativo for instalado com uma versão mais recente ou mais antiga da mesma DLL.
ms.assetid: 3b426b6c-1ad5-43b9-81ea-5e6d3c6588c8
title: Redirecionamento de biblioteca de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b575d566231058cca13c10a067a3c2e20078073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758042"
---
# <a name="dynamic-link-library-redirection"></a>Redirecionamento de biblioteca de Dynamic-Link

Os aplicativos podem depender de uma versão específica de uma DLL compartilhada e começar a falhar se outro aplicativo for instalado com uma versão mais recente ou mais antiga da mesma DLL. Há duas maneiras de garantir que seu aplicativo use o redirecionamento correto de dll: DLL e componentes lado a lado. Os desenvolvedores e administradores devem usar o redirecionamento de DLL para aplicativos existentes, pois não exigem nenhuma alteração no aplicativo. Se você estiver criando um novo aplicativo ou atualizando um aplicativo e quiser isolar o aplicativo de problemas potenciais, crie um [componente lado a lado](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

Para habilitar a máquina de redirecionamento de DLL, você deve criar uma nova chave do registro. Crie uma nova chave DWORD chamada **DevOverrideEnable** em **HKLM\Software\Microsoft\Windows NT\CurrentVersion\Image opções de execução de arquivo** e defina-a como 1. Depois disso, você deve reiniciar o computador para ver os efeitos.

Para usar o redirecionamento de DLL, crie um *arquivo de redirecionamento* para seu aplicativo. O arquivo de redirecionamento deve ser nomeado da seguinte maneira: *\_ nome do aplicativo*. local. Por exemplo, se o nome do aplicativo for Editor.exe, o arquivo de redirecionamento deverá ser nomeado Editor.exe. local. Você deve instalar o arquivo. local no diretório do aplicativo. Você também deve instalar as DLLs no diretório do aplicativo.

O conteúdo de um arquivo de redirecionamento é ignorado, mas sua presença faz com que o Windows Verifique o diretório do aplicativo primeiro sempre que ele carrega uma DLL, independentemente do caminho especificado para [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). Se a DLL não for encontrada no diretório do aplicativo, essas funções usarão sua ordem de pesquisa usual. Por exemplo, se o aplicativo c: \\ myapp \\myapp.exe chamar **LoadLibrary** usando o seguinte caminho:

c: \\ arquivos de programa arquivos \\ comuns do \\ sistema \\mydll.dll

E, se a unidade c: \\ myapp \\myapp.exe. local e c: \\ MyApp \\mydll.dll existir, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) carregará c: \\ MyApp \\mydll.dll. Caso contrário, **LoadLibrary** carrega c: \\ arquivos de programa \\ Arquivos comuns \\mydll.dll do sistema \\ .

Como alternativa, se um diretório chamado c: \\ myapp \\myapp.exe. local existir e contiver mydll.dll, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) carregará c: \\ MyApp \\myapp.exe. local \\mydll.dll.

Se o aplicativo tiver um manifesto, todos os arquivos. local serão ignorados.

Se você estiver usando o redirecionamento de DLL e o aplicativo não tiver acesso a todas as unidades e diretórios na ordem de pesquisa, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) interromperá a pesquisa assim que o acesso for negado. (Se você não estiver usando o redirecionamento de DLL, **LoadLibrary** ignora os diretórios que ele não pode acessar e, em seguida, continua pesquisando.)

É uma boa prática instalar DLLs de aplicativo no mesmo diretório que contém o aplicativo, mesmo que você não esteja usando o redirecionamento de DLL. Isso garante que a instalação do aplicativo não substitui outras cópias da DLL e faz com que outros aplicativos falhem. Além disso, se você seguir essa boa prática, outros aplicativos não substituirão sua cópia da DLL e farão com que seu aplicativo falhe.

 

 
