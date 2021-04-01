---
description: 'Saiba mais sobre: exemplos da ferramenta VShadow'
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Exemplos da ferramenta VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65fd2bfa1c390b1bd5310cd80f02e029dbf935f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647167"
---
# <a name="vshadow-tool-examples"></a>Exemplos da ferramenta VShadow

Os exemplos a seguir mostram como usar a ferramenta VShadow para executar as tarefas mais comuns:

-   [Acessando Propriedades de cópia de sombra de um script CMD](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [Acessando cópias de sombra não persistentes](#accessing-nonpersistent-shadow-copies)
-   [Copiando um arquivo de uma cópia de sombra](#copying-a-file-from-a-shadow-copy)
-   [Enumerando todos os arquivos em um dispositivo de cópia de sombra](#enumerating-all-files-on-a-shadow-copy-device)
-   [Importando uma cópia de sombra transportável](#importing-a-transportable-shadow-copy)
-   [Incluindo gravadores ou componentes](#including-writers-or-components)
-   [Excluindo gravadores ou componentes](#excluding-writers-or-components)
-   [Quebrando conjuntos de cópias de sombra usando o método BreakSnapshotSetEx](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

Para obter uma lista completa das opções de linha de comando e seu uso, consulte a [ferramenta VShadow e o exemplo](vshadow-tool-and-sample.md).

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a>Acessando Propriedades de cópia de sombra de um script CMD

Se você usar o sinalizador opcional **-script** ao criar cópias de sombra, o VShadow criará um arquivo de script cmd contendo variáveis de ambiente relacionadas às cópias de sombra recém-criadas, como as seguintes:

-   A ID do conjunto de cópias de sombra, que é armazenada na variável de ambiente% VSHADOW \_ set \_ ID%
-   As IDs de cópia de sombra, que são armazenadas em variáveis do formato% VSHADOW \_ ID \_ *nnn*%, em que *nnn* representa o índice do volume de origem na linha de comando VSHADOW
-   Os nomes do dispositivo de cópia de sombra, que são armazenados em variáveis do formato% VSHADOW do \_ dispositivo \_ *nnn*%, em que *nnn* é o índice do volume de origem na linha de comando VSHADOW

Você pode usar o arquivo CMD gerado para executar operações de gerenciamento limitadas nas cópias de sombra.

> [!Note]  
> O evento do gravador [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) é enviado após a execução do script **-exec** . O VSS chama o método **IVssBackupComponents:: BackupComplete** para sinalizar para os gravadores que o backup está concluído e os gravadores podem truncar os logs neste ponto. Portanto, é importante verificar se a sombra/backup realmente foi concluída. Se o backup tiver falhado, você poderá cancelar o processo de criação retornando um código de saída diferente de zero no script/comando executado. (Consulte a documentação do comando exit na referência de [linha de comando do Windows](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) Se o comando personalizado retornar com um código de saída diferente de zero, a criação da cópia de sombra será cancelada e **IVssBackupComponents:: BackupComplete** não será chamado.

 

O exemplo a seguir mostra como criar uma cópia de sombra persistente a partir da linha de comando e usar o script CMD para expô-la.

1.  **vshadow-p-NW-script = SETVAR1. cmd c:**
2.  **chamar SETVAR1. cmd**
3.  **C: \\>vshadow-El =% vshadow \_ ID \_ 1%, c: \\ directory1**

## <a name="accessing-nonpersistent-shadow-copies"></a>Acessando cópias de sombra não persistentes

As cópias de sombra não persistentes são excluídas automaticamente quando o programa que as cria (neste caso, VShadow) é encerrado. Para acessar o conteúdo dessas cópias de sombra, o VShadow permite que você execute um script depois que as cópias de sombra são criadas, mas antes da saída do programa VShadow.

O exemplo a seguir mostra como usar a opção de linha de comando-exec para executar um script chamado "enum. cmd":

**vshadow-NW-exec = enum. cmd c:**

No script executado, você também pode executar o script SETVAR gerado neste comando personalizado. Isso permite que o script acesse o conteúdo das cópias de sombra diretamente. Lembre-se de que o dispositivo de sombra pode ser recuperado da \_ variável de ambiente do dispositivo VSHADOW \_ nnn.

Aqui está um exemplo de script enum. cmd:

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

Aqui está a linha de comando para executar o script enum. cmd:

**vshadow-NW-exec = c: \\ enum. cmd-script = setvar1. cmd c:**

## <a name="copying-a-file-from-a-shadow-copy"></a>Copiando um arquivo de uma cópia de sombra

O exemplo a seguir mostra como copiar um arquivo de uma cópia de sombra.

1.  **Dir > c: \\somefile.txt**
2.  **vshadow-p-NW-script = SETVAR1. cmd c:**
3.  **chamar SETVAR1. cmd**
4.  **copiar% VSHADOW do \_ dispositivo \_ 1% \\somefile.txt c: \\ algum \_bak.txt**

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a>Enumerando todos os arquivos em um dispositivo de cópia de sombra

O exemplo a seguir mostra como enumerar todos os arquivos em um dispositivo de cópia de sombra de um arquivo em lotes.

1.  **Dir > c: \\somefile.txt**
2.  **vshadow-p-NW-script = SETVAR1. cmd c:**
3.  **chamar SETVAR1. cmd**
4.  **para/R% VSHADOW \_ dispositivo \_ 1% \\ %% i in ( \* ) do @echo %% i**

## <a name="importing-a-transportable-shadow-copy"></a>Importando uma cópia de sombra transportável

Para criar uma cópia de sombra transportável em um computador e importá-la para outra máquina, você deve ter dois computadores conectados (por meio de uma configuração de SAN) a uma matriz de armazenamento que ofereça suporte a cópias de sombra de hardware do VSS. Um provedor de hardware VSS deve ser instalado em cada computador.

O exemplo a seguir mostra como criar e importar a cópia de sombra.

1.  Crie o conjunto de cópias de sombra no computador A (o servidor de produção) digitando o seguinte comando após o prompt de comando:

    **vshadow-p-t =bc1.xml**

    Isso não vai expor nenhum dispositivo de cópia de sombra no computador A.

2.  Copie o documento de componentes de backup (bc1.xml) do computador A para o computador B.
3.  Importe o conjunto de sombras no computador B digitando o seguinte comando:

    **vshadow-i =bc1.xml**

Opcionalmente, você pode expor essas cópias de sombra como letras de unidade ou pastas montadas. Além disso, você poderia interromper o conjunto de sombras para fazer os novos volumes de cópia de sombra de leitura/gravação.

Para automatizar o processo de gerenciamento do conjunto de sombras, você pode usar a opção de linha de comando **-script** para gerar o script cmd que contém as IDs de cópia de sombra. Em seguida, você pode copiar o script gerado junto com os componentes de backup para o outro computador.

O exemplo a seguir mostra como criar, expor e quebrar cópias de sombra transportáveis usando scripts CMD.

1.  Crie o conjunto de cópias de sombra no computador A (o servidor de produção) na linha de comando da seguinte maneira:

    **vshadow-p-t =bc1.xml-script = SC1. cmd**

    Especifique a opção **-script** para gerar o script que contém as definições de variável de ambiente adequadas. Observe que isso não vai expor nenhum dispositivo de cópia de sombra no computador A.

2.  Copie o documento de componentes de backup (bc1.xml) e o script gerado (SC1. cmd) do computador A para o computador B.
3.  Importe o conjunto de sombras no computador B digitando o seguinte comando:

    **vshadow-i =bc1.xml**

    Isso causará a superfície dos dispositivos criados no computador B.

4.  Execute o script gerado para definir as variáveis de ambiente para o conjunto de cópias de sombra digitando o nome do arquivo no prompt de comando, como no exemplo a seguir:

    **SC1. cmd**

    Isso definirá as variáveis de ambiente relevantes, conforme descrito em acessar propriedades de cópia de sombra de um script CMD.

5.  Expor as cópias de sombra no computador B digitando os seguintes comandos:
    1.  **rmdir/s c: \\ ponto de montagem \_**
    2.  **mkdir c: \\ ponto de montagem \_**
    3.  **vshadow – El =% VSHADOW \_ ID \_ 1%, c: \\ ponto de montagem \_**

    Isso causará a superfície dos dispositivos de cópia de sombra criados no computador B.
6.  Interrompa o conjunto de cópias de sombra para tornar os volumes graváveis digitando o seguinte comando:**C: \\>vshadow – BW =% vshadow \_ set \_ ID%**

Observe que as cópias de sombra transportáveis não persistentes também podem ser importadas, mas são excluídas automaticamente quando o processo **vshadow** **-i** é encerrado. Para importar as cópias de sombra antes que elas sejam excluídas, você deve usar a opção de linha de comando **-exec** , conforme descrito em acessar cópias de sombra não persistentes.

## <a name="including-writers-or-components"></a>Incluindo gravadores ou componentes

Por padrão, todos os gravadores participam da criação da cópia de sombra. Para determinar quais gravadores e componentes serão incluídos em um conjunto de cópias de sombra, use a opção de linha de comando **-WM** ou **-wm2** , conforme descrito em [listando o status do gravador e os metadados](vshadow-tool-and-sample.md).

Para verificar se todos os componentes de um gravador estão incluídos, use o sinalizador opcional **-Wi** em qualquer um dos seguintes formatos:

-   **vshadow** **-Wi** *WriterName*
-   **vshadow** **-Wi** **"**_cadeia de nome do gravador_*_"_*
-   **vshadow** **-Wi** **{**_WriterId_*_}_*
-   **vshadow** **-Wi** **{**_InstanceId_*_}_*

Para verificar se os componentes específicos estão incluídos, use o sinalizador opcional **-Wi** em qualquer um dos seguintes formatos:

-   **vshadow** **-Wi** *WriterName ***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-Wi** **"**_cadeia de nome do gravador_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-Wi** **{**_WriterId_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-Wi** **{**_InstanceId_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

Os exemplos a seguir mostram como usar o sinalizador opcional **-Wi** .

-   Especificando *WriterName*: \\ *LogicalPath* \\ *ComponentName*:

    **vshadow-Wi = "gravador do registro: \\ registro"**

-   Especificando {*WriterId*}:

    **vshadow-Wi = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Especificando mais de um gravador ou componente:

    **vshadow-Wi = "gravador do registro: \\ registro"-Wi = "gravador REGDB com+"**

## <a name="excluding-writers-or-components"></a>Excluindo gravadores ou componentes

Para excluir todos os gravadores, use o sinalizador opcional **-NW** ao criar a cópia de sombra.

Para excluir todos os componentes de um gravador, use o sinalizador opcional **-WX** em qualquer um dos seguintes formatos:

-   **vshadow** **-WX** *WriterName*
-   **vshadow** **-WX** **"**_cadeia de nome do gravador_*_"_*
-   **vshadow** **-WX** **{**_WriterId_*_}_*
-   **vshadow** **-WX** **{**_InstanceId_*_}_*

Para excluir componentes específicos, use o sinalizador opcional **-WX** em qualquer um dos seguintes formatos:

-   **vshadow** **-WX** *WriterName ***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-WX** **"**_cadeia de nome do gravador_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-WX** **{**_WriterId_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-WX** **{**_InstanceId_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

Os exemplos a seguir mostram como usar o sinalizador opcional **-WX** .

-   Especificando *WriterName*: \\ *LogicalPath* \\ *ComponentName*:

    **vshadow-WX = "gravador do registro: \\ registro"**

-   Especificando {*WriterId*}:

    **vshadow-WX = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Especificando mais de um gravador ou componente:

    **vshadow-WX = "gravador do registro: \\ registro"-WX = "gravador REGDB do com+"**

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a>Quebrando conjuntos de cópias de sombra usando o método BreakSnapshotSetEx

Os exemplos a seguir mostram como usar a opção de linha de comando **-Bex** .

-   Especificar que o LUN de cópia de sombra será mascarado do host:

    **vshadow** **-Bex** **-Mask**

-   Especificar que o LUN de cópia de sombra será exposto ao host como um volume de leitura/gravação:

    **vshadow** **-Bex** **-RW**

-   Especificar que o LUN de cópia de sombra será exposto ao host como um volume de leitura/gravação e que nenhuma das assinaturas de disco nos LUNs de cópia de sombra será revertida para o dos LUNs originais:

    **vshadow** **-Bex** **-norevert**

 

 
