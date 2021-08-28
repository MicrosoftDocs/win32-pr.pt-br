---
description: 'Saiba mais sobre: Função JetOpenFileInstance'
title: Função JetOpenFileInstance
TOCTitle: JetOpenFileInstance Function
ms:assetid: 44af9549-77ef-48f4-8580-507f7199f281
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269238(v=EXCHG.10)
ms:contentKeyID: 32765540
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileInstanceA
- JetOpenFileInstanceW
- JetOpenFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba66545c65abcaa3d3969ec7c3d61d73c57be732
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983369"
---
# <a name="jetopenfileinstance-function"></a>Função JetOpenFileInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetopenfileinstance-function"></a>Função JetOpenFileInstance

A **função JetOpenFileInstance** abre um banco de dados anexado, um arquivo de patch de banco de dados ou um arquivo de log de transações de uma instância ativa com a finalidade de executar um backup difuso de streaming. Os dados desses arquivos podem ser lidos posteriormente pelo handle retornado usando [JetReadFileInstance](./jetreadfileinstance-function.md). O alça retornado deve ser fechado usando [JetCloseFileInstance](./jetclosefileinstance-function.md). Um backup externo da instância deve ter sido iniciado anteriormente usando [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).

**Windows XP:****JetOpenFileInstance** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetOpenFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a>Parâmetros

*Instância*

A instância a ser usada para essa chamada.

Por Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância. O uso dessa instância global está implícito nesse caso.

Para Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só poderá ser chamada quando o mecanismo estiver no modo herdado (modo de compatibilidade do Windows 2000), em que há suporte para apenas uma instância. Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.

*szFileName*

O caminho relativo ou absoluto para um banco de dados anexado, arquivo de patch de banco de dados ou arquivo de log de transações gerenciado pela instância que é lida para backup.

*phfFile*

Ponteiro para o buffer de saída que recebe um ponteiro para o arquivo a ser lido.

*pulFileSizeLow*

Ponteiro para o buffer de saída que recebe os 32 bits menos significativos do tamanho do arquivo.

*pulFileSizeHigh*

Ponteiro para o buffer de saída que recebe os 32 bits mais significativos do tamanho do arquivo.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</p> | 
| <p>Jet_errfileaccessdenied</p> | <p>A operação falhou porque não pôde abrir o arquivo solicitado devido a uma violação de compartilhamento ou privilégios insuficientes.</p> | 
| <p>JET_errFileNotFound</p> | <p>A operação falhou porque não foi possível abrir o arquivo solicitado porque ele não pôde ser encontrado no caminho especificado. Esse erro só será retornado por Windows 2000.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>A operação de backup falhou porque foi chamada fora de sequência.</p> | 
| <p>JET_errInvalidPath</p> | <p>A operação falhou porque não foi possível encontrar o caminho especificado.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer para <strong>JetOpenFileInstance</strong> quando:</p><ul><li><p>O handle de instância especificado é inválido (Windows XP e versões posteriores).</p></li><li><p>O parâmetro filename especificado é NULL ou uma cadeia de caracteres de comprimento zero (Windows XP e versões posteriores).</p></li></ul> | 
| <p>JET_errMissingFileToBackup</p> | <p>Não foi possível abrir o arquivo solicitado para backup porque ele não pôde ser encontrado. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errNoBackup</p> | <p>A operação falhou porque nenhum backup externo está em andamento.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errOutOfMemory</p> | <p>A operação falhou porque não foi possível alocar memória suficiente para a conclusão. <strong>JetOpenFileInstance</strong> retornará JET_errOutOfMemory se for feita uma tentativa de abrir outro arquivo antes que o arquivo anterior aberto usando <strong>JetOpenFileInstance</strong> tenha sido fechado por <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>. No momento, há suporte para apenas um alça de arquivo pendente.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (Windows modo de compatibilidade 2000), em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 



Em caso de êxito, um handle para o arquivo solicitado é retornado. Se o handle for para um arquivo de banco de dados, esse arquivo de banco de dados será preparado para um backup de streaming que pode resultar na criação de um arquivo de patch de banco de dados no mesmo local que o arquivo de banco de dados. O arquivo de patch do banco de dados tem exatamente o mesmo caminho e nome de arquivo que o arquivo de banco de dados, mas com um . Extensão PAT. O tamanho do arquivo também será retornado.

Em caso de falha, o estado dos buffers de saída será indefinido. Um arquivo de patch de banco de dados pode ser criado temporariamente no disco e qualquer arquivo existente no local do arquivo de patch pode ser excluído. A falha resultará no cancelamento de todo o processo de backup para a instância. No Windows XP e versões posteriores, o backup não será cancelado se tiver sido feita uma tentativa de fazer backup de um banco de dados que não estava anexado à instância no momento da chamada.

**Aviso**  Por motivos de segurança, é importante observar que **JetOpenFileInstance** não verifica se o caminho do arquivo solicitado está associado ao conjunto de arquivos que têm backup feito para a instância. Como resultado, é possível usar essa função para acessar qualquer arquivo que possa ser aberto pelo contexto de segurança atual do thread. É imperativo que o aplicativo restrinja os caminhos passados para essa função para um conjunto conhecido de bons caminhos de arquivo ou uma divulgação de ataque de informações possa ser possibilitada.

#### <a name="remarks"></a>Comentários

Os buffers de saída de tamanho de arquivo e de alça devem estar presentes. Se eles não estão presentes, o mecanismo falhará porque os parâmetros do buffer de saída não são validados.

Neste momento, apenas um arquivo pode ser aberto para backup a qualquer momento.

**JetOpenFileInstance** não declara o privilégio de backup antes de abrir o arquivo solicitado.

O tamanho do arquivo a ser lido conforme relatado por essa função pode não corresponder ao tamanho do arquivo em disco. No Windows XP e versões posteriores, informações adicionais podem ser acrescentadas a um arquivo de banco de dados que é usado pelo mecanismo de banco de dados durante uma operação de restauração. Assim, o aplicativo deve depender apenas do tamanho do arquivo retornado por **JetOpenFileInstance** ou do número real de bytes de dados retornados por [JetReadFileInstance](./jetreadfileinstance-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetOpenFileInstanceW</strong> (Unicode) e <strong>JetOpenFileInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFileInstance](./jetclosefileinstance-function.md)  
[JetGetAttachInfoInstance](./jetgetattachinfoinstance-function.md)  
[JetGetLogInfoInstance](./jetgetloginfoinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopBackupInstance](./jetstopbackupinstance-function.md)  
[JetTruncateLogInstance](./jettruncateloginstance-function.md)
