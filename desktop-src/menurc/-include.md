---
title: " include"
description: A diretiva \ include faz com que o compilador de recurso processe o arquivo especificado no parâmetro filename.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8d36f1d0ae24f3dc21d67eec57056872aabdbd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369170"
---
# <a name="-include"></a>incluir

A diretiva **\# include** faz com que o compilador de recurso processe o arquivo especificado no parâmetro *filename* . Esse arquivo deve ser um arquivo de cabeçalho que define as constantes usadas no arquivo de definição de recurso. O arquivo pode usar caracteres de byte único, dois bytes ou Unicode.

``` syntax
#include filename
```

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*
</dt> <dd>

Nome do arquivo a ser incluído. Se o arquivo estiver no diretório atual, a cadeia de caracteres deverá ser colocada entre aspas duplas; Se o arquivo estiver no diretório especificado pela variável de ambiente INCLUDE, a cadeia de caracteres deverá ser colocada entre os caracteres inferior e maior que (<>). Você deve fornecer um caminho completo entre aspas duplas (") se o arquivo não estiver no diretório atual ou no diretório especificado pela variável de ambiente INCLUDE.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use a instrução a seguir no arquivo de cabeçalho para instruções surround que podem ser compiladas por um compilador C, mas não por RC:

``` syntax
#ifndef RC_INVOKED
```

Dessa forma, você pode usar os mesmos arquivos de inclusão nos arquivos. c e. rc.

## <a name="example"></a>Exemplo

Este exemplo processa os arquivos de cabeçalho Windows. h e MyDefs. h durante a compilação do arquivo de definição de recurso:

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador](preprocessor-directives.md)
</dt> </dl>

 

 




