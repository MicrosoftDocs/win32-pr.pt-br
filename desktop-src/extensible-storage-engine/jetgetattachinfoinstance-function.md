---
description: 'Saiba mais sobre: função JetGetAttachInfoInstance'
title: Função JetGetAttachInfoInstance
TOCTitle: JetGetAttachInfoInstance Function
ms:assetid: 978e7817-0720-42fc-a5c1-46e4d44239f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269350(v=EXCHG.10)
ms:contentKeyID: 32765637
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfoInstanceW
- JetGetAttachInfoInstanceA
- JetGetAttachInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8bbfac13e1536c0a8261e3c63a4308a84a60cf09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474092"
---
# <a name="jetgetattachinfoinstance-function"></a>Função JetGetAttachInfoInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetattachinfoinstance-function"></a>Função JetGetAttachInfoInstance

A função **JetGetAttachInfoInstance** é usada durante um backup iniciado pelo [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) para consultar uma instância para obter os nomes dos arquivos de banco de dados que devem se tornar parte do conjunto de arquivos de backup. Somente os bancos de dados que estão conectados à instância no momento usando [JetAttachDatabase](./jetattachdatabase-function.md) serão considerados. Esses arquivos podem ser abertos subsequentemente usando [JetOpenFileInstance](./jetopenfileinstance-function.md) e lidos usando [JetReadFileInstance](./jetreadfileinstance-function.md).

**Windows xp: o JetGetAttachInfoInstance** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetGetAttachInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parâmetros

*cópia*

A instância a ser usada para esta chamada.

para Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância. O uso dessa instância global é implícito nesse caso.

para Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só pode ser chamada quando o mecanismo está no modo herdado (modo de compatibilidade Windows 2000) em que há suporte para apenas uma instância. Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.

*szz*

O buffer de saída que recebe a lista de cadeias de caracteres terminadas em nulo que descreve o conjunto de arquivos de banco de dados que deve ser parte do conjunto de arquivos de backup. A lista de cadeias de caracteres retornada nesse buffer está no mesmo formato que uma cadeia de caracteres múltipla usada pelo registro. Cada cadeia de caracteres terminada em nulo é retornada em sequência seguida por um terminador nulo final.

*cbMax*

O tamanho máximo em bytes do buffer de saída.

*pcbActual*

Ponteiro para o buffer de saída que recebe a quantidade real de dados de cadeia de caracteres.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>A operação de backup falhou porque ela foi chamada fora de sequência. <strong>JetGetAttachInfoInstance</strong> retornará esse erro se o backup atual não for um backup completo.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. isso pode ocorrer para <strong>JetGetAttachInfoInstance</strong> quando o identificador de instância especificado é inválido (Windows XP e versões posteriores).</p> | 
| <p>JET_errNoBackup</p> | <p>A operação falhou porque nenhum backup externo está em andamento.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>a operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (Windows modo de compatibilidade 2000) em que há suporte para apenas uma instância quando, na verdade, várias instâncias já existem.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 



Em caso de sucesso, as informações solicitadas sobre o conjunto de arquivos de banco de dados que devem ser parte do conjunto de arquivos de backup serão colocadas nos buffers de saída onde forem fornecidos.

Em caso de falha, o estado dos buffers de saída é indefinido. A falha resultará no cancelamento de todo o processo de backup da instância.

#### <a name="remarks"></a>Comentários

É importante observar que essa API não retornará um erro ou aviso se o buffer de saída for muito pequeno para aceitar a lista completa de arquivos que devem fazer parte do conjunto de arquivos de backup. O aplicativo sempre deve fornecer um buffer para receber o tamanho real dessa lista e usar essas informações para determinar se a lista foi truncada.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetAttachInfoInstanceW</strong> (Unicode) e <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopBackupInstance](./jetstopbackupinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)
