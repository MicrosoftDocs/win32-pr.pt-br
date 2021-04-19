---
description: 'Saiba mais sobre: função JetOpenFile'
title: Função JetOpenFile
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2996ffc46e2f6b37cdfec12cd4ee2fc62efa188a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783757"
---
# <a name="jetopenfile-function"></a>Função JetOpenFile


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetopenfile-function"></a>Função JetOpenFile

A função **JetOpenFile** abre um banco de dados anexado, um arquivo de patch de banco de dados ou um arquivo de log de transações de uma instância ativa com a finalidade de executar um backup difuso de streaming. Os dados desses arquivos podem, subsequentemente, ser lidos por meio do identificador retornado usando [JetReadFile](./jetreadfile-function.md). O identificador retornado deve ser fechado usando [JetCloseFile](./jetclosefile-function.md). Um backup externo da instância deve ter sido iniciado anteriormente usando [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a>Parâmetros

*szFileName*

O caminho relativo ou absoluto para um banco de dados anexado, um arquivo de patch de banco de dados ou um arquivo de log de transações gerenciado pela instância do que será lida para backup.

*phfFile*

O buffer de saída que recebe um identificador para o arquivo a ser lido.

*pulFileSizeLow*

O buffer de saída que recebe os 32 bits menos significativos do tamanho do arquivo.

*pulFileSizeHigh*

O buffer de saída que recebe os 32 bits mais significativos do tamanho do arquivo.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileAccessDenied</p></td>
<td><p>A operação falhou porque não pôde abrir o arquivo solicitado devido a uma violação de compartilhamento ou privilégios insuficientes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>A operação falhou porque não pôde abrir o arquivo solicitado porque ele não foi encontrado no caminho especificado. Esse erro só será retornado pelo Windows 2000.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>A operação de backup falhou porque ela foi chamada fora de sequência.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode ocorrer para <strong>JetOpenFile</strong> quando:</p>
<ul>
<li><p>O identificador de instância especificado é inválido (Windows XP e versões posteriores).</p></li>
<li><p>O parâmetro filename especificado é nulo ou uma cadeia de caracteres de comprimento zero (Windows XP e versões posteriores).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>A operação falhou porque o caminho especificado não foi encontrado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFileToBackup</p></td>
<td><p>Não foi possível abrir o arquivo solicitado para backup porque ele não foi encontrado. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>A operação falhou porque nenhum backup externo está em andamento.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>A operação falhou porque não foi possível alocar memória suficiente para concluí-la. <strong>JetOpenFile</strong> retornará JET_errOutOfMemory se for feita uma tentativa de abrir outro arquivo antes que o arquivo anterior aberto usando <strong>JetOpenFile</strong> tenha sido fechado pelo <a href="gg294127(v=exchg.10).md">JetCloseFile</a>. No momento, há suporte para apenas um identificador de arquivo pendente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada. JET_errRestoreInProgress não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, será retornado um identificador para o arquivo solicitado. Se o identificador for para um arquivo de banco de dados, esse arquivo de banco de dados será preparado para o backup de streaming, o que pode resultar na criação de um arquivo de patch de banco de dados no mesmo local que o arquivo de banco de dados. O arquivo de patch do banco de dados tem exatamente o mesmo caminho e nome de arquivo do banco de dados, mas tem um. Extensão PAT. O tamanho do arquivo também será retornado.

Em caso de falha, o estado dos buffers de saída será indefinido. Um arquivo de patch de banco de dados pode ser criado temporariamente no disco e qualquer arquivo existente no local do arquivo de patch pode ser excluído. A falha resultará no cancelamento de todo o processo de backup da instância. No Windows XP e versões posteriores, o backup não será cancelado se for feita uma tentativa de fazer backup de um banco de dados que não foi anexado à instância no momento da chamada.

**Aviso**  Por motivos de segurança, é importante observar que o **JetOpenFile** não verifica se o caminho do arquivo solicitado está associado ao conjunto de arquivos cujo backup deve ser feito para a instância. Como resultado, é possível usar essa função para acessar qualquer arquivo que possa ser aberto pelo contexto de segurança atual do thread. É imperativo que o aplicativo restrinja os caminhos passados para essa função para um conjunto conhecido de bons caminhos de arquivo ou uma divulgação de ataque de informações poderia ser possível.

#### <a name="remarks"></a>Comentários

Os buffers de saída de identificador e de tamanho de arquivo devem estar presentes. Se eles não estiverem presentes, o mecanismo falhará porque os parâmetros do buffer de saída não são validados.

Neste momento, apenas um arquivo pode ser aberto para backup a qualquer momento.

**JetOpenFile** não declara o privilégio de backup antes de abrir o arquivo solicitado.

O tamanho do arquivo a ser lido como relatado por essa função pode não corresponder ao tamanho do arquivo no disco. No Windows XP e versões posteriores, informações extras podem ser acrescentadas a um arquivo de banco de dados que é usado pelo mecanismo de banco de dados durante uma operação de restauração. Como tal, o aplicativo deve confiar apenas no tamanho do arquivo retornado por **JetOpenFile** ou no número real de bytes de dados retornados por [JetReadFile](./jetreadfile-function.md).

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetOpenFileW</strong> (Unicode) e <strong>JetOpenFileA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
