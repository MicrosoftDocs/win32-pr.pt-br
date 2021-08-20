---
title: Criando um filtro de consulta
description: Um filtro de consulta instrui Active Directory Domain Services localizar dados em uma sintaxe de consulta LDAP. Todas as tecnologias de acesso a dados especificadas listadas no tópico escolhendo a tecnologia de pesquisa dão suporte à sintaxe de consulta LDAP.
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, criando um filtro de consulta
- filtros de consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5241cb288051515c1198c9979ef7d1a71d18524b3b2f3504f2b9141b6fb8a24c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020856"
---
# <a name="creating-a-query-filter"></a>Criando um filtro de consulta

Um filtro de consulta instrui Active Directory Domain Services localizar dados em uma sintaxe de consulta LDAP. Todas as tecnologias de acesso a dados especificadas listadas no tópico [escolhendo a tecnologia de pesquisa](choosing-the-search-technology.md) dão suporte à sintaxe de consulta LDAP.

A sintaxe de consulta LDAP é a seguinte:


```C++
<expression><expression>...
```



Um filtro pode conter uma ou mais expressões. Uma expressão tem o seguinte formato:


```C++
(<logicaloperator><comparison><comparison...>)
```



em que " &lt; LogicalOperator &gt; " é um dos seguintes.



| Operador        | Descrição                |
|-----------------|----------------------------|
| "\|"<br/> | **Or** lógico<br/>  |
| "&"<br/>  | **And** lógico<br/> |
| "!"<br/>  | **Não** lógico<br/> |



 

e " &lt; Comparison &gt; " é o seguinte:


```C++
(<attribute><operator><value>)
```



onde " &lt; Attribute &gt; " é o **lDAPDisplayName** do atributo a ser avaliado, " &lt; Value &gt; " é o valor a ser comparado e " &lt; Operator &gt; " é um dos operadores de comparação a seguir.



| Operador           | Descrição                         |
|--------------------|-------------------------------------|
| "="<br/>     | Igual a<br/>                   |
| "~="<br/>    | Aproximadamente é igual a<br/>     |
| "<="<br/> | Menor que ou igual a<br/>    |
| ">="<br/> | Maior ou igual a<br/> |



 

Além disso, dependendo da sintaxe do atributo, o " &lt; valor &gt; " pode conter o símbolo curinga (" \* "). Um " &lt; valor &gt; " que contém apenas um caractere curinga verificará a existência de qualquer valor em " &lt; Attribute &gt; ". Se nenhum valor for definido para " &lt; Attribute &gt; ", o teste falhará.

Se qualquer um dos seguintes caracteres especiais precisar aparecer no filtro de consulta como literais, eles deverão ser substituídos pela sequência de escape listada.



| Caractere ASCII    | Sequência de escape substituída |
|--------------------|----------------------------|
| \*<br/>      | " \\ 2a"<br/>          |
| (<br/>       | " \\ 28"<br/>          |
| )<br/>       | " \\ 29"<br/>          |
| \\<br/>      | " \\ 5C"<br/>          |
| **NUL**<br/> | " \\ 00"<br/>          |



 

Além disso, dados binários arbitrários podem ser representados usando a sintaxe da sequência de escape codificando cada byte de dados binários com a barra invertida seguida de dois dígitos hexadecimais. Por exemplo, o valor de quatro bytes 0x00000004 é codificado como " \\ 00 \\ 00 \\ 00 \\ 04" em uma cadeia de caracteres de filtro.

## <a name="examples"></a>Exemplos

A cadeia de caracteres de consulta a seguir pesquisará todos os objetos do tipo "computador".


```C++
(objectCategory=computer)
```



A cadeia de caracteres de consulta a seguir pesquisará todos os objetos do tipo "computador" com um nome que começa com "desktop".


```C++
(&(objectCategory=computer)(name=desktop*))
```



A cadeia de caracteres de consulta a seguir pesquisará todos os objetos do tipo "computador" com um nome que comece com "desktop" ou um nome que comece com "Notebook".


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



A cadeia de caracteres de consulta a seguir pesquisará todos os objetos do tipo "usuário" que têm um número de telefone residencial.


```C++
(&(objectCategory=user)(homePhone=*))
```



Para obter mais informações sobre cadeias de caracteres de filtro de consulta e exemplos de uso, consulte:

-   [Localizando objetos por classe](finding-objects-by-class.md)
-   [Localizando objetos por nome](finding-objects-by-name.md)
-   [Localizando uma lista de atributos a serem consultados](finding-a-list-of-attributes-to-query.md)
-   [Verificando a sintaxe do filtro de consulta](checking-the-query-filter-syntax.md)
-   [Como especificar valores de comparação](how-to-specify-comparison-values.md)

 

 





