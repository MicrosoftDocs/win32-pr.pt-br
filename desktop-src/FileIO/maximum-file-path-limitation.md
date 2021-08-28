---
description: Limitação de comprimento máximo do caminho.
title: Limitação Máxima do Comprimento do Caminho
ms.topic: article
ms.custom: contperf-fy21q1
ms.date: 09/15/2020
ms.openlocfilehash: f57aba8d022e3b193289c8abf884e661797a0cf8585b7537fae19c171250eb12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914756"
---
# <a name="maximum-path-length-limitation"></a>Limitação Máxima do Comprimento do Caminho

Na API Windows (com algumas exceções discutidas nos parágrafos a seguir), o comprimento máximo de um caminho é **MAX \_ PATH,** que é definido como 260 caracteres. Um caminho local é estruturado na seguinte ordem: letra da unidade, dois-pontos, invertida, componentes de nome separados por malhas invertida e um caractere nulo de terminação. Por exemplo, o caminho máximo na unidade D é "D: alguns NUL de cadeia de caracteres de caminho de \\ *256* caracteres" em que " NUL " representa o caractere nulo de terminação invisível para a página de código do sistema &lt; &gt; &lt; &gt; atual. (Os caracteres < > são usados aqui para maior clareza visual e não podem fazer parte de uma cadeia de caracteres de caminho válida.)

Por exemplo, você poderá atingir essa limitação se estiver clonando um repositório git que tenha nomes de arquivo longos em uma pasta que tenha um nome longo.


> [!Note]  
> As funções de E/S de arquivo na API do Windows convertem "/" em " como parte da conversão do nome em um nome de estilo NT, exceto ao usar o prefixo " ? ", conforme detalhado nas seções a \\ \\ \\ \\ seguir.

A API Windows tem muitas funções que também têm versões Unicode para permitir um caminho de comprimento estendido para um comprimento total máximo de caminho de 32.767 caracteres. Esse tipo de caminho é composto por componentes separados por malhas invertida, cada um até o valor retornado no parâmetro *lpMaximumComponentLength* da função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) (esse valor geralmente tem 255 caracteres). Para especificar um caminho de comprimento estendido, use o prefixo " \\ \\ \\ ? ". Por exemplo, " \\ \\ ? \\ D: \\ *caminho muito longo*".

> [!Note]  
> O caminho máximo de 32.767 caracteres é aproximado, porque o prefixo " ? " pode ser expandido para uma cadeia de caracteres mais longa pelo sistema em tempo de operação e essa expansão se aplica ao \\ \\ \\ comprimento total.

O prefixo " ? " também pode ser usado com caminhos construídos de acordo com \\ \\ a UNC \\ (convenção de nomenização universal). Para especificar esse caminho usando UNC, use o \\ \\ " ? \\ UNC \\ " prefixo. Por exemplo, " \\ \\ ? \\ Compartilhamento de servidor UNC", em que "servidor" é o nome do computador \\ \\ e "compartilhamento" é o nome da pasta compartilhada. Esses prefixos não são usados como parte do próprio caminho. Eles indicam que o caminho deve ser passado para o sistema com modificação mínima, o que significa que você não pode usar barras para representar separadores de caminho ou um período para representar o diretório atual ou pontos duplos para representar o diretório pai. Como você não pode usar o prefixo " ? " com um caminho relativo, os caminhos relativos são sempre limitados \\ \\ a um total de \\ **caracteres \_ MAX PATH.**

Não é necessário executar nenhuma normalização Unicode em cadeias de caracteres de nome de arquivo e caminho para uso pelas funções de API de E/S de arquivo Windows porque o sistema de arquivos trata nomes de caminho e arquivo como uma sequência opaca de **WCHAR** s. Qualquer normalização que seu aplicativo exige deve ser executada com isso em mente, externa a todas as chamadas para funções Windows API de E/S de arquivo relacionadas.

Ao usar uma API para criar um diretório, o caminho especificado não pode ser tão longo que você não possa anexar um nome de arquivo 8.3 (ou seja, o nome do diretório não pode exceder **MAX \_ PATH** menos 12).

O shell e o sistema de arquivos têm requisitos diferentes. É possível criar um caminho com a API Windows que a interface do usuário do shell não é capaz de interpretar corretamente.

## <a name="enable-long-paths-in-windows-10-version-1607-and-later"></a>Habilitar caminhos longos Windows 10, versão 1607 e posteriores

A partir Windows 10, versão 1607, as limitações **MAX \_ PATH** foram removidas das funções comuns de arquivo e diretório Win32. No entanto, você deve optar pelo novo comportamento.

Para habilitar o novo comportamento de caminho longo, ambas as seguintes condições devem ser atendidas:

* A chave do `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` Registro deve existir e ser definida como 1. O valor da chave será armazenado em cache pelo sistema (por processo) após a primeira chamada para uma função de diretório ou arquivo Win32 afetada (veja abaixo a lista de funções). A chave do Registro não será recarregada durante o tempo de vida do processo. Para que todos os aplicativos no sistema reconheçam o valor da chave, uma reinicialização pode ser necessária porque alguns processos podem ter sido iniciados antes da chave ser definida.

Você também pode copiar esse código para um arquivo que pode definir isso para você ou usar o comando do PowerShell em uma janela do terminal com `.reg` privilégios elevados:
# <a name="cmd"></a>[cmd](#tab/cmd)

```cmd
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem]
"LongPathsEnabled"=dword:00000001

```

# <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" `
-Name "LongPathsEnabled" -Value 1 -PropertyType DWORD -Force

```

---

> [!NOTE]  
> Essa chave do Registro também pode ser controlada por meio Política de Grupo em `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths` .

* O [manifesto do aplicativo](../sbscs/application-manifests.md) também deve incluir o elemento `longPathAware` .

    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
            <ws2:longPathAware>true</ws2:longPathAware>
        </windowsSettings>
    </application>
    ```

Essas são as funções de gerenciamento de diretório que não têm mais restrições **\_ MAX PATH** se você optar por um comportamento de caminho longo: CreateDirectoryW, CreateDirectoryExW GetCurrentDirectoryW RemoveDirectoryW SetCurrentDirectoryW.

Essas são as funções de gerenciamento de arquivos que não têm mais restrições **MAX \_ PATH** se você optar por um comportamento de caminho longo: CopyFileW, CopyFile2, CopyFileExW, CreateFileW, CreateFile2, CreateHardLinkW, CreateSymbolicLinkW, DeleteFileW, FindFirstFileW, FindFirstFileExW, FindNextFileW, GetFileAttributesW, GetFileAttributesExW, SetFileAttributesW, GetFullPathNameW, GetLongPathNameW, MoveFileW, MoveFileExW, MoveFileWithProgressW, ReplaceFileW, SearchPathW, FindFirstFileNameW, FindNextFileNameW, FindFirstStreamW, FindNextStreamW, GetCompressedFileSizeW, GetFinalPathNameByHandleW.
