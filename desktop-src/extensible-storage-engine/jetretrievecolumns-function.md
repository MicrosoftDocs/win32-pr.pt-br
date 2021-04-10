---
description: 'Saiba mais sobre: função JetRetrieveColumns'
title: Função JetRetrieveColumns
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 515be3a36932c9a56843f51d2e1b32a41ca94e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171617"
---
# <a name="jetretrievecolumns-function"></a>Função JetRetrieveColumns


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetretrievecolumns-function"></a>Função JetRetrieveColumns

A função **JetRetrieveColumns** recupera vários valores de coluna do registro atual em uma única operação. Uma matriz de estruturas de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) é usada para descrever o conjunto de valores de coluna a serem recuperados e para descrever os buffers de saída para cada valor de coluna a ser recuperado.

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*pretrievecolumn*

Um ponteiro para uma matriz de uma ou mais estruturas de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) . Cada estrutura inclui descrições de qual valor de coluna recuperar e onde armazenar dados retornados.

*cretrievecolumn*

O número de estruturas de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) na matriz fornecida por *pretrievecolumn*.

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
<td><p>JET_errBadItagSequence</p></td>
<td><p>Um valor de número de sequência de coluna com valores múltiplos inválido foi passado em pretinfo- &gt; itagSequence. Os valores válidos para os números de sequência de valor de coluna com valores múltiplos são 1 ou mais. Um valor de 0 (zero) é válido para essa função, mas é inválido para <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadColumnId</p></td>
<td><p>A ID de coluna fornecida está fora dos limites legais de uma ID de coluna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>A coluna descrita pelo <em>columnid</em> fornecido não existe na tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex</p></td>
<td><p>As colunas indexadas como subcadeias de caracteres não podem ser recuperadas do índice, já que apenas uma pequena parte da coluna está normalmente presente em cada entrada de índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Em alguns casos, o buffer fornecido para a coluna de recuperação deve ser suficientemente dimensionado para retornar qualquer valor do valor da coluna. Por exemplo, colunas atualizáveis de caução são ajustadas para serem consistentes para o contexto transacional da sessão de chamada e esse ajuste requer o buffer fornecido pelo chamador. Se espaço de buffer insuficiente for fornecido, JET_errInvalidBufferSize será retornado e nenhum dado de coluna será retornado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>As opções fornecidas são desconhecidas ou uma combinação ilegal de configurações de bit conhecido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um ou mais dos parâmetros fornecidos estão incorretos. Isso pode acontecer se o retinfo. cbStruct for menor que o tamanho de <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>O cursor não está posicionado em um registro. Isso pode ocorrer por vários motivos diferentes. Por exemplo, isso ocorrerá se o cursor estiver posicionado no momento após o último registro no índice atual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>O valor da coluna inteira não pôde ser recuperado porque o buffer fornecido é menor do que o tamanho da coluna.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, os dados de colunas e o tamanho da coluna são retornados nos buffers fornecidos descritos na matriz de estruturas de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) . Se um *itagSequence* foi definido como 0 (zero) para indicar que o número de instâncias de um campo com valores múltiplos foi desejado em vez dos dados da coluna, o número de instâncias de uma coluna com vários valores será retornado no próprio campo *itagSequence* . Cada estrutura de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) tem um campo de erro que contém avisos para a coluna recuperada. Se a coluna fosse um valor **nulo** , o código de erro será definido como JET_wrnColumnNull.

Em caso de falha, o local do cursor permanece inalterado e nenhum dado é copiado no buffer fornecido.

#### <a name="remarks"></a>Comentários

O **JetRetrieveColumns** dá suporte a um recurso que o [JetRetrieveColumn](./jetretrievecolumn-function.md) não faz. Essa é a capacidade de recuperar o número de instâncias de uma coluna com vários valores. A finalidade desse recurso é permitir que um aplicativo Recupere todos os valores de uma coluna. Isso pode ser feito determinando primeiro o número de valores que uma coluna tem. Em seguida, seus comprimentos podem ser determinados chamando **JetRetrieveColumns** novamente com uma estrutura de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) alocada para cada valor para determinar o comprimento dos dados da coluna. Isso pode ser feito passando ponteiros _PvData_ **nulos** com *cbMax* de 0 (zero) e recuperando o comprimento da coluna em *cbActual*. A terceira e última chamada podem ser feitas com memória alocada para os dados de valor da coluna.

Se qualquer coluna recuperada for truncada devido a um buffer de comprimento insuficiente, a API retornará JET_wrnBufferTruncated. No entanto, outros erros JET_wrnColumnNull são retornados somente no campo de erro em [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md). A razão para isso é que os aplicativos muitas vezes desejam garantir que todos os dados foram recuperados e retornar esse erro do **JetRetrieveColumns** facilite essa compreensão.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
