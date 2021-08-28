---
description: 'Saiba mais sobre: Função JetStopServiceInstance'
title: Função JetStopServiceInstance
TOCTitle: JetStopServiceInstance Function
ms:assetid: d8d3d047-91d6-4054-b3e1-44174666900e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294108(v=EXCHG.10)
ms:contentKeyID: 32765723
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopServiceInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55f9a8c6e91a70e447f03bc19bcd191d01ba0e08
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984299"
---
# <a name="jetstopserviceinstance-function"></a>Função JetStopServiceInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetstopserviceinstance-function"></a>Função JetStopServiceInstance

A **função JetStopServiceInstance** prepara uma instância para encerramento.

**Windows XP:****JetStopServiceInstance** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parâmetros

*Instância*

A instância em execução a ser usada para a chamada à API.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>O parâmetro de instância especificado tem um valor inválido (não uma instância que está em execução no momento).</p><p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p> | 



Se essa função for bem-sucedida, ela se preparará para um encerramento futuro. As etapas tomadas para se preparar para um encerramento incluem o seguinte:

  - Pare a desfragmentação online se ela estiver em execução.

  - Inicie uma limpeza do armazenamento de versão.

  - Reduza a profundidade do ponto de verificação iniciando a liberação de páginas sujas no gerenciador de buffers.

  - Impedir chamadas futuras para a maioria das funções para essa instância.

Se essa função falhar, nenhuma das etapas de preparação para uma terminação de instância será realizada, portanto, nenhuma alteração no estado da instância ocorrerá.

#### <a name="remarks"></a>Comentários

Essa função reduzirá o trabalho que a instância terá que fazer quando terminar, mas não encerrará a instância. Como resultado, essa função é apenas uma otimização e não é obrigatória para uso. Observe que a quantidade de trabalho feito na preparação foi menor Windows 2000 e Windows XP. Depois que a função for bem-sucedida, chamar funções que não são mais permitidas retornará JET_errClientRequestToStopJetService. As funções que ainda são permitidas após essa chamada são: [JetRollback,](./jetrollback-function.md) [JetCloseTable,](./jetclosetable-function.md) [JetEndSession,](./jetendsession-function.md) [JetCloseDatabase,](./jetclosedatabase-function.md) [JetDetachDatabase](./jetdetachdatabase-function.md) e [JetResetSessionContext.](./jetresetsessioncontext-function.md)

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
