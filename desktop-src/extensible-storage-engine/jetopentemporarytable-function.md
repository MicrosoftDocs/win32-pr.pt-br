---
description: 'Saiba mais sobre: Função JetOpenTemporaryTable'
title: Função JetOpenTemporaryTable
TOCTitle: JetOpenTemporaryTable Function
ms:assetid: feacd0b8-2298-4ec6-aa59-0fede08474bc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294144(v=EXCHG.10)
ms:contentKeyID: 32765758
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTemporaryTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a67a26a396f2910dd22fea351cc3d9b8a32a1c49
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983359"
---
# <a name="jetopentemporarytable-function"></a>Função JetOpenTemporaryTable


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetopentemporarytable-function"></a>Função JetOpenTemporaryTable

A **função JetOpenTemporaryTable** cria uma tabela volátil com um único índice que pode ser usado para armazenar e recuperar registros, assim como uma tabela comum criada por meio de [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).

**Windows Vista:****JetOpenTemporaryTable** é introduzido no Windows Vista.  

As tabelas temporárias são mais rápidas do que as tabelas comuns devido à sua natureza volátil. Eles podem classificar e executar rapidamente a remoção duplicada em conjuntos de registros quando são acessados de maneira puramente sequencial.

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão que será usada para essa chamada.

*popentemporarytable*

