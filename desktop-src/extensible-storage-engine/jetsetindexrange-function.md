---
description: 'Saiba mais sobre: função JetSetIndexRange'
title: Função JetSetIndexRange
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 330adc9b4d18a7bfa66ced0c9cb5776f31162be5
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988449"
---
# <a name="jetsetindexrange-function"></a>Função JetSetIndexRange


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetsetindexrange-function"></a>Função JetSetIndexRange

A função **JetSetIndexRange** limita temporariamente o conjunto de entradas de índice que o cursor pode percorrer usando [JetMove](./jetmove-function.md) para aqueles que começam da entrada de índice atual e terminam na entrada de índice que corresponde aos critérios de pesquisa especificados pela chave de pesquisa nesse cursor e os critérios de associação especificados. Uma chave de pesquisa deve ter sido construída anteriormente usando [JetMakeKey](./jetmakekey-function.md).

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*tableidSrc*

O cursor a ser usado para esta chamada.

*grbit*

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos seguintes:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRangeInclusive</p> | <p>Esta presença ou ausência dessa opção indica os critérios de limite do intervalo de índice. Quando presente, essa opção indica que o limite do intervalo de índice é inclusivo. Quando ausente, essa opção indica que o limite do intervalo de índice é exclusivo. Quando o limite do intervalo de índice é inclusivo, as entradas de índice que correspondem exatamente aos critérios de pesquisa são incluídas no intervalo.</p> | 
| <p>JET_bitRangeInstantDuration</p> | <p>Essa opção solicita que o intervalo de índice seja removido assim que tiver sido estabelecido. Todos os outros aspectos da operação permanecem inalterados. Isso é útil para testar a existência de entradas de índice que correspondam aos critérios de pesquisa.</p> | 
| <p>JET_bitRangeRemove</p> | <p>Essa opção solicita que um intervalo de índice existente no cursor seja cancelado. Depois que o intervalo de índice for cancelado, será possível mover-se além do final do intervalo de índice usando <a href="gg294117(v=exchg.10).md">JetMove</a>. Se um intervalo de índice ainda não estiver em vigor, <strong>JetSetIndexRange</strong> falhará com JET_errInvalidOperation.</p><p>Quando essa opção é especificada, todas as outras opções são ignoradas.</p> | 
| <p>JET_bitRangeUpperLimit</p> | <p>Se essa opção for usada, a chave de pesquisa no cursor representará os critérios de pesquisa para a entrada de índice mais próxima do final do índice que corresponderá ao intervalo de índice. O intervalo de índice será estabelecido entre a posição atual do cursor e essa entrada de índice para que todas as correspondências possam ser encontradas percorrendo o índice usando <a href="gg294117(v=exchg.10).md">JetMove</a> com JET_MoveNext ou um deslocamento positivo.</p><p>Não é significativo usar essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga para localizar entradas de índice mais próximas ao início do índice.</p><p>Se essa opção for omitida, a chave de pesquisa no cursor representará os critérios de pesquisa para a entrada de índice mais próxima do início do índice que corresponderá ao intervalo de índice. O intervalo de índice será estabelecido entre a posição atual do cursor e essa entrada de índice para que todas as correspondências possam ser encontradas com a movimentação para trás no índice usando <a href="gg294117(v=exchg.10).md">JetMove</a> com JET_MovePrevious ou um deslocamento negativo.</p><p>Não é significativo omitir essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga destinada a encontrar entradas de índice mais próximas ao final do índice.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p><p>Para <strong>JetSetIndexRange</strong>, isso significa que um intervalo de índice existente foi cancelado ou que há pelo menos uma entrada de índice dentro do intervalo de índice.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p>esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidOperation</p> | <p>Esse erro será retornado por <strong>JetSetIndexRange</strong> quando JET_bitRangeRemove foi especificado e nenhum intervalo de índice estava em vigor.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Não há uma chave de pesquisa atual para o cursor. <strong>JetSetIndexRange</strong> exige que o cursor tenha uma chave de pesquisa válida porque usará isso para os critérios de pesquisa usados para localizar entradas de índice.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>Não há índice atual para o cursor. Isso ocorrerá para <strong>JetSetIndexRange</strong> se o cursor estiver no índice clusterizado de uma tabela, um índice primário não foi definido. Não há suporte para a definição de um intervalo de índice em tal índice.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Esse erro será retornado por <strong>JetSetIndexRange</strong> para indicar que não há entradas de índice dentro do intervalo de índice.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p>esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 



Em caso de sucesso, se JET_bitRangeRemove for especificado, o intervalo de índice que está atualmente em vigor será cancelado. Se JET_bitRangeRemove não for especificado e JET_bitRangeInstantDuration for especificado, nenhum intervalo de índice estará em vigor. Se nem JET_bitRangeRemove nem JET_bitRangeInstantDuration for especificado, um novo intervalo de índice estará em vigor. Esse intervalo de índice limitará temporariamente o conjunto de entradas de índice que o cursor pode percorrer usando [JetMove](./jetmove-function.md) para aqueles que começam da entrada de índice atual e terminando na entrada de índice que corresponde aos critérios de pesquisa. A posição do cursor permanecerá inalterada. Se uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída. Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, se JET_errNoCurrentRecord não for retornado, nenhum intervalo de índice estará em vigor. Se JET_errNoCurrentRecord for retornado, um novo intervalo de índice estará em vigor. Esse intervalo de índice limitará temporariamente o conjunto de entradas de índice que o cursor pode percorrer usando [JetMove](./jetmove-function.md) para aqueles que começam da entrada de índice atual e terminando na entrada de índice que corresponde aos critérios de pesquisa. A posição do cursor permanecerá inalterada. Se JET_errNoCurrentRecord for retornado e uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Um intervalo de índice é volátil e será cancelado automaticamente se qualquer navegação diferente de [JetMove](./jetmove-function.md) for executada no cursor.

Os intervalos de índice funcionam apenas em uma direção. Se um limite superior for estabelecido, somente o movimento de encaminhamento usando [JetMove](./jetmove-function.md) com JET_MoveNext ou um deslocamento positivo será impedido depois que o final do intervalo de índice for atingido. Ainda é possível deixar o intervalo de índice nesse caso usando [JetMove](./jetmove-function.md) com JET_MovePrevious ou um deslocamento negativo. Uma situação análoga ocorre para um limite inferior.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetMove](./jetmove-function.md)  
[JetSetIndexRange]()  
[JetStopService](./jetstopservice-function.md)
