---
description: 'Saiba mais sobre: função JetSetColumns'
title: Função JetSetColumns
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4535b66064c19257f4bb7b51b059453660916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089876"
---
# <a name="jetsetcolumns-function"></a>Função JetSetColumns


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetsetcolumns-function"></a>Função JetSetColumns

A função **JetSetColumns** é semelhante ao comportamento de [JetSetColumn](./jetsetcolumn-function.md) , mas permite que um aplicativo defina vários valores de coluna em uma única operação. Uma matriz de estruturas de [JET_SETCOLUMN](./jet-setcolumn-structure.md) é usada para descrever o conjunto de valores de coluna a ser definido e para descrever os buffers de entrada para cada valor de coluna a ser definido.

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*psetcolumn*

Um ponteiro para uma matriz de uma ou mais estruturas de [JET_SETCOLUMN](./jet-setcolumn-structure.md) . Cada estrutura inclui descrições de qual valor de coluna definir e de onde obter dados de coluna a serem definidos.

*csetcolumn*

O número de estruturas de [JET_SETCOLUMN](./jet-setcolumn-structure.md) na matriz fornecida por *psetcolumn*.

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
<td><p>JET_errBadColumnId</p></td>
<td><p>A ID de coluna fornecida está fora dos limites legais de uma ID de coluna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>O mesmo que JET_errNullInvalid.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>A coluna descrita pelo <em>columnid</em> fornecido não existe na tabela.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable</p></td>
<td><p>Foi feita uma tentativa ilegal de atualizar um valor longo durante uma operação de exclusão de atualização original de cópia de inserção.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig</p></td>
<td><p>Os dados de valor de coluna fornecidos no buffer de entrada excedem a limitação de tamanho natural para uma coluna de comprimento fixo ou configurados para texto de comprimento fixo ou colunas binárias. Esse erro também é retornado ao passar mais de 1024 bytes de dados para uma coluna longa e definir o sinalizador de JET_bitSetIntrinsicLV.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>O tamanho de dados do valor da coluna fornecido não corresponde ao que é natural para o tipo de dados de comprimento fixo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Foi feita uma tentativa ilegal de atualizar uma coluna de incremento automático durante uma operação de inserção ou atualização, ou para atualizar uma coluna de versão durante uma operação de substituição.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>As opções fornecidas são desconhecidas ou uma combinação ilegal de configurações de bit conhecido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>O psetinfo- &gt; cbStruct fornecido não é um tamanho válido para a estrutura de <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate</p></td>
<td><p>A operação definir coluna tentou criar um valor duplicado e especificou JET_bitSetUniqueMultiValues ou JET_bitSetUniqueNormalizedMultiValues.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Foi feita uma tentativa ilegal de atualizar um valor de coluna longo quando a sessão de chamada não estava em uma transação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid</p></td>
<td><p>Foi feita uma tentativa ilegal de definir uma coluna não nula como nula.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>O valor da coluna não pôde ser definido como o valor no buffer de entrada porque ele teria feito com que o registro excedesse sua limitação de tamanho relacionada ao tamanho da página. As colunas do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> podem ser armazenadas separadamente dos dados de registro restantes. No entanto, outras colunas devem ser armazenadas com o registro e podem fazer com que a limitação do tamanho do registro seja excedida. Colunas longas exigem 5 bytes de espaço dentro do registro como uma ligação e isso também pode levar a JET_errRecordTooBig retornando.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>O cursor não está atualmente no processo de inserir um novo registro ou atualizar um registro existente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>O valor da coluna no buffer de entrada excedeu o comprimento máximo configurado para uma coluna de comprimento variável e foi truncado.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, para cada coluna descrita no psetcolumns, a parte desejada do valor da coluna é definida com os dados copiados do buffer de entrada. O conjunto de dados de coluna pode ter sido truncado se excedeu o comprimento máximo especificado para uma coluna de comprimento variável.

Em caso de falha, o local do cursor permanece inalterado e nenhum dado do valor da coluna é atualizado no buffer de cópia.

#### <a name="remarks"></a>Comentários

Se qualquer operação de conjunto de colunas individuais retornar um erro, a operação **JetSetColumns** inteira retornará um erro. Os avisos, em geral, são retornados em psetcolumns- \> Error e não no código de retorno dessa função. No entanto, se o último conjunto de colunas tiver um aviso, esse aviso será retornado do **JetSetColumns** em si.

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
