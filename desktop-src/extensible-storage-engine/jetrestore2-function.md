---
description: 'Saiba mais sobre: Função JetRestore2'
title: Função JetRestore2
TOCTitle: JetRestore2 Function
ms:assetid: 7f7fc2e3-727a-43e4-8497-64ff56d92b9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269313(v=EXCHG.10)
ms:contentKeyID: 32765603
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore2
- JetRestore2A
- JetRestore2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 464fbc228acc1d73b50253b2312edd3889289e2d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987249"
---
# <a name="jetrestore2-function"></a>Função JetRestore2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetrestore2-function"></a>Função JetRestore2

O **JetRestore2** restaura e recupera um backup de streaming de uma instância, incluindo todos os bancos de dados anexados. Essa função é principalmente para compatibilidade com versões anteriores com Windows 2000 e mecanismos de banco de dados anteriores, em que apenas uma instância de um banco de dados é permitida. Nesse caso, a instância ativa é a instância restaurada.

```cpp
    JET_ERR JET_API JetRestore2(
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parâmetros

*Sz*

A pasta em que o backup está localizado. O backup deve ter sido gerado usando as APIs [do JetBackup.](./jetbackup-function.md)

*szDest*

Nome da pasta em que os arquivos de banco de dados do conjunto de backup serão copiados e recuperados. Se isso for definido como NULL (que é o caso do [JetRestore](./jetrestore-function.md)herdado), os arquivos de banco de dados serão copiados e recuperados para seu local original.

*pfn*

O ponteiro opcional para a função que será chamada como informações de notificação sobre o progresso da operação de restauração.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>A operação falhou porque o mecanismo já foi inicializado para essa instância.</p> | 
| <p>JET_errInvalidLogSequence</p> | <p>O conjunto de arquivos de log do conjunto de backup e do caminho de log atual não é igual.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Esse erro será retornado por <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> quando o mecanismo estiver no modo de várias instâncias e o pinstance se referir a uma instância inválida Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidPath</p> | <p>A operação falhou porque alguns dos caminhos fornecidos são inválidos (o caminho de backup, o caminho de destino, o log ou o caminho do sistema para a instância).</p> | 
| <p>JET_errPageSizeMismatch</p> | <p>A operação falhou porque o mecanismo está configurado para usar um tamanho de página de banco de dados (usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para JET_paramDatabasePageSize ) que não corresponder ao tamanho da página do banco de dados usado para criar os arquivos de log de transações ou os bancos de dados associados <a href="gg269337(v=exchg.10).md">aos</a>arquivos de log de transações.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>A operação falhou porque os parâmetros implicaram no modo de instância única (Windows modo de compatibilidade 2000) e o mecanismo já está no modo de várias instâncias.</p> | 



Em caso de êxito, os arquivos de banco de dados do conjunto de backup serão restaurados para seu local e a recuperação será realizada de forma que os bancos de dados estarão em um estado de consistência transacional limpo. A recuperação repetirá os arquivos de log do conjunto de backup e os arquivos de log do caminho de log se esses arquivos existirem. Essa recuperação resultará em alterações no arquivo de ponto de verificação, nos arquivos de log de transações e em todos os bancos de dados referenciados por esses arquivos de log de transações.

Em caso de falha, a instância permanece em um estado não reinicializado. O estado dos arquivos de log de transações e os bancos de dados referenciados por esses arquivos de log de transações provavelmente terão sido alterados na tentativa de inicializar a restauração e recuperar os bancos de dados.

#### <a name="remarks"></a>Comentários

O processo de recuperação reconstruirá os bancos de dados anexados à instância durante o backup e salvará as alterações nos arquivos de banco de dados. O resultado serão bancos de dados consistentes com a transação. Se possível, ele também salvará no banco de dados as alterações feitas desde que o backup foi feito até a alteração mais recente encontrada nos logs de transações. Isso seria possível se os logs de transação gerados desde que o backup foi feito ainda estivesse presente no diretório de log de transações. Observe que, se o log circular tiver sido habilitado para a instância, os logs de transação gerados serão reutilizados de modo que a recuperação possa salvar as alterações que ocorreram até o momento do backup. Em qualquer caso, é possível que esse processo leve algum tempo se o número de arquivos de log de transações a repetir nos bancos de dados for grande.

[As funções JetRestore](./jetrestore-function.md) devem ser chamadas em uma instância antes que [JetInit](./jetinit-function.md) seja chamado para essa instância.

Como durante a recuperação um número significativo de páginas de banco de dados e logs de transações será usado, há uma série inteira de erros que pode ser retornada por essas funções. Esses erros podem ser de falhas temporárias de alocação de recursos, como Jet_errOutOfMemory a erros que representam danos físicos, como JET_errReadVerifyFailure, JET_errLogFileCorrupt ou JET_errBadPageLink. Esses erros quase sempre são causados por problemas de hardware e, portanto, não podem ser evitados. O erro de uso do arquivo se manifesta com mais frequência, JET_errMissingLogFile ou JET_errAttachedDatabaseMismatch ou JET_errDatabaseSharingViolation ou JET_errInvalidLogSequence. Esses erros são impedidas pelo aplicativo. O aplicativo deve ter cuidado para proteger o repositório desses arquivos contra manipulação por força externas, como o usuário ou outros aplicativos. Se o aplicativo desejar destruir uma instância inteiramente, todos os arquivos associados à instância deverão ser excluídos. Isso inclui o arquivo de ponto de verificação, os arquivos de log de transações e todos os arquivos de banco de dados anexados à instância.

As diferentes etapas da recuperação terão entradas do Log de Eventos geradas, incluindo o progresso da reprodução do log de transações e o resultado final da restauração.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetRestore2W</strong> (Unicode) e <strong>JetRestore2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
