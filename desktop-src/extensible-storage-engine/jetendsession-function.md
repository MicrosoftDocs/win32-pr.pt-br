---
description: 'Saiba mais sobre: função JetEndSession'
title: Função JetEndSession
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b96ae49ef907cea158d1496339a740e1026ffea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472562"
---
# <a name="jetendsession-function"></a>Função JetEndSession


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetendsession-function"></a>Função JetEndSession

A função **JetEndSession** encerra a sessão e limpa e desaloca todos os recursos associados à sessão especificada.

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser encerrada. Os recursos associados são liberados quando a sessão termina.

*grbit*

Reservado. Esse parâmetro pode conter o sinalizador JET_bitForceSessionClosed, mas esse sinalizador é reservado e a configuração não tem nenhum efeito.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro gerou um resultado inesperado.</p> | 
| <p>JET_errInvalidSesid</p> | <p>A sessão não era uma sessão JET válida.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errOutOfMemory</p> | <p>A operação falhou porque não foi possível alocar memória.</p> | 
| <p>JET_errSessionInUse</p> | <p>Isso significa que a sessão estava em uso em outro thread ou a sessão não foi definida ou redefinida corretamente.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p>esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errOutOfBuffers</p> | <p>Erro do sistema que indica que não há mais buffers.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 



Em caso de sucesso, o identificador de sessão é fechado e não está disponível e todos os recursos relacionados a essa sessão são limpos.

Em caso de falha, há vários erros adicionais que podem ocorrer como parte do fechamento da tabela de classificação, fechamento do cursor e reversão da transação. Esses erros são bastante improvável e extremamente improvável se suas sessões não estiverem totalmente em uso quando **JetEndSession** for chamado. Esses erros serão retornados se alguma parte da sessão não puder ser limpa corretamente.

#### <a name="remarks"></a>Comentários

Essa API reverterá todas as transações abertas (não confirmadas no nível 0). Além disso, todos os cursores associados a essa sessão e quaisquer tabelas de classificação que foram criadas ou abertas serão limpos.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
