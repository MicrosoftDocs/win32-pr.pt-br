---
title: " define"
description: A diretiva \ define atribui o valor fornecido ao nome especificado. Todas as ocorrências subsequentes do nome são substituídas pelo valor.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8e8f99dc592eefb1fb79201883e8a32837633814b79d7819e84d283709a46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826046"
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

 

 




