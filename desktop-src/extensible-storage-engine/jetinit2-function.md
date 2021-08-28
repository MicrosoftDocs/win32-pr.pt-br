---
description: 'Saiba mais sobre: função JetInit2'
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
ms.openlocfilehash: 7874c475dc18beb5d7f6849b9f628ea06cbc32a3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470451"
---
# <a name="jetinit2-function"></a>Função JetInit2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetinit2-function"></a>Função JetInit2

A função **JetInit2** coloca o mecanismo de banco de dados em um estado em que ele pode dar suporte ao uso do aplicativo de arquivos de banco de dados. O mecanismo já deve estar configurado corretamente para inicialização usando [JetSetSystemParameter](./jetsetsystemparameter-function.md). A recuperação de falhas no banco de dados é executada automaticamente como parte do processo de inicialização.

**Windows xp:** o **JetInit2** é introduzido no Windows XP.  

Essa função está obsoleta. Use [JetInit3](./jetinit3-function.md) em vez disso.

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parâmetros

*pinstance*

A instância a ser usada para esta chamada.

para Windows 2000, esse parâmetro é ignorado e sempre deve ser nulo.

para o Windows XP e versões posteriores, o uso desse parâmetro depende do modo de operação do mecanismo. se o mecanismo estiver operando no modo herdado (Windows modo de compatibilidade 2000) em que apenas uma instância tem suporte, esse parâmetro pode ser nulo ou pode ser definido como um buffer de saída válido contendo nulo ou JET_instanceNil que retorna o identificador de instância global criado como um efeito colateral da inicialização. Esse identificador de instância pode então ser passado para qualquer outra API que usa uma instância. Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro deverá ser definido como um buffer de entrada válido que contenha o identificador de instância retornado pelo [JetCreateInstance](./jetcreateinstance-function.md) que está sendo inicializado.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitReplayReplicatedLogFiles</p> | <p>Reservado para uso futuro.</p> | 
| <p>JET_bitCreateSFSVolumeIfNotExist</p> | <p>Reservado para uso futuro.</p> | 
| <p>JET_bitReplayIgnoreMissingDB</p> | <p>Essa opção permite que o usuário execute a recuperação em um conjunto de arquivos de log, sem que todos os bancos de dados estejam presentes, que foram anexados em um ponto do conjunto de logs.</p> | 
| <p>JET_bitRecoveryWithoutUndo</p> | <p>Execute a recuperação, mas pare na fase de desfazer. Isso permite que os logs de transações adicionais sejam copiados e aplicados.</p> | 
| <p>JET_bitTruncateLogsAfterRecovery</p> | <p>Na recuperação reversível bem-sucedida, TRUNCATE os arquivos de log.</p> | 
| <p>JET_bitReplayMissingMapEntryDB</p> | <p>Padrão de entrada de mapa de banco de dados ausente para o mesmo local.</p> | 
| <p>JET_bitReplayIgnoreLostLogs</p> | <p>Ignorar logs perdidos do final do fluxo de log.</p><p><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> é introduzido no Windows 7.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


#### <a name="remarks"></a>Comentários

Uma instância deve ser inicializada com uma chamada para **JetInit2** antes que possa ser usada por algo diferente de [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Uma instância é destruída por uma chamada para a função [JetTerm](./jetterm-function.md) , mesmo que essa instância nunca tenha sido inicializada usando [JetInit](./jetinit-function.md). Uma instância é a unidade de capacidade de recuperação para o mecanismo de banco de dados. Ele controla o ciclo de vida de todos os arquivos usados para proteger a integridade dos dados em um conjunto de arquivos de banco de dado. Esses arquivos incluem o arquivo de ponto de verificação e os arquivos de log de transações.

Se a recuperação estiver em execução em um conjunto de logs, para os quais nem todos os bancos de dados estão presentes (o que retornará o erro JET_errAttachedDatabaseMismatch em circunstâncias normais) e o cliente desejar que a recuperação continue apesar dos bancos de dados ausentes, o JET_ bitReplayIgnoreMissingDB será usado para continuar a recuperação para os bancos de dados disponíveis.

Consulte a seção comentários em [JetInit](./jetinit-function.md) para obter mais informações.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[arquivos do mecanismo de Armazenamento extensível](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parâmetros de recurso](./resource-parameters.md)
