---
description: 'Saiba mais sobre: função JetSetColumn'
title: Função JetSetColumn
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c1fd267bea6bbb995a13ce65f97f1f531572a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789220"
---
# <a name="jetsetcolumn-function"></a>Função JetSetColumn


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetsetcolumn-function"></a>Função JetSetColumn

A função **JetSetColumn** modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual. Ele pode substituir um valor existente, adicionar um novo valor a uma sequência de valores em uma coluna com vários valores, remover um valor de uma sequência de valores em uma coluna com vários valores, ou atualizar todo ou parte de um valor longo, uma coluna do tipo [JET_coltypLongText](./jet-coltyp.md) ou [JET_coltypLongBinary](./jet-coltyp.md).

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*columnid*

A [JET_COLUMNID](./jet-columnid.md) da coluna a ser recuperada. Como alternativa, um valor de *columnid* de 0 (zero) pode ser fornecido. Quando *columnid* 0 (zero) é fornecido, todas as colunas marcadas, as colunas esparsas e de valores múltiplos são tratadas como uma única coluna. Isso facilita a recuperação de todas as colunas esparsas que estão presentes em um registro.

*pvData*

Buffer de entrada que contém dados a serem usados para o valor da coluna.

*cbData*

Tamanho em bytes do buffer de entrada.

*grbit*

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos seguintes:

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
<td><p>JET_bitSetAppendLV</p></td>
<td><p>Essa opção é usada para acrescentar dados a uma coluna do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>. O mesmo comportamento pode ser obtido determinando o tamanho do valor longo existente e especificando <em>ibLongValue</em> em <em>psetinfo</em>. No entanto, é mais simples usar esse <em>grbit</em> , já que saber o tamanho do valor da coluna existente não é necessário.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetOverwriteLV</p></td>
<td><p>Essa opção é usada para substituir o valor longo existente pelos dados fornecidos recentemente. Quando essa opção é usada, é como se o valor longo existente tiver sido definido como 0 (zero) comprimento antes da definição dos novos dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetRevertToDefaultValue</p></td>
<td><p>Essa opção só é aplicável a colunas marcadas, esparsas ou com vários valores. Faz com que a coluna retorne o valor de coluna padrão em operações de recuperação de coluna subsequentes. Todos os valores de coluna existentes são removidos.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetSeparateLV</p></td>
<td><p>Essa opção é usada para forçar um valor longo, as colunas do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, a serem armazenadas separadamente do restante dos dados de registro. Isso ocorre normalmente quando o tamanho do valor longo impede que ele seja armazenado com os dados de registro restantes. No entanto, essa opção pode ser usada para forçar o valor longo a ser armazenado separadamente. Observe que valores longos de quatro bytes de tamanho menor não podem ser forçados a serem separados. Nesses casos, a opção é ignorada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSizeLV</p></td>
<td><p>Essa opção é usada para interpretar o buffer de entrada como um número inteiro de bytes a serem definidos como o comprimento do valor longo descrito pelo <em>columnid</em> fornecido e, se fornecido, o número de sequência em psetinfo- &gt; itagSequence. Se o tamanho fornecido for maior que o valor da coluna existente, a coluna será estendida com 0s. Se o tamanho for menor do que o valor da coluna existente, o valor será truncado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetUniqueMultiValues</p></td>
<td><p>Essa opção é usada para impor que todos os valores em uma coluna com valores múltiplos sejam distintos. Essa opção compara os dados da coluna de origem, sem nenhuma transformação, com outros valores de coluna existentes e um erro será retornado se uma duplicata for encontrada. Se essa opção for fornecida, JET_bitSetAppendLV, JET_bitSetOverwriteLV e JET_bitSetSizeLV também não poderão ser fornecidos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUniqueNormalizedMultiValues</p></td>
<td><p>Essa opção é usada para impor que todos os valores em uma coluna com valores múltiplos sejam distintos. Essa opção compara a transformação normalizada da chave de dados de coluna com outros valores de coluna existentes transformados de forma semelhante e um erro será retornado se uma duplicata for encontrada. Se essa opção for fornecida, JET_bitSetAppendLV, JET_bitSetOverwriteLV e JET_bitSetSizeLV também não poderão ser fornecidos.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetZeroLength</p></td>
<td><p>Essa opção é usada para definir um valor de comprimento zero. Normalmente, um valor de coluna é definido como <strong>NULL</strong> passando um cbMax de 0 (zero). No entanto, para alguns tipos, como <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, um valor de coluna pode ser 0 (zero), em vez de <strong>NULL</strong>, e essa opção é usada para diferenciar entre <strong>NULL</strong> e 0 (zero) comprimento.</p>
<p><strong>Observação</strong>  Em geral, se a coluna for uma coluna de comprimento fixo, esse bit será ignorado e a coluna será definida como <strong>NULL</strong>. No entanto, se a coluna for uma coluna marcada de comprimento fixo, o comprimento da coluna será definido como 0. Quando a coluna marcada de comprimento fixo for definida como 0 comprimento, as tentativas de recuperar a coluna com <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> ou <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> terão sucesso, mas o comprimento real retornado no parâmetro <em>cbActual</em> será 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIntrinsicLV</p></td>
<td><p>Essa opção é usada para armazenar o valor longo inteiro no registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetCompressed</p></td>
<td><p>Essa opção é usada para tentar a compactação de dados ao armazenar os dados.</p>
<p><strong>Windows 7:</strong>  JET_bitSetCompressed é introduzido no Windows 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUncompressed</p></td>
<td><p>Essa opção não é usada para tentar a compactação durante o armazenamento dos dados.</p>
<p><strong>Windows 7:</strong>  JET_bitSetUnCompressed é introduzido no Windows 7.</p></td>
</tr>
</tbody>
</table>


