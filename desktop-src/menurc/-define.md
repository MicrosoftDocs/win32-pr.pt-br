---
title: " define"
description: A diretiva \ define atribui o valor fornecido ao nome especificado. Todas as ocorrências subsequentes do nome são substituídas pelo valor.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636385"
---
# <a name="define"></a>\#definir

A diretiva **\# definir** atribui o valor fornecido ao nome especificado. Todas as ocorrências subsequentes do nome são substituídas pelo valor.

``` syntax
#define name value
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*nomes*
</dt> <dd>

Nome a ser definido. Esse valor é qualquer combinação de letras, dígitos e pontuação válida para o pré-processador de C/C++.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*valor*
</dt> <dd>

Inteiro, Cadeia de caracteres ou linha de texto.

</dd> </dl>

## <a name="example"></a>Exemplo

Este exemplo atribui valores aos nomes diferentes de zero e userclass:

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador](preprocessor-directives.md)
</dt> </dl>

 

 




