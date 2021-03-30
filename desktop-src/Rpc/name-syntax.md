---
title: Sintaxe do nome
description: RPC (chamada de procedimento remoto) e sintaxe de nome.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d024130a5b8a873c6bfbb2194542344953625d5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916455"
---
# <a name="name-syntax"></a>Sintaxe do nome

O Microsoft RPC aceita nomes que estão em conformidade com a seguinte sintaxe:

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="name"></span><span id="NAME"></span>nomes
</dt> <dd>

Especifica um identificador que pode conter qualquer caractere, exceto o caractere de delimitação de barra (/).

</dd> <dt>

<span id="domainname"></span><span id="DOMAINNAME"></span>DomainName
</dt> <dd>

Especifica o nome do domínio.

</dd> </dl>

Um parâmetro que seleciona o tipo de sintaxe de nome e a cadeia de caracteres que especifica o nome é fornecido para muitas das funções de RPC da interface de serviço de nome (NSI).

Somente um nome-tipo de sintaxe é suportado pelo Microsoft RPC, conforme especificado pela sintaxe constante \_ RPC \_ C \_ ns \_ DCE. Essa constante é definida no arquivo de cabeçalho RPCNSI. H.

A sintaxe de nome especificada pela \_ sintaxe RPC C \_ ns \_ \_ é uma extensão da sintaxe do nome do uso do \_ serviço de diretório de célula (CDs) do DCE. A capacidade de especificar um nome de domínio representa uma extensão para essa sintaxe. Não há nenhum limite absoluto para o número de nomes que podem ser separados por caracteres de barra, desde que a cadeia de caracteres geral tenha menos de 256 caracteres.

As barras permitem que você especifique uma estrutura lógica para o nome, mas elas não correspondem a uma estrutura lógica nos próprios objetos.

 

 




