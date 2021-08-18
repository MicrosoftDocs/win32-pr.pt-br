---
description: 'Saiba mais sobre: Função JetGotoBookmark'
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
ms.openlocfilehash: 56e94339a49cc80e8b7b416e89efc5c85079981e0430f325e29f1dd711eef63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978989"
---
# <a name="jetgotobookmark-function"></a>Função JetGotoBookmark


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgotobookmark-function"></a>Função JetGotoBookmark

A **função JetGotoBookmark** posiciona um cursor em uma entrada de índice para o registro associado ao indicador especificado. O indicador pode ser usado com qualquer índice definido em uma tabela. O indicador de um registro pode ser recuperado usando [JetGetBookmark](./jetgetbookmark-function.md).

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

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*pvBookmark*

O buffer que contém o indicador a ser usado para posicionar o cursor.

*cbBookmark*

O tamanho do indicador no buffer.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) tipo de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>A operação não pode ser concluída porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:</strong>   Esse valor de retorno foi introduzido no Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>O indicador fornecido é inválido. Isso pode ter ocorrido porque o tamanho do indicador é zero ou o ponteiro do buffer do indicador é <strong>NULL.</strong></p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>O cursor está em um índice secundário e nenhuma entrada de índice pode ser encontrada para o registro associado ao indicador.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Não foi possível encontrar o registro associado ao indicador.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p><strong>Windows XP:</strong>   Esse valor de retorno foi introduzido no Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão está sendo fechada.</p></td>
</tr>
</tbody>
</table>


Se essa função for bem-sucedida, o cursor será posicionado em uma entrada de índice para o registro associado ao indicador especificado. Se um registro tiver sido preparado para atualização, essa atualização será cancelada. Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado. Se uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída. Nenhuma alteração no estado do banco de dados ocorrerá.

Se essa função falhar, a posição do cursor permanecerá inalterada. Se um registro tiver sido preparado para atualização, essa atualização será cancelada. Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado. Se uma chave de pesquisa tiver sido construída para o cursor, essa chave de pesquisa será excluída. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Há duas maneiras de usar um indicador para posicionar um cursor em um índice. A primeira é usar o indicador para posicionar no registro diretamente. Isso ocorre quando o índice atual do cursor é o índice primário. Essa técnica funciona porque um indicador ESENT é o mesmo que a chave primária do registro associado.

A segunda maneira de usar um indicador é posicioná-lo em uma entrada em um índice secundário que corresponde ao registro associado a esse indicador. Durante esse processo, o mecanismo pesquisa o registro real usando o indicador no índice primário. Em seguida, ele usa os dados de registro e a definição de índice secundário para calcular uma chave no índice secundário que aponta para o registro. Em seguida, ele posiciona o cursor na entrada de índice para essa chave. Se o cursor estiver atualmente em um índice secundário em uma ou mais colunas de chave com vários valores, o cursor será posicionado na entrada de índice correspondente ao primeiro valor múltiplo de cada uma dessas colunas de chave.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)
