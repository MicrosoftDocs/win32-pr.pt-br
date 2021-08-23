---
title: " include"
description: A diretiva \ include faz com que o compilador de recursos processe o arquivo especificado no parâmetro filename.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bf5d6fa40e45073ca7ccb5f97dd3ddb0d13dfdfced965d5c83332183da421e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599708"
---
# <a name="-include"></a>' include'

A **\# diretiva include** faz com que o compilador de recursos processe o arquivo especificado no parâmetro *filename.* Esse arquivo deve ser um arquivo de header que define as constantes usadas no arquivo de definição de recurso. O arquivo pode usar caracteres Unicode, de byte único, de byte duplo.

``` syntax
#include filename
```

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

Nome do arquivo a ser incluído. Se o arquivo estiver no diretório atual, a cadeia de caracteres deverá ser entre aspas duplas; se o arquivo estiver no diretório especificado pela variável de ambiente INCLUDE, a cadeia de caracteres deverá ser delimitada em caracteres menores e maiores que (<>). Você deverá dar um caminho completo entre aspas duplas (") se o arquivo não estiver no diretório atual ou no diretório especificado pela variável de ambiente INCLUDE.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use a seguinte instrução no arquivo de header para cercar instruções que podem ser compiladas por um compilador C, mas não pelo RC:

``` syntax
#ifndef RC_INVOKED
```

Dessa forma, você pode usar os mesmos arquivos de inclusão em seus arquivos .c e .rc.

## <a name="example"></a>Exemplo

Este exemplo processa os arquivos de Windows.h e MyDefs.h ao compilar o arquivo de definição de recurso:

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador](preprocessor-directives.md)
</dt> </dl>

 

 




