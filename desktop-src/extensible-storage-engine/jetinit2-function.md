---
description: 'Saiba mais sobre: Função JetInit2'
title: Função JetInit2
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9b5d2a62aa448a84d539d8d2d557d06befacfbba
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988949"
---
# <a name="jetinit2-function"></a>Função JetInit2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetinit2-function"></a>Função JetInit2

A **função JetInit2** coloca o mecanismo de banco de dados em um estado em que ele pode dar suporte ao uso de aplicativos de arquivos de banco de dados. O mecanismo já deve estar configurado corretamente para inicialização usando [JetSetSystemParameter](./jetsetsystemparameter-function.md). A recuperação de falha do banco de dados é executada automaticamente como parte do processo de inicialização.

**Windows XP:****JetInit2** é introduzido no Windows XP.  

Essa função está obsoleta. Em vez disso, use [JetInit3.](./jetinit3-function.md)

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parâmetros

*pinstance*

A instância a ser usada para essa chamada.

Por Windows 2000, esse parâmetro é ignorado e sempre deve ser NULL.

Para Windows XP e versões posteriores, o uso desse parâmetro depende do modo de operação do mecanismo. Se o mecanismo estiver operando no modo herdado (modo de compatibilidade do Windows 2000), em que há suporte para apenas uma instância, esse parâmetro pode ser NULL ou pode ser definido como um buffer de saída válido contendo NULL ou JET_instanceNil que retorna o handle de instância global criado como um efeito colateral da inicialização. Esse handle de instância pode ser passado para qualquer outra API que aceita uma instância. Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro deverá ser definido como um buffer de entrada válido que contém o handle de instância retornado pelo [JetCreateInstance](./jetcreateinstance-function.md) que está sendo inicializado.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitReplayReplicatedLogFiles</p> | <p>Reservado para uso futuro.</p> | 
| <p>JET_bitCreateSFSVolumeIfNotExist</p> | <p>Reservado para uso futuro.</p> | 
| <p>JET_bitReplayIgnoreMissingDB</p> | <p>Essa opção permite que o usuário execute a recuperação em um conjunto de arquivos de log, sem que todos os bancos de dados presentes, que foram anexados em um ponto do conjunto de log.</p> | 
| <p>JET_bitRecoveryWithoutUndo</p> | <p>Execute a recuperação, mas pare na fase Desfazer. Isso permite que logs de transações adicionais são copiados e aplicados.</p> | 
| <p>JET_bitTruncateLogsAfterRecovery</p> | <p>Na recuperação suave bem-sucedida, truncar arquivos de log.</p> | 
| <p>JET_bitReplayMissingMapEntryDB</p> | <p>Entrada de mapa de banco de dados ausente padrão para o mesmo local.</p> | 
| <p>JET_bitReplayIgnoreLostLogs</p> | <p>Ignore os logs perdidos do final do fluxo de log.</p><p><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> é introduzido no Windows 7.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


#### <a name="remarks"></a>Comentários

Uma instância deve ser inicializada com uma chamada para **JetInit2** antes que ela possa ser usada por qualquer coisa diferente de [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Uma instância é destruída por uma chamada para a [função JetTerm,](./jetterm-function.md) mesmo que essa instância nunca seja inicializada usando [JetInit](./jetinit-function.md). Uma instância é a unidade de capacidade de recuperação para o mecanismo de banco de dados. Ele controla o ciclo de vida de todos os arquivos usados para proteger a integridade dos dados em um conjunto de arquivos de banco de dados. Esses arquivos incluem o arquivo de ponto de verificação e os arquivos de log de transações.

Se a recuperação estiver em execução em um conjunto de logs, para o qual nem todos os bancos de dados estão presentes (o que retornará o erro JET_errAttachedDatabaseMismatch em circunstâncias normais) e o cliente desejar que a recuperação continue apesar dos bancos de dados ausentes, o JET_ bitReplayIgnoreMissingDB será usado para continuar a recuperação para os bancos de dados disponíveis.

Consulte a seção Comentários em [JetInit](./jetinit-function.md) para obter mais informações.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[Arquivos extensíveis Armazenamento mecanismo](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parâmetros de recurso](./resource-parameters.md)
