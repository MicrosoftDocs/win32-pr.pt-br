---
description: 'Saiba mais sobre: Função JetOpenFile'
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
ms.openlocfilehash: ffe4527390e21e86ed46820125eb2a422367d8ec
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480372"
---
# <a name="jetopenfile-function"></a>Função JetOpenFile


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetopenfile-function"></a>Função JetOpenFile

A **função JetOpenFile** abre um banco de dados anexado, um arquivo de patch de banco de dados ou um arquivo de log de transações de uma instância ativa com a finalidade de executar um backup difuso de streaming. Os dados desses arquivos podem ser lidos posteriormente por meio do alça retornado usando [JetReadFile](./jetreadfile-function.md). O alça retornado deve ser fechado usando [JetCloseFile](./jetclosefile-function.md). Um backup externo da instância deve ter sido iniciado anteriormente usando [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

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

O caminho relativo ou absoluto para um banco de dados anexado, arquivo de patch de banco de dados ou arquivo de log de transações gerenciado pela instância que será lida para backup.

*phfFile*

O buffer de saída que recebe um handle para o arquivo a ser lido.

*pulFileSizeLow*

O buffer de saída que recebe os 32 bits menos significativos do tamanho do arquivo.

*pulFileSizeHigh*

O buffer de saída que recebe os 32 bits mais significativos do tamanho do arquivo.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>Jet_errfileaccessdenied</p> | <p>A operação falhou porque não pôde abrir o arquivo solicitado devido a uma violação de compartilhamento ou privilégios insuficientes.</p> | 
| <p>JET_errFileNotFound</p> | <p>A operação falhou porque não foi possível abrir o arquivo solicitado porque ele não pôde ser encontrado no caminho especificado. Esse erro só será retornado por Windows 2000.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>A operação de backup falhou porque foi chamada fora de sequência.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer para <strong>JetOpenFile</strong> quando:</p><ul><li><p>O handle de instância especificado é inválido (Windows XP e versões posteriores).</p></li><li><p>O parâmetro filename especificado é NULL ou uma cadeia de caracteres de comprimento zero (Windows XP e versões posteriores).</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>A operação falhou porque não foi possível encontrar o caminho especificado.</p> | 
| <p>JET_errMissingFileToBackup</p> | <p>Não foi possível abrir o arquivo solicitado para backup porque ele não pôde ser encontrado. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errNoBackup</p> | <p>A operação falhou porque nenhum backup externo está em andamento.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errOutOfMemory</p> | <p>A operação falhou porque não foi possível alocar memória suficiente para a conclusão. <strong>JetOpenFile</strong> retornará JET_errOutOfMemory se for feita uma tentativa de abrir outro arquivo antes que o arquivo anterior aberto usando <strong>JetOpenFile</strong> tenha sido fechado por <a href="gg294127(v=exchg.10).md">JetCloseFile</a>. No momento, há suporte para apenas um alça de arquivo pendente.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade Windows 2000), em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado. JET_errRestoreInProgress não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 



Em caso de êxito, um handle para o arquivo solicitado será retornado. Se o handle for para um arquivo de banco de dados, esse arquivo de banco de dados será preparado para o backup de streaming, o que pode resultar na criação de um arquivo de patch de banco de dados no mesmo local que o arquivo de banco de dados. O arquivo de patch do banco de dados tem exatamente o mesmo caminho e nome de arquivo que o arquivo de banco de dados, mas tem um . Extensão PAT. O tamanho do arquivo também será retornado.

Em caso de falha, o estado dos buffers de saída será indefinido. Um arquivo de patch de banco de dados pode ser criado temporariamente no disco e qualquer arquivo existente no local do arquivo de patch pode ser excluído. A falha resultará no cancelamento de todo o processo de backup para a instância. No Windows XP e versões posteriores, o backup não será cancelado se tiver sido feita uma tentativa de fazer backup de um banco de dados que não estava anexado à instância no momento da chamada.

**Aviso**  Por motivos de segurança, é importante observar que **JetOpenFile** não verifica se o caminho do arquivo solicitado está associado ao conjunto de arquivos que devem ser armazenados em backup para a instância. Como resultado, é possível usar essa função para acessar qualquer arquivo que possa ser aberto pelo contexto de segurança atual do thread. É imperativo que o aplicativo restrinja os caminhos passados para essa função para um conjunto conhecido de bons caminhos de arquivo ou uma divulgação de ataque de informações possa ser possibilitada.

#### <a name="remarks"></a>Comentários

Os buffers de saída de tamanho de arquivo e de alça devem estar presentes. Se eles não estão presentes, o mecanismo falhará porque os parâmetros do buffer de saída não são validados.

Neste momento, apenas um arquivo pode ser aberto para backup a qualquer momento.

**JetOpenFile** não declara o privilégio de backup antes de abrir o arquivo solicitado.

O tamanho do arquivo a ser lido conforme relatado por essa função pode não corresponder ao tamanho do arquivo em disco. No Windows XP e versões posteriores, informações extras podem ser acrescentadas a um arquivo de banco de dados que é usado pelo mecanismo de banco de dados durante uma operação de restauração. Dessa forma, o aplicativo deve depender apenas do tamanho do arquivo retornado por **JetOpenFile** ou do número real de bytes de dados retornados pelo [JetReadFile](./jetreadfile-function.md).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetOpenFileW</strong> (Unicode) e <strong>JetOpenFileA</strong> (ANSI).</p> | 



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
