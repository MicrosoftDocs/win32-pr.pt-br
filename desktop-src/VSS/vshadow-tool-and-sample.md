---
description: VShadow é uma ferramenta de linha de comando que você pode usar para criar e gerenciar cópias de sombra de volume.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Ferramenta VShadow e exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7a9a697ecdf39f91d43fa0c66faebd37cfbfed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461136"
---
# <a name="vshadow-tool-and-sample"></a>Ferramenta VShadow e exemplo

VShadow é uma ferramenta de linha de comando que você pode usar para criar e gerenciar cópias de sombra de volume.

> [!Note]  
> O VShadow está incluído no Microsoft Windows Software Development Kit (SDK) para Windows Vista e posterior. O SDK 7,2 do VSS inclui uma versão do VShadow que é executada somente no Windows Server 2003. Para obter informações sobre como baixar o SDK do Windows e o SDK 7,2 do VSS, consulte [serviço de cópias de sombra de volume](volume-shadow-copy-service-portal.md).

 

A ferramenta VShadow usa opções de linha de comando e sinalizadores opcionais para identificar o trabalho a ser executado. Quando usado sem nenhuma opção de linha de comando, o comando VShadow cria um novo conjunto de cópias de sombra.

Os comandos VShadow executam as seguintes operações:

-   [Criando um conjunto de cópias de sombra](#creating-a-shadow-copy-set)
-   [Importando um conjunto de cópias de sombra](#importing-a-shadow-copy-set)
-   [Consultando Propriedades de cópia de sombra](#querying-shadow-copy-properties)
-   [Excluindo cópias de sombra](#deleting-shadow-copies)
-   [Quebrando um conjunto de cópias de sombra](#breaking-a-shadow-copy-set)
-   [Quebrando um conjunto de cópias de sombra usando o método BreakSnapshotSetEx](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [Expondo uma cópia de sombra localmente](#exposing-a-shadow-copy-locally)
-   [Expondo uma cópia de sombra remotamente](#exposing-a-shadow-copy-remotely)
-   [Listando os metadados e o status do gravador](#listing-writer-status-and-metadata)
-   [Executando operações de restauração](#performing-restore-operations)
-   [Revertendo para uma cópia de sombra anterior](#reverting-to-a-previous-shadow-copy)
-   [Ressincronizando LUNs](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a>Criando um conjunto de cópias de sombra

**vshadow** \[ OptionalFlags \] *volumelist*

Este comando cria um novo conjunto de cópias de sombra.

*Volumelist* é uma lista de nomes de volume. VShadow cria uma cópia de sombra para cada volume na lista. Um nome de volume pode, opcionalmente, ser encerrado com uma barra invertida ( \\ ). Por exemplo, C: e C: \\ são nomes de volume válidos. Você também pode especificar pastas montadas (por exemplo, C: \\ DirectoryName) ou nomes de GUID de volume (por exemplo, \\ \\ ? \\ Volume {edbed95e-7e8d-11D8-9d01-505054503030}).

*OptionalFlags* é um bitmask de valores de sinalizador opcionais da tabela a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor de sinalizador opcional</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-ad"></span><span id="-AD"></span><strong>-AD</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias de sombra de hardware diferenciais. Esse sinalizador e o sinalizador <strong>-AP</strong> são mutuamente exclusivos.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-ap"></span><span id="-AP"></span><strong>-AP</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias de sombra de hardware de plex. Esse sinalizador e o sinalizador <strong>-ad</strong> são mutuamente exclusivos.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-BC =</strong><em>File</em><strong>. xml</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias de sombra não transportáveis e armazena o documento de componentes de backup no arquivo especificado. Esse arquivo pode ser usado em uma operação de restauração subsequente. Esse sinalizador e o sinalizador <strong>-t</strong> são mutuamente exclusivos.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec =</strong><em>comando</em><br/></td>
<td>Esse sinalizador opcional executa um comando ou script depois que as cópias de sombra são criadas, mas antes da ferramenta VShadow ser encerrada. O <em>comando</em> pode especificar um comando shell executável ou um arquivo cmd. Se ele especificar um comando do Shell, nenhum parâmetro de comando poderá ser especificado.<br/>
<blockquote>
[!Note]<br />
Por motivos de segurança e para manter a implementação simples, o sinalizador opcional <strong>-exec</strong> não aceitará parâmetros a serem passados para o comando ou script. A cadeia de caracteres inteira passada para o sinalizador opcional <strong>-exec</strong> é tratada como um único arquivo cmd ou exe. Para obter mais informações sobre essa limitação, consulte o código-fonte VShadow.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong><br/></td>
<td>Esse sinalizador opcional especifica que a operação de cópia de sombra deve ser concluída somente se todas as assinaturas de disco puderem ser revertidas.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Sem suporte.<br/></td>
</tr>
<tr class="even">
<td><span id="-mask"></span><span id="-MASK"></span><strong>-máscara</strong><br/></td>
<td>Esse sinalizador opcional especifica que os LUNs de cópia de sombra devem ser mascarados do computador quando o conjunto de cópias de sombra for rompido.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Sem suporte.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias de sombra sem recuperação automática. Para obter mais informações sobre essa opção, consulte a documentação do sinalizador de VSS_VOLSNAP_ATTR_NO_AUTORECOVERY da enumeração <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong><br/></td>
<td>Esse sinalizador opcional especifica que as assinaturas de disco não devem ser revertidas.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Sem suporte.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nw"></span><span id="-NW"></span><strong>-NW</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias de sombra sem envolver gravadores. Para obter mais informações sobre cópias de sombra sem participação no gravador, consulte <a href="shadow-copy-creation-details.md">detalhes da criação da cópia de sombra</a>. Esse sinalizador e os sinalizadores <strong>-Wi</strong> e <strong>-WX</strong> são mutuamente exclusivos.<br/></td>
</tr>
<tr class="even">
<td><span id="-p"></span><span id="-P"></span><strong>-p</strong><br/></td>
<td>Esse sinalizador opcional especifica <a href="vssgloss-p.md"><em>cópias de sombra persistentes</em></a>.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-rw"></span><span id="-RW"></span><strong>-RW</strong><br/></td>
<td>Esse sinalizador opcional especifica que os LUNs de cópia de sombra devem se tornar de leitura/gravação quando o conjunto de cópias de sombra é rompido.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Sem suporte.<br/></td>
</tr>
<tr class="even">
<td><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong><br/></td>
<td>Esse sinalizador opcional especifica <a href="vssgloss-c.md"><em>cópias de sombra acessíveis ao cliente</em></a>.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script =</strong><em>File</em><strong>. cmd</strong><br/></td>
<td>Esse sinalizador opcional gera um arquivo CMD contendo variáveis de ambiente relacionadas às cópias de sombra criadas, como IDs de cópia de sombra e IDs de conjunto de cópias de sombra.<br/></td>
</tr>
<tr class="even">
<td><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t =</strong><em>File</em><strong>. xml</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias de sombra transportáveis e armazena o documento de componentes de backup no arquivo especificado pelo parâmetro <em>File.xml</em> . Esse arquivo pode ser usado em uma operação de importação e/ou restauração subsequente. Esse sinalizador e o sinalizador <strong>-BC</strong> são mutuamente exclusivos.<br/> <strong>Windows server 2003, Standard Edition e Windows server 2003, Web Edition:</strong> Não há suporte para cópias de sombra transportáveis. Todas as edições do Windows Server 2003 com Service Pack 1 (SP1) oferecem suporte a cópias de sombra transportáveis.<br/></td>
</tr>
<tr class="odd">
<td><span id="-tr"></span><span id="-TR"></span><strong>-TR</strong><br/></td>
<td>Esse sinalizador opcional especifica que a recuperação TxF deve ser imposta durante a criação da cópia de sombra.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-tracing"></span><span id="-TRACING"></span><strong>-rastreamento</strong><br/></td>
<td>Esse sinalizador opcional gera uma saída detalhada que pode ser usada para solução de problemas.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wait"></span><span id="-WAIT"></span><strong>-aguardar</strong><br/></td>
<td>Esse sinalizador opcional faz com que a ferramenta VShadow aguarde a confirmação do usuário antes de sair.<br/></td>
</tr>
<tr class="even">
<td><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-Wi =</strong><em>gravador</em><br/></td>
<td>Esse sinalizador opcional verifica se o gravador ou o componente especificado está incluído na cópia de sombra. O <em>gravador</em> pode especificar um caminho de componente, o nome do gravador, a ID do gravador ou a ID da instância do gravador. Esse sinalizador e o sinalizador <strong>-NW</strong> são mutuamente exclusivos.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-WX =</strong><em>gravador</em><br/></td>
<td>Esse sinalizador opcional verifica se o gravador ou o componente especificado foi excluído da cópia de sombra. O <em>gravador</em> pode especificar um caminho de componente, o nome do gravador, a ID do gravador ou a ID da instância do gravador. Esse sinalizador e o sinalizador <strong>-NW</strong> são mutuamente exclusivos.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a>Importando um conjunto de cópias de sombra

**vshadow** \[ OptionalFlags \] **-i =**_File_*_. xml_*

A opção de linha de comando **-i** importa um conjunto de cópia de sombra transportável.

> [!Note]  
> Essa opção de linha de comando tem suporte apenas em sistemas operacionais Windows Server.

 

O arquivo de *File.xml* deve ser um arquivo de documento de componentes de backup para um conjunto de cópias de sombra transportáveis criado com o sinalizador opcional **-t** ou **-BC** .

Um conjunto de cópias de sombra é uma [*cópia de sombra persistente*](vssgloss-p.md) se foi criado com o sinalizador **-p** opcional. Se o conjunto de cópia de sombra transportável for não persistente, ele aparecerá por um curto período enquanto o comando de criação de cópia de sombra estiver em execução e será excluído automaticamente quando o comando retornar. Você pode importar cópias de sombra não persistentes somente durante a criação da cópia de sombra, criando o conjunto de cópias de sombra usando o sinalizador opcional **-exec** para executar um arquivo cmd que chama VShadow **-i**.

A opção de linha de comando **-i** não pode ser combinada com outras opções de linha de comando.

*OptionalFlags* é um bitmask de valores de sinalizador opcionais da tabela a seguir.



| Valor de sinalizador opcional                                                                                                            | Descrição                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_comando_<br/> | Esse sinalizador opcional executa um comando ou script depois que as cópias de sombra são importadas, mas antes da ferramenta VShadow ser encerrada. O *comando* pode especificar um comando shell executável ou um arquivo cmd. Se ele especificar um comando do Shell, nenhum parâmetro de comando poderá ser especificado.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-rastreamento**<br/>                                                  | Esse sinalizador opcional gera uma saída detalhada que pode ser usada para solução de problemas.<br/>                                                                                                                                                                                 |
| <span id="-wait"></span><span id="-WAIT"></span>**-aguardar**<br/>                                                           | Esse sinalizador opcional faz com que a ferramenta VShadow aguarde a confirmação do usuário antes de sair.<br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a>Consultando Propriedades de cópia de sombra

**vshadow** **-q**

**vshadow** **-qx =**_ShadowCopySetId_

**vshadow** **-s =**_ShadowCopyId_

A opção de linha de comando **-q** lista as propriedades de todas as cópias de sombra no computador.

A opção de linha de comando **-qx** lista as propriedades de todas as cópias de sombra no conjunto de cópias de sombra cuja ID é especificada por *ShadowCopySetId*.

A opção de linha de comando **-s** lista as propriedades da cópia de sombra cuja ID é especificada por *ShadowCopyId*.

Essas opções de linha de comando usam uma combinação de [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) e [**IVssBackupComponents:: getsnapshotproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) para obter as propriedades do conjunto de cópias de sombra fornecido.

As opções de linha de comando **-q**, **-qx** e **-s** são mutuamente exclusivas e não podem ser combinadas com outras opções de linha de comando.

## <a name="deleting-shadow-copies"></a>Excluindo cópias de sombra

**vshadow** **-da**

**vshadow** **-do**

**vshadow** **-DX =**_ShadowCopySetId_

**vshadow** **-DS =**_ShadowCopyId_

O comando **-da** exclui todas as cópias de sombra no computador.

> [!Note]  
> A opção de linha de comando **-da** requer a confirmação do usuário.

 

A opção de linha de comando **-** do exclui a cópia de sombra mais antiga no computador.

A opção de linha de comando **-DX** exclui todas as cópias de sombra no conjunto de cópias de sombra cuja ID é especificada por *ShadowCopySetId*.

A opção de linha de comando **-DS** exclui a cópia de sombra cuja ID é especificada por *ShadowCopyId*.

Essas opções de linha de comando são para uso somente com [*cópias de sombra persistentes*](vssgloss-p.md) . As cópias de sombra não persistentes não precisam ser excluídas explicitamente, pois são excluídas automaticamente quando o comando de criação de VShadow é encerrado.

As opções de linha de comando **-da**, **-do**, **-DX** e **-DS** são mutuamente exclusivas e não podem ser combinadas com outras opções de linha de comando.

## <a name="breaking-a-shadow-copy-set"></a>Quebrando um conjunto de cópias de sombra

**vshadow** **-b =**_ShadowCopySetId_

**vshadow** **-BW =**_ShadowCopySetId_

A opção de linha de comando **-b =**_ShadowCopySetId_ converte cada cópia de sombra no conjunto de cópias de sombra em um volume autônomo somente leitura.

A opção de linha de comando **-BW =**_ShadowCopySetId_ converte cada cópia de sombra no conjunto de cópias de sombra em um volume gravável autônomo.

> [!Note]  
> As opções de linha de comando **-b** e **-BW** têm suporte apenas em sistemas operacionais Windows Server.

 

Para obter informações sobre como dividir um conjunto de cópias de sombra, consulte [quebrando cópias de sombra](breaking-shadow-copies.md).

Depois que o conjunto de cópias de sombra é interrompido, o conjunto de cópias de sombra e as cópias de sombra individuais não existem mais e não podem ser gerenciados usando comandos VSS.

Um conjunto de cópias de sombra será persistente se tiver sido criado com o sinalizador **-p** opcional. Se o conjunto de cópia de sombra transportável for não persistente, ele aparecerá por um curto período enquanto o comando de criação de cópia de sombra estiver em execução e será excluído automaticamente quando o comando retornar. Você pode dividir conjuntos de cópias de sombra não persistentes somente durante a criação da cópia de sombra, criando o conjunto de cópias de sombra usando o sinalizador opcional **-exec** para executar um arquivo cmd que chama **vshadow** **-b** ou **vshadow** **-BW**.

As opções de linha de comando **-b** e **-BW** são mutuamente exclusivas e não podem ser combinadas com outras opções de linha de comando.

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a>Quebrando um conjunto de cópias de sombra usando o método BreakSnapshotSetEx

**vshadow** **-Bex**

A opção de linha de comando **-Bex** quebra um conjunto de cópias de sombra de acordo com as opções especificadas pelos sinalizadores opcional **-Mask**, **-RW**, **-forcerevert** e **-norevert** . Essa opção de linha de comando é semelhante às opções de linha de comando **-b** e **-BW** . A opção de linha de comando **-Bex** usa o método [**IVssBackupComponentsEx2:: BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) , enquanto as opções de linha de comando **-b** e **-BW** usam o método [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .

Para obter informações sobre como dividir um conjunto de cópias de sombra, consulte [quebrando cópias de sombra](breaking-shadow-copies.md).

> [!Note]  
> A opção de linha de comando **-Bex** tem suporte apenas em sistemas operacionais Windows Server.

 

**vshadow** **-Bex** **-Mask**

O sinalizador **-Mask** especifica que o LUN de cópia de sombra será mascarado do host. Se o sinalizador **-Mask** for especificado, os sinalizadores **-RW**, **-forcerevert** e **-norevert** não poderão ser especificados.

**vshadow** **-Bex** **-RW**

O sinalizador **-RW** especifica que o LUN de cópia de sombra será exposto ao host como um volume de leitura/gravação.

**vshadow** **-Bex** **-forcerevert**

O sinalizador **-forcerevert** especifica que os identificadores de disco de todos os LUNs de cópia de sombra serão revertidos para os LUNs originais. No entanto, se qualquer um dos LUNs originais estiver presente no sistema, a operação falhará e nenhum dos identificadores será revertido. Esse sinalizador e o sinalizador **-norevert** são mutuamente exclusivos.

**vshadow** **-Bex** **-norevert**

O sinalizador **-norevert** especifica que nenhum dos identificadores de disco do LUN de cópia de sombra será revertido. Esse sinalizador e o sinalizador **-forcerevert** são mutuamente exclusivos.

## <a name="exposing-a-shadow-copy-locally"></a>Expondo uma cópia de sombra localmente

**vshadow** **-El =**_ShadowCopyId_*_,_*_LocalEmptyDirectory_

 **vshadow** **-El =**_ShadowCopyId_*_,_*_UnusedDriveLetter_

A opção de linha de comando **-El** atribui uma pasta montada ou uma letra da unidade a uma cópia de sombra persistente. Observe que o conteúdo do volume permanecerá somente leitura, a menos que você chame subseqüentemente o **vshadow** **-BW** para interromper o conjunto de cópias de sombra.

> [!Note]  
> As cópias de sombra não persistentes e as [*cópias de sombra acessíveis ao cliente*](vssgloss-c.md) não podem ser expostas localmente.

 

Por exemplo, se {edbed95e-7e8d-11D8-9d01-505054503030} for o GUID de uma cópia de sombra persistente existente e X: for uma letra de unidade não usada, o comando a seguir expõe a cópia de sombra em X:

**vshadow** **-El = {edbed95e-7e8d-11D8-9d01-505054503030}, x:**

O exemplo a seguir mostra como expor a mesma cópia de sombra na pasta montada C: \\ ShadowCopies \\ June23:

**mkdir c: \\ ShadowCopies \\ June23**

**vshadow** **-El = {edbed95e-7e8d-11D8-9d01-505054503030}, c: \\ ShadowCopies \\ June23**

A opção de linha de comando **-El** não pode ser combinada com outras opções de linha de comando.

## <a name="exposing-a-shadow-copy-remotely"></a>Expondo uma cópia de sombra remotamente

**vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_

 **vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_

A opção de linha de comando **-er** atribui um nome de compartilhamento somente leitura ao diretório raiz (ou um subdiretório) da cópia de sombra. Observe que o conteúdo do compartilhamento permanecerá somente leitura, a menos que você chame subseqüentemente o **vshadow** **-BW** para interromper o conjunto de cópias de sombra.

> [!Note]  
> As [*cópias de sombra acessíveis ao cliente*](vssgloss-c.md) não podem ser expostas remotamente.

 

Por exemplo, se {edbed95e-7e8d-11D8-9d01-505054503030} for o GUID de uma cópia de sombra persistente existente e o compartilhamento \_ 123 for um nome de compartilhamento não usado, o comando a seguir exporá a cópia de sombra em compartilhamento \_ 123:

**vshadow** **-er = {edbed95e-7e8d-11D8-9d01-505054503030}, compartilhamento \_ 123**

O exemplo a seguir mostra como expor apenas uma subárvore (denominada "Pasta1 \\ Pasta2") da mesma cópia de sombra no mesmo compartilhamento:

**vshadow** **-er = {edbed95e-7e8d-11D8-9d01-505054503030}, compartilhamento \_ 123, Pasta1 \\ Pasta2**

A opção de linha de comando **-er** não pode ser combinada com outras opções de linha de comando.

## <a name="listing-writer-status-and-metadata"></a>Listando os metadados e o status do gravador

**vshadow** **-WS**

**vshadow** **-WM**

**vshadow** **-wm2**

**vshadow** **-WM3**

A opção de linha de comando **-WS** enumera os gravadores VSS que estão sendo executados no computador e descreve seu estado. Esse comando é equivalente ao comando [VSSadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) . Há seis possíveis valores de Estado: estável, com falha, desconhecido, aguardando congelamento, congelado e aguardando a conclusão.

A opção de linha de comando **-WM** lista um resumo dos metadados do gravador, incluindo os volumes afetados.

A opção de linha de comando **-wm2** lista todos os metadados do gravador.

A opção de linha de comando **-WM3** lista todos os metadados do gravador no formato XML bruto.

**Windows Vista e Windows Server 2003:** Não há suporte para a opção de linha de comando **-WM3** .

Você pode usar essas informações para determinar quais volumes incluir no conjunto de cópias de sombra de volume.

> [!Note]  
> Se o estado do gravador for estável ou aguardando a conclusão, o gravador poderá ser considerado em um estado estável, pronto para o próximo backup.

 

As opções de linha de comando **-WS**, **-WM**, **-wm2** e **-WM3** são mutuamente exclusivas e não podem ser combinadas com outras opções de linha de comando.

## <a name="performing-restore-operations"></a>Executando operações de restauração

**vshadow** \[ OptionalFlags \] **-r =**_File_*_. xml_*

**vshadow** \[ OptionalFlags \] **-RS =**_File_*_. xml_*

A opção de linha de comando **-r** executa uma operação de restauração.

A opção de linha de comando **-RS** executa uma operação de restauração simulada.

O arquivo de *File.xml* deve ser um arquivo de documento de componentes de backup para um conjunto de cópias de sombra que foi criado com o sinalizador opcional **-t** ou **-BC** .

As opções de linha de comando **-r** e **-RS** são mutuamente exclusivas e não podem ser combinadas com outras opções de linha de comando.

*OptionalFlags* é um bitmask de valores de sinalizador opcionais da tabela a seguir.



| Valor de sinalizador opcional                                                                                                            | Descrição                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-Wi =**_gravador_<br/>             | Esse sinalizador opcional verifica se o gravador ou o componente especificado está incluído na restauração. O *gravador* pode especificar um caminho de componente, o nome do gravador, a ID do gravador ou a ID da instância do gravador.<br/>                                                                                    |
| <span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-WX =**_gravador_<br/>             | Esse sinalizador opcional verifica se o gravador ou o componente especificado foi excluído da restauração. O *gravador* pode especificar um caminho de componente, o nome do gravador, a ID do gravador ou a ID da instância do gravador.<br/>                                                                                  |
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_comando_<br/> | Esse sinalizador opcional executa um comando ou script entre os eventos de pré e pós-restauração que são enviados aos gravadores. O *comando* pode especificar um comando shell executável ou um arquivo cmd. Se ele especificar um comando do Shell, nenhum parâmetro de comando poderá ser especificado.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-rastreamento**<br/>                                                  | Esse sinalizador opcional gera uma saída detalhada que pode ser usada para solução de problemas.<br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a>Revertendo para uma cópia de sombra anterior

**vshadow** **-REVERT =**_ShadowCopyId_

> [!Note]  
> Essa opção de linha de comando tem suporte apenas em sistemas operacionais Windows Server.

 

**Windows server 2008 e Windows server 2003:** Sem suporte.

A opção **-reverter** linha de comando reverte um volume para a cópia de sombra anterior cuja ID é especificada por *ShadowCopyId*.

A opção de linha de comando **-REVERT** não pode ser combinada com outras opções de linha de comando.

## <a name="resynchronizing-luns"></a>Ressincronizando LUNs

**vshadow** **-addresync =**_ShadowCopyId_ **-Ressync =**_BCDFileName_ \[ OptionalResyncFlags\]

**vshadow** **-addresync =**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-Ressync =**_BCDFileName_ \[ OptionalResyncFlags\]

A opção de linha de comando **-addresync** especifica os volumes a serem incluídos em uma operação de ressincronização de LUN. O parâmetro *ShadowCopyId* especifica o identificador da cópia de sombra. O parâmetro opcional *TargetVolumeDriveLetter* especifica o volume de destino onde o conteúdo do volume da cópia de sombra deve ser copiado.

A opção de linha de comando **-Ressync** inicia uma operação de ressincronização de LUN. Depois que a operação for concluída, a assinatura de cada LUN de destino deverá ser idêntica à do LUN de volume de destino. O parâmetro *BCDFileName* especifica o nome do arquivo XML que contém o documento do componente de backup.

> [!Note]  
> As opções de linha de comando **-addresync** e **-Ressync** só têm suporte em sistemas operacionais Windows Server.

 

**Windows server 2008 e Windows server 2003:** Sem suporte.

*OptionalResyncFlags* é um bitmask de valores de sinalizador opcionais da tabela a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor de sinalizador opcional</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong><br/></td>
<td>Esse sinalizador opcional especifica que, após a conclusão da operação, a assinatura de cada LUN de destino deve ser idêntica à do LUN original que foi usado para criar a cópia de sombra, não o LUN de volume de destino.<br/>
<blockquote>
[!Note]<br />
O sinalizador <strong>-revertsig</strong> tem suporte apenas em sistemas operacionais Windows Server.
</blockquote>
<br/> <strong>Windows server 2008 e Windows server 2003:</strong> Sem suporte.<br/></td>
</tr>
<tr class="even">
<td><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong><br/></td>
<td>Esse sinalizador opcional especifica que o serviço VSS não deve verificar se há volumes não selecionados que seriam substituídos pela operação de ressincronização de LUN.<br/>
<blockquote>
[!Note]<br />
O sinalizador <strong>-novolcheck</strong> tem suporte apenas em sistemas operacionais Windows Server.
</blockquote>
<br/> <strong>Windows server 2008 e Windows server 2003:</strong> Sem suporte.<br/></td>
</tr>
</tbody>
</table>



 

 

 
