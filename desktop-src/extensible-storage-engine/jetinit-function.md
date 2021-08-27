---
description: 'Saiba mais sobre: função JetInit'
title: Função JetInit
TOCTitle: JetInit Function
ms:assetid: b7f78cca-7268-4045-bda2-20746b1d6370
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294068(v=EXCHG.10)
ms:contentKeyID: 32765683
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d074e07dec88bf0b33ec56b1391986758fbd388c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984529"
---
# <a name="jetinit-function"></a>Função JetInit


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetinit-function"></a>Função JetInit

A função **JetInit** coloca o mecanismo de banco de dados em um estado em que ele pode dar suporte ao uso do aplicativo de arquivos de banco de dados. O mecanismo já deve estar configurado corretamente para inicialização usando [JetSetSystemParameter](./jetsetsystemparameter-function.md). A recuperação de falhas no banco de dados é executada automaticamente como parte do processo de inicialização.

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a>Parâmetros

*pinstance*

A instância a ser usada para esta chamada.

para Windows 2000, esse parâmetro é ignorado e sempre deve ser nulo.

para o Windows XP e versões posteriores, o uso desse parâmetro depende do modo de operação do mecanismo. se o mecanismo estiver operando no modo herdado (Windows modo de compatibilidade 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser nulo ou poderá ser definido como um buffer de saída válido que retornará o identificador de instância global criado como um efeito colateral da inicialização. Esse buffer de saída deve ser definido como nulo ou JET_instanceNil. Esse identificador de instância pode então ser passado para qualquer outra função que use uma instância do. Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro deverá ser definido como um buffer de entrada válido que contenha o identificador de instância retornado pela instância de função [JetCreateInstance](./jetcreateinstance-function.md) que está sendo inicializada.


#### <a name="remarks"></a>Comentários

Uma instância deve ser inicializada com uma chamada para **JetInit** antes que possa ser usada por algo diferente de [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Uma instância é destruída por uma chamada para a função [JetTerm](./jetterm-function.md) , mesmo que essa instância nunca tenha sido inicializada usando **JetInit**. Uma instância é a unidade de capacidade de recuperação para o mecanismo de banco de dados. Ele controla o ciclo de vida de todos os arquivos usados para proteger a integridade dos dados em um conjunto de arquivos de banco de dado. Esses arquivos incluem o arquivo de ponto de verificação e os arquivos de log de transações.

O número máximo de instâncias que podem ser criadas a qualquer momento é controlado por [JET_paramMaxInstances](./resource-parameters.md), que pode ser configurado por uma chamada para [JetSetSystemParameter](./jetsetsystemparameter-function.md). Quando o mecanismo de banco de dados é inicializado pela primeira vez, o **JetInit** criará um conjunto inicial de arquivos para dar suporte a essa instância. Esses arquivos incluem um arquivo de ponto de verificação (chamado \<[JET_paramBaseName](./transaction-log-parameters.md)\> . CHK), um conjunto de arquivos de log de transações reservadas (chamado RES1. LOG e RES2. LOG), um arquivo de log de transações inicial (chamado \<[JET_paramBaseName](./transaction-log-parameters.md)\> . LOG) e um arquivo de banco de dados temporário (nomeado de acordo com [JET_paramTempPath](./temporary-database-parameters.md)). Se [JET_paramRecovery](./transaction-log-parameters.md) for definido como "off", o arquivo de ponto de verificação e os arquivos de log não serão criados. Se [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) for definido como zero, o arquivo de banco de dados temporário não será criado. Esses arquivos representam a superfície do disco de uma instância e devem ser gerenciados com cuidado. Se esses arquivos forem corrompidos individualmente ou em relação um ao outro, os dados armazenados nos bancos de dados associados à instância poderão ser perdidos.

Quando o mecanismo de banco de dados é inicializado com um conjunto existente de arquivos de log de transações, esses arquivos serão inspecionados para ver se a versão anterior da instância sofreu uma falha. Se uma falha for detectada, a recuperação de falha será executada automaticamente. Esse processo reconstruirá os bancos de dados anexados à instância durante a versão anterior do mecanismo e salvará as alterações de volta nos arquivos de banco de dados. O resultado será os bancos de dados que são consistentes com a transação. É possível que esse processo demore um pouco de tempo se o número de arquivos de log de transações a serem reproduzidos em relação aos bancos de dados for grande.

Devido ao fato de que o **JetInit** executa a recuperação de pane, é possível que quase todos os erros do mecanismo de banco de dados sejam retornados em caso de falha. Na prática, a maioria dos erros vistos na implantação se enquadra em duas categorias: corrupção de dados e ingestão de arquivos. Os dados corrompidos serão manifestados com mais frequência nos seguintes erros ou semelhantes:

  - JET_errReadVerifyFailure

  - JET_errLogFileCorrupt

  - JET_errCheckpointCorrupt

Esses erros são quase sempre causados por problemas de hardware e, portanto, não podem ser evitados. O ingerenciamento de arquivos será manifestado com mais frequência nos seguintes erros ou semelhantes:

  - JET_errMissingLogFile

  - JET_errAttachedDatabaseMismatch

  - JET_errDatabaseSharingViolation

  - JET_errInvalidLogSequence

Se a recuperação estiver em execução em um conjunto de logs, para os quais nem todos os bancos de dados estão presentes (o que retornará o erro JET_errAttachedDatabaseMismatch em circunstâncias normais) e o cliente desejar que a recuperação continue apesar dos bancos de dados ausentes, o JET_ bitReplayIgnoreMissingDB poderá ser usado para continuar a recuperação para os bancos de dados disponíveis. Esses erros são impedidos pelo aplicativo. O aplicativo deve ter cuidado para proteger o repositório desses arquivos contra a manipulação por forças externas, como o usuário ou outros aplicativos. Se o aplicativo desejar destruir uma instância inteiramente, todos os arquivos associados à instância deverão ser excluídos. Isso inclui o arquivo de ponto de verificação, os arquivos de log de transações e os arquivos de banco de dados anexados à instância.

a função **JetInit** se comporta de forma diferente, com relação aos arquivos de banco de dados anexados à instância, entre Windows 2000 e versões posteriores.

**Windows 2000:**  no Windows 2000, qualquer banco de dados anexado à instância durante uma encarnação anterior dessa instância permanecerá anexado à instância depois que **JetInit** for concluído com êxito. Não é necessário chamar [JetAttachDatabase](./jetattachdatabase-function.md) após **JetInit** para garantir o acesso ao banco de dados posteriormente. Se a função [JetAttachDatabase](./jetattachdatabase-function.md) for chamada após a função **JetInit** , o aviso de JET_wrnDatabaseAttached será retornado. Esse aviso indica que o anexo do banco de dados foi preservado e pode ser ignorado.

**Windows XP:**  no Windows XP e versões posteriores, todos os bancos de dados são automaticamente desanexados da instância pelo **JetInit**. Isso significa que [JetAttachDatabase](./jetattachdatabase-function.md) sempre deve ser chamado depois de **JetInit** nesse caso.

qualquer aplicativo escrito para ser executado no Windows 2000 e em versões posteriores sempre deve chamar [JetAttachDatabase](./jetattachdatabase-function.md) após **JetInit**. se o aplicativo for executado no Windows 2000, ele deverá esperar ver JET_wrnDatabaseAttached em alguns casos. Consulte [JetAttachDatabase](./jetattachdatabase-function.md) para obter mais informações.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[arquivos do mecanismo de Armazenamento extensível](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_paramMaxTemporaryTables](./temporary-database-parameters.md)  
[JET_paramRecovery](./transaction-log-parameters.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
