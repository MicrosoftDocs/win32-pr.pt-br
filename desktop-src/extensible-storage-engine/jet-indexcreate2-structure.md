---
description: 'Saiba mais sobre: estrutura de JET_INDEXCREATE2'
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
ms.openlocfilehash: ac0d9a40e159a8aa5054228d18e431cee8d0319f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922948"
---
# <a name="jet_indexcreate2-structure"></a>Estrutura JET_INDEXCREATE2


_**Aplica-se a:** Windows | Windows Server_

A estrutura de **JET_INDEXCREATE2** contém as informações necessárias para criar um índice sobre os dados em um mecanismo de armazenamento extensível (ESE). A estrutura é usada por funções como [JetCreateIndex2](./jetcreateindex2-function.md)e em estruturas como [JET_TABLECREATE](./jet-tablecreate-structure.md) e [JET_TABLECREATE2](./jet-tablecreate2-structure.md).

A estrutura de **JET_INDEXCREATE2** foi introduzida no sistema operacional Windows 7.

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

**cbStruct**

O tamanho, em bytes, dessa estrutura. Defina este membro como sizeof (JET_INDEXCREATE2).

**szIndexName**

O nome do índice a ser criado.

O nome deve atender às seguintes condições:

  - Deve ser menor que JET_cbNameMost, não incluindo o nulo de terminação.

  - Ele deve consistir no seguinte conjunto de caracteres: 0 (zero) a 9, A a Z, a a z e todas as outras pontuações, exceto para " \! " (ponto de exclamação), "," (vírgula), " \[ " (colchete de abertura) e " \] " (colchete de fechamento) — ou seja, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c e 0x5d até 0x7F.

  - Ele não deve começar com um espaço.

  - Ele deve conter pelo menos um caractere que não seja de espaço.

**szKey**

Um ponteiro para uma cadeia de caracteres com terminação de nulo duplo de tokens delimitados por nulo.

Cada token tem o formato " \<direction-specifier\> \<column-name\> ", onde a especificação de direção é "+" ou "-". Por exemplo, um **szKey** de "+ ABC \\ 0-Def \\ 0 + GHI \\ 0" irá indexar as três colunas "ABC" (em ordem crescente), "def" (em ordem decrescente) e "GHI" (em ordem crescente). Na linguagem C, os literais de cadeia de caracteres têm um terminador **NULL** implícito, portanto, a cadeia de caracteres acima será encerrada por um duplo nulo.

O número de colunas especificado em **szKey** não deve exceder JET_ccolKeyMost (uma constante dependente de versão).

Pelo menos uma coluna deve ser nomeada em **szKey**.

