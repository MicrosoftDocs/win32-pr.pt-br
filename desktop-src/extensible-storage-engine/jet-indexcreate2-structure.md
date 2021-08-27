---
description: 'Saiba mais sobre: estrutura JET_INDEXCREATE2 dados'
title: Estrutura JET_INDEXCREATE2
TOCTitle: JET_INDEXCREATE2 Structure
ms:assetid: c574500e-8695-4f29-8e9d-6dff987af2a2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294082(v=EXCHG.10)
ms:contentKeyID: 32765697
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
ms.openlocfilehash: 00d5a788113b7427fb96a4f270478c1dd7572d54
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473202"
---
# <a name="jet_indexcreate2-structure"></a>Estrutura JET_INDEXCREATE2


_**Aplica-se a:** Windows | Windows Servidor_

A **JET_INDEXCREATE2** contém as informações necessárias para criar um índice sobre dados em um banco de dados ESE (Extensible Armazenamento Engine). A estrutura é usada por funções como [JetCreateIndex2](./jetcreateindex2-function.md)e em estruturas como [JET_TABLECREATE](./jet-tablecreate-structure.md) e [JET_TABLECREATE2](./jet-tablecreate2-structure.md).

A **JET_INDEXCREATE2** foi introduzida no sistema operacional Windows 7.

```cpp
typedef struct tagJET_INDEXCREATE2 {
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
  JET_SPACEHINTS* pSpacehints;
} JET_INDEXCREATE;
```

### <a name="members"></a>Membros

**Cbstruct**

O tamanho, em bytes, dessa estrutura. De definir esse membro como sizeof( JET_INDEXCREATE2 ).

**szIndexName**

O nome do índice a ser criado.

O nome deve atender às seguintes condições:

  - Ele deve ser menor que JET_cbNameMost, não incluindo o nulo de terminação.

  - Ele deve consistir no seguinte conjunto de caracteres: 0 (zero) a 9, A a Z, a a z e todas as outras pontuações, exceto " \! " (ponto de exclamação), "," (vírgula), " " (colchete de abertura) e " " (colchete de fechamento) — ou seja, caracteres ASCII 0x20, 0x22 por meio de 0x2d, 0x2f por meio \[ \] de 0x5a, 0x5c e 0x5d por meio 0x7f.

  - Ele não deve começar com um espaço.

  - Ele deve conter pelo menos um caractere sem espaço.

**szKey**

Um ponteiro para uma cadeia de caracteres terminada em nulo duplo de tokens delimitados por nulo.

Cada token é do formato " \<direction-specifier\> \<column-name\> ", em que direction-specification é "+" ou "-". Por exemplo, uma **szKey** de "+abc \\ 0-def 0+gee 0" será indexada sobre as três \\ \\ colunas "abc" (em ordem crescente), "def" (em ordem decrescente) e "gee" (em ordem crescente). Na linguagem C, literais de cadeia de caracteres têm um terminador **NULL** implícito, portanto, a cadeia de caracteres acima será encerrada por um double-NULL.

O número de colunas especificadas em **szKey** não deve exceder JET_ccolKeyMost (uma constante dependente de versão).

Pelo menos uma coluna deve ser nomeada **em szKey**.

