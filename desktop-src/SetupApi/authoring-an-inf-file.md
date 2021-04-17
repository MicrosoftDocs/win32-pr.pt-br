---
description: Ao criar um arquivo INF para um aplicativo de instalação, você também deve consultar o formato de arquivo INF documentado em diretrizes gerais para arquivos INF e seções de arquivo INF e diretivas do Microsoft Windows 2000 Driver Development Kit.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Criando um arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73807f919a016f414a248f47e53f27d5b079bb33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754109"
---
# <a name="authoring-an-inf-file"></a>Criando um arquivo INF

Ao criar um arquivo INF para um aplicativo de instalação, você também deve consultar o formato de arquivo INF documentado em *diretrizes gerais para arquivos INF* e *seções de arquivo inf e diretivas* do Microsoft Windows 2000 Driver Development Kit.

Ao criar arquivos INF para um aplicativo de instalação, siga as regras a seguir.

-   Uma seção de **versão** é necessária em todos os arquivos INF.
-   As seções devem começar com o nome da seção entre colchetes ( \[ \] ).
-   Os nomes das seções **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **cadeias de caracteres** e **versão** devem ser idênticos ao tipo de seção. Por exemplo, use \[ DestinationDirs \] . Os autores podem especificar os nomes de outros tipos de seções.
-   Os nomes das seções **SourceDisksNames** e **SourceDisksFiles** podem ser anexados a um sufixo específico da plataforma. Por exemplo, para mostrar uma seção **SourceDisksNames** específica da Intel, use \[ SourceDisksNames. x86 \] . Se as funções de instalação localizarem seções **SourceDisksNames** e **SourceDisksFiles** específicas da plataforma correspondentes à plataforma do usuário, as funções usarão as seções específicas da plataforma. Caso contrário, as funções de instalação usarão as seções **SourceDisksNames** e **SourceDisksFiles** sem sufixo. As funções de instalação podem determinar programaticamente o sistema do usuário. Consulte o [exemplo de seções inf SourceDisksNames e SourceDisksFiles](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).
-   Os valores podem ser expressos como cadeias de caracteres substituíveis usando o formato%*strKey*%. Para usar um caractere% na cadeia de caracteres, use%%. O strKey deve ser definido em uma seção de **cadeias de caracteres** do arquivo inf.

 

 



