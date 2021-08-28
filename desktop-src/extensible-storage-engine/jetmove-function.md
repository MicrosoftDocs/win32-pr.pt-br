---
description: 'Saiba mais sobre: função JetMove'
title: Função JetMove
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 020018ede6be6ff13d65667deee5c189d98e1e53
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474052"
---
# <a name="jetmove-function"></a>Função JetMove


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetmove-function"></a>Função JetMove

A função **JetMove** posiciona um cursor no início ou no final de um índice e percorre as entradas nesse índice para frente ou para trás. Também é possível mover o cursor para frente ou para trás no índice atual por um número especificado de entradas de índice. Outra abordagem é limitar artificialmente as entradas de índice que podem ser enumeradas usando **JetMove** Configurando um intervalo de índice no cursor usando [JetSetIndexRange](./jetsetindexrange-function.md).

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*Galinha*

Um deslocamento arbitrário que indica o movimento desejado do cursor no índice atual.

Além dos deslocamentos padrão, esse parâmetro também pode ser definido com uma das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_MoveFirst</p> | <p>Move o cursor para a primeira entrada de índice no índice (se houver).</p><p><strong>Observação</strong>   O valor literal de-2147483648 é usado para indicar essa opção. Não use esse valor como um deslocamento comum ou um comportamento não intencional pode resultar.</p> | 
| <p>JET_MoveLast</p> | <p>Move o cursor para a última entrada de índice no índice (se houver).</p><p><strong>Observação</strong>   O valor literal de 2147483647 é usado para indicar essa opção. Não use esse valor como um deslocamento comum ou um comportamento não intencional pode resultar.</p> | 
| <p>JET_MoveNext</p> | <p>Move o cursor para a próxima entrada de índice no índice (se houver). Esse valor é exatamente igual a um deslocamento comum de + 1.</p> | 
| <p>JET_MovePrevious</p> | <p>Move o cursor para a entrada de índice anterior no índice (se houver).</p><p>Esse valor é exatamente igual a um deslocamento comum de-1 ou 0 (zero).</p><p>O cursor permanece na posição lógica atual e a existência da entrada de índice que corresponde a essa posição lógica será testada.</p> | 



*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitMoveKeyNE</p> | <p>Move o cursor para frente ou para trás pelo número de entradas de índice necessárias para ignorar o número solicitado de valores de chave de índice encontrados no índice. Isso tem o efeito de recolher entradas de índice com valores de chave duplicados em uma única entrada de índice. Normalmente, um deslocamento moverá o cursor pelo número especificado de entradas de índice, independentemente de seus valores de chave.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso. Para <strong>JetMove</strong>, isso significa que uma entrada de índice foi encontrada no local ou deslocamento solicitado no índice atual.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>O cursor não está posicionado atualmente em uma entrada de índice. Para <strong>JetMove</strong>, isso significa que uma entrada de índice não foi encontrada no local ou deslocamento solicitado no índice atual.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRecordDeleted</p> | <p>No momento, o cursor está posicionado logicamente em uma entrada de índice que corresponde a um registro que foi excluído.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p> | 



Se essa função for bem sucedido, o cursor será posicionado em uma entrada de índice que corresponda ao local ou deslocamento solicitado. Se um registro tiver sido preparado para atualização, essa atualização será cancelada. Se um intervalo de índice estiver em vigor e JET_MoveFirst ou JET_MoveLast tiver sido especificado, esse intervalo de índice será cancelado. Nenhuma alteração no estado do banco de dados ocorrerá.

Se essa função falhar, a posição do cursor permanecerá inalterada, a menos que JET_errNoCurrentRecord tenha sido retornado. Nesse caso, o cursor será posicionado onde a entrada de índice que corresponde ao local ou deslocamento solicitado teria sido. O cursor pode ser movido em relação a essa posição, mas ainda não está em uma entrada de índice válida. Se um registro tiver sido preparado para atualização, essa atualização será cancelada. Se um intervalo de índice estiver em vigor e JET_MoveFirst ou JET_MoveLast tiver sido especificado, esse intervalo de índice será cancelado. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Um cursor pode ser movido para duas posições especiais usando **JetMove**, antes da primeira e após a última. Se o cursor estiver na primeira entrada de índice na tabela e **JetMove** for chamado com JET_MovePrevious, a chamada falhará com JET_errNoCurrentRecord e o cursor será posicionado logicamente antes da primeira entrada no índice. Essa posição lógica é mantida mesmo que outra entrada de índice seja inserida antes da primeira entrada no índice. Uma situação análoga ocorre para o depois do último em relação ao final do índice. Antes de primeiro e depois da última, as últimas são úteis ao configurar um intervalo de entradas de índice a ser iterado usando **JetMove**, usando um modelo de iterador que espera sempre mover para o próximo elemento (ou anterior) antes de usar esse elemento.

O conjunto de entradas de índice que podem ser visitadas por **JetMove** pode ser limitado Configurando um intervalo de índice no cursor. Isso é útil para aplicativos que enumeram um conjunto de entradas de índice que correspondem a critérios simples que podem ser expressos por meio de um par de chaves de pesquisa criadas para esse índice. Para obter mais informações, consulte [JetSetIndexRange](./jetsetindexrange-function.md).

em versões anteriores ao Windows Server 2003 SP1, há um problema em **JetMove** que ocorre em alguns casos específicos, que afeta a imposição correta de um intervalo de índice, conforme configurado pela função [JetSetIndexRange](./jetsetindexrange-function.md) . Se o cursor estiver no momento antes da primeira entrada de índice e um intervalo de índice for definido com um limite superior menor que a primeira entrada de índice, a próxima chamada para **JetMove** irá erroneamente para essa entrada de índice em vez de falhar com JET_errNoCurrentRecord, conforme esperado. O mesmo erro ocorrerá na situação análoga a partir do final do índice. Essa situação pode ocorrer em um aplicativo que configura um intervalo de índice e o navega usando um iterador que espera iniciar antes da primeira entrada de índice que é membro do conjunto de entradas a serem enumeradas, em vez de iniciar na primeira entrada de índice desse conjunto. Essa situação também ocorre no caso análogo, começando do final do índice. A solução alternativa é que o aplicativo Verifique manualmente se a entrada de índice adquirida está dentro do intervalo de índice, comparando a chave da entrada de índice atual (recuperada usando [JetRetrieveKey](./jetretrievekey-function.md)) com a chave que representa o final do intervalo de índice atual (recuperado usando [JetRetrieveKey](./jetretrievekey-function.md) usando JET_bitRetrieveCopy).

É importante ter cuidado ao passar deslocamentos computados para **JetMove**. Se o deslocamento calculado for menor ou igual a JET_MoveFirst, esse deslocamento deverá ser dividido em várias partes, sendo que cada uma é passada para **JetMove** separadamente, mas dentro de uma única transação para obter o efeito desejado. O mesmo é verdadeiro para deslocamentos maiores ou iguais a JET_MoveNext. É improvável que um aplicativo passe por isso no mundo real, mas é bom ter uma defesa contra esse caso, considerando a semântica muito diferente de JET_MoveFirst e JET_MoveLast de um deslocamento comum.

Quando **JetMove** é chamado com um deslocamento muito grande, como quando o parâmetro de galinha é definido como 1000, **JetMove** atravessa todas as entradas de índice 1000 para alcançar a posição final. Atualmente, a API do ESE não fornece uma maneira eficiente de mover diretamente para uma determinada entrada de índice por offset sem percorrer cada entrada de índice.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
