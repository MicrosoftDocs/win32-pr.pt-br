---
description: 'Saiba mais sobre: função JetIntersectIndexes'
title: Função JetIntersectIndexes
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9cb24ab9457cbad421d91764323b1db0e56a1ab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468903"
---
# <a name="jetintersectindexes-function"></a>Função JetIntersectIndexes


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetintersectindexes-function"></a>Função JetIntersectIndexes

A função **JetIntersectIndexes** computa a interseção entre vários conjuntos de entradas de índice de índices secundários diferentes na mesma tabela. Essa operação é útil para localizar o conjunto de registros em uma tabela que corresponde a dois ou mais critérios que podem ser expressos usando intervalos de índice.

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*rgindexrange*

Um ponteiro para uma matriz de estruturas de [JET_IndexRange](./jet-indexrange-structure.md) . Cada estrutura inclui um [JET_TABLEID](./jet-tableid.md) que foi configurado para conter um dos intervalos de índice a serem interseccionados. Para obter mais informações, consulte [JET_IndexRange](./jet-indexrange-structure.md).

*cindexrange*

O número de estruturas de [JET_IndexRange](./jet-indexrange-structure.md) na matriz contida no parâmetro *rgindexrange* .

*precabolist*

Ponteiro para uma estrutura de [JET_RECORDLIST](./jet-recordlist-structure.md) . Essa estrutura será preenchida com informações suficientes para atravessar a tabela temporária com os resultados de **JetIntersectIndexes**.

O buffer de saída que recebe uma estrutura de [JET_RECORDLIST](./jet-recordlist-structure.md) . A estrutura contém uma descrição do conjunto de resultados da interseção.

*grbit*

Reservado para uso futuro.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Uma das opções solicitadas era inválida, foi usada incorretamente ou não foi implementada.</p><p>Esse erro é retornado por <strong>JetIntersectIndexes</strong> quando:</p><p>O <em>grbit</em> contido na estrutura de <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> apontada por qualquer elemento na matriz <em>rgindexrange</em> não é igual a JET_bitRecordInIndex.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos contém um valor inesperado ou um valor que é inconsistente quando combinado com o valor de outro parâmetro.</p><p>Esse erro é retornado por <strong>JetIntersectIndexes</strong> pelos seguintes motivos:</p><ul><li><p>O parâmetro <em>precabolist</em> é nulo.</p></li><li><p>O membro <strong>cbStruct</strong> da estrutura de <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> especificada no parâmetro <em>precabolist</em> não é igual ao tamanho da estrutura de <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> .</p></li><li><p>O parâmetro <em>cindexrange</em> é zero.</p></li><li><p>O parâmetro <em>cindexrange</em> é maior que 64.</p></li><li><p>O membro <strong>cbStruct</strong> para qualquer elemento na matriz especificado pelo parâmetro <em>rgindexrange</em> não é igual ao tamanho da estrutura de <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> .</p></li><li><p>Os elementos na matriz <em>rgindexrange</em> contêm <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s de tabelas diferentes.</p></li><li><p>Um elemento na matriz <em>rgindexrange</em> contém um <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> que não está posicionado em um índice secundário.</p></li><li><p>Um ou mais dos elementos na matriz <em>rgindexrange</em> contêm <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s posicionados no mesmo índice secundário.</p></li></ul> | 
| <p>JET_errInvalidSesid</p> | <p>O identificador de sessão é inválido ou se refere a uma sessão fechada.</p><p>Esse erro não é retornado em todas as circunstâncias. Os identificadores são validados apenas com base no melhor esforço.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão não foi inicializada.</p> | 
| <p>JET_errOutOfCursors</p> | <p>A operação falhou porque o mecanismo não pôde alocar os recursos necessários para abrir um novo cursor. Os recursos de cursor são configurados chamando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <em>JET_paramMaxCursors</em> especificado no parâmetro <em>paramid</em> .</p> | 
| <p>JET_errOutOfMemory</p> | <p>A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</p><p><strong>JetIntersectIndexes</strong> pode retornar JET_errOutOfMemory se o espaço de endereço do processo do host se tornar muito fragmentado. O Gerenciador de tabela temporária sempre alocará um bloco de 1 MB de espaço de endereço para cada tabela temporária criada, independentemente da quantidade de dados a serem armazenados. <strong>JetIntersectIndexes</strong> criará uma tabela temporária para cada <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> especificado no parâmetro <em>rgindexrange</em> e uma tabela temporária para a saída em <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>É ilegal usar a mesma sessão de mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>A operação falhou porque o mecanismo não pôde alocar os recursos necessários para armazenar em cache os índices da tabela. O número de índices cujo esquema pode ser armazenado em cache é configurado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <em>JET_paramMaxOpenTables</em> especificado no parâmetro <em>paramid</em> .</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>A operação falhou porque o mecanismo não pôde alocar os recursos necessários para armazenar em cache o esquema da tabela. O número de tabelas cujo esquema pode ser armazenado em cache é configurado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <em>JET_paramMaxOpenTables</em> especificado no parâmetro <em>paramid</em> .</p> | 
| <p>JET_errTooManySorts</p> | <p>A operação falhou porque o mecanismo não pôde alocar os recursos necessários para criar uma tabela temporária. Os recursos de tabela temporária são configurados usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com JET_paramMaxTemporaryTables especificado no parâmetro <em>paramid</em> .</p> | 



