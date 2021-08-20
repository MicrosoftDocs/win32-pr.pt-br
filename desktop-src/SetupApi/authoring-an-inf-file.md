---
description: Ao desenvolver um arquivo INF para um aplicativo de Instalação, você também deve consultar o formato de arquivo INF documentado em Diretrizes gerais para arquivos INF e seções de arquivo INF e diretivas do Kit de Desenvolvimento de Driver do Microsoft Windows 2000.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Como autor de um arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3745dc16a14f603de780b15d708fbb4542ea4503052aeb2b7edb3486c5b5fc51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117966364"
---
# <a name="authoring-an-inf-file"></a>Como autor de um arquivo INF

Ao desenvolver um arquivo INF para um aplicativo de Instalação, você também deve consultar o formato de arquivo INF documentado em Diretrizes gerais para arquivos *INF* e seções de arquivo INF e *diretivas* do Kit de Desenvolvimento de Driver do Microsoft Windows 2000.

Ao autorizar arquivos INF para um aplicativo de instalação, acate as regras a seguir.

-   Uma **seção** Versão é necessária em cada arquivo INF.
-   As seções devem começar com o nome da seção entre colchetes ( \[ \] ).
-   Os nomes **das seções DestinationDirs**, **SourceDisksFiles,** **SourceDisksNames,** **Strings** e **Version** devem ser idênticos ao tipo de seção. Por exemplo, use \[ \] DestinationDirs. Os autores podem especificar os nomes de outros tipos de seções.
-   Os nomes **das seções SourceDisksNames** e **SourceDisksFiles** podem ser anexados com um sufixo específico da plataforma. Por exemplo, para mostrar uma seção **SourceDisksNames** específica da Intel, use \[ SourceDisksNames.x86 \] . Se as funções de instalação encontrarem as seções **SourceDisksNames** e **SourceDisksFiles** específicas da plataforma correspondentes à plataforma do usuário, as funções usarão as seções específicas da plataforma. Caso contrário, as funções de instalação usarão as seções **SourceDisksNames** e **SourceDisksFiles** não sufixos. As funções de instalação podem determinar programaticamente o sistema do usuário. Consulte o [Exemplo de seções SourceDisksNames e SourceDisksFiles do INF](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).
-   Os valores podem ser expressos como cadeias de caracteres substituíveis usando o formato %*strkey*%. Para usar um caractere % na cadeia de caracteres, use %%. A strkey deve ser definida em uma seção **Cadeias de caracteres** do arquivo INF.

 

 



