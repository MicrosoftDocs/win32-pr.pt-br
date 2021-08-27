---
title: Sintaxe de filtro de pesquisa
description: Os filtros de pesquisa permitem definir critérios de pesquisa e fornecer pesquisas mais eficientes e eficazes.
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- ADSI de sintaxe de filtro de pesquisa
- consultas, sintaxe de filtro de pesquisa
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 9ea6b347da1c840ef6bd1dd32bb32f96e7be86dfb93e6c1e71cdbb06bd52ba97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005486"
---
# <a name="search-filter-syntax"></a>Sintaxe de filtro de pesquisa

Os filtros de pesquisa permitem definir critérios de pesquisa e fornecer pesquisas mais eficientes e eficazes.

O ADSI dá suporte aos filtros de pesquisa LDAP conforme definido em RFC2254. Esses filtros de pesquisa são representados por cadeias de caracteres Unicode. A tabela a seguir lista alguns exemplos de filtros de pesquisa LDAP.



| Filtro de pesquisa                                                               | Descrição                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| "(objectClass= \* )"                                                          | Todos os objetos.                                               |
| "(&(objectCategory=person)(objectClass=user)(!( cn=andy)))"                  | Todos os objetos de usuário, menos "paulo".                               |
| "(sn=sm \* )"                                                                 | Todos os objetos com um sobrenome que começa com "sm".          |
| "(&(objectCategory=person)(objectClass=contact)( \| (sn=Smith)(sn=Johnson)))" | Todos os contatos com um sobrenome igual a "Smith" ou "Smith". |



 

Esses filtros de pesquisa usam um dos seguintes formatos.


```C++
<filter>=(<attribute><operator><value>)
```



ou


```C++
(<operator><filter1><filter2>)
```



