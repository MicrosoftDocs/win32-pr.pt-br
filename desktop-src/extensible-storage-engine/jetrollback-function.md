---
description: 'Saiba mais sobre: Função JetRollback'
title: Função JetRollback
TOCTitle: JetRollback Function
ms:assetid: 685c51f4-8fe4-47cc-8a8e-c42014431b8b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269273(v=EXCHG.10)
ms:contentKeyID: 32765575
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRollback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e23bd408ec88109a0f77635ac53e89003df9a992
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985549"
---
# <a name="jetrollback-function"></a>Função JetRollback


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetrollback-function"></a>Função JetRollback

A **função JetRollback** desfaz as alterações feitas no estado do banco de dados e retorna para o último ponto de salvar. **JetRollback** também fechará todos os cursores abertos durante o ponto de salvar. Se o ponto de salvar mais externo for desfeito, a sessão sairá da transação.

```cpp
    JET_ERR JET_API JetRollback(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*grbit*

Um grupo de bits que contém as opções a serem usadas para essa chamada, que incluem zero ou mais dos seguintes:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRollbackAll</p> | <p>Essa opção solicita que todas as alterações feitas no estado do banco de dados durante todos os pontos de salvar sejam desfeitas. Como resultado, a sessão sairá da transação.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errNotInTransaction</p> | <p>A operação falhou porque a sessão determinada não está em uma transação.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errRollbackError</p> | <p>Não foi possível reverter as alterações devido a um erro fatal.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 



Em caso de êxito, todas as alterações feitas no banco de dados durante o ponto de economia atual para a sessão determinada serão desfeitas e esse ponto de salvar será encerrado. Se o último ponto de salvar para a sessão tiver sido encerrado, a sessão sairá da transação.

Em caso de falha, o estado transacional da sessão permanecerá inalterado. Nenhuma alteração no estado do banco de dados ocorrerá. Uma falha durante a reação é considerada um erro de banco de dados catastrófico.

#### <a name="remarks"></a>Comentários

Deve haver uma chamada para [JetCommitTransaction](./jetcommittransaction-function.md) ou **JetRollback** para corresponder a cada chamada para [JetBeginTransaction](./jetbegintransaction-function.md) para uma determinada sessão.

Se algum cursor tiver sido aberto (usando [JetOpenTable](./jetopentable-function.md), por exemplo) durante um ponto de salvar que está sendo reenvelhado, esse cursor será fechado.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)
