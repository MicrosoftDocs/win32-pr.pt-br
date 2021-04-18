---
title: Sintaxe do filtro de pesquisa
description: Os filtros de pesquisa permitem que você defina critérios de pesquisa e forneça pesquisas mais eficientes e eficazes.
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- ADSI de sintaxe de filtro de pesquisa
- consultas, sintaxe de filtro de pesquisa
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 28875bd49a3d1df7418c37706e58852066bbe08a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105762841"
---
# <a name="search-filter-syntax"></a>Sintaxe do filtro de pesquisa

Os filtros de pesquisa permitem que você defina critérios de pesquisa e forneça pesquisas mais eficientes e eficazes.

A ADSI dá suporte aos filtros de pesquisa LDAP, conforme definido em RFC2254. Esses filtros de pesquisa são representados por cadeias de caracteres Unicode. A tabela a seguir lista alguns exemplos de filtros de pesquisa LDAP.



| Filtro de pesquisa                                                               | Descrição                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| "(objectClass = \* )"                                                          | Todos os objetos.                                               |
| "(& (objectCategory = Person) (objectClass = user) (! ( CN = Andy))) "                  | Todos os objetos de usuário, mas "Andy".                               |
| "(SN = SM \* )"                                                                 | Todos os objetos com um sobrenome que começa com "SM".          |
| "(& (objectCategory = Person) (objectClass = Contact) ( \| (SN = Smith) (SN = Johnson))" | Todos os contatos com um sobrenome igual a "Smith" ou "Johnson". |



 

Esses filtros de pesquisa usam um dos formatos a seguir.


```C++
<filter>=(<attribute><operator><value>)
```



ou


```C++
(<operator><filter1><filter2>)
```



Os filtros de pesquisa do ADSI são usados de duas maneiras. Eles formam uma parte do dialeto LDAP para enviar consultas por meio do provedor de OLE DB. Eles também são usados com a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .

## <a name="operators"></a>Operadores

A tabela a seguir lista os operadores de filtro de pesquisa usados com frequência.



| Operador lógico | Descrição                                |
|------------------|--------------------------------------------|
| =                | Igual a                                   |
| ~=               | Aproximadamente igual a                     |
| <=            | Modo lexicográfico menor ou igual a    |
| >=            | Modo lexicográfico maior ou igual a |
| &                | AND                                        |
| \|               | OU                                         |
| !                | NOT                                        |



 

Além dos operadores acima, o LDAP define dois OIDs (identificadores de objeto de regra) correspondentes que podem ser usados para executar comparações de valores numéricos. As regras de correspondência têm a seguinte sintaxe.


```C++
<attribute name>:<matching rule OID>:=<value>
```



" &lt; nome do atributo &gt; " é o **lDAPDisplayName** do atributo, " &lt; OID da regra &gt; " é o OID da regra de correspondência e " &lt; valor &gt; " é o valor a ser usado para comparação. Lembre-se de que os espaços não podem ser usados nesta cadeia de caracteres. " &lt; Value &gt; " deve ser um número decimal; ele não pode ser um número hexadecimal ou um nome de constante, como a **\_ segurança de tipo de grupo ADS \_ \_ \_ habilitada**. Para obter mais informações sobre os atributos de Active Directory disponíveis, consulte [todos os atributos](/windows/desktop/ADSchema/attributes-all).

A tabela a seguir lista os OIDs de regra de correspondência implementados pelo LDAP.



| OID da regra de correspondência       | Identificador de cadeia de caracteres (de Ntldap. h)   | Descrição                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.2.840.113556.1.4.803  | **\_ \_ \_ bit de regra de correspondência LDAP \_ e**  | Uma correspondência será encontrada somente se todos os bits do atributo corresponderem ao valor. Essa regra é equivalente a um operador **and** bit a bit.                                                                  |
| 1.2.840.113556.1.4.804  | **\_ \_ \_ bit de regra de correspondência LDAP \_ ou**   | Uma correspondência será encontrada se qualquer um dos bits do atributo corresponder ao valor. Essa regra é equivalente a **um operador OR**                                                                        |
| 1.2.840.113556.1.4.1941 | **\_ \_ regra de correspondência LDAP \_ na \_ cadeia** | Essa regra é limitada a filtros que se aplicam ao DN. Esse é um operador de correspondência "estendida" especial que percorre a cadeia de ancestrais em objetos até a raiz até encontrar uma correspondência. |



 