Comportamento obsoleto: após o terminador double-NULL, é possível especificar uma ID de idioma (um WORD que é passado para MAKELCID( langid, SORT_DEFAULT ) ) como uma maneira de especificar o LCID para o índice. É ilegal especificar uma ID de idioma em **szKey** e uma LCID no [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (definindo JET_bitIndexUnicode em *grbit*).

Preterido: após a ID de idioma, é possível passar **cbVarSegMac** como um tipo de **dados USHORT.** O comportamento será indefinido se o USHORT for definido em **szKey** e se **cbVarSegMac** estiver definido na estrutura.

**cbKey**

O comprimento, em bytes, de **szKey,** incluindo os dois nulos de terminação.

**grbit**

Um grupo de bits que contém zero ou mais das opções de valor listadas na tabela a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitIndexUnique</p> | <p>Entradas de índice duplicadas (chaves) não são permitidos. Isso é imposto quando <a href="gg269288(v=exchg.10).md">JetUpdate</a> é chamado, não quando <a href="gg294137(v=exchg.10).md">JetSetColumn</a> é chamado.</p> | 
| <p>JET_bitIndexPrimary</p> | <p>O índice é um índice primário (clusterado). Cada tabela deve ter exatamente um índice primário. Se nenhum índice primário for definido explicitamente em uma tabela, o mecanismo de banco de dados criará seu próprio índice primário.</p> | 
| <p>JET_bitIndexDisallowNull</p> | <p>Nenhuma das colunas sobre as quais o índice é criado pode conter um <strong>valor NULL.</strong></p> | 
| <p>JET_bitIndexIgnoreNull</p> | <p>Não adicione uma entrada de índice para uma linha se todas as colunas que estão sendo indexadas são <strong>NULL.</strong></p> | 
| <p>JET_bitIndexIgnoreAnyNull</p> | <p>Não adicione uma entrada de índice para uma linha se qualquer uma das colunas que está sendo indexada for <strong>NULL.</strong></p> | 
| <p>JET_bitIndexIgnoreFirstNull</p> | <p>Não adicione uma entrada de índice para uma linha se a primeira coluna que está sendo indexada for <strong>NULL.</strong></p> | 
| <p>JET_bitIndexLazyFlush</p> | <p>Especifica que as operações de índice serão registradas em lozily.</p><p>JET_bitIndexLazyFlush não afeta aziez das atualizações de dados. Se a operação de indexação for interrompida pelo encerramento do processo, a Recuperação Suave ainda poderá fazer com que o banco de dados tenha um estado consistente, mas o índice pode não estar presente.</p> | 
| <p>JET_bitIndexEmpty</p> | <p>Não tente criar o índice, pois todas as entradas serão avaliadas como <strong>NULL.</strong> <strong>grbit</strong> TAMBÉM DEVE especificar JET_bitIgnoreAnyNull quando JET_bitIndexEmpty é passado. Esse é um aprimoramento de desempenho. Por exemplo, se uma nova coluna for adicionada a uma tabela e, em seguida, um índice for criado nessa coluna recém-adicionada, todos os registros na tabela serão verificados mesmo que não sejam adicionados ao índice. Especificar JET_bitIndexEmpty ignora a verificação da tabela, o que pode levar muito tempo.</p> | 
| <p>JET_bitIndexUnversioned</p> | <p>JET_bitIndexUnversioned faz com que a criação do índice seja visível para outras transações. Normalmente, uma sessão em uma transação não poderá ver uma operação de criação de índice em outra sessão. Esse sinalizador poderá ser útil se outra transação tiver a probabilidade de criar o mesmo índice. A segunda criação de índice simplesmente falhará em vez de potencialmente causar muitas operações desnecessárias de banco de dados. A segunda transação pode não ser capaz de usar o índice imediatamente. A operação de criação de índice precisa ser concluída antes de ser acessível. No momento, a sessão não deve estar em uma transação para criar um índice sem informações de versão.</p> | 
| <p>JET_bitIndexSortNullsHigh</p> | <p>Especificar esse sinalizador faz com <strong>que os valores NULL</strong> sejam classificação após os dados de todas as colunas no índice.</p> | 
| <p>JET_bitIndexUnicode</p> | <p>Especificar esse sinalizador afeta a interpretação do campo de união lcid/pidxunicde na estrutura. Definir o bit significa que o campo pidxunicode realmente aponta para uma <a href="gg294097(v=exchg.10).md">estrutura JET_UNICODEINDEX</a> dados. JET_bitIndexUnicode é necessário para indexar dados Unicode. Ele só é necessário para personalizar a normalização de dados Unicode.</p> | 
| <p>JET_bitIndexTuples</p> | <p>Especifica que o índice é um índice de tupla. Consulte <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para ver uma descrição de um índice de tupla.</p><p>O JET_bitIndexTuples valor foi introduzido no sistema operacional Windows XP.</p> | 
| <p>JET_bitIndexTupleLimits</p> | <p>Especificar esse sinalizador afeta a interpretação do campo de união <strong>cbVarSegMac/ptuplelimits</strong> na estrutura. Definir esse bit significa que o <strong>campo ptuplelimits</strong> realmente aponta para uma estrutura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para permitir limites de índice de tupla personalizados (implica JET_bitIndexTuples).</p><p>O <strong>JET_bitIndexTupleLimits</strong> foi introduzido no sistema operacional Windows Server 2003.</p> | 
| <p>JET_bitIndexCrossProduct<br />0x00004000</p> | <p>Especificar esse sinalizador para um índice que tem mais de uma coluna de chave que é uma coluna de vários valores resultará na criação de uma entrada de índice para cada resultado de um produto cruzado de todos os valores nessas colunas de chave. Caso contrário, o índice teria apenas uma entrada para cada multivalor na coluna de chave mais significativa que é uma coluna de vários valores e cada uma dessas entradas de índice usaria o primeiro multivalor de qualquer outra coluna de chave que são colunas com valores múltiplos.</p><p>Por exemplo, se você especificou esse sinalizador para um índice sobre a coluna A que tem os valores "vermelho" e "azul" e sobre a coluna B que tem os valores "1" e "2", as seguintes entradas de índice serão criadas: "vermelho", "1"; "red", "2"; "blue", "1"; "blue", "2". Caso contrário, as seguintes entradas de índice seriam criadas: "red", "1"; "blue", "1".</p><p>O <strong>JET_bitIndexCrossProduct</strong> valor foi introduzido no Windows Vista.</p> | 
| <p>JET_bitIndexKeyMost<br />0x00008000</p> | <p>Especificar esse sinalizador fará com que o índice use o tamanho máximo da chave especificado no <strong>campo cbKeyMost</strong> na estrutura. Caso contrário, o índice usará JET_cbKeyMost (255) como seu tamanho máximo de chave.</p><p>O <strong>JET_bitIndexKeyMost</strong> foi introduzido no Windows Vista.</p> | 
| <p>JET_bitIndexDisallowTruncation<br />0x00010000</p> | <p>Especificar esse sinalizador fará com que qualquer atualização no índice que resulte em uma chave truncada falhe com o código JET_errKeyTruncated resposta. Caso contrário, as chaves serão silenciosamente truncadas. Para obter mais informações sobre truncamento de chave, <a href="gg269329(v=exchg.10).md">consulte JetMakeKey</a>.</p><p>O <strong>JET_bitIndexDisallowTruncation</strong> valor foi introduzido no Windows Vista.</p> | 



**ulDensity**

A densidade percentual da árvore de índice B+ inicial. Especificar um número menor que 100 usa mais espaço para criar o índice inicialmente, mas permite que o crescimento futuro do índice seja realizado, evitando assim a fragmentação interna.

**lcid**

O LCID (identificador de localidade) a ser usado ao normalizar os dados quando o JET_bitIndexUnicode valor não for especificado no *parâmetro grbit.* O LCID afetará a normalização se o índice estiver sobre colunas Unicode.

**pidxunicode**

Um ponteiro para uma [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) se o valor JET_bitIndexUnicode valor for especificado no parâmetro *grbit.* Isso permite que o usuário especifique sinalizadores personalizados que são passados para a [função LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) durante a normalização unicode.

**cbVarSegMac**

O comprimento máximo, em bytes, de cada coluna a ser armazenada no índice quando o JET_bitIndexTupleLimits valor não for especificado no parâmetro *grbit.*

Especificar um valor de 0 (zero) para esse campo é equivalente ao seguinte:

  - Especificando JET_cbPrimaryKeyMost para um índice primário.

  - Especificando JET_cbSecondaryKeyMost para um índice secundário.

**ptuplelimits**

Um ponteiro para uma [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) se o valor JET_bitIndexTupleLimits valor for especificado no *parâmetro grbit.*

**ptuplelimits** foi introduzido no Windows Server 2003.

**rgconditionalcolumn**

Um parâmetro opcional para uma matriz [de JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) estruturas, que são usadas para especificar as colunas condicionais no índice.

**cConditionalColumn**

A contagem de estruturas na **matriz rgconditionalcolumn.**

**Err**

Contém o código de retorno para criar esse índice.

**cbKeyMost**

Especifica o tamanho máximo permitida, em bytes, para chaves no índice. Esse parâmetro será ignorado se JET_bitIndexKeyMost não for especificado no *parâmetro grbit.* Se esse parâmetro for definido como zero e JET_bitIndexKeyMost for especificado no membro *grbit,* a função de chamada falhará com JET_err_InvalidDef.

O tamanho máximo mínimo da chave com suporte é JET_cbKeyMostMin (255), que é o tamanho máximo da chave herdado.

O tamanho máximo da chave depende do tamanho da página do banco de dados (JET_paramDatabasePageSize) da seguinte forma:

  - Se JET_paramDatabasePageSize = 2048, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)

  - Se JET_paramDatabasePageSize = 4096, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)

  - Se JET_paramDatabasePageSize = 8192, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)

