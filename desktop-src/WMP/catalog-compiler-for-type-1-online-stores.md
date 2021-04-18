---
title: Compilador de catálogo para repositórios online do tipo 1
description: Compilador de catálogo para repositórios online do tipo 1
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Armazenamentos online do Windows Media Player, compilador de catálogo
- lojas online, compilador de catálogo
- tipo 1 lojas online, compilador de catálogo
- Armazenamentos online do Windows Media Player, catcomp.exe
- lojas online, catcomp.exe
- Digite 1 lojas online, catcomp.exe
- compilador de catálogo
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c54ffd054c5e72b04ddd32eef12c7fe6b6cc89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105763364"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a>Compilador de catálogo para repositórios online do tipo 1

O compilador de catálogo (catcomp.exe) é uma ferramenta de linha de comando usada por repositórios online do tipo 1 para compilar o conjunto de arquivos TSV (valores separados por tabulação) que contém os dados do catálogo da loja online em um catálogo compactado que pode ser baixado pelo Windows Media Player. O compilador de catálogo também compila arquivos de atualização de catálogo contendo apenas as informações do catálogo que foram alteradas desde a última atualização do catálogo.

Os arquivos de catálogo compactados ou os arquivos de atualização de catálogo devem ser fornecidos ao Windows Media Player para download na implementação do plug-in da loja online de [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).

Tarefas comuns

-   [Compilando um catálogo completo de arquivos TSV](compiling-a-full-catalog-from-tsv-files.md)
-   [Compilando uma atualização de catálogo de catálogos completos](compiling-a-catalog-update-from-full-catalogs.md)

Tarefas de diagnóstico

-   [Exibindo a ajuda](displaying-help.md)
-   [Recuperando Informações do catálogo](retrieving-catalog-information.md)
-   [Aplicando uma atualização a um catálogo](applying-an-update-to-a-catalog.md)

 

 




