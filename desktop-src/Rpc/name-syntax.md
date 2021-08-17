---
title: Sintaxe de nome
description: RPC (Chamada de Procedimento Remoto) e sintaxe de nome.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f63c86e6fe9283855e886014787fe36361bfbcdea3bc53e4078bbb43d193293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927815"
---
# <a name="name-syntax"></a>Sintaxe de nome

O Microsoft RPC aceita nomes que estão em conformidade com a seguinte sintaxe:

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Especifica um identificador que pode conter qualquer caractere, exceto o caractere de barra delimitador (/).

</dd> <dt>

<span id="domainname"></span><span id="DOMAINNAME"></span>Domainname
</dt> <dd>

Especifica o nome do domínio.

</dd> </dl>

Um parâmetro que seleciona o tipo de sintaxe de nome e a cadeia de caracteres que especifica o nome são fornecidos para muitas das funções RPC da interface de serviço de nome (NSI).

Somente um tipo de sintaxe de nome é suportado pelo Microsoft RPC, conforme especificado pela constante SINTAXE \_ \_ NS NS de RPC \_ \_ DCE. Essa constante é definida no arquivo de header RPCNSI.H.

A sintaxe de nome especificada pelo RPC C NS SYNTAX DCE é uma extensão da sintaxe de nome CDS (Serviço de Diretório de Célula) do \_ \_ \_ \_ \_ OSF DCE. A capacidade de especificar um nome de domínio representa uma extensão para essa sintaxe. Não há nenhum limite absoluto no número de nomes que podem ser separados por caracteres de barra, desde que a cadeia de caracteres geral seja menor que 256 caracteres.

As barras permitem que você especifique uma estrutura lógica para o nome, mas elas não correspondem a uma estrutura lógica nos próprios objetos.

 

 




