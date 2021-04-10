---
description: 'Saiba mais sobre: função JetEnumerateColumns'
title: Função JetEnumerateColumns
TOCTitle: JetEnumerateColumns Function
ms:assetid: 8413d056-cdb1-420e-9dd3-7280ad510165
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269321(v=EXCHG.10)
ms:contentKeyID: 32765611
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnumerateColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b913fb970232ca6f0fc21eb846df85e1db684f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170541"
---
# <a name="jetenumeratecolumns-function"></a>Função JetEnumerateColumns


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetenumeratecolumns-function"></a>Função JetEnumerateColumns

A função **JetEnumerateColumns** recupera com eficiência um conjunto de colunas e seus valores do registro atual de um cursor ou o buffer de cópia desse cursor. As colunas e os valores recuperados podem ser restringidos por uma lista de IDs de coluna, números de *itagSequence* e outras características. Essa API de recuperação de coluna é exclusiva, pois retorna informações na memória alocada dinamicamente que é obtida usando um retorno de chamada compatível de [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornecido pelo usuário. Essa nova flexibilidade permite a recuperação eficiente de dados de coluna com características específicas (como tamanho e multiplicidade) que são desconhecidos para o chamador. Isso elimina a necessidade de usar os modos de descoberta de [JetRetrieveColumn](./jetretrievecolumn-function.md) para determinar essas características a fim de configurar uma chamada final para [JetRetrieveColumn](./jetretrievecolumn-function.md) que recuperará com êxito os dados desejados.

**Windows XP: o JetEnumerateColumns** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetEnumerateColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long cEnumColumnId,
      __in_opt      JET_ENUMCOLUMNID* rgEnumColumnId,
      __out         unsigned long* pcEnumColumn,
      __out         JET_ENUMCOLUMN** prgEnumColumn,
      __in          JET_PFNREALLOC pfnRealloc,
      __in          void* pvReallocContext,
      __in          unsigned long cbDataMost,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*cEnumColumnId*

Uma matriz de IDs de coluna, cada uma com uma matriz opcional de números *itagSequence* para enumerar.

Se *cEnumColumnId* for 0 (zero), então *rgEnumColumnId* será ignorado e todos os valores de coluna serão enumerados e retornados ao chamador. Se um elemento da matriz de ID de coluna se referir a uma ID de coluna 0 (zero), a enumeração dessa coluna será ignorada e um slot correspondente na saída será gerado com um status de coluna de JET_wrnColumnSkipped.

Se *ctagSequence* for 0 (zero) para um determinado elemento da matriz de ID de coluna, *rgtagSequence* será ignorado e todos os valores de coluna para essa ID de coluna serão enumerados e retornados ao chamador. Se um elemento de uma matriz de número *itagSequence* se referir a um número de *itagSequence* de 0 (zero), a enumeração desse número de *itagSequence* será ignorada e um slot correspondente na saída será gerado com um status de valor de coluna de JET_wrnColumnSkipped.

*rgEnumColumnId*

Consulte *cEnumColumnId*.

*pcEnumColumn*

Retorna a matriz enumerada de colunas e seus valores na memória alocada por meio do retorno de chamada compatível com *itagSequence* fornecido.

Se uma matriz de IDs de coluna for solicitada na entrada, a ordem e o tamanho da matriz de saída refletirão a ordem e o tamanho da matriz de entrada. Da mesma forma, se uma matriz de números *itagSequence* for solicitada para uma ID de coluna específica na entrada, a ordem e o tamanho da matriz de saída de valores de coluna para essa coluna refletirão a ordem e o tamanho da matriz de entrada.

Os parâmetros de saída são definidos como 0 (zero) e **nulos** em qualquer erro, exceto JET_errBadColumnId e JET_errColumnNotFound. Quando esses erros são retornados, os dados de saída são válidos e concluídos para todas as identificações de coluna afetadas. O código de status de cada uma das IDs de coluna afetadas é definido como um desses erros para que o chamador possa determinar quais IDs de coluna eram ruins e, potencialmente, tomar uma ação corretiva.

*prgEnumColumn*

Consulte *pcEnumColumn*.

*pfnRealloc*

Identifica um retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) e um ponteiro de contexto opcional usado para alocar memória para a matriz de saída de colunas e seus valores.

