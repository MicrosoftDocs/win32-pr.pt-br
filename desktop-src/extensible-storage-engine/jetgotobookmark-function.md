---
description: 'Saiba mais sobre: função JetGotoBookmark'
title: Função JetGotoBookmark
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54a6370badcdd83e1beed4cc50f42a52eab797ba
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984639"
---
# <a name="jetgotobookmark-function"></a>Função JetGotoBookmark


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgotobookmark-function"></a>Função JetGotoBookmark

A função **JetGotoBookmark** posiciona um cursor para uma entrada de índice para o registro associado ao indicador especificado. O indicador pode ser usado com qualquer índice definido em uma tabela. O indicador de um registro pode ser recuperado usando [JetGetBookmark](./jetgetbookmark-function.md).

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*pvBookmark*

O buffer que contém o indicador a ser usado para posicionar o cursor.

*cbBookmark*

O tamanho do indicador no buffer.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>   esse valor de retorno foi introduzido no Windows XP.</p> | 
| <p>JET_errInvalidBookmark</p> | <p>O indicador fornecido é inválido. Isso pode ter ocorrido porque o tamanho do indicador é zero ou o ponteiro do buffer do indicador é <strong>nulo</strong>.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>O cursor está em um índice secundário e nenhuma entrada de índice foi encontrada para o registro associado ao indicador.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Não foi possível encontrar o registro associado ao indicador.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong>   esse valor de retorno foi introduzido no Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p> | 



Se essa função for bem sucedido, o cursor será posicionado em uma entrada de índice para o registro associado ao indicador especificado. Se um registro tiver sido preparado para atualização, essa atualização será cancelada. Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado. Se uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída. Nenhuma alteração no estado do banco de dados ocorrerá.

Se essa função falhar, a posição do cursor permanecerá inalterada. Se um registro tiver sido preparado para atualização, essa atualização será cancelada. Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado. Se uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Há duas maneiras de usar um indicador para posicionar um cursor em um índice. A primeira é usar o indicador para posicioná-lo diretamente no registro. Isso ocorre quando o índice atual do cursor é o índice primário. Essa técnica funciona porque um indicador de ESENT é o mesmo que a chave primária do registro associado.

A segunda maneira de usar um indicador é posicioná-lo em uma entrada em um índice secundário que corresponda ao registro associado a esse indicador. Durante esse processo, o mecanismo pesquisa o registro real usando o indicador no índice primário. Em seguida, ele usa os dados de registro e a definição de índice secundário para computar uma chave no índice secundário que aponta para o registro. Em seguida, ele posiciona o cursor na entrada de índice para essa chave. Se o cursor estiver atualmente em um índice secundário em uma ou mais colunas de chave com valores múltiplos, o cursor será posicionado na entrada de índice correspondente ao primeiro valor múltiplo de cada uma dessas colunas de chave.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)
