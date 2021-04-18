---
description: 'Saiba mais sobre: função JetOpenTempTable3'
title: Função JetOpenTempTable3
TOCTitle: JetOpenTempTable3 Function
ms:assetid: 58d6e264-705e-402b-928f-96eefe5e9771
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269255(v=EXCHG.10)
ms:contentKeyID: 32765557
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable3
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7820f90ef0192c1f700759835bf1572b187cf3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785031"
---
# <a name="jetopentemptable3-function"></a>Função JetOpenTempTable3


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetopentemptable3-function"></a>Função JetOpenTempTable3

A função **JetOpenTempTable3** cria uma tabela temporária com um único índice que pode ser usado para armazenar e recuperar registros, assim como uma tabela comum criada usando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil. Eles também podem ser usados para classificar e executar com muita rapidez a remoção de duplicidades em conjuntos de registros quando acessados de forma puramente sequencial.

```cpp
    JET_ERR JET_API JetOpenTempTable3(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in_opt      JET_UNICODEINDEX* pidxunicode,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*prgcolumndef*

Identifica as definições de coluna das colunas a serem criadas na tabela temporária.

Existem limitações importantes nas opções de definição de coluna que podem ser usadas com uma tabela temporária. Consulte a seção Comentários para obter mais informações.

Além das opções de definição de coluna usual, zero ou mais das opções a seguir também podem ser especificadas, que são relevantes apenas no contexto de uma tabela temporária.

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
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Essa opção indica que a ordem de classificação da coluna de chave para a tabela temporária deve ser decrescente em vez de crescente. Se essa opção for especificada sem JET_bitColumnTTKey, essa opção será ignorada.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Essa opção indica que a coluna será uma coluna de chave para a tabela temporária.</p>
<p>A ordem das definições de coluna com essa opção especificada na matriz de entrada determinará a precedência de cada coluna de chave para a tabela temporária. A primeira definição de coluna na matriz com esse conjunto de opções será a coluna de chave mais significativa e assim por diante. Se mais colunas de chave forem solicitadas do que o mecanismo de banco de dados pode ter suporte, essa opção será ignorada para as colunas de chave sem suporte.</p></td>
</tr>
</tbody>
</table>


*ccolumn*

Consulte *prgcolumndef*.

*pidxunicode*

Os sinalizadores de ID de localidade e normalização que serão usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária.

Quando esse parâmetro não estiver presente, o LCID padrão será usado para comparar todas as colunas de chave Unicode na tabela temporária. O LCID padrão é a localidade inglês dos EUA.

Quando esse parâmetro não estiver presente, os sinalizadores de normalização padrão serão usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária. Os sinalizadores de normalização padrão são: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

*grbit*

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.

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
<td><p>JET_bitTTErrorOnDuplicateInsertion</p></td>
<td><p>Essa opção solicita que qualquer tentativa de inserir um registro com a mesma chave de índice que um registro inserido anteriormente falhará imediatamente com JET_errKeyDuplicate. Se essa opção não for solicitada, uma duplicata poderá ser detectada imediatamente e falhará ou poderá ser removida silenciosamente mais tarde, dependendo da estratégia escolhida pelo mecanismo de banco de dados para implementar a tabela temporária com base na funcionalidade solicitada.</p>
<p>Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForceMaterialization</p></td>
<td><p>Essa opção força o Gerenciador de tabelas temporária a abandonar qualquer tentativa de escolher uma estratégia inteligente para gerenciar a tabela temporária que resultará em desempenho aprimorado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTForwardOnly</p></td>
<td><p>Essa opção solicita que a tabela temporária só seja criada se o Gerenciador de tabelas temporárias puder usar a implementação otimizada para resultados de consulta intermediários. Se qualquer característica da tabela temporária impedir o uso dessa otimização, a operação falhará com JET_errCannotMaterializeForwardOnlySort.</p>
<p>Um efeito colateral dessa opção é permitir que a tabela temporária contenha registros com chaves de índice duplicadas. Consulte JET_bitTTUnique para obter mais informações.</p>
<p>Essa opção só está disponível no Windows Server 2003 e versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTIndexed</p></td>
<td><p>Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir o uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para pesquisar registros por chave de índice.</p>
<p>Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTUnique</p></td>
<td><p>Essa opção solicita que os registros com chaves de índice duplicados sejam removidos do conjunto final de registros na tabela temporária.</p>
<p>Antes do Windows Server 2003, o mecanismo de banco de dados sempre assumiu que essa opção está em vigor devido ao fato de que todos os índices clusterizados também devem ser uma chave primária e, portanto, devem ser exclusivos. A partir do Windows Server 2003, agora é possível criar uma tabela temporária que não remove duplicatas quando a opção de JET_bitTTForwardOnly também é especificada.</p>
<p>Não é possível saber qual duplicata será vencedora e quais duplicatas serão descartadas em geral. No entanto, quando a opção JET_bitTTErrorOnDuplicateInsertion for solicitada, o primeiro registro com uma determinada chave de índice a ser inserida na tabela temporária sempre vencerá.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTUpdatable</p></td>
<td><p>Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir que os registros que foram inseridos anteriormente sejam alterados posteriormente. Se essa funcionalidade não for necessária, é melhor não solicitá-la.</p>
<p>Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTScrollable</p></td>
<td><p>Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir que os registros sejam verificados em ordem e direção arbitrárias usando <a href="gg294117(v=exchg.10).md">JetMove</a>.</p>
<p>Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTSortNullsHigh</p></td>
<td><p>Essa opção solicita que os valores da coluna de chave nula se aproximem do final do índice que os valores de coluna de chave não nulos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTIntrinsicLVsOnly</p></td>
<td><p>Solicitações para permitir somente valores longos intrínsecos.</p>
<p><strong>Windows 7</strong>: o <strong>JET_bitTTIntrinsicLVsOnly</strong> é introduzido no Windows 7.</p></td>
</tr>
</tbody>
</table>


*ptableid*

O buffer de saída que receberá o novo cursor aberto na tabela temporária recém-criada.

*prgcolumnid*

O buffer de saída que receberá a matriz de IDs de coluna geradas durante a criação da tabela temporária.

As IDs de coluna nessa matriz correspondem exatamente à matriz de entrada de definições de coluna. Como resultado, o tamanho desse buffer deve corresponder ao tamanho da matriz de entrada.

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
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p><strong>JetOpenTempTable3</strong> falhou porque JET_bitTTForwardOnly foi especificado e a tabela temporária como especificada não pôde ser criada usando a otimização somente de encaminhamento. Esse erro só será retornado pelo Windows Server 2003 e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Não foi possível criar o índice porque uma definição de índice inválida foi especificada. <strong>JetOpenTempTable3</strong> retornará este erro quando:</p>
<ul>
<li><p>A localidade neutra do idioma é especificada.</p></li>
<li><p>Um conjunto inválido de sinalizadores de normalização foi especificado.</p></li>
</ul>
<p>Esse erro só será retornado pelo Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>O membro <strong>CP</strong> da estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como uma página de código válida. Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200). Um valor de 0 significa que o padrão será usado (Inglês, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>O membro <strong>coltyp</strong> da estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como um tipo de coluna válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Não foi possível criar o índice porque foi feita uma tentativa de usar uma identificação de localidade inválida. A ID de localidade pode ser completamente inválida ou o pacote de idiomas associado pode não estar instalado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>Não foi possível criar o índice porque foi feita uma tentativa de usar um conjunto inválido de sinalizadores de normalização. Esse erro só será retornado pelo Windows XP e por versões posteriores. No Windows 2000, sinalizadores de normalização inválidos resultarão em JET_errIndexInvalidDef em vez disso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>O identificador de sessão é inválido ou se refere a uma sessão fechada. Esse erro não é retornado em todas as circunstâncias. Os identificadores são validados apenas com base no melhor esforço.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para abrir um novo cursor. Os recursos de cursor são configurados usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</p>
<p><strong>JetOpenTempTable3</strong> pode retornar JET_errOutOfMemory se o espaço de endereço do processo do host se tornar muito fragmentado. O Gerenciador de tabela temporária sempre alocará um bloco de 1 MB de espaço de endereço para cada tabela temporária criada, independentemente da quantidade de dados a serem armazenados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p>Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Foi feita uma tentativa de adicionar muitas colunas à tabela. Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para armazenar em cache os índices da tabela. O número de índices cujo esquema pode ser armazenado em cache é configurado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para armazenar em cache o esquema da tabela. O número de tabelas cujo esquema pode ser armazenado em cache é configurado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para criar uma tabela temporária. Os recursos de tabela temporária são configurados usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, será retornado um cursor aberto na tabela temporária recém-criada. O estado do banco de dados temporário será preparado para conter a nova tabela temporária. O estado de qualquer banco de dados comum em uso pelo mecanismo de banco de dados permanecerá inalterado.

Em caso de falha, a tabela temporária não será criada e um cursor não será retornado. O estado do banco de dados temporário pode ser alterado. O estado de qualquer banco de dados comum em uso pelo mecanismo de banco de dados permanecerá inalterado.

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

[Erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md)  
[Parâmetros de tratamento de erros](./error-handling-parameters.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetMove](./jetmove-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
