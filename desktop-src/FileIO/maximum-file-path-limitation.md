---
description: Limitação do comprimento máximo do caminho.
title: Limitação do comprimento máximo do caminho
ms.topic: article
ms.custom: contperf-fy21q1
ms.date: 09/15/2020
ms.openlocfilehash: 3d71d87f69aeb224cde256ce78bd29fd0bf5c291
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314799"
---
# <a name="maximum-path-length-limitation"></a>Limitação do comprimento máximo do caminho

Na API do Windows (com algumas exceções discutidas nos parágrafos a seguir), o comprimento máximo de um caminho é o **\_ caminho máximo**, que é definido como 260 caracteres. Um caminho local é estruturado na seguinte ordem: letra da unidade, dois-pontos, barra invertida, componentes de nome separados por barras invertidas e um caractere nulo de terminação. Por exemplo, o caminho máximo na unidade D é "D: \\ *uma cadeia de caracteres de caminho de caractere 256* &lt; nul &gt; ", em que " &lt; nul &gt; " representa o caractere nulo de terminação invisível para a página de código do sistema atual. (Os caracteres < > são usados aqui para clareza visual e não podem fazer parte de uma cadeia de caracteres de caminho válida.)

Por exemplo, você pode atingir essa limitação se estiver clonando um repositório git que tem nomes de arquivo longos em uma pasta que tem um nome longo.


> [!Note]  
> As funções de e/s de arquivo na API do Windows convertem "/" em " \\ " como parte da conversão do nome em um nome de estilo NT, exceto ao usar o \\ \\ prefixo "? \\ ", conforme detalhado nas seções a seguir.

A API do Windows tem muitas funções que também têm versões Unicode para permitir um caminho de tamanho estendido para um tamanho de caminho total máximo de 32.767 caracteres. Esse tipo de caminho é composto por componentes separados por barras invertidas, cada um até o valor retornado no parâmetro *lpMaximumComponentLength* da função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) (esse valor é normalmente de 255 caracteres). Para especificar um caminho de comprimento estendido, use o \\ \\ prefixo "? \\ ". Por exemplo, " \\ \\ ? \\ D: \\ *caminho muito longo*".

> [!Note]  
> O caminho máximo de 32.767 caracteres é aproximado, pois o \\ \\ prefixo "? \\ " pode ser expandido para uma cadeia de caracteres mais longa pelo sistema em tempo de execução, e essa expansão se aplica ao comprimento total.

O \\ \\ prefixo "? \\ " também pode ser usado com caminhos construídos de acordo com a UNC (Convenção de nomenclatura universal). Para especificar esse caminho usando UNC, use o " \\ \\ ? \\ \\Prefixo "UNC. Por exemplo, " \\ \\ ? \\ \\Compartilhamento de servidor UNC \\ ", onde" servidor "é o nome do computador e" compartilhamento "é o nome da pasta compartilhada. Esses prefixos não são usados como parte do próprio caminho. Eles indicam que o caminho deve ser passado para o sistema com a modificação mínima, o que significa que você não pode usar barras para representar separadores de caminho ou um período para representar o diretório atual ou pontos duplos para representar o diretório pai. Como não é possível usar o \\ \\ prefixo "? \\ " com um caminho relativo, os caminhos relativos são sempre limitados a um total de caracteres de **\_ caminho máximo** .

Não é necessário executar qualquer normalização Unicode nas cadeias de caracteres de nome de arquivo e caminho para uso pelas funções da API de e/s de arquivo do Windows porque o sistema de arquivos trata os nomes de caminho e arquivo como uma sequência opaca de **WCHAR** s. Qualquer normalização que seu aplicativo requer deve ser executada com isso em mente, externamente de todas as chamadas para funções de API de e/s de arquivo do Windows relacionadas.

Ao usar uma API para criar um diretório, o caminho especificado não pode ser tão longo que você não pode acrescentar um nome de arquivo 8,3 (ou seja, o nome do diretório não pode exceder o **\_ caminho máximo** menos 12).

O Shell e o sistema de arquivos têm requisitos diferentes. É possível criar um caminho com a API do Windows que a interface do usuário do shell não possa interpretar corretamente.

## <a name="enable-long-paths-in-windows-10-version-1607-and-later"></a>Habilitar caminhos longos no Windows 10, versão 1607 e posterior

A partir do Windows 10, versão 1607, as limitações **máximas de \_ caminho** foram removidas das funções comuns de arquivo e diretório do Win32. No entanto, você deve aceitar o novo comportamento.

Para habilitar o novo comportamento de caminho longo, ambas as condições a seguir devem ser atendidas:

* A chave do registro `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` deve existir e ser definida como 1. O valor da chave será armazenado em cache pelo sistema (por processo) após a primeira chamada para uma função de diretório ou arquivo Win32 afetado (veja abaixo a lista de funções). A chave do registro não será recarregada durante o tempo de vida do processo. Para que todos os aplicativos no sistema reconheçam o valor da chave, uma reinicialização pode ser necessária porque alguns processos podem ter começado antes da definição da chave.

Você também pode copiar esse código para um `.reg` arquivo que pode definir isso para você:
```cmd
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem]
"LongPathsEnabled"=dword:00000001

```

> [!NOTE]  
> Essa chave do registro também pode ser controlada por meio de Política de Grupo em `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths` .

* O [manifesto do aplicativo](../sbscs/application-manifests.md) também deve incluir o `longPathAware` elemento.

    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
            <ws2:longPathAware>true</ws2:longPathAware>
        </windowsSettings>
    </application>
    ```

Essas são as funções de gerenciamento de diretório que não têm mais restrições de **\_ caminho máximo** se você aceitar o comportamento de caminho longo: CreateDirectoryW, CreateDirectoryExW GetCurrentDirectoryW RemoveDirectoryW SetCurrentDirectoryW.

Essas são as funções de gerenciamento de arquivo que não têm mais restrições de **\_ caminho máximo** se você aceitar o comportamento de caminho longo: CopyFileW, CopyFile2, CopyFileExW, CreateFileW, createfile2, CreateHardLinkW, CreateSymbolicLinkW, DeleteFileW, FindFirstFileW, FindFirstFileExW, FindNextFileW, GetFileAttributesW, GetFileAttributesExW, SetFileAttributesW, GetFullPathNameW, GetLongPathNameW, MoveFileW, MoveFileExW, MoveFileWithProgressW, ReplaceFileW, SearchPathW, FindFirstFileNameW, FindNextFileNameW, FindFirstStreamW, FindNextStreamW, GetCompressedFileSizeW, GetFinalPathNameByHandleW
