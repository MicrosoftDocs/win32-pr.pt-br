---
description: Coloca uma instrução include C ou IDL no código gerado.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: Elemento literalInclude
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcfbd72300607dd2c6f3f21e4be3666083b559cb
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625312"
---
# <a name="literalinclude-element"></a>Elemento literalInclude

Coloca uma instrução include C ou IDL no código gerado.

## <a name="usage"></a>Uso

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Type</th>
<th>Obrigatório</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Idioma</strong><br/></td>
<td>cadeia de caracteres de linguagem<br/></td>
<td>Não<br/></td>
<td>O tipo de arquivo de header a ser incluído. <br/> <br/>
<dt><strong>C</strong></dt> <dd> Inclua um arquivo de header C.<br/> </dd> <dt><strong>IDL</strong></dt> <dd> Inclua um arquivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Local</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Esse atributo só é usado quando <strong>Language</strong> é definido como &quot; &quot; C.<br/> <br/>
<dt><strong>Verdade</strong></dt> <dd> Pesquisa o diretório atual para o header nomeado antes de pesquisar os diretórios do sistema.<br/> </dd> <dt><strong>False</strong></dt> <dd> Pesquise apenas os diretórios do sistema para o header nomeado.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**file**](file.md)<br/> | Saída de um arquivo do gerador de código.<br/> <br/> |



## <a name="remarks"></a>Comentários

Os exemplos a seguir mostram o código gerado de diferentes **elementos literalIncluir.**

### <a name="example-1---generating-a-c-include-statement"></a>Exemplo 1 – Gerando uma instrução de inclusão C

XML de entrada:

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

Código de saída:

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a>Exemplo 2 – Gerando uma instrução de inclusão C

XML de entrada:

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

Código de saída:

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a>Exemplo 3 – Gerando uma instrução de importação de IDL

XML de entrada:

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

Código de saída:

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




