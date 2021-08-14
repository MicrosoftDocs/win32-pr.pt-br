---
title: Importar arquivos de cabeçalho do sistema
description: Embora geralmente seja possível usar a diretiva \ include para incluir arquivos de header no arquivo IDL, não é recomendável.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- importando MIDL , arquivos de header do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070351ecd47b24d16d3baa2dde33b0199b02f4bf12e8ccc8f5628564a88dd6a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383873"
---
# <a name="importing-system-header-files"></a>Importar arquivos de cabeçalho do sistema

Embora geralmente seja possível usar a diretiva **\# include** para incluir arquivos de header no arquivo IDL, não é recomendável. O compilador MIDL gerará stubs para todas as funções definidas no arquivo IDL que está sendo compilado. Normalmente, um arquivo de header contém vários protótipos que você não precisa **\#** nem deseja incluir em seus arquivos stub, e uma inclusão efetivamente coloca todas essas definições em seu arquivo IDL principal. Além disso, se houver tipos nãoremestável definidos no arquivo de header, o arquivo IDL poderá não ser compilado.

Há duas maneiras de incluir definições de tipo de arquivos de header em um arquivo IDL:

-   Use a [**diretiva import**](import.md) para incluir tipos de dados definidos em um arquivo de header. Ao contrário da **\#** diretiva include da linguagem C, a diretiva **de** importação apenas escolhe definições de tipo e constante e ignora os protótipos de procedimento. Essa abordagem funcionará desde que o arquivo IDL principal não faça referência a nenhum tipo nãoremestável definido no arquivo de header.
-   Crie um arquivo IDL auxiliar com uma interface fiada que inclui os arquivos de header. Em seguida, use [**a diretiva import**](import.md) para incluir o arquivo auxiliar. Dessa forma, somente [**os typedef**](typedef.md)s aparecerão nos stubs compilados. Por exemplo:

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
