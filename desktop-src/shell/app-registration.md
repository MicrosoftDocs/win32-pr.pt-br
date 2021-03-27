---
description: Este tópico discute como os aplicativos podem expor informações sobre eles próprios necessários para habilitar determinados cenários.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: registro de Aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857e96893d2fe717f1a4939d06c77af043ead318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920758"
---
# <a name="application-registration"></a>registro de Aplicativo

Este tópico discute como os aplicativos podem expor informações sobre eles próprios necessários para habilitar determinados cenários. Isso inclui as informações necessárias para localizar o aplicativo, os verbos aos quais o aplicativo dá suporte e os tipos de arquivos que um aplicativo pode manipular.

Este tópico é organizado da seguinte maneira:

-   [Encontrando um executável de aplicativo](#finding-an-application-executable)
-   [Registrando aplicativos](#registering-applications)
    -   [Usando a subchave de caminhos do aplicativo](#using-the-app-paths-subkey)
    -   [Usando a subchave Applications](#using-the-applications-subkey)
-   [Registrando verbos e outras informações de associação de arquivo](#registering-verbs-and-other-file-association-information)
-   [Registrando um tipo percebido](#registering-a-perceived-type)
-   [Tópicos relacionados](#related-topics)

> [!Note]  
> Os aplicativos também podem ser registrados nos aplicativos definir o acesso do programa e padrões do computador (SPAD) e definir os programas padrão (SYDP) do painel de controle. Para obter informações sobre o registro de aplicativo SPAD e SYDP, consulte [diretrizes para associações de arquivo e programas padrão](appguide-fa-defpro.md)e [definir o acesso do programa e padrões do computador (SPAD)](cpl-setprogramaccess.md).

 

## <a name="finding-an-application-executable"></a>Encontrando um executável de aplicativo

Quando a função [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) é chamada com o nome de um arquivo executável em seu parâmetro *lpFile* , há vários locais em que a função procura o arquivo. É recomendável registrar seu aplicativo na subchave do registro de **caminhos do aplicativo** . Isso evita a necessidade de aplicativos para modificar a variável de ambiente do caminho do sistema.

O arquivo é procurado nos seguintes locais:

-   O diretório de trabalho atual.
-   Somente o diretório do **Windows** (nenhum subdiretório é pesquisado).
-   O diretório **Windows \\ System32** .
-   Diretórios listados na variável de ambiente PATH.
-   Recomendado: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **app Paths**

## <a name="registering-applications"></a>Registrando aplicativos

As subchaves de registro de **aplicativos** e **caminhos de aplicativo** são usadas para registrar e controlar o comportamento do sistema em nome dos aplicativos. A subchave de **caminhos do aplicativo** é o local preferencial.

### <a name="using-the-app-paths-subkey"></a>Usando a subchave de caminhos do aplicativo

No Windows 7 e posterior, é altamente recomendável que você instale aplicativos por usuário, em vez de por computador. Um aplicativo que é instalado para por usuário pode ser registrado em **HKEY \_ Current \_ User** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **app Paths**. Um aplicativo que é instalado para todos os usuários do computador pode ser registrado em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **app Paths**.

As entradas encontradas em **caminhos de aplicativo** são usadas principalmente para as seguintes finalidades:

-   Para mapear o nome do arquivo executável de um aplicativo para o caminho totalmente qualificado desse arquivo.
-   Para obter informações autônomas para a variável de ambiente PATH em uma base por aplicativo, por processo.

Se o nome de uma subchave dos **caminhos do aplicativo** corresponder ao nome do arquivo, o Shell executará duas ações:

-   A entrada (padrão) é usada como o caminho totalmente qualificado do arquivo.
-   A entrada de caminho para essa subchave é precedente à variável de ambiente PATH do processo. Se isso não for necessário, o valor do caminho poderá ser omitido.

Os possíveis problemas a serem considerados incluem:

-   O Shell limita o comprimento de uma linha de comando para o \_ caminho máximo \* 2 caracteres. Se houver muitos arquivos listados como entradas de registro ou seus caminhos forem longos, os nomes de arquivo mais tarde na lista poderão ser perdidos à medida que a linha de comando estiver truncada.
-   Alguns aplicativos não aceitam vários nomes de arquivo em uma linha de comando.
-   Alguns aplicativos que aceitam vários nomes de arquivo não reconhecem o formato no qual o Shell os fornece. O Shell fornece a lista de parâmetros como uma cadeia de caracteres entre aspas, mas alguns aplicativos podem exigir cadeias sem aspas.
-   Nem todos os itens que podem ser arrastados fazem parte do sistema de arquivos; por exemplo, impressoras. Esses itens não têm um caminho Win32 padrão, portanto, não há como fornecer um valor *lpParameters* significativo para [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

O uso da entrada DropTarget evita esses possíveis problemas fornecendo acesso a todos os formatos da área de transferência, incluindo [CFSTR \_ SHELLIDLIST](clipboard.md) (para listas de arquivos longos) e [CFSTR \_ FileContent](clipboard.md) (para objetos que não são do sistema de arquivos).

**Para registrar e controlar o comportamento de seus aplicativos com a subchave de caminhos do aplicativo**:

1.  Adicione uma subchave com o mesmo nome do arquivo executável à subchave de **caminhos do aplicativo** , conforme mostrado na entrada do registro a seguir.

    ```
    HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   App Paths
                      file.exe
                         (Default)
                         DontUseDesktopChangeRouter
                         DropTarget
                         Path
                         UseUrl
    ```

2.  Consulte a tabela a seguir para obter detalhes das entradas de subchave de **caminhos do aplicativo** . 

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Entrada de registro</th>
    <th>Detalhes</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>(Padrão)</td>
    <td>É o caminho totalmente qualificado para o aplicativo. O nome do aplicativo fornecido na entrada (padrão) pode ser declarado com ou sem sua extensão. exe. Se necessário, a função <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> adiciona a extensão ao pesquisar a subchave de <strong>caminhos do aplicativo</strong> . A entrada é do tipo de <strong>REG_SZ</strong> .</td>
    </tr>
    <tr class="even">
    <td>DontUseDesktopChangeRouter</td>
    <td>É obrigatório para aplicativos de depurador evitar deadlocks de diálogo de arquivo ao depurar o processo do Windows Explorer. No entanto, definir a entrada DontUseDesktopChangeRouter produz um tratamento ligeiramente menos eficiente das notificações de alteração. A entrada é do tipo de <strong>REG_DWORD</strong> e o valor é 0x1.</td>
    </tr>
    <tr class="odd">
    <td>DropTarget</td>
    <td>É um identificador de classe (CLSID). A entrada DropTarget contém o CLSID de um objeto (geralmente um servidor local em vez de um servidor em processo) que implementa <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>. Por padrão, quando o destino de soltura é um arquivo executável e nenhum valor de DropTarget é fornecido, o Shell converte a lista de arquivos soltos em um parâmetro de linha de comando e passa-o para <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> por meio de <em>lpParameters</em>.</td>
    </tr>
    <tr class="even">
    <td>Caminho</td>
    <td>Fornece uma cadeia de caracteres (na forma de uma lista de diretórios separados por ponto e vírgula) para acrescentar à variável de ambiente PATH quando um aplicativo é iniciado chamando <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>. É o caminho totalmente qualificado para o. exe. É de <strong>REG_SZ</strong>. No <strong>Windows 7 e posterior</strong>, o tipo pode ser <strong>REG_EXPAND_SZ</strong>e geralmente é <strong>REG_EXPAND_SZ</strong> % ProgramFiles%.
    <blockquote>
    [!Note]<br />
Além das entradas (padrão), Path e DropTarget reconhecidas pelo shell, um aplicativo também pode adicionar valores personalizados à subchave de <strong>caminhos do aplicativo</strong> do arquivo executável. Incentivamos os desenvolvedores de aplicativos a usar a subchave de <strong>caminhos</strong> do aplicativo para fornecer um caminho específico do aplicativo em vez de fazer adições ao caminho do sistema global.
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td>SupportedProtocols</td>
    <td>Cria uma cadeia de caracteres que contém os esquemas de protocolo de URL para uma determinada chave. Isso pode conter vários valores de registro para indicar quais esquemas têm suporte. Essa cadeia de caracteres segue o formato de <strong>scheme1: scheme2</strong>. Se essa lista não estiver vazia, <strong>file:</strong> será adicionado à cadeia de caracteres. Esse protocolo tem suporte implícito quando <em>SupportedProtocols</em> é definido. <br/></td>
    </tr>
    <tr class="even">
    <td>UseUrl</td>
    <td>Indica que seu aplicativo pode aceitar uma URL (em vez de um nome de arquivo) na linha de comando. Os aplicativos que podem abrir documentos diretamente da Internet, como navegadores da Web e media players, devem definir essa entrada. <br/> Quando a função <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> inicia um aplicativo e o valor UseUrl = 1 não é definido, <strong>ShellExecuteEx</strong> baixa o documento em um arquivo local e invoca o manipulador na cópia local.<br/> Por exemplo, se o aplicativo tiver essa entrada definida e um usuário clicar com o botão direito do mouse em um arquivo armazenado em um servidor Web, o verbo aberto será disponibilizado. Caso contrário, o usuário precisará baixar o arquivo e abrir a cópia local. <br/> A entrada UseUrl é do tipo <strong>REG_DWORD</strong> e o valor é 0x1.<br/> No Windows Vista e versões anteriores, essa entrada indicou que a URL deve ser passada para o aplicativo junto com um nome de arquivo local, quando chamado via ShellExecuteEx. No Windows 7, ele indica que o aplicativo pode entender qualquer URL http ou HTTPS que é transmitida a ele, sem precisar fornecer o nome do arquivo de cache também. Essa chave do registro está associada à chave <em>SupportedProtocols</em> .<br/></td>
    </tr>
    </tbody>
    </table>

    

     

### <a name="using-the-applications-subkey"></a>Usando a subchave Applications

Por meio da inclusão de entradas do registro na subchave **HKEY \_ classes \_ raiz** \\ **Applications** \\ *ApplicationName.exe* , os aplicativos podem fornecer as informações específicas do aplicativo mostradas na tabela a seguir.



| Entrada de registro                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| verbo do Shell \\                      | Fornece o método verbo para chamar o aplicativo a partir de OpenWith. Sem uma definição de verbo especificada aqui, o sistema pressupõe que o aplicativo dá suporte a [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)e passa o nome do arquivo na linha de comando. Essa funcionalidade se aplica a todos os métodos de verbo, incluindo DropTarget, ExecuteCommand e troca dinâmica de dados (DDE).                                                                                                                                                                                                                                                                                                                            |
| DefaultIcon                      | Permite que um aplicativo forneça um ícone específico para representar o aplicativo em vez do primeiro ícone armazenado no arquivo. exe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| FriendlyAppName                  | Fornece uma maneira de obter um nome localizável a ser exibido para um aplicativo, em vez de apenas as informações de versão que aparecem, o que pode não ser localizável. A consulta de associação [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) lê esse valor de entrada de registro e volta a usar o nome FileDescription nas informações de versão. Se esse nome estiver ausente, a consulta de associação usa como padrão o nome de exibição do arquivo. Os aplicativos devem usar **ASSOCSTR \_ FRIENDLYAPPNAME** para recuperar essas informações para obter o comportamento adequado.                                                                                                                                                                        |
| SupportedTypes                   | Lista os tipos de arquivos aos quais o aplicativo dá suporte. Isso permite que o aplicativo seja listado no menu cascata da caixa de diálogo **abrir com** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| NoOpenWith                       | Indica que nenhum aplicativo foi especificado para abrir esse tipo de arquivo. Lembre-se de que, se uma subchave OpenWithProgIDs tiver sido definida para um aplicativo por tipo de arquivo e a subchave ProgID também não tiver uma entrada NoOpenWith, esse aplicativo será exibido na lista de aplicativos recomendados ou disponíveis, mesmo que tenha especificado a entrada NoOpenWith. Para obter mais informações, consulte [como incluir um aplicativo na caixa de diálogo abrir com](how-to-include-an-application-on-the-open-with-dialog-box.md) e [como excluir um aplicativo da caixa de diálogo abrir com](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).<br/> |
| IsHostApp                        | Indica que o processo é um processo de host, como Rundll32.exe ou Dllhost.exe, e não deve ser considerado para fixação do menu **Iniciar** ou inclusão na lista de usados com mais frequência (MFU). Quando iniciado com um atalho que contém uma lista de argumentos não nulos ou um [AppUserModelIDs (IDs de modelo de usuário de aplicativo)](appids.md)explícitas, o processo pode ser fixado (como esse atalho). Esses atalhos são candidatos para inclusão na lista de MFU.                                                                                                                                                                                                                                                  |
| NoStartPage                      | Indica que o executável do aplicativo e os atalhos devem ser excluídos do menu **Iniciar** e da fixação ou inclusão na lista MFU. Essa entrada normalmente é usada para excluir ferramentas, instaladores e desinstaladores do sistema e arquivos Leiame.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| UseExecutableForTaskbarGroupIcon | Faz com que a barra de tarefas use o ícone padrão desse executável se não houver nenhum atalho fixas para esse aplicativo e, em vez do ícone da janela que foi encontrada pela primeira vez.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| TaskbarGroupIcon                 | Especifica o ícone usado para substituir o ícone da barra de tarefas. O ícone de janela normalmente é usado para a barra de tarefas. Definir a entrada TaskbarGroupIcon faz com que o sistema use o ícone do. exe para o aplicativo em vez disso.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Exemplos

Veja a seguir alguns exemplos de registros de aplicativo por meio da subchave **HKEY \_ classes \_ raiz** \\ **Applications** \\ *ApplicationName.exe* . Todos os valores de entrada do registro são do tipo **reg \_ sz** , com a exceção de **DefaultIcon** , que é do tipo **reg \_ Expand \_ sz** .

```
HKEY_CLASSES_ROOT
   Applications
      wordpad.exe
         FriendlyAppName = @%SystemRoot%\System32\shell32.dll,-22069
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         SupportedTypes
            .3gp2
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         DefaultIcon
            (Default) = %SystemRoot%\system32\wmploc.dll,-730
```

```
HKEY_CLASSES_ROOT
   Applications
      WScript.exe
         NoOpenWith
```

```
HKEY_CLASSES_ROOT
   Applications
      photoviewer.dll
         shell
            open
               DropTarget
                  Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
```

```
HKEY_CLASSES_ROOT
   Applications
      mspaint.exe
         SupportedTypes
            .bmp
            .dib
            .rle
            .jpg
            .jpeg
            .jpe
            .jfif
            .gif
            .emf
            .wmf
            .tif
            .tiff
            .png
            .ico
```

## <a name="registering-verbs-and-other-file-association-information"></a>Registrando verbos e outras informações de associação de arquivo

As subchaves registradas em **HKEY \_ classes \_ root** \\ **SystemFileAssociations** permitem que o Shell defina o comportamento padrão de atributos para tipos de arquivo e habilite associações de arquivos compartilhados. Quando os usuários alteram o aplicativo padrão para um tipo de arquivo, o ProgID do novo aplicativo padrão tem prioridade no fornecimento de verbos e outras informações de associação. Essa prioridade se deve ao fato de ser a primeira entrada na matriz de associação. Se o programa padrão for alterado, as informações no ProgID anterior não estarão mais disponíveis.

Para lidar de forma proativa com as consequências de uma alteração nos programas padrão, você pode usar a **\_ \_ raiz das classes hKey** \\ **SystemFileAssociations** para registrar verbos e outras informações de associação. Devido ao seu local após o ProgID na matriz de associação, esses registros são de prioridade mais baixa. Esses SystemFileAssociationsregistrations são estáveis mesmo quando os usuários alteram os programas padrão e fornecem um local para registrar os verbos secundários que sempre estarão disponíveis para um determinado tipo de arquivo. Para obter um exemplo de registro, consulte [registrando um tipo percebido](#registering-a-perceived-type) posteriormente neste tópico.

O exemplo de registro a seguir mostra o que acontece quando o usuário executa o item **programas padrão** no painel de controle para alterar o padrão para arquivos. mp3 para App2ProgID. Depois de alterar o padrão, Verb1 não estará mais disponível e Verb2 se tornará o padrão.

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = App1ProgID
```

```
HKEY_CLASSES_ROOT
   App1ProgID
      shell
         Verb1
```

```
HKEY_CLASSES_ROOT
   App2ProgID
      shell
         Verb2
```

## <a name="registering-a-perceived-type"></a>Registrando um tipo percebido

Os valores do registro para tipos observados são definidos como subchaves da subchave **HKEY \_ classes \_ root** \\ **SystemFileAssociations** do registro. Por exemplo, o **texto** do tipo percebido é registrado da seguinte maneira:

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      text
         shell
            edit
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
            open
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
```

O tipo percebido de um tipo de arquivo é indicado pela inclusão de um valor percebido na subchave do tipo de arquivo. O valor percebidotype é definido como o nome do tipo percebido registrado na subchave do registro de **\_ classes \_** \\ **SystemFileAssociations** do hKey, conforme mostrado no exemplo de registro anterior. Para declarar arquivos. cpp como sendo do tipo percebido "text", por exemplo, adicione a seguinte entrada de registro:

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de arquivo](fa-file-types.md)
</dt> <dt>

[Como funcionam as associações de arquivo](fa-how-work.md)
</dt> <dt>

[Exibição de conteúdo por tipo de arquivo ou tipo](prophand-content-view.md)
</dt> <dt>

[Verificador de tipo de arquivo](file-type-verifier.md)
</dt> <dt>

[Manipuladores de tipo de arquivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores programáticos](fa-progids.md)
</dt> <dt>

[Tipos observados](fa-perceivedtypes.md)
</dt> <dt>

[Matrizes de associação](fa-associationarray.md)
</dt> </dl>

