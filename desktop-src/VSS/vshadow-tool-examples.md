---
description: 'Saiba mais sobre: Exemplos da Ferramenta VShadow'
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Exemplos da ferramenta VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ec0a753f2865be98cfed76cd192a73cfc785b3fcdc487f7685c9f4ae7d52e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056344"
---
# <a name="vshadow-tool-examples"></a>Exemplos da ferramenta VShadow

Os exemplos a seguir mostram como usar a ferramenta VShadow para executar as tarefas mais comuns:

-   [Acessando propriedades de cópia de sombra de um script CMD](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [Acessando cópias de sombra não persistentes](#accessing-nonpersistent-shadow-copies)
-   [Copiando um arquivo de uma cópia de sombra](#copying-a-file-from-a-shadow-copy)
-   [Enumerando todos os arquivos em um dispositivo de cópia de sombra](#enumerating-all-files-on-a-shadow-copy-device)
-   [Importando uma cópia de sombra transportável](#importing-a-transportable-shadow-copy)
-   [Incluindo autores ou componentes](#including-writers-or-components)
-   [Excluindo autores ou componentes](#excluding-writers-or-components)
-   [Conjuntos de cópias de sombra de quebra usando o método BreakSnapshotSetEx](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

Para ver uma lista completa das opções de linha de comando e seu uso, consulte [Ferramenta VShadow e Exemplo.](vshadow-tool-and-sample.md)

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a>Acessando propriedades de cópia de sombra de um script CMD

Se você usar o **sinalizador opcional -script** ao criar cópias de sombra, o VShadow criará um arquivo de script CMD contendo variáveis de ambiente relacionadas às cópias de sombra recém-criadas, como o seguinte:

-   A ID do conjunto de cópias de sombra, que é armazenada na variável de ambiente %VSHADOW \_ SET \_ ID%
-   As IDs de cópia de sombra, que são armazenadas em variáveis do formato %VSHADOW \_ ID \_ *NNN*%, em que *NNN* representa o índice do volume de origem na linha de comando VShadow
-   Os nomes de dispositivo de cópia de sombra, que são armazenados em variáveis do formato %VSHADOW DEVICE NNN %, em que NNN é o índice do volume de origem na linha de comando \_ \_ VShadow 

Você pode usar o arquivo CMD gerado para executar operações de gerenciamento limitadas nas cópias de sombra.

> [!Note]  
> O [**evento de autor BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) é enviado depois que o script **-exec** é executado. O VSS chama o método **IVssBackupComponents::BackupComplete** para sinalizar aos autores que o backup foi concluído, e os autores podem potencialmente truncar logs neste ponto. Portanto, é importante verificar se a sombra/backup realmente foi concluída. Se o backup falhar, você poderá cancelar o processo de criação retornando um código de saída diferente de zero no script/comando executado. (Consulte a documentação do comando exit no [Windows de linha de comando](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) Se o comando personalizado retornar com um código de saída que não seja zero, a criação da cópia de sombra será cancelada e **IVssBackupComponents::BackupComplete** não será chamado.

 

O exemplo a seguir mostra como criar uma cópia de sombra persistente da linha de comando e usar o script CMD para expô-la.

1.  **vshadow -p -nw -script=SETVAR1.cmd c:**
2.  **chame SETVAR1.cmd**
3.  **C: \\>vshadow -el=%VSHADOW \_ ID \_ 1%,c: \\ directory1**

## <a name="accessing-nonpersistent-shadow-copies"></a>Acessando cópias de sombra não persistentes

Cópias de sombra não persistentes são excluídas automaticamente quando o programa que as cria (nesse caso, VShadow) é excluído. Para acessar o conteúdo dessas cópias de sombra, o VShadow permite que você execute um script depois que as cópias de sombra são criadas, mas antes que o programa VShadow saia.

O exemplo a seguir mostra como usar a opção de linha de comando -exec para executar um script chamado "enum.cmd":

**vshadow -nw -exec=enum.cmd c:**

No script executado, você também pode executar o script SETVAR gerado neste comando personalizado. Isso permite que o script acesse o conteúdo das cópias de sombra diretamente. Lembre-se de que o dispositivo de sombra pode ser recuperado da variável de ambiente \_ \_ NNN VSHADOW DEVICE.

Veja um exemplo de script enum.cmd:

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

Aqui está a linha de comando para executar o script enum.cmd:

**vshadow -nw -exec=c: \\ enum.cmd -script=setvar1.cmd c:**

## <a name="copying-a-file-from-a-shadow-copy"></a>Copiando um arquivo de uma cópia de sombra

O exemplo a seguir mostra como copiar um arquivo de uma cópia de sombra.

1.  **dir > c: \\somefile.txt**
2.  **vshadow -p -nw -script=SETVAR1.cmd c:**
3.  **chame SETVAR1.cmd**
4.  **copy %VSHADOW \_ DEVICE \_ 1% \\somefile.txt c: \\ somefile \_bak.txt**

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a>Enumerando todos os arquivos em um dispositivo de cópia de sombra

O exemplo a seguir mostra como enumerar todos os arquivos em um dispositivo de cópia de sombra de um arquivo em lotes.

1.  **dir > c: \\somefile.txt**
2.  **vshadow -p -nw -script=SETVAR1.cmd c:**
3.  **chame SETVAR1.cmd**
4.  **para /R %VSHADOW \_ DEVICE \_ 1% \\ %i em ( \* ) do @echo %%i**

## <a name="importing-a-transportable-shadow-copy"></a>Importando uma cópia de sombra transportável

Para criar uma cópia de sombra transportável em um computador e importá-la para outro computador, você deve ter dois computadores conectados (por meio de uma configuração de SAN) a uma matriz de armazenamento que dá suporte a cópias de sombra de hardware do VSS. Um provedor de hardware VSS deve ser instalado em cada computador.

O exemplo a seguir mostra como criar e importar a cópia de sombra.

1.  Crie o conjunto de cópias de sombra no computador A (o servidor de produção) digitando o seguinte comando após o prompt de comando:

    **vshadow -p -t=bc1.xml**

    Isso não exporá nenhum dispositivo de cópia de sombra no computador A.

2.  Copie o documento de componentes de backup (bc1.xml) do computador A para o computador B.
3.  Importe o conjunto de sombras no computador B digitando o seguinte comando:

    **vshadow -i=bc1.xml**

Opcionalmente, você pode expor essas cópias de sombra como letras de unidade ou pastas montadas. Além disso, você pode potencialmente quebrar o conjunto de sombras para fazer com que os novos volumes de cópia de sombra leiam e escrevam.

Para automatizar o processo de gerenciamento do conjunto de sombras, você pode usar a opção de linha de **comando -script** para gerar o script CMD que contém as IDs de cópia de sombra. Em seguida, você pode copiar o script gerado juntamente com os componentes de backup para o outro computador.

O exemplo a seguir mostra como criar, expor e quebrar cópias de sombra transportáveis usando scripts CMD.

1.  Crie o conjunto de cópias de sombra no computador A (o servidor de produção) na linha de comando da seguinte forma:

    **vshadow -p -t=bc1.xml -script=sc1.cmd**

    Especifique **a opção -script** para gerar o script que contém as definições de variável de ambiente apropriadas. Observe que isso não exporá nenhum dispositivo de cópia de sombra no computador A.

2.  Copie o documento de componentes de backup (bc1.xml) e o script gerado (sc1.cmd) do computador A para o computador B.
3.  Importe o conjunto de sombras no computador B digitando o seguinte comando:

    **vshadow -i=bc1.xml**

    Isso vai aparecer nos dispositivos criados no computador B.

4.  Execute o script gerado para definir as variáveis de ambiente para o conjunto de cópia de sombra digitando o nome do arquivo no prompt de comando, como no exemplo a seguir:

    **sc1.cmd**

    Isso definirá as variáveis de ambiente relevantes, conforme descrito em Acessar propriedades de cópia de sombra de um script CMD.

5.  Exponha as cópias de sombra no computador B digitando os seguintes comandos:
    1.  **rmdir /s c: \\ ponto de \_ montagem**
    2.  **mkdir c: \\ ponto de \_ montagem**
    3.  **vshadow –el=%VSHADOW \_ ID \_ 1%,c: \\ ponto de \_ montagem**

    Isso vai aparecer nos dispositivos de cópia de sombra criados no computador B.
6.  Quebre o conjunto de cópia de sombra para tornar os volumes que podem ser escritos digitando o seguinte **comando: C: \\>vshadow –bw=%VSHADOW \_ SET \_ ID%**

Observe que cópias de sombra transportáveis não persistentes também podem ser importadas, mas elas são excluídas automaticamente quando o processo **vshadow** **-i** é final. Para importar as cópias de sombra antes que elas sejam excluídas, você deve usar a opção de linha de comando **-exec,** conforme descrito em Acessar Cópias de Sombra NãoPersistentes.

## <a name="including-writers-or-components"></a>Incluindo autores ou componentes

Por padrão, todos os autores participam da criação da cópia de sombra. Para determinar quais autores e componentes serão incluídos em um conjunto de cópias de sombra, use a opção de linha de comando **-wm** ou **-wm2,** conforme descrito em [Listing Writer Status and Metadata](vshadow-tool-and-sample.md).

Para verificar se todos os componentes de um autor estão incluídos, use o sinalizador **opcional -wi** em qualquer um dos seguintes formatos:

-   **vshadow** **-wi** *WriterName*
-   **vshadow** **-wi** **" Writer**_Name String_*_"_*
-   **vshadow** **-wi** **{**_WriterID_*_}_*
-   **vshadow** **-wi** **{**_InstanceID_*_}_*

Para verificar se componentes específicos estão incluídos, use o **sinalizador opcional -wi** em qualquer um dos seguintes formatos:

-   **vshadow** **-wi** *WriterName***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-wi** **"** Writer Name _String_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wi** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wi** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

Os exemplos a seguir mostram como usar o **sinalizador opcional -wi.**

-   Especificando *WriterName:* \\ *LogicalPath* \\ *ComponentName:*

    **vshadow -wi="Registry Writer: \\ Registry"**

-   Especificando {*WriterID*}:

    **vshadow -wi={BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Especificando mais de um autor ou componente:

    **vshadow -wi="Registry Writer: \\ Registry" -wi="COM+ REGDB Writer"**

## <a name="excluding-writers-or-components"></a>Excluindo autores ou componentes

Para excluir todos os autores, use o **sinalizador opcional -nw** ao criar a cópia de sombra.

Para excluir todos os componentes de um autor, use o **sinalizador opcional -wx** em qualquer um dos seguintes formatos:

-   **vshadow** **-wx** *WriterName*
-   **vshadow** **-wx** **" Writer**_Name String_*_"_*
-   **vshadow** **-wx** **{**_WriterID_*_}_*
-   **vshadow** **-wx** **{**_InstanceID_*_}_*

Para excluir componentes específicos, use **o sinalizador opcional -wx** em qualquer um dos seguintes formatos:

-   **vshadow** **-wx** *WriterName***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-wx** **"** Writer Name _String_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wx** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wx** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

Os exemplos a seguir mostram como usar o **sinalizador opcional -wx.**

-   Especificando *WriterName:* \\ *LogicalPath* \\ *ComponentName:*

    **vshadow -wx="Registry Writer: \\ Registry"**

-   Especificando {*WriterID*}:

    **vshadow -wx={BE000CBE-11FE-4426-9C58-531AAA6355FC4}**

-   Especificando mais de um autor ou componente:

    **vshadow -wx="Registry Writer: \\ Registry" -wx="COM+ REGDB Writer"**

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a>Conjuntos de cópias de sombra de quebra usando o método BreakSnapshotSetEx

Os exemplos a seguir mostram como usar a opção de linha de comando **-bex.**

-   Especificando que o LUN de cópia de sombra será mascarado do host:

    **vshadow** **-bex** **-mask**

-   Especificando que o LUN de cópia de sombra será exposto ao host como um volume de leitura/gravação:

    **vshadow** **-bex** **-rw**

-   Especificando que o LUN de cópia de sombra será exposto ao host como um volume de leitura/gravação e que nenhuma das assinaturas de disco nos LUNs de cópia de sombra será revertida para a dos LUNs originais:

    **vshadow** **-bex** **-norevert**

 

 
