---
title: Tipos de dados no corpo da interface
description: O corpo da interface, que é colocado entre chaves (), contém os tipos de dados que serão usados em chamadas de procedimento remoto e protótipos para as funções que serão executadas remotamente.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- MIDL de interfaces, tipos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bdbbb90c4cbecd4a6a4e3cc74ba9775772dd0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757798"
---
# <a name="data-types-in-the-interface-body"></a>Tipos de dados no corpo da interface

O corpo da interface, que está entre chaves ({}), contém os tipos de dados que serão usados em chamadas de procedimento remoto e protótipos para as funções que serão executadas remotamente. Um corpo de interface pode conter importações, pragmas, declarações constantes, declarações de tipo e declarações de função. Exceto no modo de compatibilidade com uso, o compilador MIDL também permite declarações implícitas na forma de definições de variáveis.

Observe que a especificação uso-DCE para interfaces RPC não permite várias interfaces em um único arquivo IDL. Portanto, se você estiver compilando no modo de compatibilidade uso ( [**/OSF**](-osf.md)) do MIDL, o arquivo IDL poderá conter apenas uma interface.

Para obter detalhes sobre como usar o compilador MIDL para produzir bibliotecas de tipos, consulte [gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md).

No Microsoft RPC, um arquivo IDL pode conter várias interfaces e essas interfaces podem ser encaminhadas declaradas (dentro do arquivo IDL que as define). Por exemplo:

``` syntax
interface ITwo; //forward declaration
interface IOne 
{
...uses ITwo...
}
interface ITwo 
{
...uses IOne...
}
```

 

 




