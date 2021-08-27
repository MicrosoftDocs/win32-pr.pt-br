---
description: 'Saiba mais sobre: estrutura JET_INDEXCREATE dados'
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
ms.openlocfilehash: 237e6351c7baf7f418c5160797f413d78ce034bd
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984149"
---
# <a name="jet_indexcreate-structure"></a>Estrutura JET_INDEXCREATE


_**Aplica-se a:** Windows | Windows Servidor_

A **JET_INDEXCREATE** contém as informações necessárias para criar um índice sobre dados em um banco de dados ESE (Extensible Armazenamento Engine). A estrutura é usada por funções como [JetCreateIndex2](./jetcreateindex2-function.md)e em estruturas como [JET_TABLECREATE](./jet-tablecreate-structure.md) e [JET_TABLECREATE2](./jet-tablecreate2-structure.md).

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

**Cbstruct**

O tamanho, em bytes, dessa estrutura. De definir esse membro como sizeof( JET_INDEXCREATE ).

**szIndexName**

O nome do índice a ser criado.

O nome do índice deve atender às seguintes condições:

  - Ele deve ser menor que JET_cbNameMost, não incluindo o nulo de terminação.

  - Ele deve consistir nos seguintes caracteres: 0 (zero) a 9, A a Z, a a z e todas as outras pontuações, exceto " \! " (ponto de exclamação), "," (vírgula), " " (colchete de abertura) e " " (colchete de fechamento) — ou seja, caracteres ASCII 0x20, 0x22 0x2d, 0x2f por meio de \[ \] 0x5a, 0x5c, 0x5d por meio 0x7f.

  - Ele não deve começar com um espaço.

  - Ele deve consistir em pelo menos um caractere não espaço.

**szKey**

Um ponteiro para uma cadeia de caracteres terminada em nulo duplo de tokens delimitados por nulo.

Cada token é do formato " \<direction-specifier\> \<column-name\> ", em que direction-specification é "+" ou "-". Por exemplo, uma **szKey** de "+abc \\ 0-def 0+gee 0" será indexada sobre as três \\ \\ colunas "abc" (em ordem crescente), "def" (em ordem decrescente) e "gee" (em ordem crescente). Na linguagem C, literais de cadeia de caracteres têm um **terminador NULL** implícito; portanto, a cadeia de caracteres acima será encerrada por um double-NULL.

O número de colunas especificadas em **szKey** pode não exceder o valor de JET_ccolKeyMost **(uma** constante dependente de versão).

Pelo menos uma coluna deve ser nomeada **em szKey**.