Os filtros de pesquisa ADSI são usados de duas maneiras. Eles fazem parte do dialeto LDAP para enviar consultas por meio do provedor OLE DB dados. Eles também são usados com a interface [**IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

## <a name="operators"></a>Operadores

A tabela a seguir lista os operadores de filtro de pesquisa usados com frequência.



| Operador lógico | Descrição                                |
|------------------|--------------------------------------------|
| =                | Igual a                                   |
| ~=               | Aproximadamente igual a                     |
| <=            | Lexicograficamente menor ou igual a    |
| >=            | Lexicograficamente maior ou igual a |
| &                | AND                                        |
| \|               | OU                                         |
| !                | NOT                                        |



 

Além dos operadores acima, o LDAP define dois OIDs (identificadores de objeto de regra) correspondentes que podem ser usados para executar comparações bit a bit de valores numéricos. As regras de correspondência têm a sintaxe a seguir.


```C++
<attribute name>:<matching rule OID>:=<value>
```



" &lt; attribute name " é o &gt; **lDAPDisplayName** do atributo , " rule OID " é o OID para a regra de correspondência e " value " é o valor a ser usado para &lt; &gt; &lt; &gt; comparação. Esteja ciente de que os espaços não podem ser usados nesta cadeia de caracteres. " value " deve ser um número decimal; ele não pode ser um número hexadecimal ou um nome constante, como &lt; ADS GROUP TYPE SECURITY &gt; **\_ \_ \_ \_ ENABLED.** Para obter mais informações sobre os atributos disponíveis do Active Directory, consulte [Todos os atributos](/windows/desktop/ADSchema/attributes-all).

A tabela a seguir lista as OIDs de regra de correspondência implementadas pelo LDAP.



| OID da regra de correspondência       | Identificador de cadeia de caracteres (de Ntldap.h)   | Descrição                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.2.840.113556.1.4.803  | **BIT DE REGRA DE CORRESPONDÊNCIA LDAP \_ \_ \_ \_ E**  | Uma corresponder será encontrada somente se todos os bits do atributo corresponderem ao valor. Essa regra é equivalente a um operador **AND bit** a bit.                                                                  |
| 1.2.840.113556.1.4.804  | **BIT DE REGRA DE CORRESPONDÊNCIA LDAP \_ \_ \_ \_ OU**   | Uma combinação será encontrada se algum bits do atributo corresponderem ao valor. Essa regra é equivalente a um operador **OR bit** a bit.                                                                        |
| 1.2.840.113556.1.4.1941 | **REGRA DE CORRESPONDÊNCIA LDAP \_ \_ EM \_ \_ CADEIA** | Essa regra é limitada a filtros que se aplicam ao DN. Esse é um operador de combinação "estendido" especial que percorre a cadeia de ancestry em objetos até a raiz até encontrar uma combinação. |



 

A cadeia de caracteres de consulta de exemplo a seguir pesquisa objetos de grupo que têm o sinalizador **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** definido. Esteja ciente de que o valor decimal de **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** (0x80000000 = 2147483648) é usado para o valor de comparação.


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



A **REGRA DE CORRESPONDÊNCIA LDAP EM \_ \_ \_ \_ CADEIA** é uma OID de regra correspondente que foi projetada para fornecer um método para procurar a ancestry de um objeto. Muitos aplicativos que usam o AD e AD LDS geralmente funcionam com dados hierárquicos, que são ordenados por relações pai-filho. Anteriormente, os aplicativos realizavam a expansão transitiva do grupo para descobrir a associação de grupo, que usava muita largura de banda de rede; aplicativos necessários para fazer várias idas e voltas para descobrir se um objeto entrou "na cadeia" se um link for percorrido até o final.

Um exemplo dessa consulta foi projetado para verificar se um usuário "user1" é membro do grupo "group1". Você definiria a base para o DN do usuário `(cn=user1, cn=users, dc=x)` e o escopo como e usaria a consulta a `base` seguir.


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



Da mesma forma, para encontrar todos os grupos dos quais "user1" é membro, de definir a base para o contêiner de grupos DN; por `(OU=groupsOU, dc=x)` exemplo, e o escopo `subtree` para e use o filtro a seguir.


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



Observe que, ao usar **LDAP \_ MATCHING RULE IN \_ \_ \_ CHAIN**, o escopo não é limitado– pode ser `base` , ou `one-level` `subtree` . Algumas dessas consultas em subárvores podem ser mais intensivas no processador, como links de busca com um alto fan-out; ou seja, listando todos os grupos dos que um usuário é membro. Pesquisas ineficientes registrarão em log as mensagens de log de eventos apropriadas, assim como acontece com qualquer outro tipo de consulta.

## <a name="wildcards"></a>Curingas

Você também pode adicionar curingas e condições a um filtro de pesquisa LDAP. Os exemplos a seguir mostram substrings que podem ser usadas para pesquisar o diretório.

Obter todas as entradas:


```C++
(objectClass=*)
```



Obter entradas que contêm "bob" em algum lugar no nome comum:


```C++
(cn=*bob*)
```



Obter entradas com um nome comum maior ou igual a "bob":


```C++
(cn>='bob')
```



Obter todos os usuários com um atributo de email:


```C++
(&(objectClass=user)(email=*))
```



Obter todas as entradas de usuário com um atributo de email e um sobrenome igual a "smith":


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



Obter todas as entradas de usuário com um nome comum que começa com "paulo", "steve" ou "andy":


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



Obter todas as entradas sem um atributo de email:


```C++
(!(email=*))
```



A definição formal do filtro de pesquisa é a seguinte [(do RFC 2254](https://tools.ietf.org/html/rfc2254)):


```C++
<filter> ::= '(' <filtercomp> ')'
<filtercomp> ::= <and> | <or> | <not> | <item>
<and> ::= '&' <filterlist>
<or> ::= '|' <filterlist>
<not> ::= '!' <filter>
<filterlist> ::= <filter> | <filter> <filterlist>
<item>::= <simple> | <present> | <substring>
<simple> ::= <attr> <filtertype> <value><filtertype> ::= <equal> | <approx> | <ge> | <le>
<equal> ::= '='
<approx> ::= '~='
<ge> ::= '>='
<le> ::= '<='
<present> ::= <attr> '=*'
<substring> ::= <attr> '=' <initial> <any> <final>
<initial> ::= NULL | <value><any> ::= '*' <starval>
<starval> ::= NULL | <value>'*' <starval>
<final> ::= NULL | <value>
```



O token &lt; attr &gt; é uma cadeia de caracteres que representa um AttributeType. O valor do token é uma cadeia de caracteres que representa um AttributeValue cujo &lt; formato é definido pelo serviço de diretório &gt; subjacente.

Se um valor deve conter o caractere asterisco ( ), parêntese esquerdo &lt; &gt; ((), ou \* parêntese direito ()), o caractere deverá ser precedido pelo caractere de escape de invertida ( \\ ).

## <a name="special-characters"></a>Caracteres Especiais

Se qualquer um dos caracteres especiais a seguir deve aparecer no filtro de pesquisa como literais, eles devem ser substituídos pela sequência de escape listada.



| Caractere ASCII | Substituição de sequência de escape |
|-----------------|----------------------------|
| \*              | \\2a                       |
| (               | \\28                       |
| )               | \\29                       |
| \\              | \\5c                       |
| NUL             | \\00                       |
| /               | \\2f                       |



 

> [!Note]  
> Nos casos em que um Conjunto de Caracteres MultiByte está sendo usado, as sequências de escape listadas acima devem ser usadas se a pesquisa for executada pelo ADO com o dialeto SQL.

 

Além disso, dados binários arbitrários podem ser representados usando a sintaxe de sequência de escape codificando cada byte de dados binários com a barra invertida ( ) seguida por dois \\ dígitos hexadecimais. Por exemplo, o valor de quatro 0x00000004 é codificado como \\ 00 \\ 00 \\ 00 \\ 04 em uma cadeia de caracteres de filtro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dialeto LDAP](ldap-dialect.md)
</dt> <dt>

[SQL dialeto](sql-dialect.md)
</dt> <dt>

[Pesquisando com a interface IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Pesquisando com OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 