O tamanho máximo de chave com suporte para a instância também pode ser lido do parâmetro JET_paramKeyMost sistema.

**cbKeyMost** foi introduzido no Windows Vista.

**pSpacehints**

Um ponteiro para uma [estrutura JET_SPACEHINTS](./jet-spacehints-structure.md) dados.

**pSpacehints** foi introduzido no Windows 7.

### <a name="remarks"></a>Comentários

O ESE dá suporte à indexação em colunas de chave que contêm vários valores. Para usar esse recurso, a coluna deve ser um tipo de coluna marcada (JET_bitColumnTagged) e deve ser sinalizada para ter seus vários valores indexados com JET_bitColumnMultiValued. Em versões Windows anteriores ao Windows Vista, somente a primeira coluna de chave com vários valores no índice terá seus valores expandidos no índice. Todas as outras colunas com valores múltiplos e marcados terão apenas seus primeiros valores expandidos no índice.

Supondo que as linhas a seguir existam em uma tabela (a coluna Alfa não tem vários valores, enquanto as colunas Beta, Gama e Delta são multivaloradas) e um índice é criado como "+Alfa \\ 0+Beta \\ 0+Gama \\ 0+Delta \\ \\ 0 0":


| <p>Alpha</p> | <p>Beta</p> | <p>Gama</p> | <p>Delta</p> | 
|--------------|-------------|--------------|--------------|
| <p>1</p> | <p>ABC<br />GHI<br />JKL</p> | <p>MNO<br />PQR<br />STU</p> | <p>VWX<br />YZ</p> | 
| <p>2</p> | <p>O</p> | <p>CHUVA<br />ESPANHA</p> | <p>IN<br />CAI</p> | 



As seguintes tuplas de índice serão armazenadas:

{1,ABC, MNO, VWX}  
{1,GEE, MNO, VWX}  
{1,JKL, MNO, VWX}  
{2,THE,RAIN,IN}

Observe que {2,THE,SPAIN,IN} não está armazenado, embora a coluna Alfa na segunda linha tenha um único multivalor.

Em versões do Windows do Windows Vista, todas as colunas com vários valores podem ser expandidas no índice especificando JET_bitIndexCrossProduct.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_ INDEXCREATE2_W</strong> (Unicode) <strong>e JET_ INDEXCREATE2_A</strong> (ANSI).</p> | 



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
