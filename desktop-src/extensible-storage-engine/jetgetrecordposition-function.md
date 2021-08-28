---
description: 'Saiba mais sobre: função JetGetRecordPosition'
title: Função JetGetRecordPosition
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd1e84b995485afd46119b78289c1cac23e19215
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982429"
---
# <a name="jetgetrecordposition-function"></a>Função JetGetRecordPosition


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetrecordposition-function"></a>Função JetGetRecordPosition

A função **JetGetRecordPosition** retorna a posição fracionária do registro atual no índice atual na forma de uma estrutura de [JET_RECPOS](./jet-recpos-structure.md) . Essa estrutura descreve as posições fracionárias em termos de um número aproximado de entradas de índice antes do registro atual e um número total aproximado de entradas no índice.

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*precpos*

A descrição da fração a ser usada para obter a posição do registro atual no índice atual.

*cbRecpos*

O tamanho da memória alocada em *precpos*.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Esta operação não pode ser concluída porque a instância, associada à sessão, encontrou um erro fatal. É necessário que o acesso a todos os dados seja revogado a fim de proteger a integridade desses dados.</p><p><strong>Windows 2000:</strong>  esse erro não será retornado pelo sistema operacional Windows 2000.</p> | 
| <p>JET_errInvalidParameter</p> | <p>O tamanho da memória alocada em <em>precpos</em> não é um tamanho suficiente.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>O cursor não está em um registro no momento e não pode retornar uma posição.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p><strong>Windows 2000:</strong>  esse erro não será retornado pelo sistema operacional Windows 2000.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p> | 



Em caso de sucesso, o número aproximado de entradas de índice que antecedem o registro atual no índice são retornados em precpos- \> centriesLT. 1 é retornado em precpos- \> centriesInRange. O número aproximado de entradas no índice é retornado em precpos- \> centriesTotal.

Em caso de falha, nenhuma alteração é feita na memória alocada em *precpos*.

#### <a name="remarks"></a>Comentários

Essa operação retorna dados variados quando as atualizações ocorrem continuamente na tabela. As alterações nos valores nem sempre corresponderão às expectativas com base no conhecimento das atualizações, já que os valores são aproximações com base nas propriedades físicas do índice. O isolamento transacional não se aplica a posições de **JetGetRecordPosition** , pois os valores dependem das propriedades físicas do índice que não são isoladas da transação.

[JET_RECPOS](./jet-recpos-structure.md) não deve ser usado para descrever um registro em uma tabela ou para reposicionar um registro próximo a um registro existente. Em vez disso, os indicadores para um registro existente devem ser recuperados e, em seguida, usados para reposicionar o mesmo registro.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RECPOS](./jet-recpos-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetGotoPosition](./jetgotoposition-function.md)  
[JetStopService](./jetstopservice-function.md)
