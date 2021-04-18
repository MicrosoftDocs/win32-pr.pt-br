---
description: Coloca uma instrução de inclusão C ou IDL no código gerado.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: elemento literalInclude
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2701b2b21d14b629d5d9b61dcbc73e11371f54e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772975"
---
# <a name="literalinclude-element"></a>elemento literalInclude

Coloca uma instrução de inclusão C ou IDL no código gerado.

## <a name="usage"></a>Uso

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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
<td>Cadeia de caracteres de idioma<br/></td>
<td>No<br/></td>
<td>O tipo de arquivo de cabeçalho a ser incluído. <br/> <br/>
<dt><strong>&</strong></dt> <dd> Incluir um arquivo de cabeçalho C.<br/> </dd> <dt><strong>INSERI</strong></dt> <dd> Incluir um arquivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Local</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Esse atributo só é usado quando o <strong>idioma</strong> é definido como &quot; C &quot; .<br/> <br/>
<dt><strong>True</strong></dt> <dd> Pesquisa o diretório atual para o cabeçalho nomeado antes de Pesquisar os diretórios do sistema.<br/> </dd> <dt><strong>For</strong></dt> <dd> Pesquise somente os diretórios do sistema para o cabeçalho nomeado.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Grupo**](file.md)<br/> | Gera um arquivo do gerador de código.<br/> <br/> |



## <a name="remarks"></a>Comentários

Os exemplos a seguir mostram o código gerado de diferentes elementos **literalInclude** .

### <a name="example-1---generating-a-c-include-statement"></a>Exemplo 1-gerando uma instrução C include

XML de entrada:

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

Código de saída:

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a>Exemplo 2-gerando uma instrução C include

XML de entrada:

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

Código de saída:

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a>Exemplo 3-gerando uma instrução de importação de IDL

XML de entrada:

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

Código de saída:

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