Em caso de sucesso, uma nova tabela temporária é retornada contendo os indicadores dos registros que correspondem aos critérios representados por cada uma das descrições de intervalo de índice de entrada.

Em caso de falha, a tabela temporária que contém os resultados não será criada. O estado do banco de dados temporário pode ser alterado. O estado de qualquer banco de dados comum em uso pelo mecanismo de banco de dados permanecerá inalterado. A posição atual das [JET_TABLEID](./jet-tableid.md)s fornecidas para essa função pode ser alterada.

#### <a name="remarks"></a>Comentários

**JetIntersectIndexes** pode ser usado para filtrar com eficiência os registros em uma tabela por vários critérios se esses critérios puderem ser expressos em termos dos índices secundários nessa tabela. Por exemplo, considere que você tem uma tabela muito grande que contém pessoas. A tabela pode ter colunas para sua ID de usuário, nome, sobrenome e assim por diante. Suponha que cada uma dessas colunas seja indexada separadamente e que o índice principal da tabela esteja acima da ID de usuário. Se você quisesse encontrar todos cujo primeiro nome começa com um e cujo sobrenome começa com G, você executaria as seguintes etapas:

1.  Abra um novo cursor na tabela e defina esse cursor para usar o índice na coluna "First Name". Em seguida, configure um intervalo de índice para todas as pessoas cujo "primeiro nome" seja iniciado com ' A ' e crie um [JET_IndexRange](./jet-indexrange-structure.md) struct que contenha esse cursor.

2.  Repita a etapa 1 com um novo cursor no índice "Last Name" para todas as pessoas cujo "Last Name" começou com "G".

3.  Passe esses critérios para **JetIntersectIndexes** para computar o resultado em uma tabela temporária.

4.  Percorra a tabela temporária e recupere cada um dos registros que passam os critérios por indicador.

A tabela temporária que contém o conjunto de resultados é uma tabela simples com uma coluna que contém o indicador de cada registro que passou todos os critérios usados para calcular a interseção. O conjunto de resultados é classificado na mesma ordem que o índice primário e não contém entradas duplicadas. O aplicativo pode enumerar os resultados da interseção enumerando as linhas na tabela temporária, recuperando o indicador para cada resultado usando [JetRetrieveColumn](./jetretrievecolumn-function.md)e, em seguida, visitando o registro no banco de dados chamando [JetGotoBookmark](./jetgotobookmark-function.md) com esse indicador em um cursor posicionado no índice primário.

A tabela temporária retornada por **JetIntersectIndexes** só pode ser verificada em uma direção de encaminhamento. Ele também deve ser fechado por meio de [JetCloseTable](./jetclosetable-function.md) quando a verificação for concluída. Para obter mais informações sobre tabelas temporárias e como elas funcionam, consulte [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

O **JetIntersectIndexes** geralmente é uma maneira eficiente e conveniente de filtrar registros com base em vários critérios indexados. No entanto, há algumas dicas importantes que devem ser seguidas para maximizar a utilidade desse recurso. Se você souber que um dos critérios é tão restritivo que o intervalo de índice resultante tem poucos registros, é provável que seja melhor simplesmente percorrer esse intervalo de índice e filtrar os registros no nível do aplicativo. Além disso, se você souber que tem critérios muito menos restritivos do que outros critérios em sua interseção, você pode considerar descartar os critérios muito menos restritivos da interseção. Por fim, se você souber que um dos critérios não é tão restritivo, de modo que o intervalo de índice resultante seja quase tão grande quanto o índice primário, é improvável que a interseção com esse intervalo de índice se beneficiará (reduza o tamanho do) do conjunto de resultados. Em todos os casos, você deve estar selecionando critérios de uma maneira que utilizará o menor número possível de entradas de índice na entrada e gerará o conjunto mais específico de indicadores na saída para o desempenho máximo.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_IndexRange](./jet-indexrange-structure.md)  
[JET_RECORDLIST](./jet-recordlist-structure.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
