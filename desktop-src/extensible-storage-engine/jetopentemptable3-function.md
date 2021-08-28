---
description: 'Saiba mais sobre: Função JetOpenTempTable3'
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
ms.openlocfilehash: a1005f9804e0ccf9c4aa5080b3985906471b1386
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988909"
---
# <a name="jetopentemptable3-function"></a>Função JetOpenTempTable3


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetopentemptable3-function"></a>Função JetOpenTempTable3

A **função JetOpenTempTable3** cria uma tabela temporária com um único índice que pode ser usado para armazenar e recuperar registros, assim como uma tabela comum criada usando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil. Eles também podem ser usados para classificar e executar a remoção duplicada muito rapidamente em conjuntos de registros quando acessados de maneira puramente sequencial.

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

A sessão a ser usada para essa chamada.

*prgcolumndef*

Identifica as definições de coluna das colunas a serem criadas na tabela temporária.

Existem limitações importantes para as opções de definição de coluna que podem ser usadas com uma tabela temporária. Consulte a seção Comentários para obter mais informações.

Além das opções comuns de definição de coluna, zero ou mais das opções a seguir também podem ser especificadas que são relevantes apenas no contexto de uma tabela temporária.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>Essa opção indica que a ordem de classificação da coluna de chave para a tabela temporária deve ser decrescente em vez de crescente. Se essa opção for especificada sem JET_bitColumnTTKey, essa opção será ignorada.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Essa opção indica que a coluna será uma coluna de chave para a tabela temporária.</p><p>A ordem das definições de coluna com essa opção especificada na matriz de entrada determinará a precedência de cada coluna de chave para a tabela temporária. A primeira definição de coluna na matriz com esse conjunto de opções será a coluna de chave mais significativa e assim por diante. Se mais colunas de chave são solicitadas do que o mecanismo de banco de dados pode dar suporte, essa opção é ignorada para as colunas de chave sem suporte.</p> | 



*ccolumn*

Consulte *prgcolumndef*.

*pidxunicode*

A ID de localidade e sinalizadores de normalização que serão usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária.

Quando esse parâmetro não estiver presente, o LCID padrão será usado para comparar as colunas de chave Unicode na tabela temporária. O LCID padrão é a localidade em inglês dos EUA.

Quando esse parâmetro não estiver presente, os sinalizadores de normalização padrão serão usados para comparar dados de coluna de chave Unicode na tabela temporária. Os sinalizadores de normalização padrão são: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

*grbit*

Um grupo de bits que contém as opções a serem usadas para essa chamada, que incluem zero ou mais dos seguintes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Essa opção solicita que qualquer tentativa de inserir um registro com a mesma chave de índice que um registro inserido anteriormente falhe imediatamente com JET_errKeyDuplicate. Se essa opção não for solicitada, uma duplicata poderá ser detectada imediatamente e falhar ou poderá ser removida silenciosamente posteriormente, dependendo da estratégia escolhida pelo mecanismo de banco de dados para implementar a tabela temporária com base na funcionalidade solicitada.</p><p>Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o gerenciador de tabela temporário poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Essa opção força o gerenciador de tabela temporário a abandonar qualquer tentativa de escolher uma estratégia inteligente para gerenciar a tabela temporária que resultará em desempenho aprimorado.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>Essa opção solicita que a tabela temporária seja criada somente se o gerenciador de tabela temporário puder usar a implementação otimizada para resultados intermediários da consulta. Se qualquer característica da tabela temporária impedir o uso dessa otimização, a operação falhará com JET_errCannotMaterializeForwardOnlySort.</p><p>Um efeito colateral dessa opção é permitir que a tabela temporária contenha registros com chaves de índice duplicadas. Consulte JET_bitTTUnique para obter mais informações.</p><p>Essa opção só está disponível no Windows Server 2003 e versões posteriores.</p> | 
| <p>JET_bitTTIndexed</p> | <p>Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir o uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para procurar registros por chave de índice.</p><p>Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o gerenciador de tabela temporário poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p> | 
| <p>JET_bitTTUnique</p> | <p>Essa opção solicita que os registros com chaves de índice duplicadas sejam removidos do conjunto final de registros na tabela temporária.</p><p>Antes do Windows Server 2003, o mecanismo de banco de dados sempre presumia que essa opção estava em vigor devido ao fato de que todos os índices clusterados também devem ser uma chave primária e, portanto, devem ser exclusivos. A partir Windows Server 2003, agora é possível criar uma tabela temporária que NÃO remove duplicatas quando a opção JET_bitTTForwardOnly também é especificada.</p><p>Não é possível saber qual duplicata vencerá e quais duplicatas serão descartadas em geral. No entanto, quando a JET_bitTTErrorOnDuplicateInsertion for solicitada, o primeiro registro com uma determinada chave de índice a ser inserido na tabela temporária sempre vencerá.</p> | 
| <p>JET_bitTTUpdatable</p> | <p>Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir que os registros inseridos anteriormente sejam alterados posteriormente. Se essa funcionalidade não for necessária, é melhor não solicitá-la.</p><p>Se essa funcionalidade não for solicitada, o gerenciador de tabela temporário poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p> | 
| <p>JET_bitTTScrollable</p> | <p>Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir que os registros sejam verificados em ordem arbitrária e direção usando <a href="gg294117(v=exchg.10).md">JetMove</a>.</p><p>Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o gerenciador de tabela temporário poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>Essa opção solicita que os valores de coluna de chave NULL são classificar mais próximos ao final do índice do que valores de coluna de chave não NULL.</p> | 
| <p>JET_bitTTIntrinsicLVsOnly</p> | <p>Solicitações para permitir apenas valores longos intrínsecos.</p><p><strong>Windows 7:</strong> <strong>JET_bitTTIntrinsicLVsOnly</strong> é introduzido no Windows 7.</p> | 



