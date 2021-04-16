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
ms.openlocfilehash: 1e66b4e5242710c89ca7e7964ecd0a72774b719d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765137"
---
# <a name="jetstopservice-function"></a>Função JetStopService


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetstopservice-function"></a>Função JetStopService

A função **JetStopService** prepara uma instância para encerramento.

**JetStopService** é a chamada herdada quando apenas uma instância é permitida. Nesse caso, a única instância ativa é aquela que está sendo preparada para encerramento.

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

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
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Não está claro qual instância deve ser preparada para encerramento ao usar <strong>JetStopService</strong> com o modo de várias instâncias.</p>
<p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
</tbody>
</table>


Se essa função for realizada com sucesso, ela se prepara para um encerramento futuro. As etapas seguidas para se preparar para um encerramento incluem o seguinte:

  - Pare a desfragmentação online se ela estiver em execução.

  - Iniciar uma limpeza do repositório de versão.

  - Reduza a profundidade do ponto de verificação iniciando a liberação de páginas sujas no Gerenciador de buffer.

  - Impeça chamadas futuras para a maioria das funções para essa instância.

Se essa função falhar, nenhuma das etapas para se preparar para um encerramento da instância será realizada, portanto, nenhuma alteração no estado da instância ocorrerá.

#### <a name="remarks"></a>Comentários

Essa função reduz o trabalho que a instância terá que fazer quando for encerrada, mas não encerrará a instância. Como resultado, essa função é apenas uma otimização e não é obrigatória para uso. Observe que a quantidade de trabalho realizado na preparação era menor no Windows 2000 e no Windows XP. Depois que a função for realizada com sucesso, a chamada a funções que não são mais permitidas retornará JET_errClientRequestToStopJetService. As funções que ainda são permitidas após essa chamada são: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).

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
</tbody>
</table>


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