O exemplo de cadeia de caracteres de consulta a seguir procura objetos de grupo que têm o sinalizador de **\_ segurança de tipo de grupo ADS \_ \_ \_ habilitado** definido. Lembre-se de que o valor decimal do **\_ tipo de grupo ADS \_ \_ segurança \_ habilitado** (0x80000000 = 2147483648) é usado para o valor de comparação.


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



A **\_ regra de correspondência LDAP \_ \_ na \_ cadeia** é um OID de regra de correspondência projetado para fornecer um método para pesquisar o ancestrais de um objeto. Muitos aplicativos que usam o AD e o AD LDS geralmente funcionam com dados hierárquicos, que são ordenados por relações pai-filho. Anteriormente, os aplicativos executaram a expansão de grupo transitiva para descobrir a associação de grupo, que usava muita largura de banda de rede; os aplicativos precisavam fazer várias viagens de ida e volta para descobrir se um objeto ficou "na cadeia" se um link for percorrido até o final.

Um exemplo de tal consulta é um projetado para verificar se um usuário "Usuário1" é membro do grupo "grupo1". Você definiria a base para o DN de usuário `(cn=user1, cn=users, dc=x)` e o escopo como e `base` usará a consulta a seguir.


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



Da mesma forma, para localizar todos os grupos dos quais "Usuário1" é um membro, defina a base como o DN do contêiner de grupos; por exemplo `(OU=groupsOU, dc=x)` , e o escopo para `subtree` , e use o filtro a seguir.


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



Observe que, ao usar a **\_ \_ regra de correspondência LDAP \_ na \_ cadeia**, o escopo não é limitado — pode ser `base` , `one-level` ou `subtree` . Algumas dessas consultas em subárvores podem ser mais intensivas no processador, como links de caça com um alto Fan-out; ou seja, listando todos os grupos dos quais um usuário é membro. Pesquisas ineficientes registrarão as mensagens de log de eventos apropriadas, assim como com qualquer outro tipo de consulta.

## <a name="wildcards"></a>Curingas

Você também pode adicionar curingas e condições a um filtro de pesquisa LDAP. Os exemplos a seguir mostram subcadeias de caracteres que podem ser usadas para pesquisar o diretório.

Obter todas as entradas:


```C++
(objectClass=*)
```



Obter entradas contendo "Bob" em algum lugar no nome comum:


```C++
(cn=*bob*)
```



Obter entradas com um nome comum maior ou igual a "Bob":


```C++
(cn>='bob')
```



Obter todos os usuários com um atributo de email:


```C++
(&(objectClass=user)(email=*))
```



Obter todas as entradas de usuário com um atributo de email e um sobrenome igual a "Smith":


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



Obtenha todas as entradas de usuário com um nome comum que comece com "Andy", "Steve" ou "Margaret":


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



Obter todas as entradas sem um atributo de email:


```C++
(!(email=*))
```



A definição formal do filtro de pesquisa é a seguinte (da [RFC 2254](https://tools.ietf.org/html/rfc2254)):


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



O símbolo &lt; attr &gt; é uma cadeia de caracteres que representa um attributeType. O valor do token &lt; &gt; é uma cadeia de caracteres que representa um AttributeValue cujo formato é definido pelo serviço de diretório subjacente.

Se um &lt; valor &gt; precisar conter o caractere asterisco ( \* ), parêntese esquerdo (() ou parêntese direito ()), o caractere deverá ser precedido pelo caractere de escape de barra invertida ( \\ ).

## <a name="special-characters"></a>Caracteres Especiais

Se qualquer um dos seguintes caracteres especiais precisar aparecer no filtro de pesquisa como literais, eles deverão ser substituídos pela sequência de escape listada.



| Caractere ASCII | Sequência de escape substituída |
|-----------------|----------------------------|
| \*              | \\2a                       |
| (               | \\38                       |
| )               | \\29                       |
| \\              | \\5C                       |
| NUL             | \\00                       |
| /               | \\2F                       |



 

> [!Note]  
> Nos casos em que um conjunto de caracteres MultiByte está sendo usado, as sequências de escape listadas acima devem ser usadas se a pesquisa for executada pelo ADO com o dialeto SQL.

 

Além disso, dados binários arbitrários podem ser representados usando a sintaxe da sequência de escape codificando cada byte de dados binários com a barra invertida ( \\ ) seguida de dois dígitos hexadecimais. Por exemplo, o valor de quatro bytes 0x00000004 é codificado como \\ 00 \\ 00 \\ 00 \\ 04 em uma cadeia de caracteres de filtro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dialeto LDAP](ldap-dialect.md)
</dt> <dt>

[Dialeto SQL](sql-dialect.md)
</dt> <dt>

[Pesquisando com a interface IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Pesquisando com OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 
