---
title: Compilando uma atualização de catálogo de catálogos completos
description: Compilando uma atualização de catálogo de catálogos completos
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Windows Media Player online, compilando catálogos
- lojas online, compilando catálogos
- tipo 1 lojas online, compilando catálogos
- Windows Media Player online, atualizações de catálogo
- lojas online, atualizações de catálogo
- tipo 1 lojas online, atualizações de catálogo
- Windows Media Player online, catálogos completos
- lojas online, catálogos completos
- tipo 1 lojas online, catálogos completos
- compilando catálogos
- atualizações de catálogo
- catálogos completos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306412d98f315a6a63aa40974b03a51a388b6db5c9e09c8d5b8907ef2cc15704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763946"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a>Compilando uma atualização de catálogo de catálogos completos

Uma atualização de catálogo que contém as alterações entre duas versões de um catálogo compilado pode ser criada usando a sintaxe abaixo, em que *path1* é o diretório que contém o primeiro catálogo, *path2* é o diretório que contém o segundo catálogo e a depuração pode ser incluída opcionalmente para exibir informações de erro detalhadas na tela. Os arquivos de catálogo devem estar em formato descompactado– o nome do arquivo do catálogo compilado seria catalog.wmdb, em vez de catalog.wmdb.lz.


```C++
catcomp diff <path1> <path2> [debug]
```



Por exemplo, se o diretório C: Catalog210 contiver a versão 210 de um catálogo compilado completo e C: Catalog211 contiver a versão \\ \\ \\ 211, o comando a seguir criará um arquivo de diferença que contém as alterações entre as duas \\ versões:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



Para exibir informações de erro detalhadas, você pode adicionar o parâmetro de depuração opcional da seguinte forma:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



Se a compilação for bemcatcomp.exe criará os arquivos de saída listados abaixo e os salvará no diretório que contém o primeiro catálogo.



| Nome do arquivo             | Descrição                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| catalog.diff          | Arquivo de diferença compilado descompactado.                                                                                                                                                           |
| catalog.diff.lz       | Versão compactada do arquivo de atualização do catálogo. O plug-in pode dar o local desse arquivo para Windows Media Player em [IWMPContentPartner::GetCatalogURL.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl) |
| catalog.wmdb.delta    | Arquivo de saída intermediário. Não usado por Windows Media Player                                                                                                                                       |
| catalog.wmdb.modified | Arquivo de saída intermediário. Não usado por Windows Media Player                                                                                                                                       |



 

 

 




