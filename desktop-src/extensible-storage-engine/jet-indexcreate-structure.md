---
description: 'Saiba mais sobre: estrutura de JET_INDEXCREATE'
title: Estrutura JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE Structure
ms:assetid: 0c55f25c-d42a-49ba-a1fe-549850fdc9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269186(v=EXCHG.10)
ms:contentKeyID: 32765489
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 31b6b72cba336e3f7251bacfb1836673086ba9c2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467623"
---
# <a name="jet_indexcreate-structure"></a>Estrutura JET_INDEXCREATE


_**Aplica-se a:** Windows | Windows Servidor_

a estrutura de **JET_INDEXCREATE** contém as informações necessárias para criar um índice sobre os dados em um banco de dado ESE (mecanismo de Armazenamento extensível). A estrutura é usada por funções como [JetCreateIndex2](./jetcreateindex2-function.md)e em estruturas como [JET_TABLECREATE](./jet-tablecreate-structure.md) e [JET_TABLECREATE2](./jet-tablecreate2-structure.md).

``` c++
typedef struct tagJET_INDEXCREATE {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
  unsigned long cbKeyMost;
} JET_INDEXCREATE;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho, em bytes, dessa estrutura. Defina este membro como sizeof (JET_INDEXCREATE).

**szIndexName**

O nome do índice a ser criado.

O nome do índice deve atender às seguintes condições:

  - Ele deve ser menor que JET_cbNameMost, não incluindo o nulo de terminação.

  - Ele deve consistir nos seguintes caracteres: 0 (zero) a 9, A a Z, a a z e todas as outras pontuações, exceto para " \! " (ponto de exclamação), "," (vírgula), " \[ " (colchete de abertura) e " \] " (colchete de fechamento) — ou seja, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c, 0x5d até 0x7F.

  - Ele não deve começar com um espaço.

  - Ele deve consistir em pelo menos um caractere que não seja de espaço.

**szKey**

Um ponteiro para uma cadeia de caracteres com terminação de nulo duplo de tokens delimitados por nulo.

Cada token tem o formato " \<direction-specifier\> \<column-name\> ", onde a especificação de direção é "+" ou "-". Por exemplo, um **szKey** de "+ ABC \\ 0-Def \\ 0 + GHI \\ 0" irá indexar as três colunas "ABC" (em ordem crescente), "def" (em ordem decrescente) e "GHI" (em ordem crescente). Na linguagem C, literais de cadeia de caracteres têm um terminador **NULL** implícito; Portanto, a cadeia de caracteres acima será encerrada por um duplo nulo.

O número de colunas especificado em **szKey** não pode exceder o valor de **JET_ccolKeyMost** (uma constante dependente de versão).

Pelo menos uma coluna deve ser nomeada em **szKey**.

Comportamento obsoleto: após o terminador de nulo duplo, é possível especificar uma ID de idioma (uma palavra que é passada em MAKELCID (LangID, SORT_DEFAULT)) como uma maneira de especificar o LCID para o índice. É ilegal especificar uma ID de idioma em **szKey** e um LCID em [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (definindo JET_bitIndexUnicode em *grbit*).

Preterido: após a ID do idioma, é possível passar **cbVarSegMac** como um ushort. O comportamento será indefinido se USHORT estiver definido em **szKey** e se **cbVarSegMac** for definido na estrutura.

**cbKey**

O comprimento, em bytes, de **szKey** , incluindo os dois nulos de terminação.

**grbit**

Um grupo de bits que inclui zero ou mais valores listados na tabela a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitIndexUnique</p> | <p>Não são permitidas entradas de índice duplicadas (chaves). Isso é imposto quando <a href="gg269288(v=exchg.10).md">JetUpdate</a> é chamado, não quando <a href="gg294137(v=exchg.10).md">JetSetColumn</a> é chamado.</p> | 
| <p>JET_bitIndexPrimary</p> | <p>O índice é um índice primário (clusterizado). Cada tabela deve ter exatamente um índice primário. Se nenhum índice primário for explicitamente definido em uma tabela, o mecanismo de banco de dados criará seu próprio índice primário.</p> | 
| <p>JET_bitIndexDisallowNull</p> | <p>Nenhuma das colunas sobre as quais o índice é criado pode conter um valor <strong>nulo</strong> .</p> | 
| <p>JET_bitIndexIgnoreNull</p> | <p>Não adicione uma entrada de índice para uma linha se todas as colunas que estão sendo indexadas forem <strong>nulas</strong>.</p> | 
| <p>JET_bitIndexIgnoreAnyNull</p> | <p>Não adicione uma entrada de índice para uma linha se qualquer uma das colunas que estão sendo indexadas for <strong>nula</strong>.</p> | 
| <p>JET_bitIndexIgnoreFirstNull</p> | <p>Não adicione uma entrada de índice para uma linha se a primeira coluna que está sendo indexada for <strong>nula</strong>.</p> | 
| <p>JET_bitIndexLazyFlush</p> | <p>As operações de índice serão registradas lentamente.</p><p>JET_bitIndexLazyFlush não afeta a ociosa das atualizações de dados. Se a operação de indexação for interrompida pelo encerramento do processo, a recuperação simples ainda poderá obter o banco de dados para um estado consistente, mas o índice poderá não estar presente.</p> | 
| <p>JET_bitIndexEmpty</p> | <p>Não tente Compilar o índice, pois todas as entradas seriam avaliadas como <strong>nulas</strong>. <strong>grbit</strong> também deve especificar JET_bitIgnoreAnyNull quando JET_bitIndexEmpty for passado. Esse é um aprimoramento de desempenho. Por exemplo, se uma nova coluna for adicionada a uma tabela, um índice será criado nessa coluna recém-adicionada e todos os registros na tabela serão verificados, mesmo que não sejam adicionados ao índice. Especificar JET_bitIndexEmpty ignora a verificação da tabela, o que pode levar muito tempo.</p> | 
| <p>JET_bitIndexUnversioned</p> | <p>Faz com que a criação do índice seja visível para outras transações. Normalmente, uma sessão em uma transação não poderá ver uma operação de criação de índice em outra sessão. Esse sinalizador pode ser útil se outra transação provavelmente criar o mesmo índice. O segundo índice-Create falhará em vez de causar muitas operações desnecessárias de banco de dados. A segunda transação pode não ser capaz de usar o índice imediatamente. A operação de criação de índice deve ser concluída antes de ser utilizável. A sessão não deve estar em uma transação no momento para criar um índice sem informações de versão.</p> | 
| <p>JET_bitIndexSortNullsHigh</p> | <p>A especificação desse sinalizador faz com que valores <strong>nulos</strong> sejam classificados após os dados de todas as colunas no índice.</p> | 
| <p>JET_bitIndexUnicode</p> | <p>A especificação desse sinalizador afeta a interpretação do campo de União LCID/pidxunicde na estrutura. Definir o bit significa que o campo <strong>pidxunicode</strong> realmente aponta para uma estrutura de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> . JET_bitIndexUnicode não é necessário para indexar dados Unicode. Ele é usado apenas para personalizar a normalização de dados Unicode.</p> | 
| <p>JET_bitIndexTuples</p> | <p>Especifica que o índice é um índice de tupla. Consulte <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para obter uma descrição de um índice de tupla.</p><p>JET_bitIndexTuples foi introduzido no sistema operacional Windows XP.</p> | 
| <p>JET_bitIndexTupleLimits</p> | <p>A especificação desse sinalizador afeta a interpretação do campo de União <strong>cbVarSegMac/ptuplelimits</strong> na estrutura. Definir esse bit significa que o campo <strong>ptuplelimits</strong> realmente aponta para uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para permitir limites de índice de tupla personalizados (implica JET_bitIndexTuples).</p><p>JET_bitIndexTupleLimits foi introduzido no sistema operacional Windows Server 2003.</p> | 
| <p>JET_bitIndexCrossProduct 0x00004000</p> | <p>A especificação desse sinalizador para um índice que tenha mais de uma coluna de chave que seja uma coluna de vários valores resultará na criação de uma entrada de índice para cada resultado de um produto cruzado de todos os valores nessas colunas de chave. Caso contrário, o índice terá apenas uma entrada para cada vários valores na coluna de chave mais significativa, que é uma coluna com vários valores, e cada uma dessas entradas de índice usará os primeiros valores de quaisquer outras colunas de chave que tenham colunas com vários valores.</p><p>Por exemplo, se você tiver especificado esse sinalizador para um índice na coluna A que tem os valores "vermelho" e "azul" e na coluna B que tem os valores "1" e "2", as seguintes entradas de índice serão criadas: "vermelho", "1"; "vermelho", "2"; "azul", "1"; "Blue", "2". Caso contrário, as seguintes entradas de índice seriam criadas: "vermelho", "1"; "Blue", "1".</p><p>JET_bitIndexCrossProduct foi introduzido no sistema operacional Windows Vista.</p> | 
| <p>JET_bitIndexKeyMost 0x00008000</p> | <p>A especificação desse sinalizador fará com que o índice use o tamanho máximo de chave especificado no campo <strong>cbKeyMost</strong> na estrutura. Caso contrário, o índice usará JET_cbKeyMost (255) como o tamanho máximo da chave.</p><p>o JET_bitIndexKeyMost foi introduzido no Windows Vista.</p> | 
| <p>JET_bitIndexDisallowTruncation 0x00010000</p> | <p>A especificação desse sinalizador fará com que qualquer atualização do índice que resulte em uma chave truncada falhe com JET_errKeyTruncated. Caso contrário, as chaves serão truncadas silenciosamente. Para obter mais informações sobre o truncamento de chave, consulte a função <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</p><p><strong>Windows vista: JET_bitIndexDisallowTruncation</strong> é introduzido no Windows Vista.</p> | 
| <p>JET_bitIndexNestedTable 0x00020000</p> | <p>A especificação desse sinalizador causará a atualização do índice em várias colunas com vários valores, mas somente com os valores do mesmo <strong>itagSequence</strong>.</p><p>JET_bitIndexNestedTable foi introduzido no Windows Vista.</p> | 



**ulDensity**

A densidade percentual da árvore de índice B+ inicial. Especificar um número menor que 100 usa mais espaço para criar o índice inicialmente, mas permite que o crescimento futuro do índice seja realizado, evitando assim a fragmentação interna.

**lcid**

O LCID (identificador de localidade) a ser usado ao normalizar os dados quando o JET_bitIndexUnicode valor não for especificado no *parâmetro grbit.* O LCID afetará a normalização se o índice estiver sobre colunas Unicode.

**pidxunicode**

Um ponteiro para uma [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) se o valor JET_bitIndexUnicode valor for especificado no parâmetro *grbit.* Isso permite que o usuário especifique sinalizadores personalizados que são passados para a [função LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) durante a normalização unicode.

**cbVarSegMac**

O comprimento máximo, em bytes, de cada coluna a ser armazenada no índice quando o JET_bitIndexTupleLimits valor não for especificado no *parâmetro grbit.*

Especificar um valor de 0 (zero) para esse campo é equivalente a:

  - Especificando JET_cbPrimaryKeyMost para um índice primário.

  - Especificando JET_cbSecondaryKeyMost para um índice secundário.

**ptuplelimits**

Um ponteiro para uma [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) se o valor JET_bitIndexTupleLimits valor for especificado no parâmetro *grbit.*

ptuplelimits foi introduzido no Windows Server 2003.

**rgconditionalcolumn**

Um parâmetro opcional para uma matriz [de JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) estruturas, que são usadas para especificar as colunas condicionais no índice.

**cConditionalColumn**

A contagem de estruturas na **matriz rgconditionalcolumn.**

**Err**

Contém o código de retorno para criar esse índice.

**cbKeyMost**

Especifica o tamanho máximo permitida, em bytes, para chaves no índice. Esse parâmetro será ignorado se o valor JET_bitIndexKeyMost valor não for especificado no *parâmetro grbit.* Se esse parâmetro for definido como zero e JET_bitIndexKeyMost for especificado no parâmetro *grbit,* a função de chamada falhará com JET_err_InvalidDef.

O tamanho máximo mínimo da chave com suporte é JET_cbKeyMostMin (255), que é o tamanho máximo da chave herdado.

O tamanho máximo da chave depende do tamanho da página do banco de dados (JET_paramDatabasePageSize), da seguinte forma:

  - Se JET_paramDatabasePageSize = 2048, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)

  - Se JET_paramDatabasePageSize = 4096, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)

  - Se JET_paramDatabasePageSize = 8192, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)

O tamanho máximo de chave com suporte para a instância também pode ser lido do parâmetro JET_paramKeyMost sistema.

**cbKeyMost** foi introduzido no Windows Vista.

### <a name="remarks"></a>Comentários

O ESE dá suporte à indexação em colunas de chave que contêm vários valores. Para usar esse recurso, a coluna deve ser um tipo de coluna marcada (JET_bitColumnTagged) e deve ser sinalizada para ter seus vários valores indexados com JET_bitColumnMultiValued. Em versões Windows anteriores ao Windows Vista, somente a primeira coluna de chave com vários valores no índice terá seus valores expandidos no índice. Todas as outras colunas com valores múltiplos e marcados terão apenas seus primeiros valores expandidos no índice.

Supondo que as linhas a seguir existam em uma tabela (a coluna Alfa não tem vários valores, enquanto as colunas Beta, Gama e Delta são multivaloradas) e um índice é criado como "+Alfa \\ 0+Beta \\ 0+Gama \\ 0+Delta \\ \\ 0 0":


| <p>Alpha</p> | <p>Beta</p> | <p>Gama</p> | <p>Delta</p> | 
|--------------|-------------|--------------|--------------|
| <p>1</p> | <p>ABC<br />GHI<br />JKL</p> | <p>MNO<br />PQR<br />STU</p> | <p>VWX<br />YZ</p> | 
| <p>2</p> | <p>O</p> | <p>CHUVA<br />ESPANHA</p> | <p>IN<br />CAI</p> | 



As tuplas de índice em queda serão armazenadas:

{1,ABC, MNO, VWX}  
{1,GEE, MNO, VWX}  
{1,JKL, MNO, VWX}  
{2,THE,RAIN,IN}

Observe que {2,THE,SPAIN,IN} não está armazenado, embora a coluna Alfa na segunda linha tenha um único multivalor.

Em versões do Windows do Windows Vista, todas as colunas com vários valores podem ser expandidas no índice especificando JET_bitIndexCrossProduct.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_ INDEXCREATE_W</strong> (Unicode) <strong>e JET_ INDEXCREATE_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Confira também

[JET_COLTYP](./jet-coltyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)
