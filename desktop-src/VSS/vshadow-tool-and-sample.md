---
description: O VShadow é uma ferramenta de linha de comando que você pode usar para criar e gerenciar cópias de sombra de volume.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Ferramenta VShadow e exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306d759d10875b03cb0d2e4e2064a85614400ff5240800da3fc4c1ce94add8c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998065"
---
# <a name="vshadow-tool-and-sample"></a>Ferramenta VShadow e exemplo

O VShadow é uma ferramenta de linha de comando que você pode usar para criar e gerenciar cópias de sombra de volume.

> [!Note]  
> O VShadow está incluído no SDK (Software Development Kit) do Microsoft Windows para Windows Vista e posterior. O SDK do VSS 7.2 inclui uma versão do VShadow que é executado somente no Windows Server 2003. Para obter informações sobre como baixar o SDK do Windows e o SDK do VSS 7.2, [consulte Serviço de Cópias de Sombra de Volume](volume-shadow-copy-service-portal.md).

 

A ferramenta VShadow usa opções de linha de comando e sinalizadores opcionais para identificar o trabalho a ser executar. Quando usado sem opções de linha de comando, o comando VShadow cria um novo conjunto de cópias de sombra.

Os comandos VShadow executam as seguintes operações:

-   [Criando um conjunto de cópias de sombra](#creating-a-shadow-copy-set)
-   [Importando um conjunto de cópias de sombra](#importing-a-shadow-copy-set)
-   [Consultando propriedades de cópia de sombra](#querying-shadow-copy-properties)
-   [Excluindo cópias de sombra](#deleting-shadow-copies)
-   [Quebrando um conjunto de cópias de sombra](#breaking-a-shadow-copy-set)
-   [Quebre um conjunto de cópias de sombra usando o método BreakSnapshotSetEx](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [Expondo uma cópia de sombra localmente](#exposing-a-shadow-copy-locally)
-   [Expondo uma cópia de sombra remotamente](#exposing-a-shadow-copy-remotely)
-   [Listando o status e os metadados do autor](#listing-writer-status-and-metadata)
-   [Executando operações de restauração](#performing-restore-operations)
-   [Revertendo para uma cópia de sombra anterior](#reverting-to-a-previous-shadow-copy)
-   [Ressincronizando LUNs](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a>Criando um conjunto de cópias de sombra

**vshadow** \[ OptionalFlags \] *VolumeList*

Esse comando cria um novo conjunto de cópias de sombra.

*VolumeList* é uma lista de nomes de volume. O VShadow cria uma cópia de sombra para cada volume na lista. Opcionalmente, um nome de volume pode ser encerrado com uma faixa invertida ( \\ ). Por exemplo, C: e C: \\ são nomes de volume válidos. Você também pode especificar pastas montadas (por exemplo, C: \\ DirectoryName) ou nomes GUID de volume (por exemplo, \\ \\ ? \\ Volume{edbed95e-7e8d-11d8-9d01-505054503030}).

*OptionalFlags* é um bitmask de valores de sinalizador opcionais da tabela a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor do sinalizador opcional</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias de sombra de hardware diferenciais. Esse sinalizador e o <strong>sinalizador -ap</strong> são mutuamente exclusivos.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador só tem suporte em sistemas operacionais Windows servidor.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-ap"></span><span id="-AP"></span><strong>-ap</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias de sombra de hardware do plex. Esse sinalizador e o <strong>sinalizador -ad</strong> são mutuamente exclusivos.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador só tem suporte em sistemas operacionais Windows servidor.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-bc=</strong><em>Arquivo</em> <strong>.xml</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias de sombra não transportáveis e armazena o Documento de Componentes de Backup no arquivo especificado. Esse arquivo pode ser usado em uma operação de restauração subsequente. Esse sinalizador e o <strong>sinalizador -t</strong> são mutuamente exclusivos.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador só tem suporte em sistemas operacionais Windows servidor.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>Comando -exec=</strong><em></em><br/></td>
<td>Esse sinalizador opcional executa um comando ou script depois que as cópias de sombra são criadas, mas antes que a ferramenta VShadow saia. <em>O</em> comando pode especificar um comando de shell executável ou um arquivo CMD. Se ele especificar um comando de shell, nenhum parâmetro de comando poderá ser especificado.<br/>
<blockquote>
[!Note]<br />
Por motivos de segurança e para manter a implementação simples, o sinalizador opcional <strong>-exec</strong> não aceitará parâmetros a serem passados para o comando ou script. Toda a cadeia de caracteres passada para <strong>o sinalizador opcional -exec</strong> é tratada como um único arquivo CMD ou EXE. Para obter mais informações sobre essa limitação, consulte o código-fonte do VShadow.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong><br/></td>
<td>Esse sinalizador opcional especifica que a operação de cópia de sombra deve ser concluída somente se todas as assinaturas de disco puderem ser revertidas.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador só tem suporte em sistemas operacionais Windows servidor.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Sem suporte.<br/></td>
</tr>
<tr class="even">
<td><span id="-mask"></span><span id="-MASK"></span><strong>-mask</strong><br/></td>
<td>Esse sinalizador opcional especifica que os LUNs de cópia de sombra devem ser mascarados do computador quando o conjunto de cópias de sombra for desfeito.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador só tem suporte em sistemas operacionais Windows servidor.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Sem suporte.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias de sombra sem recuperação automática. Para obter mais informações sobre essa opção, consulte a documentação do sinalizador VSS_VOLSNAP_ATTR_NO_AUTORECOVERY da <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>enumeração _VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> dados.<br/></td>
</tr>
<tr class="even">
<td><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong><br/></td>
<td>Esse sinalizador opcional especifica que as assinaturas de disco não devem ser revertidas.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador só tem suporte em sistemas operacionais Windows servidor.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Sem suporte.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nw"></span><span id="-NW"></span><strong>-nw</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias de sombra sem envolver os autores. Para obter mais informações sobre cópias de sombra sem a participação do autor, consulte <a href="shadow-copy-creation-details.md">Detalhes de criação da cópia de sombra.</a> Esse sinalizador e os <strong>sinalizadores -wi</strong> e <strong>-wx</strong> são mutuamente exclusivos.<br/></td>
</tr>
<tr class="even">
<td><span id="-p"></span><span id="-P"></span><strong>-p</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias <a href="vssgloss-p.md"><em>de sombra persistentes.</em></a><br/>
<blockquote>
[!Note]<br />
Esse sinalizador só tem suporte em sistemas operacionais Windows servidor.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-rw"></span><span id="-RW"></span><strong>-rw</strong><br/></td>
<td>Esse sinalizador opcional especifica que os LUNs de cópia de sombra devem ser feitos para leitura/gravação quando o conjunto de cópias de sombra for desfeito.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador só tem suporte em sistemas operacionais Windows servidor.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Sem suporte.<br/></td>
</tr>
<tr class="even">
<td><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias <a href="vssgloss-c.md"><em>de sombra acessíveis pelo cliente.</em></a><br/>
<blockquote>
[!Note]<br />
Esse sinalizador só tem suporte em sistemas operacionais Windows servidor.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script=</strong><em>Arquivo</em><strong>.cmd</strong><br/></td>
<td>Esse sinalizador opcional gera um arquivo CMD que contém variáveis de ambiente relacionadas às cópias de sombra criadas, como IDs de cópia de sombra e IDs do conjunto de cópias de sombra.<br/></td>
</tr>
<tr class="even">
<td><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t=</strong><em>Arquivo</em> <strong>.xml</strong><br/></td>
<td>Esse sinalizador opcional especifica cópias de sombra transportáveis e armazena o Documento de Componentes de Backup no arquivo especificado pelo parâmetro <em>File.xml</em> backup. Esse arquivo pode ser usado em uma operação subsequente de importação e/ou restauração. Esse sinalizador e o <strong>sinalizador -bc</strong> são mutuamente exclusivos.<br/> <strong>Windows Server 2003, Edição Standard e Windows Server 2003, Web Edition:</strong> Não há suporte para cópias de sombra transportáveis. Todas as edições do Windows Server 2003 com Service Pack 1 (SP1) são suportadas por cópias de sombra transportáveis.<br/></td>
</tr>
<tr class="odd">
<td><span id="-tr"></span><span id="-TR"></span><strong>-tr</strong><br/></td>
<td>Esse sinalizador opcional especifica que a recuperação TxF deve ser imposta durante a criação da cópia de sombra.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador só tem suporte em sistemas operacionais Windows servidor.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-tracing"></span><span id="-TRACING"></span><strong>-tracing</strong><br/></td>
<td>Esse sinalizador opcional gera uma saída detalhada que pode ser usada para solução de problemas.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wait"></span><span id="-WAIT"></span><strong>-wait</strong><br/></td>
<td>Esse sinalizador opcional faz com que a ferramenta VShadow aguarde a confirmação do usuário antes de sair.<br/></td>
</tr>
<tr class="even">
<td><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-wi=</strong><em>Writer</em><br/></td>
<td>Esse sinalizador opcional verifica se o autor ou componente especificado está incluído na cópia de sombra. <em>O</em> writer pode especificar um caminho de componente, o nome do autor, a ID do autor ou a ID da instância do autor. Esse sinalizador e o <strong>sinalizador -nw</strong> são mutuamente exclusivos.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-wx=</strong><em>Writer</em><br/></td>
<td>Esse sinalizador opcional verifica se o autor ou componente especificado foi excluído da cópia de sombra. <em>O</em> writer pode especificar um caminho de componente, o nome do autor, a ID do autor ou a ID da instância do autor. Esse sinalizador e o <strong>sinalizador -nw</strong> são mutuamente exclusivos.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a>Importando um conjunto de cópias de sombra

**vshadow** \[ OptionalFlags \] **-i=**_Arquivo_ *_.xml_*

A opção de linha de comando **-i** importa um conjunto de cópias de sombra transportável.

> [!Note]  
> Essa opção de linha de comando só tem suporte em sistemas operacionais Windows servidor.

 

O *File.xml* deve ser um arquivo de Documento de Componentes de Backup para um conjunto de cópias de sombra transportável que foi criado com o sinalizador opcional **-t** ou **-bc.**

Um conjunto de cópias de sombra [*será uma cópia de sombra persistente*](vssgloss-p.md) se tiver sido criado com o sinalizador opcional **-p.** Se o conjunto de cópias de sombra transportável for não persistente, ele será exibido por um curto período enquanto o comando de criação da cópia de sombra estiver em execução e será excluído automaticamente quando o comando retornar. Você pode importar cópias de sombra não persistentes somente durante a criação da cópia de sombra, criando o conjunto de cópias de sombra usando o sinalizador opcional **-exec** para executar um arquivo CMD que chama VShadow **-i**.

A opção de linha de comando **-i** não pode ser combinada com outras opções de linha de comando.

*OptionalFlags* é um bitmask de valores de sinalizador opcionais da tabela a seguir.



| Valor do sinalizador opcional                                                                                                            | Descrição                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**Comando -exec=**<br/> | Esse sinalizador opcional executa um comando ou script depois que as cópias de sombra são importadas, mas antes que a ferramenta VShadow saia. *O* comando pode especificar um comando de shell executável ou um arquivo CMD. Se ele especificar um comando de shell, nenhum parâmetro de comando poderá ser especificado.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-tracing**<br/>                                                  | Esse sinalizador opcional gera uma saída detalhada que pode ser usada para solução de problemas.<br/>                                                                                                                                                                                 |
| <span id="-wait"></span><span id="-WAIT"></span>**-wait**<br/>                                                           | Esse sinalizador opcional faz com que a ferramenta VShadow aguarde a confirmação do usuário antes de sair.<br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a>Consultando propriedades de cópia de sombra

**vshadow** **-q**

**vshadow** **-qx=**_ShadowCopySetId_

**vshadow** **-s=**_ShadowCopyId_

A opção de linha de comando **-q** lista as propriedades de todas as cópias de sombra no computador.

A opção de linha de **comando -qx** lista as propriedades de todas as cópias de sombra no conjunto de cópias de sombra cuja ID é especificada por *ShadowCopySetId.*

A opção de linha de comando **-s** lista as propriedades da cópia de sombra cuja ID é especificada por *ShadowCopyId.*

Essas opções de linha de comando usam uma combinação de [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) e [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) para obter as propriedades do conjunto de cópias de sombra determinado.

As opções de linha de comando **-q**, **-qx** e **-s** são mutuamente exclusivas e não podem ser combinadas com outras opções de linha de comando.

## <a name="deleting-shadow-copies"></a>Excluindo cópias de sombra

**vshadow** **-da**

**vshadow** **-do**

**vshadow** **-dx=**_ShadowCopySetId_

**vshadow** **-ds=**_ShadowCopyId_

O **comando -da** exclui todas as cópias de sombra no computador.

> [!Note]  
> A opção de linha de comando **-da** requer confirmação do usuário.

 

A opção de linha de comando **-do** exclui a cópia de sombra mais antiga no computador.

A opção de linha de **comando -dx** exclui todas as cópias de sombra no conjunto de cópias de sombra cuja ID é especificada por *ShadowCopySetId.*

A opção de linha de **comando -ds** exclui a cópia de sombra cuja ID é especificada por *ShadowCopyId.*

Essas opções de linha de comando são para uso somente [*com cópias de sombra persistentes.*](vssgloss-p.md) Cópias de sombra não persistentes não precisam ser excluídas explicitamente, pois são excluídas automaticamente quando o comando de criação VShadow é final.

As opções de linha de comando **-da**, **-do**, **-dx** e **-ds** são mutuamente exclusivas e não podem ser combinadas com outras opções de linha de comando.

## <a name="breaking-a-shadow-copy-set"></a>Quebrando um conjunto de cópias de sombra

**vshadow** **-b=**_ShadowCopySetId_

**vshadow** **-bw=**_ShadowCopySetId_

A opção de linha de comando **-b=**_ShadowCopySetId_ converte cada cópia de sombra no conjunto de cópia de sombra em um volume somente leitura autônomo.

A opção de linha de **comando -bw=**_ShadowCopySetId_ converte cada cópia de sombra no conjunto de cópia de sombra em um volume que pode ser escrito autônomo.

> [!Note]  
> As opções de linha de comando **-b** **e -bw** têm suporte apenas em sistemas operacionais Windows servidor.

 

Para obter informações sobre como quebrar um conjunto de cópias de sombra, consulte [Cópias de sombra de quebra.](breaking-shadow-copies.md)

Depois que o conjunto de cópias de sombra for desfeito, o conjunto de cópias de sombra e as cópias de sombra individuais não existirão mais e não poderão ser gerenciados usando comandos VSS.

Um conjunto de cópias de sombra será persistente se tiver sido criado com o **sinalizador opcional -p.** Se o conjunto de cópias de sombra transportável for não persistente, ele será exibido por um curto período enquanto o comando de criação da cópia de sombra estiver em execução e será excluído automaticamente quando o comando retornar. Você pode quebrar conjuntos de cópias de sombra não persistentes somente durante a criação da cópia de sombra, criando o conjunto de cópias de sombra usando o sinalizador opcional **-exec** para executar um arquivo CMD que chama **vshadow** **-b** **ou vshadow** **-bw**.

As **opções de** linha de comando **-b e -bw** são mutuamente exclusivas e não podem ser combinadas com outras opções de linha de comando.

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a>Quebre um conjunto de cópias de sombra usando o método BreakSnapshotSetEx

**vshadow** **-bex**

A opção de linha de **comando -bex** interrompe um conjunto de cópias de sombra de acordo com as opções especificadas pelos sinalizadores **opcional -mask**, **-rw**, **-forcerevert** e **-norevert.** Essa opção de linha de comando é semelhante às opções de linha de comando **-b** **e -bw.** A opção de linha de comando **-bex** usa o método [**IVssBackupComponentsEx2::BreakSnapshotSetEx,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) enquanto as opções de linha de comando **-b** e **-bw** usam o método [**IVssBackupComponents::BreakSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)

Para obter informações sobre como quebrar um conjunto de cópias de sombra, consulte [Cópias de sombra de quebra.](breaking-shadow-copies.md)

> [!Note]  
> A opção de linha de **comando -bex** só tem suporte em sistemas operacionais Windows servidor.

 

**vshadow** **-bex** **-mask**

O **sinalizador -mask** especifica que o LUN de cópia de sombra será mascarado do host. Se o **sinalizador -mask** for especificado, os sinalizadores **-rw**, **-forcerevert** e **-norevert** não poderão ser especificados.

**vshadow** **-bex** **-rw**

O **sinalizador -rw** especifica que o LUN de cópia de sombra será exposto ao host como um volume de leitura/gravação.

**vshadow** **-bex** **-forcerevert**

O **sinalizador -forcerevert** especifica que os identificadores de disco de todos os LUNs de cópia de sombra serão revertidos para os LUNs originais. No entanto, se qualquer um dos LUNs originais estiver presente no sistema, a operação falhará e nenhum dos identificadores será revertido. Esse sinalizador e o **sinalizador -norevert** são mutuamente exclusivos.

**vshadow** **-bex** **-norevert**

O **sinalizador -norevert** especifica que nenhum dos identificadores de disco LUN de cópia de sombra será revertido. Esse sinalizador e o **sinalizador -forcerevert** são mutuamente exclusivos.

## <a name="exposing-a-shadow-copy-locally"></a>Expondo uma cópia de sombra localmente

**vshadow** **-el=**_ShadowCopyId,_**_LocalEmptyDirectory_

 **vshadow** **-el=**_ShadowCopyId,_**_UnusedDriveLetter_

A opção de linha de comando **-el** atribui uma pasta montada ou uma letra da unidade a uma cópia de sombra persistente. Observe que o conteúdo do volume permanecerá somente leitura, a menos que você chame **posteriormente vshadow** **-bw** para quebrar o conjunto de cópias de sombra.

> [!Note]  
> Cópias de sombra não persistentes e cópias de sombra acessíveis ao cliente não podem ser [*expostas*](vssgloss-c.md) localmente.

 

Por exemplo, se {edbed95e-7e8d-11d8-9d01-505054503030} for o GUID de uma cópia de sombra persistente existente e X: for uma letra de unidade nãoutilada, o comando a seguir exporá a cópia de sombra em X:

**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},x:**

O exemplo a seguir mostra como expor a mesma cópia de sombra na pasta montada C: \\ ShadowCopies \\ june23:

**mkdir c: \\ ShadowCopies \\ june23**

**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},c: \\ ShadowCopies \\ June23**

A opção de linha de comando **-el** não pode ser combinada com outras opções de linha de comando.

## <a name="exposing-a-shadow-copy-remotely"></a>Expondo uma cópia de sombra remotamente

**vshadow** **-er=**_ShadowCopyId,_**_UnusedShareName_

 **vshadow** **-er=**_ShadowCopyId,_**_UnusedShareName,_**_PathFromRootOnShadow_

A opção de linha de comando **-er** atribui um nome de compartilhamento somente leitura ao diretório raiz (ou um subdiretório) da cópia de sombra. Observe que o conteúdo do compartilhamento permanecerá somente leitura, a menos que você chame **posteriormente vshadow** **-bw** para quebrar o conjunto de cópias de sombra.

> [!Note]  
> [*Cópias de sombra acessíveis pelo cliente não*](vssgloss-c.md) podem ser expostas remotamente.

 

Por exemplo, se {edbed95e-7e8d-11d8-9d01-505054503030} for o GUID de uma cópia de sombra persistente existente e o compartilhamento 123 for um nome de compartilhamento nãoutilado, o comando a seguir exporá a cópia de sombra no \_ \_ compartilhamento 123:

**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030}, \_ compartilhar 123**

O exemplo a seguir mostra como expor apenas uma subárvore (chamada "Folder1 Folder2") da mesma cópia \\ de sombra no mesmo compartilhamento:

**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share \_ 123,Folder1 \\ Folder2**

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

**vshadow** \[ OptionalFlags \] **-r =**_arquivo_ *_.xml_*

**vshadow** \[ OptionalFlags \] **-RS =**_arquivo_ *_.xml_*

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
> essa opção de linha de comando tem suporte apenas em sistemas operacionais Windows server.

 

**Windows server 2008 e Windows server 2003:** Sem suporte.

A opção **-reverter** linha de comando reverte um volume para a cópia de sombra anterior cuja ID é especificada por *ShadowCopyId*.

A opção de linha de comando **-REVERT** não pode ser combinada com outras opções de linha de comando.

## <a name="resynchronizing-luns"></a>Ressincronizando LUNs

**vshadow** **-addresync =**_ShadowCopyId_ **-Ressync =**_BCDFileName_ \[ OptionalResyncFlags\]

**vshadow** **-addresync =**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-Ressync =**_BCDFileName_ \[ OptionalResyncFlags\]

A opção de linha de comando **-addresync** especifica os volumes a serem incluídos em uma operação de ressincronização de LUN. O parâmetro *ShadowCopyId* especifica o identificador da cópia de sombra. O parâmetro opcional *TargetVolumeDriveLetter* especifica o volume de destino onde o conteúdo do volume da cópia de sombra deve ser copiado.

A opção de linha de comando **-Ressync** inicia uma operação de ressincronização de LUN. Depois que a operação for concluída, a assinatura de cada LUN de destino deverá ser idêntica à do LUN de volume de destino. O parâmetro *BCDFileName* especifica o nome do arquivo XML que contém o documento do componente de backup.

> [!Note]  
> as opções de linha de comando **-addresync** e **-ressync** só têm suporte em sistemas operacionais Windows server.

 

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
o sinalizador <strong>-revertsig</strong> tem suporte apenas em sistemas operacionais do Windows server.
</blockquote>
<br/> <strong>Windows server 2008 e Windows server 2003:</strong> Sem suporte.<br/></td>
</tr>
<tr class="even">
<td><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong><br/></td>
<td>Esse sinalizador opcional especifica que o serviço VSS não deve verificar se há volumes não selecionados que seriam substituídos pela operação de ressincronização de LUN.<br/>
<blockquote>
[!Note]<br />
o sinalizador <strong>-novolcheck</strong> tem suporte apenas em sistemas operacionais do Windows server.
</blockquote>
<br/> <strong>Windows server 2008 e Windows server 2003:</strong> Sem suporte.<br/></td>
</tr>
</tbody>
</table>



 

 

 