Comportamento obsoleto: após o terminador de nulo duplo, é possível especificar uma ID de idioma (uma palavra que é passada em MAKELCID (LangID, SORT_DEFAULT)) como uma maneira de especificar o LCID para o índice. É ilegal especificar uma ID de idioma em **szKey** e um LCID em [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (definindo JET_bitIndexUnicode em *grbit*).

Preterido: após a ID do idioma, é possível passar **cbVarSegMac** como um tipo de dados **UShort** . O comportamento será indefinido se USHORT estiver definido em **szKey** e se **cbVarSegMac** for definido na estrutura.

**cbKey**

O comprimento, em bytes, de **szKey**, incluindo os dois nulos de terminação.

**grbit**

Um grupo de bits que contém zero ou mais das opções de valor listadas na tabela a seguir.

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
<td><p>JET_bitIndexUnique</p></td>
<td><p>Entradas de índice duplicadas (chaves) não são permitidas. Isso é imposto quando <a href="gg269288(v=exchg.10).md">JetUpdate</a> é chamado, não quando <a href="gg294137(v=exchg.10).md">JetSetColumn</a> é chamado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexPrimary</p></td>
<td><p>O índice é um índice primário (clusterizado). Cada tabela deve ter exatamente um índice primário. Se nenhum índice primário for explicitamente definido em uma tabela, o mecanismo de banco de dados criará seu próprio índice primário.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexDisallowNull</p></td>
<td><p>Nenhuma das colunas sobre as quais o índice é criado pode conter um valor <strong>nulo</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexIgnoreNull</p></td>
<td><p>Não adicione uma entrada de índice para uma linha se todas as colunas que estão sendo indexadas forem <strong>nulas</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexIgnoreAnyNull</p></td>
<td><p>Não adicione uma entrada de índice para uma linha se qualquer uma das colunas que estão sendo indexadas for <strong>nula</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexIgnoreFirstNull</p></td>
<td><p>Não adicione uma entrada de índice para uma linha se a primeira coluna que está sendo indexada for <strong>nula</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexLazyFlush</p></td>
<td><p>Especifica que as operações de índice serão registradas lentamente.</p>
<p>JET_bitIndexLazyFlush não afeta a ociosa das atualizações de dados. Se a operação de indexação for interrompida pelo encerramento do processo, a recuperação simples ainda poderá obter o banco de dados para um estado consistente, mas o índice poderá não estar presente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexEmpty</p></td>
<td><p>Não tente Compilar o índice, pois todas as entradas seriam avaliadas como <strong>nulas</strong>. <strong>grbit</strong> Também é necessário especificar JET_bitIgnoreAnyNull quando JET_bitIndexEmpty é passado. Esse é um aprimoramento de desempenho. Por exemplo, se uma nova coluna for adicionada a uma tabela e um índice for criado nessa coluna recém-adicionada, todos os registros na tabela serão verificados, mesmo que não sejam adicionados ao índice. Especificar JET_bitIndexEmpty ignora a verificação da tabela, o que pode levar muito tempo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexUnversioned</p></td>
<td><p>JET_bitIndexUnversioned faz com que a criação do índice seja visível para outras transações. Normalmente, uma sessão em uma transação não poderá ver uma operação de criação de índice em outra sessão. Esse sinalizador pode ser útil se outra transação provavelmente criar o mesmo índice. O segundo índice-Create simplesmente falhará em vez de causar muitas operações desnecessárias de banco de dados. A segunda transação pode não ser capaz de usar o índice imediatamente. A operação de criação de índice deve ser concluída antes de ser utilizável. A sessão não deve estar em uma transação no momento para criar um índice sem informações de versão.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexSortNullsHigh</p></td>
<td><p>A especificação desse sinalizador faz com que valores <strong>nulos</strong> sejam classificados após os dados de todas as colunas no índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexUnicode</p></td>
<td><p>A especificação desse sinalizador afeta a interpretação do campo de União LCID/pidxunicde na estrutura. Definir o bit significa que o campo pidxunicode realmente aponta para uma estrutura de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> . Não é necessário JET_bitIndexUnicode para indexar dados Unicode. Só é necessário personalizar a normalização de dados Unicode.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexTuples</p></td>
<td><p>Especifica que o índice é um índice de tupla. Consulte <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para obter uma descrição de um índice de tupla.</p>
<p>O valor de JET_bitIndexTuples foi introduzido no sistema operacional Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexTupleLimits</p></td>
<td><p>A especificação desse sinalizador afeta a interpretação do campo de União <strong>cbVarSegMac/ptuplelimits</strong> na estrutura. Definir esse bit significa que o campo <strong>ptuplelimits</strong> realmente aponta para uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> para permitir limites de índice de tupla personalizados (implica JET_bitIndexTuples).</p>
<p>O valor de <strong>JET_bitIndexTupleLimits</strong> foi introduzido no sistema operacional Windows Server 2003.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexCrossProduct<br />
0x00004000</p></td>
<td><p>A especificação desse sinalizador para um índice que tenha mais de uma coluna de chave que seja uma coluna de vários valores resultará na criação de uma entrada de índice para cada resultado de um produto cruzado de todos os valores nessas colunas de chave. Caso contrário, o índice teria apenas uma entrada para cada vários valores na coluna de chave mais significativa, que é uma coluna com vários valores, e cada uma dessas entradas de índice usaria os primeiros valores de outras colunas de chave que são colunas com valores múltiplos.</p>
<p>Por exemplo, se você tiver especificado esse sinalizador para um índice na coluna A que tem os valores de &quot; vermelho &quot; e &quot; azul &quot; e sobre a coluna B que tem os valores &quot; 1 &quot; e &quot; 2 &quot; , as seguintes entradas de índice serão criadas: &quot; vermelho &quot; , &quot; 1 &quot; ; &quot; vermelho &quot; , &quot; 2 &quot; ; &quot; azul &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 2 &quot; . Caso contrário, as seguintes entradas de índice seriam criadas: &quot; vermelho &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 1 &quot; .</p>
<p>O valor <strong>JET_bitIndexCrossProduct</strong> foi introduzido no Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexKeyMost<br />
0x00008000</p></td>
<td><p>A especificação desse sinalizador fará com que o índice use o tamanho máximo de chave especificado no campo <strong>cbKeyMost</strong> na estrutura. Caso contrário, o índice usará JET_cbKeyMost (255) como o tamanho máximo da chave.</p>
<p>O valor <strong>JET_bitIndexKeyMost</strong> foi introduzido no Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexDisallowTruncation<br />
0x00010000</p></td>
<td><p>A especificação desse sinalizador causará a falha de qualquer atualização no índice que resultaria em uma chave truncada com o código de resposta JET_errKeyTruncated. Caso contrário, as chaves serão truncadas silenciosamente. Para obter mais informações sobre o truncamento de chave, consulte <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</p>
<p>O valor <strong>JET_bitIndexDisallowTruncation</strong> foi introduzido no Windows Vista.</p></td>
</tr>
</tbody>
</table>


**ulDensity**

A densidade percentual da árvore inicial do índice B +. A especificação de um número menor que 100 usa mais espaço para criar o índice inicialmente, mas permite que o crescimento futuro do índice esteja em vigor, evitando, assim, a fragmentação interna.

**lcid**

O LCID (identificador de localidade) a ser usado ao normalizar os dados quando o valor de JET_bitIndexUnicode não for especificado no parâmetro *grbit* . O LCID afetará a normalização se o índice estiver sobre colunas Unicode.

**pidxunicode**

Um ponteiro para uma estrutura de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) se o valor de JET_bitIndexUnicode for especificado no parâmetro *grbit* . Isso permite que o usuário especifique sinalizadores personalizados que são passados para a função [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) durante a normalização Unicode.