*pvReallocContext*

Consulte *pfnRealloc*.

*cbDataMost*

Define um limite na quantidade de dados a serem retornados de uma coluna longa de texto longo ou binário longo.

Esse parâmetro pode ser usado para impedir a enumeração de um valor de coluna muito grande. Normalmente, essa enumeração pode falhar na chamada à API com JET_errOutOfMemory. Se um valor de coluna grande for truncado de tal maneira, o status do valor da coluna será JET_wrnColumnTruncated.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitEnumerateCompressOutput</p></td>
<td><p>Ao enumerar valores de coluna, todas as colunas para as quais estamos recuperando todos os valores e que têm apenas um valor de coluna não nula podem ser retornadas em um formato compactado. O status dessas colunas será definido como JET_wrnColumnSingleValue e o tamanho do valor da coluna e a memória que contém o valor da coluna serão retornados diretamente na estrutura de <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> . Não há garantia de que todas as colunas qualificadas sejam compactadas dessa maneira. Consulte <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> para obter mais informações.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateCopy</p></td>
<td><p>Essa opção indica que os valores de coluna modificados do registro devem ser enumerados em vez dos valores de coluna originais. Se um valor de coluna não tiver sido modificado, o valor da coluna original será enumerado. Dessa forma, um valor de coluna que ainda não foi inserido ou atualizado pode ser enumerado ao inserir ou atualizar um registro.</p>
<p>Essa opção é idêntica à JET_bitRetrieveCopy quando usada com <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> ou <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumerateIgnoreDefault</p></td>
<td><p>Se uma determinada coluna não estiver presente no registro, nenhum valor de coluna será retornado. Normalmente, o valor padrão para a coluna, se houver, seria retornado nesse caso. É garantido que, se a coluna for definida como um valor diferente do valor padrão, esse valor diferente será retornado (ou seja, se uma coluna com um valor padrão for explicitamente definida como <strong>NULL</strong> , um <strong>NULL</strong> será retornado como o valor dessa coluna). Observe que, mesmo que essa opção seja solicitada, ainda é possível ver um valor de coluna que é igual ao valor padrão. Nenhum esforço é feito para remover valores de coluna que correspondam aos valores padrão.</p>
<p>É importante observar que essa opção afeta a saída de <strong>JetEnumerateColumns</strong> quando usada com JET_bitEnumeratePresenceOnly ou JET_bitEnumerateTaggedOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateIgnoreUserDefinedDefault</p></td>
<td><p>Se uma determinada coluna não estiver presente no registro e tiver um valor padrão definido pelo usuário, nenhum valor de coluna será retornado. Essa opção impedirá o retorno de chamada que computa o valor padrão definido pelo usuário para que a coluna seja chamada ao enumerar os valores para essa coluna.</p>
<p><strong>Windows Server 2003 e anterior:  </strong> Para o Windows Server 2003 e versões anteriores, a operação falhará com JET_errCallbackFailed.</p>
<p><strong>Windows Server 2003 SP1:  </strong> Esse valor possível só está disponível para o Windows Server 2003 SP1 e sistemas operacionais posteriores. Se esse valor possível for especificado e a tabela contiver uma coluna que tenha um valor padrão definido pelo usuário, a operação falhará com JET_errCallbackFailed.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumeratePresenceOnly</p></td>
<td><p>Se existir um valor não nulo para o valor de coluna ou coluna solicitado, os dados associados não serão retornados. Em vez disso, o status associado para essa coluna ou valor de coluna será definido como JET_wrnColumnPresent. Se o valor da coluna ou coluna for <strong>nulo</strong> , JET_wrnColumnNull será retornado como de costume.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateTaggedOnly</p></td>
<td><p>Ao enumerar todos os valores de coluna no registro (por exemplo, ou seja, quando <em>cEnumColumnId</em> for zero), somente os valores de coluna marcados serão retornados. Essa opção não é permitida ao enumerar uma matriz específica de IDs de coluna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumerateInRecordOnly</p></td>
<td><p><strong>Windows 7:  </strong> JET_bitEnumerateInRecordOnly é introduzido no Windows 7.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errBadColumnId</p></td>
<td><p>A ID de coluna fornecida está fora dos limites legais de uma ID de coluna. Esse erro será retornado por <strong>JetEnumerateColumns</strong> se forem solicitadas IDs de coluna específicas, uma dessas IDs de coluna era inválida e a primeira ID de coluna inválida falhou com esse erro para seu código de status de coluna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>A coluna descrita pela ID de coluna fornecida não existe na tabela. Esse erro será retornado por <strong>JetEnumerateColumns</strong> se forem solicitadas IDs de coluna específicas, uma dessas IDs de coluna era inválida e a primeira ID de coluna inválida falhou com esse erro para seu código de status de coluna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:  </strong> Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Uma das opções solicitadas era inválida ou não foi implementada. Esse erro será retornado por <strong>JetEnumerateColumns</strong> quando:</p>
<ul>
<li><p>JET_bitEnumerateLocal está especificado.</p></li>
<li><p>Um <em>grbit</em> inválido foi especificado.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Esse erro será retornado por <strong>JetEnumerateColumns</strong> quando:</p>
<ul>
<li><p><em>pcEnumColumn</em> é <strong>nulo</strong>.</p></li>
<li><p><em>prgEnumColumn</em> é <strong>nulo</strong>.</p></li>
<li><p><em>pfnRealloc</em> é <strong>nulo</strong>.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>O cursor não está posicionado em um registro. Isso pode ocorrer por vários motivos diferentes. Por exemplo, isso ocorrerá se o cursor estiver posicionado no momento após o último registro no índice atual.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>O cursor está posicionado em um registro que foi excluído. Isso pode ocorrer por vários motivos diferentes. O motivo mais comum é que a sessão não está em uma transação, o cursor foi posicionado em um registro, esse registro foi excluído e, em seguida, o cursor tentou fazer referência a esse registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p><strong>Windows XP:  </strong> Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, os dados solicitados serão retornados nos buffers de saída. É responsabilidade do chamador liberar qualquer memória alocada por esse retorno de chamada e retornada nos buffers de saída. Essa memória deve ser liberada por meio do retorno de chamada compatível de [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornecida. Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, nenhum dos dados solicitados será retornado. Qualquer memória que foi alocada durante a chamada será liberada automaticamente usando o retorno de chamada compatível de [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornecido. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Se você estiver enumerando todos os valores de coluna no registro e não tiver especificado JET_bitEnumerateIgnoreDefaults, não será possível pressupor que você nunca verá um valor de coluna ou coluna com um código de status de JET_wrnColumnNull. Você poderá ver esse código de status se uma coluna tiver um valor padrão e tiver sido explicitamente definida como **nula** ou se a coluna for uma coluna não esparsa (por exemplo, uma coluna fixa ou variável).

O parâmetro *cbDataMost* não se aplica a todos os valores de coluna. Esse parâmetro truncará apenas os valores de texto longo e de coluna binária longa que são tão grandes que foram armazenados separadamente do registro.

Se **JetEnumerateColumns** retornar dados em seus parâmetros de saída, o chamador será responsável por liberar a memória na matriz, bem como qualquer memória referenciada por ponteiros inseridos nessa matriz.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista ou o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008 ou o Windows Server 2003.</p></td>
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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JET_PFNREALLOC](./jet-pfnrealloc-callback-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
