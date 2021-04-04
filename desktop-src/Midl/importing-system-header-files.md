---
title: Importar arquivos de cabeçalho do sistema
description: Embora geralmente seja possível usar a diretiva \ include para incluir arquivos de cabeçalho em seu arquivo IDL, isso não é recomendado.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- importando MIDL, arquivos de cabeçalho do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663852"
---
# <a name="importing-system-header-files"></a>Importar arquivos de cabeçalho do sistema

Embora muitas vezes seja possível usar a diretiva **\# include** para incluir arquivos de cabeçalho em seu arquivo IDL, isso não é recomendado. O compilador MIDL irá gerar stubs para todas as funções definidas no arquivo IDL que está sendo compilado. Normalmente, um arquivo de cabeçalho contém um número de protótipos que você não precisa nem deseja incluir nos arquivos de stub, e um **\# inclui** efetivamente coloca todas essas definições em seu arquivo IDL principal. Além disso, se houver tipos não-Remotable definidos no arquivo de cabeçalho, o arquivo IDL não poderá ser compilado.

Há duas maneiras de incluir definições de tipo de arquivos de cabeçalho em um arquivo IDL:

-   Use a diretiva de [**importação**](import.md) para incluir tipos de dados definidos em um arquivo de cabeçalho. Ao contrário da diretiva de **\# inclusão** de linguagem C, a diretiva de **importação** só seleciona o tipo e as definições constantes e ignora os protótipos de procedimento. Essa abordagem funcionará contanto que seu arquivo IDL principal não referencie nenhum tipo de não-Remotable definido no arquivo de cabeçalho.
-   Crie um arquivo IDL auxiliar com uma interface fictícia que inclua os arquivos de cabeçalho. Em seguida, use a diretiva de [**importação**](import.md) para incluir o arquivo auxiliar. Dessa forma, somente os s de [**typedef**](typedef.md)serão exibidos nos stubs compilados. Por exemplo:

```syntax
//in helper.idl:
interface dummy
{ 
   #include "kitchensink.h"
   #include "system.h"
}

//in main.idl:
import "helper.idl";
```
