---
description: 'Saiba mais sobre: função JetStopService'
title: Função JetStopService
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75e8622d79f2757bee8ab3041250b2ba78499194
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480302"
---
# <a name="jetstopservice-function"></a>Função JetStopService


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetstopservice-function"></a>Função JetStopService

A função **JetStopService** prepara uma instância para encerramento.

**JetStopService** é a chamada herdada quando apenas uma instância é permitida. Nesse caso, a única instância ativa é aquela que está sendo preparada para encerramento.

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Não está claro qual instância deve ser preparada para encerramento ao usar <strong>JetStopService</strong> com o modo de várias instâncias.</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 



Se essa função for realizada com sucesso, ela se prepara para um encerramento futuro. As etapas seguidas para se preparar para um encerramento incluem o seguinte:

  - Pare a desfragmentação online se ela estiver em execução.

  - Iniciar uma limpeza do repositório de versão.

  - Reduza a profundidade do ponto de verificação iniciando a liberação de páginas sujas no Gerenciador de buffer.

  - Impeça chamadas futuras para a maioria das funções para essa instância.

Se essa função falhar, nenhuma das etapas para se preparar para um encerramento da instância será realizada, portanto, nenhuma alteração no estado da instância ocorrerá.

#### <a name="remarks"></a>Comentários

Essa função reduz o trabalho que a instância terá que fazer quando for encerrada, mas não encerrará a instância. Como resultado, essa função é apenas uma otimização e não é obrigatória para uso. observe que a quantidade de trabalho realizado na preparação foi menor em Windows 2000 e Windows XP. Depois que a função for realizada com sucesso, a chamada a funções que não são mais permitidas retornará JET_errClientRequestToStopJetService. As funções que ainda são permitidas após essa chamada são: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



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