*Ptableid*

O buffer de saída que receberá o novo cursor aberto na tabela temporária recém-criada.

*prgcolumnid*

O buffer de saída que receberá a matriz de IDs de coluna geradas durante a criação da tabela temporária.

As IDs de coluna nessa matriz corresponderão exatamente à matriz de entrada de definições de coluna. Como resultado, o tamanho desse buffer deve corresponder ao tamanho da matriz de entrada.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort</p> | <p><strong>JetOpenTempTable3</strong> falhou porque JET_bitTTForwardOnly foi especificado e a tabela temporária, conforme especificado, não pôde ser criada usando a otimização somente de encaminhamento. Esse erro só será retornado pelo Windows Server 2003 e versões posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Não foi possível criar o índice porque uma definição de índice inválida foi especificada. <strong>JetOpenTempTable3</strong> retornará esse erro quando:</p><ul><li><p>A localidade Neutra da Linguagem é especificada.</p></li><li><p>Um conjunto inválido de sinalizadores de normalização é especificado.</p></li></ul><p>Esse erro só será retornado por Windows 2000.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>O <strong>membro cp</strong> da estrutura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como uma página de código válida. Os únicos valores válidos para colunas de texto são inglês (1252) e Unicode (1200). Um valor de 0 significa que o padrão será usado (inglês, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>O <strong>membro coltyp</strong> da <a href="gg294130(v=exchg.10).md">estrutura JET_COLUMNDEF</a> não foi definido como um tipo de coluna válido.</p> | 
| <p>JET_errInvalidLanguageId</p> | <p>Não foi possível criar o índice porque foi feita uma tentativa de usar uma ID de localidade inválida. A ID da localidade pode ser completamente inválida ou o pacote de idiomas associado pode não estar instalado.</p> | 
| <p>JET_errInvalidLCMapStringFlags</p> | <p>Não foi possível criar o índice porque foi feita uma tentativa de usar um conjunto inválido de sinalizadores de normalização. Esse erro só será retornado por Windows XP e versões posteriores. No Windows 2000, sinalizadores de normalização inválidos resultarão em JET_errIndexInvalidDef.</p> | 
| <p>JET_errInvalidSesid</p> | <p>O alça de sessão é inválido ou refere-se a uma sessão fechada. Esse erro não é retornado em todas as circunstâncias. Os alças são validados apenas com base no melhor esforço.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errOutOfCursors</p> | <p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para abrir um novo cursor. Os recursos de cursor são configurados <a href="gg294044(v=exchg.10).md">usando JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">com JET_paramMaxCursors</a>.</p> | 
| <p>JET_errOutOfMemory</p> | <p>A operação falhou porque não foi possível alocar memória suficiente para a conclusão.</p><p><strong>JetOpenTempTable3</strong> poderá retornar JET_errOutOfMemory se o espaço de endereço do processo de host ficar muito fragmentado. O gerenciador de tabela temporário sempre alocará uma parte de 1 MB de espaço de endereço para cada tabela temporária criada, independentemente da quantidade de dados a serem armazenados.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p>Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Foi feita uma tentativa de adicionar muitas colunas à tabela. Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para armazenar em cache os índices da tabela. O número de índices cujo esquema pode ser armazenado em cache é configurado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para armazenar em cache o esquema da tabela. O número de tabelas cujo esquema pode ser armazenado em cache é configurado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">com JET_paramMaxOpenTables</a>.</p> | 
| <p>JET_errTooManySorts</p> | <p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para criar uma tabela temporária. Os recursos de tabela temporários são configurados <a href="gg294044(v=exchg.10).md">usando JetSetSystemParameter</a> <a href="gg294140(v=exchg.10).md">com JET_paramMaxTemporaryTables</a>.</p> | 



Em caso de sucesso, um cursor aberto na tabela temporária recém-criada será retornado. O estado do banco de dados temporário será preparado para conter a nova tabela temporária. O estado de quaisquer bancos de dados comuns em uso pelo mecanismo de banco de dados permanecerá inalterado.

Em caso de falha, a tabela temporária não será criada e um cursor não será retornado. O estado do banco de dados temporário pode ser alterado. O estado de quaisquer bancos de dados comuns em uso pelo mecanismo de banco de dados permanecerá inalterado.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[Erros de mecanismo Armazenamento extensível](./extensible-storage-engine-errors.md)  
[Parâmetros de tratamento de erro](./error-handling-parameters.md)  
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
