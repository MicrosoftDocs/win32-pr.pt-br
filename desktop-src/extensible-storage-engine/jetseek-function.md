---
description: 'Saiba mais sobre: Função JetSeek'
title: Função JetSeek
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fbc980a838742971d2ecc3dfeebf5efb6295ea3
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985539"
---
# <a name="jetseek-function"></a>Função JetSeek


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetseek-function"></a>Função JetSeek

A **função JetSeek** posiciona com eficiência um cursor para uma entrada de índice que corresponde aos critérios de pesquisa especificados pela chave de pesquisa nesse cursor e a desigualdade especificada. Uma chave de pesquisa deve ter sido construída anteriormente usando [JetMakeKey.](./jetmakekey-function.md)

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*grbit*

Um grupo de bits que contém as opções a serem usadas para essa chamada. *Grbit* deve ser não zero e deve incluir um ou mais dos valores listados na tabela a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitCheckUniqueness</p> | <p>Um código de erro especial, JET_wrnUniqueKey, será retornado se puder ser determinado de maneira barata que há exatamente uma entrada de índice que corresponde à chave de pesquisa.</p><p>Essa opção é ignorada, a menos que JET_bitSeekEQ também seja especificado.</p><p>Essa opção só está disponível no Windows Server 2003 e versões posteriores.</p> | 
| <p>JET_bitSeekEQ</p> | <p>O cursor será posicionado na entrada de índice mais próxima do início do índice que corresponde exatamente à chave de pesquisa. O início do índice é a entrada de índice encontrada ao mover para o primeiro registro nesse índice. O início do índice não é o mesmo que a extremidade baixa do índice, que pode mudar dependendo da ordem de classificação das colunas de chave no índice.</p><p>Não é significativo usar essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga.</p> | 
| <p>JET_bitSeekGE</p> | <p>O cursor será posicionado na entrada de índice mais próxima do início do índice que é maior ou igual a uma entrada de índice que corresponderia exatamente aos critérios de pesquisa. O início do índice é a entrada de índice encontrada ao mover para o primeiro registro nesse índice. O início do índice não é o mesmo que a extremidade baixa do índice, que pode mudar dependendo da ordem de classificação das colunas de chave no índice.</p><p>Não é significativo usar essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga destinada a encontrar entradas de índice mais próximas ao final do índice.</p> | 
| <p>JET_bitSeekGT</p> | <p>O cursor será posicionado na entrada de índice mais próxima ao início do índice maior que uma entrada de índice que corresponderia exatamente aos critérios de pesquisa. O início do índice é a entrada de índice encontrada ao mover para o primeiro registro nesse índice. O início do índice não é o mesmo que a extremidade baixa do índice, que pode mudar dependendo da ordem de classificação das colunas de chave no índice.</p><p>Não é significativo usar essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga destinada a encontrar entradas de índice mais próximas do início do índice.</p> | 
| <p>JET_bitSeekLE</p> | <p>O cursor será posicionado na entrada de índice mais próxima ao final do índice que é menor ou igual a uma entrada de índice que corresponderia exatamente aos critérios de pesquisa. O final do índice é a entrada de índice encontrada ao mover para o último registro nesse índice. O final do índice não é o mesmo que o alto final do índice, que pode mudar dependendo da ordem de classificação das colunas de chave no índice.</p><p>Não é significativo usar essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga destinada a encontrar entradas de índice mais próximas do início do índice.</p> | 
| <p>JET_bitSeekLT</p> | <p>O cursor será posicionado na entrada de índice mais próxima ao final do índice que é menor que uma entrada de índice que corresponderia exatamente aos critérios de pesquisa. O final do índice é a entrada de índice encontrada ao mover para o último registro nesse índice. O final do índice não é o mesmo que o alto final do índice, que pode mudar dependendo da ordem de classificação das colunas de chave no índice.</p><p>Não é significativo usar essa opção com uma chave de pesquisa que foi construída usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando uma opção curinga destinada a encontrar entradas de índice mais próximas ao final do índice.</p> | 
| <p>JET_bitSetIndexRange</p> | <p>Um intervalo de índice será configurado automaticamente para todas as chaves que corresponderem exatamente à chave de pesquisa. O intervalo de índice resultante é idêntico a um que teria sido criado de outra forma por uma chamada para <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> com as JET_bitRangeInclusive e JET_bitRangeUpperLimit opções. Consulte <a href="gg294112(v=exchg.10).md">JetSetIndexRange para</a> obter mais informações.</p><p>Esse é um método conveniente para descobrir todas as entradas de índice que corresponderem aos mesmos critérios de pesquisa.</p><p>Essa opção é ignorada, a menos que JET_bitSeekEQ também seja especificado.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função permite o retorno de [qualquer](./jet-err.md) JET_ERRs que são definidas nesta API. Para obter mais informações sobre erros do Jet, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p><p>Para <strong>JetSeek</strong>, isso significa que foi encontrada uma entrada de índice que corresponderam exatamente aos critérios de pesquisa.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p>Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Não há nenhuma chave de pesquisa atual para o cursor. <strong>JetSeek</strong> requer que o cursor tenha uma chave de pesquisa válida, pois ele o usará para os critérios de pesquisa usados para encontrar entradas de índice.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRecordNotFound</p> | <p>Nenhuma entrada de índice que corresponder aos critérios de pesquisa foi encontrada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_wrnSeekNotEqual</p> | <p>Foi encontrada uma entrada de índice que corresponderia aos critérios de pesquisa. No entanto, essa entrada de índice não era uma combinação exata.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p>Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_wrnUniqueKey</p> | <p>Foi encontrada exatamente uma entrada de índice que corresponderam exatamente aos critérios de pesquisa. Esse erro só será retornado se JET_bitSeekCheckUniqueness foi especificado e foi barato determinar que a entrada de índice correspondente era a única entrada de índice que corresponde exatamente aos critérios de pesquisa.</p><p>Esse erro só será retornado pelo Windows Server 2003 e versões posteriores.</p> | 



Em caso de êxito, o cursor será posicionado em uma entrada de índice que corresponde aos critérios de pesquisa. Se um registro tiver sido preparado para atualização, essa atualização será cancelada. Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado. Se uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída. Nenhuma alteração no estado do banco de dados ocorrerá. Quando várias entradas de índice têm o mesmo valor, a entrada mais próxima ao início do índice é sempre selecionada.

Em caso de falha, a posição do cursor permanecerá inalterada, a menos que JET_errRecordNotFound tenha sido retornado. Nesse caso, o cursor será posicionado em que a entrada de índice que corresponder aos critérios de pesquisa especificados pela chave de pesquisa nesse cursor e a desigualdade especificada teria sido. O cursor pode ser movido em relação a essa posição, mas ainda não está em uma entrada de índice válida. Se um registro tiver sido preparado para atualização, essa atualização será cancelada. Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado. Se uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída. Nenhuma alteração no estado do banco de dados ocorrerá.

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
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