*psetinfo*

Ponteiro para parâmetros de entrada opcionais que podem ser definidos para essa função usando a estrutura de [JET_SETINFO](./jet-setinfo-structure.md) .

Se *psetinfo* for atribuído como **NULL** , a função se comporta como se um *ItagSequence* de 1 e um *ibLongValue* de 0 (zero) fossem fornecidos. Isso faz com que o conjunto de colunas defina o primeiro valor de uma coluna com valores múltiplos e defina dados longos começando no deslocamento 0 (zero).

As seguintes opções podem ser definidas para este parâmetro:

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
<td><p>ibLongValue</p></td>
<td><p>Deslocamento binário em um valor de coluna longo em que os dados definidos devem começar.</p></td>
</tr>
<tr class="even">
<td><p>itagSequence</p></td>
<td><p>Número de sequência do valor de coluna de valores múltiplos desejado a ser definido. Se <em>itagSequence</em> for definido como 0 (zero), o valor fornecido deverá ser acrescentado ao final da sequência de valores com vários valors. Se o número de sequência fornecido for maior do que o último valor de valores múltiplos, o valor especificado será acrescentado ao final da sequência. Se o número de sequência corresponder a um valor existente, esse valor será substituído pelo valor especificado.</p></td>
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
<td><p>A ID de coluna fornecida está fora dos limites legais de uma ID de coluna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
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
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
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
<td><p>Foi feita uma tentativa ilegal de definir uma coluna não<strong>nula</strong> como <strong>nula</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>O mesmo que JET_errNullInvalid.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig</p></td>
<td><p>O valor da coluna não pôde ser definido como o valor no buffer de entrada porque ele teria feito com que o registro excedesse sua limitação de tamanho relacionada ao tamanho da página. As colunas do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> podem ser armazenadas separadamente dos dados de registro restantes. No entanto, outras colunas devem ser armazenadas com o registro e podem fazer com que a limitação do tamanho do registro seja excedida. Colunas longas exigem 5 bytes de espaço dentro do registro como uma ligação e isso também pode levar a JET_errRecordTooBig retornando.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>O cursor não está atualmente no processo de inserir um novo registro ou atualizar um registro existente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Esse erro ocorrerá quando o tamanho configurado do repositório de versão for insuficiente para manter todas as atualizações pendentes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>O valor da coluna no buffer de entrada excedeu o comprimento máximo configurado para uma coluna de comprimento variável e foi truncado.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, a parte desejada de um valor de coluna para a coluna especificada é definida com os dados copiados do buffer de entrada. O conjunto de dados pode ter sido truncado se ele excedeu o comprimento máximo especificado para uma coluna de comprimento variável.

Em caso de falha, o local do cursor permanece inalterado e nenhum dado do valor da coluna é atualizado no buffer de cópia.

#### <a name="remarks"></a>Comentários

Definir valores longos, valores para colunas [JET_coltypLongBinary](./jet-coltyp.md) do tipo [JET_coltypLongText](./jet-coltyp.md) ou [JET_coltypLongBinary](./jet-coltyp.md), deve ser feito somente quando a sessão de chamada estiver em uma transação. Se a sessão de chamada não estiver em uma transação, as modificações a valores longos armazenados separadamente poderão ser confirmadas completamente mesmo quando a operação de atualização for cancelada posteriormente. Se a sessão de chamada estiver em uma transação, os efeitos da atualização poderão ser totalmente revertidos cancelando a atualização e revertendo a transação da sessão.

As atualizações de índice não são executadas como resultado de operações de **JetSetColumn** . Em vez disso, os índices são atualizados somente depois que todas as modificações de coluna são concluídas e [JetUpdate](./jetupdate-function.md) é chamado. Isso permite a atualização mais eficiente de índices quando os índices envolvem mais de uma coluna que está sendo modificada.

Um registro é limitado em tamanho com base no tamanho da página do banco de dados. Todos os valores longos no registro com mais de cinco bytes serão armazenados separados do registro se os dados no registro excederem seu limite como resultado de uma operação **JetSetColumn** . O erro JET_errRecordTooBig será retornado somente depois que todos os dados da coluna de registro separáveis tiverem sido armazenados separadamente do registro e o registro ainda exceder o limite de tamanho do registro.

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
