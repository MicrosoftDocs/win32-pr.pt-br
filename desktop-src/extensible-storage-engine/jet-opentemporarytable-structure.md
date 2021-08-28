---
description: 'Saiba mais sobre: estrutura JET_OPENTEMPORARYTABLE dados'
title: Estrutura JET_OPENTEMPORARYTABLE dados
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
ms.openlocfilehash: 625de51bf265be02fa48beb2872797cd5bd6ba26
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986909"
---
# <a name="jet_opentemporarytable-structure"></a>Estrutura JET_OPENTEMPORARYTABLE dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_opentemporarytable-structure"></a>Estrutura JET_OPENTEMPORARYTABLE dados

A **estrutura JET_OPENTEMPORARYTABLE** contém uma coleção extensível de parâmetros facilmente para a função **JET_OPENTEMPORARYTABLE** configuração. Essa estrutura é o equivalente de tabela temporária da [estrutura JET_TABLECREATE](./jet-tablecreate-structure.md) dados.

**Windows Vista:** A **estrutura JET_OPENTEMPORARYTABLE** é introduzida no Windows Vista.

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

**Cbstruct**

O tamanho dessa estrutura em bytes (para expansão futura). Ele deve ser definido como sizeof( JET_TABLECREATE ) em bytes.

**prgcolumndef**

Definições de coluna para as colunas criadas na tabela temporária.

**Existem** limitações importantes para as opções de definição de coluna que são usadas com uma tabela temporária. Consulte a seção Comentários para obter mais informações.

Além das opções comuns de definição de coluna, zero ou mais das opções a seguir também podem ser especificadas que são relevantes apenas no contexto de uma tabela temporária.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>A ordem de classificação da coluna de chave para a tabela temporária deve ser decrescente em vez de crescente. Se essa opção for especificada sem JET_bitColumnTTKey, essa opção será ignorada.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>A coluna será uma coluna de chave para a tabela temporária.</p><p>A ordem das definições de coluna com essa opção especificada na matriz de entrada determinará a precedência de cada coluna de chave para a tabela temporária. A primeira definição de coluna na matriz que tem essa opção definida será a coluna de chave mais significativa e assim por diante. Se mais colunas de chave são solicitadas do que o mecanismo de banco de dados pode dar suporte, essa opção é ignorada para as colunas de chave sem suporte.</p> | 



**ccolumn**

Consulte *prgcolumndef*.

**pidxunicode**

A ID de localidade e os sinalizadores de normalização a usar para comparar quaisquer dados de coluna de chave Unicode na tabela temporária.

Quando esse parâmetro não estiver presente e quando o parâmetro *lcid* não estiver presente, o LCID padrão será usado para comparar as colunas de chave Unicode na tabela temporária. O LCID padrão é a localidade em inglês dos EUA.

Quando esse parâmetro não estiver presente, os sinalizadores de normalização padrão serão usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária. Os sinalizadores de normalização padrão são: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

**grbit**

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTTIndexed</p> | <p>Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir o uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para procurar registros por chave de índice.</p><p>Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o gerenciador de tabela temporário poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p> | 
| <p>JET_bitTTUnique</p> | <p>Solicitações que registros com chaves de índice duplicadas sejam removidos do conjunto final de registros na tabela temporária.</p><p>Antes do Windows Server 2003, o mecanismo de banco de dados sempre presumiu que essa opção estava em vigor devido ao fato de que todos os índices clusterados também devem ser uma chave primária e, portanto, devem ser exclusivos. A partir Windows Server 2003, agora é possível criar uma tabela temporária que não remove duplicatas quando a opção JET_bitTTForwardOnly também é especificada.</p><p>Não é possível saber qual duplicata terá êxito e quais duplicatas serão descartadas, em geral. No entanto, quando a JET_bitTTErrorOnDuplicateInsertion for solicitada, o primeiro registro com uma determinada chave de índice a ser inserido na tabela temporária sempre terá êxito.</p> | 
| <p>JET_bitTTUpdatable</p> | <p>Solicita que a tabela temporária seja flexível o suficiente para permitir que os registros inseridos anteriormente sejam alterados posteriormente. Se essa funcionalidade não for necessária, é melhor não solicitá-la.</p><p>Se essa funcionalidade não for solicitada, o gerenciador de tabela temporário poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p> | 
| <p>JET_bitTTScrollable</p> | <p>Solicita que a tabela temporária seja flexível o suficiente para permitir que os registros sejam verificados em ordem arbitrária e direção usando <a href="gg294117(v=exchg.10).md">JetMove.</a></p><p>Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o gerenciador de tabela temporário poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>Solicita que <strong>os valores de</strong> coluna de chave NULL são classificar mais próximos ao final do índice do que valores de coluna de chave não NULL.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Força o gerenciador de tabela temporário a abandonar a pesquisa da melhor estratégia para usar o gerenciamento da tabela temporária que resultará em desempenho aprimorado.</p> | 
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Qualquer tentativa de inserir um registro com a mesma chave de índice que um registro inserido anteriormente falhará imediatamente com JET_errKeyDuplicate. Se essa opção não for solicitada, uma duplicata será detectada imediatamente e falhará ou será removida silenciosamente posteriormente, dependendo da estratégia escolhida pelo mecanismo de banco de dados para implementar a tabela temporária, com base na funcionalidade solicitada.</p><p>Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o gerenciador de tabela temporário poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>A tabela temporária só será criada se o gerenciador de tabela temporário puder usar a implementação otimizada para resultados intermediários da consulta. Se qualquer característica da tabela temporária impedir o uso dessa otimização, a operação falhará com JET_errCannotMaterializeForwardOnlySort.</p><p>Um efeito colateral dessa opção é permitir que a tabela temporária contenha registros com chaves de índice duplicadas. Consulte JET_bitTTUnique para obter mais informações.</p><p><strong>Windows Server 2003:</strong> Essa opção só está disponível no Windows Server 2003 e versões posteriores.</p> | 



**prgcolumnid**

O buffer de saída que recebe a matriz de IDs de coluna geradas durante a criação da tabela temporária.

As IDs de coluna nessa matriz corresponderão exatamente à matriz de entrada de definições de coluna. Como resultado, o tamanho desse buffer deve corresponder ao tamanho da matriz de entrada.

**cbKeyMost**

O tamanho máximo de uma chave que representa uma determinada linha.

O tamanho máximo da chave pode ser definido para controlar como as chaves são truncadas. O truncamento de chave é importante porque pode afetar quando as linhas são consideradas distintas.

Se esse parâmetro for definido como 0 ou JET_cbKeyMostMin (255), o tamanho máximo da chave e sua semântica permanecerão idênticos ao tamanho máximo da chave com suporte do Windows Server 2003 e das versões anteriores. Esse parâmetro também pode ser definido como um valor maior como uma função do tamanho da página do banco de dados para a instância (JET_paramDatabasePageSize). Consulte JET_paramKeyMost para obter mais informações.

**cbVarSegMac**

A quantidade máxima de dados que serão usados de qualquer coluna de comprimento variável para construir uma chave para uma determinada linha.

Esse parâmetro pode ser usado para controlar a quantidade de espaço de chave consumida por qualquer coluna de chave determinada. Esse limite é em bytes. Se esse parâmetro for zero ou for o mesmo que o *parâmetro cbKeyMost,* nenhum limite está em vigor.

**Tableid**

O handle de tabela para a tabela temporária criada como resultado de uma chamada bem-sucedida para [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTemporaryTable](./jetopentemporarytable-function.md)  
[Parâmetros do sistema Armazenamento mecanismo extensível](./extensible-storage-engine-system-parameters.md)
