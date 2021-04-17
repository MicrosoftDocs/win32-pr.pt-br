---
title: " undef"
description: A diretiva \ undef remove a definição atual do nome especificado. Todas as ocorrências subsequentes do nome são processadas sem substituição.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798091"
---
# <a name="undef"></a>\#undef

A diretiva **\# undef** remove a definição atual do nome especificado. Todas as ocorrências subsequentes do nome são processadas sem substituição.

``` syntax
#undef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*nomes*
</dt> <dd>

Nome a ser removido. Esse valor é qualquer combinação de letras, dígitos e pontuação válida para o pré-processador de C/C++.

</dd> </dl>

## <a name="example"></a>Exemplo

Este exemplo remove as definições para os nomes diferentes de zero e userclass:

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador](preprocessor-directives.md)
</dt> </dl>

 

 




