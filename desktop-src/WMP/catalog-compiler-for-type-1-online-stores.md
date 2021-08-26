---
title: Compilador de catálogo para lojas online do tipo 1
description: Compilador de catálogo para lojas online do tipo 1
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Windows Media Player online, compilador de catálogo
- lojas online, compilador de catálogo
- type 1 online stores,catalog compiler
- Windows Media Player online, catcomp.exe
- lojas online, catcomp.exe
- tipo 1 lojas online, catcomp.exe
- compilador de catálogo
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2764da5e19c84145bd0a11127aebc8f518031744626ca1b41c75c43c6e10093f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864206"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a>Compilador de catálogo para lojas online do tipo 1

O compilador de catálogo (catcomp.exe) é uma ferramenta de linha de comando usada pelos armazenamentos online do Tipo 1 para compilar o conjunto de arquivos TSV (valores separados por tabulação) que contêm os dados do catálogo do armazenamento online em um catálogo compactado que pode ser baixado pelo Windows Media Player. O compilador de catálogo também compila arquivos de atualização de catálogo que contêm apenas as informações do catálogo que foram alteradas desde a última atualização do catálogo.

Os arquivos de catálogo compactados ou arquivos de atualização de catálogo devem ser fornecidos ao Windows Media Player para download na implementação do plug-in da loja online [de IWMPContentPartner::GetCatalogURL.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)

Tarefas comuns

-   [Compilando um catálogo completo de arquivos TSV](compiling-a-full-catalog-from-tsv-files.md)
-   [Compilando uma atualização de catálogo de catálogos completos](compiling-a-catalog-update-from-full-catalogs.md)

Tarefas de diagnóstico

-   [Exibindo ajuda](displaying-help.md)
-   [Recuperando informações do catálogo](retrieving-catalog-information.md)
-   [Aplicando uma atualização a um catálogo](applying-an-update-to-a-catalog.md)

 

 