Comportamento obsoleto: após o terminador double-NULL, é possível especificar uma ID de idioma (um WORD que é passado para MAKELCID( langid, SORT_DEFAULT ) ) como uma maneira de especificar o LCID para o índice. É ilegal especificar uma ID de idioma em **szKey** e uma LCID no [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (definindo JET_bitIndexUnicode em *grbit*).

Preterido: após a ID de idioma, é possível passar **cbVarSegMac** como um USHORT. O comportamento será indefinido se o USHORT for definido em **szKey** e se **cbVarSegMac** estiver definido na estrutura.

**cbKey**

O comprimento, em bytes, de **szKey,** incluindo os dois nulos de terminação.

**grbit**

Um grupo de bits que inclui zero ou mais dos valores listados na tabela a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitIndexUnique</p> | <p>Entradas de índice duplicadas (chaves) não são permitidas. Isso é imposto quando <a href="gg269288(v=exchg.10).md">JetUpdate</a> é chamado, não quando <a href="gg294137(v=exchg.10).md">JetSetColumn</a> é chamado.</p> | 
| <p>JET_bitIndexPrimary</p> | <p>O índice é um índice primário (clusterado). Cada tabela deve ter exatamente um índice primário. Se nenhum índice primário for definido explicitamente em uma tabela, o mecanismo de banco de dados criará seu próprio índice primário.</p> | 
| <p>JET_bitIndexDisallowNull</p> | <p>Nenhuma das colunas sobre as quais o índice é criado pode conter um <strong>valor NULL.</strong></p> | 
| <p>JET_bitIndexIgnoreNull</p> | <p>Não adicione uma entrada de índice para uma linha se todas as colunas que estão sendo indexadas são <strong>NULL.</strong></p> | 
| <p>JET_bitIndexIgnoreAnyNull</p> | <p>Não adicione uma entrada de índice para uma linha se qualquer uma das colunas que está sendo indexada for <strong>NULL.</strong></p> | 
| <p>JET_bitIndexIgnoreFirstNull</p> | <p>Não adicione uma entrada de índice para uma linha se a primeira coluna que está sendo indexada for <strong>NULL.</strong></p> | 
| <p>JET_bitIndexLazyFlush</p> | <p>As operações de índice serão registradas de forma descomplicada.</p><p>JET_bitIndexLazyFlush não afeta a disposição das atualizações de dados. Se a operação de indexação for interrompida pelo encerramento do processo, a Recuperação Suave ainda poderá fazer com que o banco de dados tenha um estado consistente, mas o índice pode não estar presente.</p> | 
| <p>JET_bitIndexEmpty</p> | <p>Não tente criar o índice, pois todas as entradas serão avaliadas como <strong>NULL.</strong> <strong>grbit</strong> também deve especificar JET_bitIgnoreAnyNull quando JET_bitIndexEmpty é passado. Esse é um aprimoramento de desempenho. Por exemplo, se uma nova coluna for adicionada a uma tabela, um índice será criado nessa coluna recém-adicionada e todos os registros na tabela serão verificados, mesmo que não sejam adicionados ao índice. Especificar JET_bitIndexEmpty ignora a verificação da tabela, o que pode levar muito tempo.</p> | 
| <p>JET_bitIndexUnversioned</p> | <p>Faz com que a criação do índice seja visível para outras transações. Normalmente, uma sessão em uma transação não poderá ver uma operação de criação de índice em outra sessão. Esse sinalizador poderá ser útil se outra transação tiver a probabilidade de criar o mesmo índice. A segunda criação de índice falhará em vez de potencialmente causar muitas operações desnecessárias de banco de dados. A segunda transação pode não ser capaz de usar o índice imediatamente. A operação de criação de índice precisa ser concluída antes de ser acessível. No momento, a sessão não deve estar em uma transação para criar um índice sem informações de versão.</p> | 
| <p>JET_bitIndexSortNullsHigh</p> | <p>Especificar esse sinalizador faz com <strong>que os valores NULL</strong> sejam classificação após os dados de todas as colunas no índice.</p> | 
| <p>JET_bitIndexUnicode</p> | <p>Especificar esse sinalizador afeta a interpretação do campo de união lcid/pidxunicde na estrutura. Definir o bit significa que o <strong>campo pidxunicode</strong> realmente aponta para uma <a href="gg294097(v=exchg.10).md">estrutura JET_UNICODEINDEX</a> dados. JET_bitIndexUnicode não é necessário para indexar dados Unicode. Ele só é usado para personalizar a normalização de dados Unicode.</p> | 
| <p>JET_bitIndexTuples</p> | <p>Especifica que o índice é um índice de tupla. Consulte <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> uma descrição de um índice de tupla.</p><p>JET_bitIndexTuples foi introduzido no sistema operacional Windows XP.</p> | 
| <p>JET_bitIndexTupleLimits</p> | <p>Especificar esse sinalizador afeta a interpretação do campo de união <strong>cbVarSegMac/ptuplelimits</strong> na estrutura. Definir esse bit significa que o <strong>campo ptuplelimits</strong> realmente aponta para uma estrutura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para permitir limites de índice de tupla personalizados (implica JET_bitIndexTuples).</p><p>JET_bitIndexTupleLimits foi introduzido no sistema operacional Windows Server 2003.</p> | 
| <p>JET_bitIndexCrossProduct 0x00004000</p> | <p>Especificar esse sinalizador para um índice que tem mais de uma coluna de chave que é uma coluna de vários valores resultará na criação de uma entrada de índice para cada resultado de um produto cruzado de todos os valores nessas colunas de chave. Caso contrário, o índice teria apenas uma entrada para cada multivalor na coluna de chave mais significativa que é uma coluna de vários valores e cada uma dessas entradas de índice usaria o primeiro multivalor de qualquer outra coluna de chave que são colunas com vários valores.</p><p>Por exemplo, se você especificou esse sinalizador para um índice sobre a coluna A que tem os valores "vermelho" e "azul" e sobre a coluna B que tem os valores "1" e "2", as seguintes entradas de índice serão criadas: "red", "1"; "red", "2"; "blue", "1"; "blue", "2". Caso contrário, as seguintes entradas de índice seriam criadas: "red", "1"; "blue", "1".</p><p>JET_bitIndexCrossProduct foi introduzido no sistema operacional Windows Vista.</p> | 
| <p>JET_bitIndexKeyMost 0x00008000</p> | <p>Especificar esse sinalizador fará com que o índice use o tamanho máximo da chave especificado no <strong>campo cbKeyMost</strong> na estrutura. Caso contrário, o índice usará JET_cbKeyMost (255) como seu tamanho máximo de chave.</p><p>JET_bitIndexKeyMost foi introduzido no Windows Vista.</p> | 
| <p>JET_bitIndexDisallowTruncation 0x00010000</p> | <p>Especificar esse sinalizador fará com que qualquer atualização no índice que resulte em uma chave truncada falhe com JET_errKeyTruncated. Caso contrário, as chaves serão silenciosamente truncadas. Para obter mais informações sobre truncamento de chave, consulte a <a href="gg269329(v=exchg.10).md">função JetMakeKey.</a></p><p><strong>Windows Vista: JET_bitIndexDisallowTruncation</strong> é introduzido no Windows Vista.</p> | 
| <p>JET_bitIndexNestedTable 0x00020000</p> | <p>Especificar esse sinalizador fará com que o índice seja atualizado em várias colunas de vários valores, mas apenas com valores do mesmo <strong>itagSequence</strong>.</p><p>o JET_bitIndexNestedTable foi introduzido no Windows Vista.</p> | 



**ulDensity**

A densidade percentual da árvore inicial do índice B +. A especificação de um número menor que 100 usa mais espaço para criar o índice inicialmente, mas permite que o crescimento futuro do índice esteja em vigor, evitando, assim, a fragmentação interna.

**lcid**

O LCID (identificador de localidade) a ser usado ao normalizar os dados quando o valor de JET_bitIndexUnicode não for especificado no parâmetro *grbit* . O LCID afetará a normalização se o índice estiver sobre colunas Unicode.

**pidxunicode**

Um ponteiro para uma estrutura de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) se o valor de JET_bitIndexUnicode for especificado no parâmetro *grbit* . Isso permite que o usuário especifique sinalizadores personalizados que são passados para a função [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) durante a normalização Unicode.

