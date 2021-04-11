---
title: Extraindo os exemplos de código
description: Embora os exemplos de código sejam divididos em uma série de lições do tutorial, os agrupamentos de exemplo apropriados podem ser facilmente extraídos da coleção.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a593cf36b2fa235813c291eb35307153b28a2aa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363867"
---
# <a name="extracting-the-code-samples"></a>Extraindo os exemplos de código

Embora os exemplos de código sejam divididos em uma série de lições do tutorial, os agrupamentos de exemplo apropriados podem ser facilmente extraídos da coleção. A maioria dos diretórios de exemplo individuais tem como objetivo trabalhar em conjunto com pelo menos um outro diretório de exemplo. Os exemplos relacionados a componentes consistem em um par de cliente e servidor, com o servidor que requer o uso do utilitário de amostra de registro. Aqui está um resumo dos agrupamentos de exemplo e como extrair cada grupo como uma unidade compilável. Para cada Agrupamento de exemplo, copie o conteúdo dos diretórios mostrados. O diretório pai de \[ destino \] mostrado não requer nenhum conteúdo da ramificação de exemplos. No entanto, os menus de ajuda nos exemplos em execução pressupõem que o tutorial apropriado. Arquivos de ajuda HTM estão localizados neste diretório pai de \[ destino \] .

Para o aplicativo Win32 READTUT:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

Para o aplicativo de esqueleto do Win32 EXE:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

Para o esqueleto da DLL do Win32:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

Para os exemplos de objeto COM básico:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

Para obter os exemplos de cliente/servidor de componente de DLL em processo básico:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

Para os exemplos de cliente/servidor de componente licenciado:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

Para os exemplos de marshaling padrão:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

Para os exemplos de cliente/servidor local fora do processo:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    LOCSERVE
    LOCCLIEN
```

Para os exemplos de cliente de modelo de apartamento/servidor:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    APTCLIEN
```

Para os exemplos de cliente/servidor DCOM (COM distribuído):

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    REMCLIEN
```

Para os exemplos de cliente/servidor de Threading livre:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

Para os exemplos de cliente/servidor do objeto COM Connect:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

Para os exemplos de cliente/servidor de armazenamento estruturado:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

Para o objeto persistente, exemplos de cliente/servidor:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    PERSERVE
    PERTEXT
    PERDRAW
    PERCLIEN
```

Para os exemplos de cliente/servidor de segurança DCOM:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DCDMARSH
    DCDSERVE
    DCOMDRAW
```

 

 




