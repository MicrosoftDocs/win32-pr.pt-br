---
description: 'Saiba mais sobre: estrutura de JET_OPENTEMPORARYTABLE'
title: Estrutura de JET_OPENTEMPORARYTABLE
TOCTitle: JET_OPENTEMPORARYTABLE Structure
ms:assetid: 23f4fb0f-ca60-498b-9b8e-14de6188eb87
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269206(v=EXCHG.10)
ms:contentKeyID: 32765509
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51ae9026098e82538940bde2ef182ba0a7a11c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296820"
---
# <a name="jet_opentemporarytable-structure"></a>Estrutura de JET_OPENTEMPORARYTABLE


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_opentemporarytable-structure"></a>Estrutura de JET_OPENTEMPORARYTABLE

A estrutura de **JET_OPENTEMPORARYTABLE** contém uma coleção facilmente extensível de parâmetros para a função **JET_OPENTEMPORARYTABLE** . Essa estrutura é a tabela temporária equivalente da estrutura de [JET_TABLECREATE](./jet-tablecreate-structure.md) .

**Windows Vista:** A estrutura de **JET_OPENTEMPORARYTABLE** é introduzida no Windows Vista.

```cpp
    typedef struct tagJET_OPENTEMPORARYTABLE {
      unsigned long cbStruct;
      const JET_COLUMNDEF* prgcolumndef;
      unsigned long ccolumn;
      JET_UNICODEINDEX* pidxunicode;
      JET_GRBIT grbit;
      JET_COLUMNID* prgcolumnid;
      unsigned long cbKeyMost;
      unsigned long cbVarSegMac;
      JET_TABLEID tableid;
    } JET_OPENTEMPORARYTABLE;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho dessa estrutura em bytes (para expansão futura). Ele deve ser definido como sizeof (JET_TABLECREATE) em bytes.

**prgcolumndef**

Definições de coluna para as colunas criadas na tabela temporária.

Existem limitações **importantes** para as opções de definição de coluna usadas com uma tabela temporária. Consulte a seção Comentários para obter mais informações.

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
<td><p>A ordem de classificação da coluna de chave para a tabela temporária deve ser decrescente em vez de crescente. Se essa opção for especificada sem JET_bitColumnTTKey, essa opção será ignorada.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>A coluna será uma coluna de chave para a tabela temporária.</p>
<p>A ordem das definições de coluna com essa opção especificada na matriz de entrada determinará a precedência de cada coluna de chave para a tabela temporária. A primeira definição de coluna na matriz que tem esse conjunto de opções será a coluna de chave mais significativa e assim por diante. Se mais colunas de chave forem solicitadas do que o mecanismo de banco de dados pode ter suporte, essa opção será ignorada para as colunas de chave sem suporte.</p></td>
</tr>
</tbody>
</table>


**ccolumn**

Consulte *prgcolumndef*.

**pidxunicode**

Os sinalizadores de ID de localidade e normalização a serem usados para comparar qualquer dado de coluna de chave Unicode na tabela temporária.

Quando esse parâmetro não estiver presente e quando o parâmetro *LCID* não estiver presente, o LCID padrão será usado para comparar as colunas de chave Unicode na tabela temporária. O LCID padrão é a localidade inglês dos EUA.

Quando esse parâmetro não estiver presente, os sinalizadores de normalização padrão serão usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária. Os sinalizadores de normalização padrão são: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

**grbit**

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
<td><p>JET_bitTTIndexed</p></td>
<td><p>Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir o uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para pesquisar registros por chave de índice.</p>
<p>Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTUnique</p></td>
<td><p>As solicitações que os registros com chaves de índice duplicadas são removidas do conjunto final de registros na tabela temporária.</p>
<p>Antes do Windows Server 2003, o mecanismo de banco de dados sempre assumiu que essa opção está em vigor devido ao fato de que todos os índices clusterizados também devem ser uma chave primária e, portanto, devem ser exclusivos. A partir do Windows Server 2003, agora é possível criar uma tabela temporária que não remove duplicatas quando a opção de JET_bitTTForwardOnly também é especificada.</p>
<p>Não é possível saber qual duplicata terá sucesso e quais duplicatas serão descartadas, em geral. No entanto, quando a opção JET_bitTTErrorOnDuplicateInsertion for solicitada, o primeiro registro com uma determinada chave de índice a ser inserida na tabela temporária sempre terá sucesso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTUpdatable</p></td>
<td><p>Solicita que a tabela temporária seja flexível o suficiente para permitir que os registros que foram inseridos anteriormente sejam alterados posteriormente. Se essa funcionalidade não for necessária, é melhor não solicitá-la.</p>
<p>Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTScrollable</p></td>
<td><p>Solicita que a tabela temporária seja flexível o suficiente para permitir que os registros sejam verificados em ordem e direção arbitrárias usando <a href="gg294117(v=exchg.10).md">JetMove</a>.</p>
<p>Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTSortNullsHigh</p></td>
<td><p>Solicita que os valores da coluna de chave <strong>nula</strong> sejam mais próximos do final do índice que os valores de coluna de chave não nulos.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForceMaterialization</p></td>
<td><p>Força o Gerenciador de tabelas temporária a abandonar a pesquisa para que a melhor estratégia use o gerenciamento da tabela temporária, o que resultará em desempenho aprimorado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTErrorOnDuplicateInsertion</p></td>
<td><p>Qualquer tentativa de inserir um registro com a mesma chave de índice que um registro inserido anteriormente irá falhar imediatamente com JET_errKeyDuplicate. Se essa opção não for solicitada, uma duplicata será detectada imediatamente e falhará ou será removida silenciosamente mais tarde, dependendo da estratégia escolhida pelo mecanismo de banco de dados para implementar a tabela temporária, com base na funcionalidade solicitada.</p>
<p>Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForwardOnly</p></td>
<td><p>A tabela temporária só será criada se o Gerenciador de tabelas temporárias puder usar a implementação otimizada para resultados de consulta intermediários. Se qualquer característica da tabela temporária impedir o uso dessa otimização, a operação falhará com JET_errCannotMaterializeForwardOnlySort.</p>
<p>Um efeito colateral dessa opção é permitir que a tabela temporária contenha registros com chaves de índice duplicadas. Consulte JET_bitTTUnique para obter mais informações.</p>
<p><strong>Windows Server 2003:  </strong> Essa opção só está disponível no Windows Server 2003 e versões posteriores.</p></td>
</tr>
</tbody>
</table>


**prgcolumnid**

O buffer de saída que recebe a matriz de IDs de coluna geradas durante a criação da tabela temporária.

As IDs de coluna nessa matriz correspondem exatamente à matriz de entrada de definições de coluna. Como resultado, o tamanho desse buffer deve corresponder ao tamanho da matriz de entrada.

**cbKeyMost**

O tamanho máximo de uma chave que representa uma determinada linha.

O tamanho máximo da chave pode ser definido para controlar como as chaves são truncadas. O truncamento de chave é importante porque pode afetar quando as linhas são consideradas distintas.

Se esse parâmetro for definido como 0 ou JET_cbKeyMostMin (255), o tamanho máximo da chave e sua semântica permanecerão idênticos ao tamanho máximo da chave com suporte no Windows Server 2003 e versões anteriores. Esse parâmetro também pode ser definido como um valor maior como uma função do tamanho da página do banco de dados para a instância (JET_paramDatabasePageSize). Consulte JET_paramKeyMost para obter mais informações.

**cbVarSegMac**

A quantidade máxima de dados que serão usados de qualquer coluna de comprimento variável para construir uma chave para uma determinada linha.

Esse parâmetro pode ser usado para controlar a quantidade de espaço de chave consumida por qualquer coluna de chave fornecida. Esse limite está em bytes. Se esse parâmetro for zero ou for o mesmo que o parâmetro *cbKeyMost* , nenhum limite estará em vigor.

**TableID**

O identificador de tabela para a tabela temporária criada como resultado de uma chamada bem-sucedida para [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTemporaryTable](./jetopentemporarytable-function.md)  
[Parâmetros do sistema do mecanismo de armazenamento extensível](./extensible-storage-engine-system-parameters.md)