**cbVarSegMac**

O comprimento máximo, em bytes, de cada coluna a ser armazenada no índice quando o valor de JET_bitIndexTupleLimits não é especificado no parâmetro *grbit* .

A especificação de um valor de 0 (zero) para esse campo é equivalente a:

  - Especificando JET_cbPrimaryKeyMost para um índice primário.

  - Especificando JET_cbSecondaryKeyMost para um índice secundário.

**ptuplelimits**

Um ponteiro para uma estrutura de [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) se o valor de JET_bitIndexTupleLimits for especificado no parâmetro *grbit* .

o ptuplelimits foi introduzido no Windows Server 2003.

**rgconditionalcolumn**

Um parâmetro opcional para uma matriz de estruturas [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) , que são usadas para especificar as colunas condicionais no índice.

**cConditionalColumn**

A contagem de estruturas na matriz **rgconditionalcolumn** .

**erra**

Contém o código de retorno para a criação deste índice.

**cbKeyMost**

Especifica o tamanho máximo permitido, em bytes, para chaves no índice. Esse parâmetro será ignorado se o valor de JET_bitIndexKeyMost não for especificado no parâmetro *grbit* . Se esse parâmetro for definido como zero e JET_bitIndexKeyMost for especificado no parâmetro *grbit* , a função de chamada falhará com JET_err_InvalidDef.

O tamanho mínimo de chave máximo suportado é JET_cbKeyMostMin (255), que é o tamanho de chave máximo herdado.

O tamanho máximo da chave depende do tamanho da página do banco de dados (JET_paramDatabasePageSize), da seguinte maneira:

  - Se JET_paramDatabasePageSize = 2048, então JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)

  - Se JET_paramDatabasePageSize = 4096, então JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)

  - Se JET_paramDatabasePageSize = 8192, então JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)

O tamanho máximo de chave com suporte para a instância também pode ser lido a partir do parâmetro do sistema JET_paramKeyMost.

o **cbKeyMost** foi introduzido no Windows Vista.

### <a name="remarks"></a>Comentários

O ESE dá suporte à indexação em colunas de chave que contêm vários valores. Para usar esse recurso, a coluna deve ser um tipo de coluna marcado (JET_bitColumnTagged) e deve ser sinalizada para ter vários valores indexados com JET_bitColumnMultiValued. em versões do Windows anteriores ao Windows Vista, somente a primeira coluna de chave com valores de várias valores no índice terá os respectivos valor expandido no índice. Todas as outras colunas com e sem valores terão apenas seus primeiros valores expandidos no índice.

Supondo que as linhas a seguir existam em uma tabela (a coluna Alpha não tem valores de multivalor, enquanto as colunas beta, gama e Delta têm valores de multivalor) e um índice é criado como "+ alfa \\ 0 + beta \\ 0 + gama \\ 0 + Delta \\ 0 \\ 0":


| <p>Alpha</p> | <p>Beta</p> | <p>Gama</p> | <p>Delta</p> | 
|--------------|-------------|--------------|--------------|
| <p>1</p> | <p>ABC<br />GHI<br />JKL</p> | <p>MNO<br />PQR<br />STU</p> | <p>VWX<br />YZ</p> | 
| <p>2</p> | <p>DOS</p> | <p>CHUVA<br />ESPANHA</p> | <p>IN<br />QUADRA</p> | 



O índice de queda-tuplas serão armazenadas:

{1, ABC, MNO, VWX}  
{1, GHI, MNO, VWX}  
{1, JKL, MNO, VWX}  
{2, A, CHUVA, IN}

Observe que {2, a, Espanha, IN} não é armazenada, mesmo que a coluna alfa na segunda linha tenha um único valores.

em versões do Windows a partir do Windows Vista, todas as colunas com valores de multivalor podem ser expandidas no índice especificando JET_bitIndexCrossProduct.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_ INDEXCREATE_W</strong> (Unicode) e <strong>JET_ INDEXCREATE_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte também

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
