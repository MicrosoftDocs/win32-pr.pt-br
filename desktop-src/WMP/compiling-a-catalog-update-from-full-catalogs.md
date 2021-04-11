---
title: Compilando uma atualização de catálogo de catálogos completos
description: Compilando uma atualização de catálogo de catálogos completos
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Lojas online do Windows Media Player, compilando catálogos
- lojas online, compilando catálogos
- Digite 1 lojas online, compilando catálogos
- Armazenamentos online do Windows Media Player, atualizações de catálogo
- lojas online, atualizações de catálogo
- Digite 1 lojas online, atualizações de catálogo
- Lojas online do Windows Media Player, catálogos completos
- lojas online, catálogos completos
- Digite 1 lojas online, catálogos completos
- Compilando catálogos
- atualizações do catálogo
- catálogos completos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293752"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a>Compilando uma atualização de catálogo de catálogos completos

Uma atualização de catálogo que contém as alterações entre duas versões de um catálogo compilado pode ser criada usando a sintaxe abaixo, em que *caminho1* é o diretório que contém o primeiro catálogo, o *caminho* 2 é o diretório que contém o segundo catálogo e a depuração pode ser incluída opcionalmente para exibir informações detalhadas de erro na tela. Os arquivos de catálogo devem estar em formato descompactado – o nome de arquivo do catálogo compilado seria Catalog. wmdb, em vez de Catalog. wmdb. LZ.


```C++
catcomp diff <path1> <path2> [debug]
```



Por exemplo, se o diretório C: \\ Catalog210 \\ contiver a versão 210 de um catálogo completo compilado e C: \\ Catalog211 \\ contiver a versão 211, o comando a seguir criará um arquivo de diferenças que contém as alterações entre as duas versões:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



Para exibir informações detalhadas de erro, você pode adicionar o parâmetro de depuração opcional da seguinte maneira:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



Se a compilação for bem-sucedida, catcomp.exe criará os arquivos de saída listados abaixo e os salvará no diretório que contém o primeiro catálogo.



| Nome do arquivo             | Descrição                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Catalog. diff          | Arquivo de diferença compilado não compactado.                                                                                                                                                           |
| Catalog. diff. LZ       | Versão compactada do arquivo de atualização do catálogo. Seu plug-in pode fornecer o local desse arquivo ao Windows Media Player em [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). |
| Catalog. wmdb. Delta    | Arquivo de saída intermediário. Não usado pelo Windows Media Player                                                                                                                                       |
| Catalog. wmdb. Modified | Arquivo de saída intermediário. Não usado pelo Windows Media Player                                                                                                                                       |



 

 

 