**cbVarSegMac**

O comprimento máximo, em bytes, de cada coluna a ser armazenada no índice quando o valor de JET_bitIndexTupleLimits não é especificado no parâmetro *grbit* .

A especificação de um valor de 0 (zero) para esse campo é equivalente à seguinte:

  - Especificando JET_cbPrimaryKeyMost para um índice primário.

  - Especificando JET_cbSecondaryKeyMost para um índice secundário.

**ptuplelimits**

Um ponteiro para uma estrutura de [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) se o valor de JET_bitIndexTupleLimits for especificado no parâmetro *grbit* .

o **ptuplelimits** foi introduzido no Windows Server 2003.

**rgconditionalcolumn**

Um parâmetro opcional para uma matriz de estruturas [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) , que são usadas para especificar as colunas condicionais no índice.

**cConditionalColumn**

A contagem de estruturas na matriz **rgconditionalcolumn** .

**erra**

Contém o código de retorno para a criação deste índice.

**cbKeyMost**

Especifica o tamanho máximo permitido, em bytes, para chaves no índice. Esse parâmetro será ignorado se JET_bitIndexKeyMost não for especificado no parâmetro *grbit* . Se esse parâmetro for definido como zero e JET_bitIndexKeyMost for especificado no membro *grbit* , a função de chamada falhará com JET_err_InvalidDef.

O tamanho mínimo de chave máximo suportado é JET_cbKeyMostMin (255), que é o tamanho de chave máximo herdado.

O tamanho máximo da chave depende do tamanho da página do banco de dados (JET_paramDatabasePageSize) da seguinte maneira:

  - Se JET_paramDatabasePageSize = 2048, então JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)

  - Se JET_paramDatabasePageSize = 4096, então JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)

  - Se JET_paramDatabasePageSize = 8192, então JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)

O tamanho máximo de chave com suporte para a instância também pode ser lido a partir do parâmetro do sistema JET_paramKeyMost.

o **cbKeyMost** foi introduzido no Windows Vista.

**pSpacehints**

Um ponteiro para uma estrutura de [JET_SPACEHINTS](./jet-spacehints-structure.md) .

o **pSpacehints** foi introduzido no Windows 7.

### <a name="remarks"></a>Comentários

O ESE dá suporte à indexação em colunas de chave que contêm vários valores. Para usar esse recurso, a coluna deve ser um tipo de coluna marcado (JET_bitColumnTagged) e deve ser sinalizada para ter vários valores indexados com JET_bitColumnMultiValued. Em versões do Windows anteriores ao Windows Vista, somente a primeira coluna de chave com valores de várias valores no índice terá os respectivos valor expandido no índice. Todas as outras colunas com e sem valores terão apenas seus primeiros valores expandidos no índice.

Supondo que as linhas a seguir existam em uma tabela (a coluna Alpha não tem valores de multivalor, enquanto as colunas beta, gama e Delta têm valores de multivalor) e um índice é criado como "+ alfa \\ 0 + beta \\ 0 + gama \\ 0 + Delta \\ 0 \\ 0":

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Alpha</p></th>
<th><p>Beta</p></th>
<th><p>Gama</p></th>
<th><p>Delta</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>ABC<br />
GHI<br />
JKL</p></td>
<td><p>MNO<br />
PQR<br />
STU</p></td>
<td><p>VWX<br />
YZ</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>DOS</p></td>
<td><p>REDUNDANT<br />
Espanha</p></td>
<td><p>IN<br />
QUADRA</p></td>
</tr>
</tbody>
</table>


As tuplas de índice a seguir serão armazenadas:

{1, ABC, MNO, VWX}  
{1, GHI, MNO, VWX}  
{1, JKL, MNO, VWX}  
{2, A, CHUVA, IN}

Observe que {2, a, Espanha, IN} não é armazenada, mesmo que a coluna alfa na segunda linha tenha um único valores.

Em versões do Windows a partir do Windows Vista, todas as colunas com valores de multivalor podem ser expandidas no índice, especificando JET_bitIndexCrossProduct.

### <a name="requirements"></a>Requisitos

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
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JET_ INDEXCREATE2_W</strong> (Unicode) e <strong>JET_ INDEXCREATE2_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