Um ponteiro para uma [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) que contém a descrição da tabela temporária a ser criado na entrada. Após uma chamada bem-sucedida, a estrutura contém o identificador para as identificações de tabela e coluna temporárias.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errOutOfMemory</p> | <p>A operação falhou porque não foi possível alocar memória suficiente para a conclusão.</p><p><strong>JetOpenTemporaryTable</strong> poderá retornar JET_errOutOfMemory se o espaço de endereço do processo de host ficar muito fragmentado. O gerenciador de tabela temporário alocará uma parte de 1 MB de espaço de endereço para cada tabela temporária criada, independentemente da quantidade de dados armazenados.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro resultou em um resultado inesperado.</p><p>Esse erro é retornado por <strong>JetOpenTemporaryTable</strong> nas seguintes condições:</p><ul><li><p>O <strong>membro cbStruct</strong> da <a href="gg269206(v=exchg.10).md">estrutura JET_OPENTEMPORARYTABLE</a> não corresponde a uma versão dessa estrutura que é suportada por essa versão do mecanismo de banco de dados</p></li><li><p>O <strong>membro cbKeyMost</strong> da estrutura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> é menor que JET_cbKeyMostMin.</p></li><li><p>O <strong>membro cbKeyMost</strong> da estrutura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> é maior que o maior valor com suporte para o tamanho da página do banco de dados para a instância (JET_paramDatabasePageSize). Consulte o JET_paramKeyMost na lista de <a href="gg269241(v=exchg.10).md">Parâmetros Informacionais</a> para obter mais informações.</p></li><li><p>O membro cbVarSegMac da <a href="gg269206(v=exchg.10).md">estrutura JET_OPENTEMPORARYTABLE</a> é maior que o <strong>membro cbKeyMost.</strong></p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo fechada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong>  Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidSesid</p> | <p>O alça de sessão é inválido ou refere-se a uma sessão fechada.</p><p><strong>Observação</strong>  Esse erro não é retornado em todas as circunstâncias. Os alças são validados apenas com base no melhor esforço.</p> | 
| <p>JET_errOutOfCursors</p> | <p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para abrir um novo cursor. Os recursos de cursor são configurados usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">com JET_paramMaxCursors</a>.</p> | 
| <p>JET_errTooManySorts</p> | <p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para criar uma tabela temporária. Os recursos de tabela temporários são configurados <a href="gg294044(v=exchg.10).md">usando JetSetSystemParameter</a> <a href="gg294140(v=exchg.10).md">com JET_paramMaxTemporaryTables</a>.</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort</p> | <p><strong>JetOpenTemporaryTable</strong> falhou porque JET_bitTTForwardOnly foi especificada e a tabela temporária especificada não pôde ser criada usando a otimização somente de encaminhamento.</p><p><strong>Windows Server 2003:</strong>  Esse erro só será retornado pelo Windows Server 2003 e versões posteriores.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Foi feita uma tentativa de adicionar muitas colunas à tabela. Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para armazenar em cache o esquema da tabela. Para configurar o número de tabelas que têm esquemas que podem ser armazenados em cache, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>O <strong>membro cp</strong> da estrutura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como uma página de código válida. Os únicos valores válidos para colunas de texto são inglês (1252) e Unicode (1200). Um valor de 0 significa que o padrão será usado (inglês, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>O <strong>membro coltyp</strong> da <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como um tipo de coluna válido.</p> | 
| <p>JET_errInvalidLanguageId</p> | <p>Não foi possível criar o índice porque foi feita uma tentativa de usar uma ID de localidade inválida. A ID da localidade pode ser completamente inválida ou o pacote de idiomas associado pode não estar instalado.</p> | 
| <p>JET_errInvalidLCMapStringFlags</p> | <p>Não foi possível criar o índice porque foi feita uma tentativa de usar um conjunto inválido de sinalizadores de normalização.</p><p><strong>Windows XP:</strong>  Esse erro só será retornado por Windows XP e versões posteriores.</p><p><strong>Windows 2000:</strong>  No Windows 2000, sinalizadores de normalização inválidos resultarão em JET_errIndexInvalidDef.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Não foi possível criar o índice porque uma definição de índice inválida foi especificada. <strong>JetOpenTemporaryTable</strong> retornará esse erro sob as seguintes condições:</p><ul><li><p>A localidade Neutra da Linguagem é especificada.</p></li><li><p>Um conjunto inválido de sinalizadores de normalização é especificado.</p></li></ul><p><strong>Windows 2000:</strong>  Esse erro só será retornado por Windows 2000.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para armazenar em cache os índices da tabela. Para configurar o número de índices que têm esquemas que podem ser armazenados em cache, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p> | 



Em caso de sucesso, um cursor aberto na tabela temporária recém-criada será retornado. O estado do banco de dados temporário será preparado para conter a nova tabela temporária. O estado de quaisquer bancos de dados comuns em uso pelo mecanismo de banco de dados permanecerá inalterado.

Em caso de falha, a tabela temporária não será criada e um cursor não será retornado. O estado do banco de dados temporário pode ser alterado. O estado de quaisquer bancos de dados comuns em uso pelo mecanismo de banco de dados permanecerá inalterado.

#### <a name="remarks"></a>Comentários

As tabelas temporárias não são suportadas pelo complemento completo das opções de definição de coluna que normalmente são suportadas pelo mecanismo de banco de dados. Na verdade, somente JET_bitColumnFixed e JET_bitColumnTagged têm suporte. Isso significa que não é possível criar uma coluna com incremento automático, versão ou vários valores em uma tabela temporária. Por fim, não há suporte para colunas de atualização de escrow porque elas só podem ser usadas por uma sessão por vez. Se qualquer uma dessas opções for solicitada, elas serão ignoradas.

As tabelas temporárias não dão suporte a valores padrão. Se for fornecida uma definição de coluna que contenha uma especificação de valor padrão, essa especificação será ignorada.

As tabelas temporárias são retornadas ao chamador como resultado de muitas funções diferentes do ESE. Por exemplo, [JetGetIndexInfo](./jetgetindexinfo-function.md) com a opção JET_IdxInfo definida retornará uma tabela temporária contendo uma lista de todas as colunas de chave em um determinado índice. As tabelas temporárias seguem as mesmas regras de ciclo de vida que as tabelas temporárias comuns, conforme descrito aqui.

As tabelas temporárias também são usadas internamente pelo mecanismo de banco de dados para muitas tarefas. A mais importante dessas tarefas é a criação de um índice em uma tabela existente. Uma tabela temporária será usada para classificar as chaves de índice que são usadas para construir esse índice.

Todas as tabelas temporárias são armazenadas no banco de dados temporário. O banco de dados temporário é um arquivo de banco de dados especial que é mantido durante o tempo de vida de uma instância do ESE e é excluído quando essa instância é desligada ou reiniciada. O local do banco de dados temporário pode ser configurado usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com [JET_paramTempPath](./temporary-database-parameters.md). O posicionamento do banco de dados temporário em disco em relação aos arquivos de log de transações e arquivos de banco de dados poderá ser importante se seu aplicativo fizer uso intensivo de tabelas temporárias ou criar índices com frequência.

O ciclo de vida de uma tabela temporária é vinculado aos cursores que fazem referência a ela. Se todos os cursores que fazem referência a uma tabela temporária forem fechados, implicitamente ou explicitamente, a tabela temporária será excluída. Se uma tabela temporária for criada dentro de uma transação e essa transação for revertida posteriormente, a tabela temporária será excluída porque todos os cursores que fazem referência a ela neste momento serão fechados implicitamente. Novos cursores podem fazer referência a uma tabela temporária somente por meio do uso de [JetDupCursor](./jetdupcursor-function.md). Nesse caso, os novos cursores serão posicionados na primeira entrada de índice da tabela temporária. [JetDupCursor](./jetdupcursor-function.md) só funcionará durante determinadas fases de uso para a tabela temporária. Consulte os comentários sobre os recursos de cursor de tabela temporária para obter mais informações. Não é possível fazer referência a uma tabela temporária de mais de uma sessão por vez.

**Cuidado**  Há um problema importante no [JetDupCursor](./jetdupcursor-function.md) que afeta as tabelas temporárias. Se for feita uma tentativa de duplicar uma tabela temporária que está no modo somente de encaminhamento, o cursor resultante não será criado corretamente e não terá funcionamento adequado. Ainda é seguro duplicar um cursor em uma tabela temporária materializada.

O Gerenciador de tabelas temporárias pode implementar uma tabela temporária de três maneiras. O primeiro método é manter uma tabela na memória. Essa estratégia é a mais rápida, mas só pode ser usada para tabelas pequenas, simples e temporárias. O segundo método é criar uma classificação baseada em disco que possa ser controlada usando um iterador somente de encaminhamento. Essa estratégia só pode ser usada em determinadas circunstâncias e é a maneira mais rápida de classificar e remover duplicatas de um conjunto de dados muito grande. O terceiro método é criar uma árvore B + no banco de dados temporário para manter a tabela temporária. Essa estratégia é a mais lenta, mas a mais versátil e é conhecida como uma tabela temporária materializada. Essas estratégias podem ser usadas em combinação para atingir por fim a funcionalidade solicitada pela tabela temporária.

Quando a tabela temporária não está materializada, ela é usada principalmente em duas fases principais. A primeira fase é a fase de inserção em que a tabela é populada com seu conjunto de dados inicial. Durante essa fase, apenas a inserção de dados é permitida. Essa fase termina quando é feita uma tentativa de mover o cursor usando [JetMove](./jetmove-function.md) ou [JetSeek](./jetseek-function.md). A segunda fase é a fase de extração de dados. Durante essa fase, os dados armazenados na tabela temporária podem ser extraídos de acordo com os recursos que foram solicitados quando a tabela temporária foi criada.

**Recursos de cursor de tabela temporária**

Quando a tabela temporária é materializada, o cursor tem os seguintes recursos, mas pode ser ainda mais limitado pelas opções que são solicitadas:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDelete](./jetdelete-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetCursorInfo](./jetgetcursorinfo-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordSize](./jetgetrecordsize-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetGotoBookmark](./jetgotobookmark-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetSetIndexRange](./jetsetindexrange-function.md)

  - [JetSetLS](./jetsetls-function.md)

  - [JetUpdate](./jetupdate-function.md)

Quando a tabela temporária não está materializada e está na fase de inserção, o cursor tem os seguintes recursos, mas pode ser ainda mais limitado pelas opções que são solicitadas:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)
    
    **Observação**  Faz a transição para a fase de extração.

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)
    
    **Observação**  Faz a transição para a fase de extração.

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetUpdate](./jetupdate-function.md)

Quando a tabela temporária não está materializada e está na fase de extração, o cursor tem os seguintes recursos, mas pode ser ainda mais limitado pelas opções que são solicitadas:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)
    
    **Observação**  Se for feita uma tentativa de duplicar uma tabela temporária que está no modo somente de encaminhamento, o cursor resultante não será criado corretamente e não terá funcionamento adequado. Ainda é seguro duplicar um cursor em uma tabela temporária materializada.

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordSize](./jetgetrecordsize-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetGotoBookmark](./jetgotobookmark-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [JetSetIndexRange](./jetsetindexrange-function.md)

  - [JetSetLS](./jetsetls-function.md)

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows Server 2008.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetMove](./jetmove-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parâmetros informativos](./informational-parameters.md)  
[Parâmetros de banco de dados temporários](./temporary-database-parameters.md)
