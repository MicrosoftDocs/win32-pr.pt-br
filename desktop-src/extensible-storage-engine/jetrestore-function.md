---
description: 'Saiba mais sobre: função JetRestore'
title: Função JetRestore
TOCTitle: JetRestore Function
ms:assetid: cdfb8823-6260-46f2-adfc-77e2512a68fd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294093(v=EXCHG.10)
ms:contentKeyID: 32765708
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore
- JetRestoreW
- JetRestoreA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ed164bb6775150f9745cb0e6d9b158a5f03f146
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103930781"
---
# <a name="jetrestore-function"></a>Função JetRestore


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetrestore-function"></a>Função JetRestore

A função **JetRestore** restaura e recupera um backup de streaming de uma instância, incluindo todos os bancos de dados anexados. Essa função é usada principalmente para compatibilidade com versões anteriores com o Windows 2000 e com mecanismos de banco de dados anterior, em que apenas uma instância de um banco de dados é permitida. Nesse caso, a instância ativa é a instância que é restaurada. Com **JetRestore**, o local dos bancos de dados restaurados não pode ser especificado.

```cpp
JET_ERR JET_API JetRestore(
  __in          JET_PCSTR sz,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a>Parâmetros

*sz*

A pasta onde o backup está localizado. O backup deve ter sido gerado usando a função [JetBackup](./jetbackup-function.md) .

*PFN*

O ponteiro opcional para a função que será chamada como informações de notificação sobre o progresso da operação de restauração.

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
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>A operação falhou porque o mecanismo já foi inicializado para esta instância.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLogSequence</p></td>
<td><p>O conjunto de arquivos de log do conjunto de backup e do caminho de log atual não coincidem.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>A operação falhou porque alguns caminhos fornecidos são inválidos (o caminho de backup, o caminho de destino, o log ou o caminho do sistema para a instância).</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch</p></td>
<td><p>A operação falhou porque o mecanismo está configurado para usar um tamanho de página de banco de dados (usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) que não corresponde ao tamanho da página do banco de dados usado para criar os arquivos de log de transações ou os bancos de dados associados aos arquivos de log de transações.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>A operação falhou porque o modo de instância única implícito de parâmetros (modo de compatibilidade do Windows 2000) e o mecanismo já estão no modo de várias instâncias.</p></td>
</tr>
</tbody>
</table>


Em caso de êxito, os arquivos de banco de dados do conjunto de backup serão restaurados para seu local e a recuperação será executada de modo que os bancos estejam em um estado de consistência transacional limpo. A recuperação reproduzirá os arquivos de log do conjunto de backup e dos arquivos de log do caminho de log, se esses arquivos existirem. Essa recuperação resultará em alterações no arquivo de ponto de verificação, nos arquivos de log de transações e em qualquer banco de dados referenciado por esses arquivos de log de transações.

Em caso de falha, a instância permanece em um estado não inicializado. O estado dos arquivos de log de transações e quaisquer bancos de dados referenciados por esses arquivos de log de transações provavelmente serão alterados na tentativa de inicializar a restauração e recuperar os bancos de dados.

#### <a name="remarks"></a>Comentários

O processo de recuperação reconstruirá os bancos de dados anexados à instância durante o backup e salvará as alterações de volta nos arquivos de banco de dados. O resultado será os bancos de dados que são consistentes com a transação. Se possível, ele também será salvo no banco de dados as alterações feitas desde que o backup foi feito até a alteração mais recente encontrada nos logs de transações. Isso seria possível se os logs de transações gerados desde que o backup foi feito ainda estiverem presentes no diretório de log de transações. Observe que, se o log circular tiver sido habilitado para a instância, os logs de transação gerados serão reutilizados, de modo que a recuperação poderá salvar as alterações que foram realizadas até o momento do backup. Em qualquer caso, é possível que esse processo demore algum tempo se o número de arquivos de log de transações a serem reproduzidos em relação aos bancos de dados for grande.

As funções **JetRestore** devem ser chamadas em uma instância antes que [JetInit](./jetinit-function.md) seja chamado para essa instância.

Como, durante a recuperação, um número significativo de páginas de banco de dados e logs de transações serão usados, há uma série completa de erros que podem ser retornados por essas funções. Esses erros podem ser de falhas temporárias de alocação de recursos, como Jet_errOutOfMemory a erros que representam as corrupções físicas, como JET_errReadVerifyFailure, JET_errLogFileCorrupt ou JET_errBadPageLink. Esses erros são quase sempre causados por problemas de hardware e, portanto, não podem ser evitados. O ingerenciamento de arquivos será manifestado com mais frequência como JET_errMissingLogFile ou JET_errAttachedDatabaseMismatch ou JET_errDatabaseSharingViolation ou JET_errInvalidLogSequence. Esses erros são impedidos pelo aplicativo. O aplicativo deve ter cuidado para proteger o repositório desses arquivos contra a manipulação por forças externas, como o usuário ou outros aplicativos. Se o aplicativo desejar destruir uma instância inteiramente, todos os arquivos associados à instância deverão ser excluídos. Isso inclui o arquivo de ponto de verificação, os arquivos de log de transações e os arquivos de banco de dados anexados à instância.

As diferentes etapas da recuperação terão entradas de log de eventos geradas, incluindo o progresso da reprodução do log de transações e o resultado final da restauração.

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
<td><p>Implementado como <strong>JetRestoreW</strong> (Unicode) e <strong>JetRestoreA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
