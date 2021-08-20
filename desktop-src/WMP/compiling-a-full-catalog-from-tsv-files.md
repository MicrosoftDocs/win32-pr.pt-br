---
title: Compilando um catálogo completo de arquivos TSV
description: Compilando um catálogo completo de arquivos TSV
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Windows Media Player lojas online, compilando catálogos
- lojas online, compilando catálogos
- Digite 1 lojas online, compilando catálogos
- Windows Media Player lojas online, arquivos TSV
- lojas online, arquivos TSV
- tipo 1 lojas online, arquivos TSV
- Windows Media Player lojas online catcomp.exe
- lojas online, catcomp.exe
- Digite 1 lojas online, catcomp.exe
- catcomp.exe
- Compilando catálogos
- arquivos de valores separados por tabulação (TSV)
- Arquivos TSV (valores separados por tabulação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c5bc0648c19c3c8a6f9ddb819d77e48235bcd684d4911bc8a324a109c49daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863796"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a>Compilando um catálogo completo de arquivos TSV

Novos catálogos são criados a partir de um conjunto de arquivos TSV (valores separados por tabulação). Os arquivos devem estar no formato Unicode. Coloque os arquivos TSV necessários listados abaixo em uma pasta (o argumento de caminho de entrada para catcomp.exe) e chame catcomp.exe usando a seguinte sintaxe:


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



Se um número de versão não for fornecido, o número de versão será definido como 0. Se nenhuma ID de localidade for fornecida, a localidade do sistema será usada. Se apenas um argumento opcional numérico for fornecido, supõe-se que seja o número de versão. Se Debug for especificado, a saída para a tela fornecerá informações de diagnóstico mais detalhadas.

Por exemplo, o seguinte compilará um catálogo dos arquivos em C: \\ CatalogData \\ 210 e atribuirá ao catálogo um número de versão de 210:


```C++
catcomp C:\CatalogData\210 210
```



Para exibir mensagens de erro mais detalhadas, o argumento de depuração opcional pode ser adicionado, da seguinte maneira:


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a>Arquivos TSV necessários

Cada um dos arquivos a seguir deve estar presente, mas um arquivo vazio pode ser usado se não houver dados para um arquivo. Por exemplo, se o catálogo não contiver canais de rádio, radio.csv poderá ficar vazia. Os arquivos devem ser nomeados exatamente como listados.

[track.csv](track-csv.md)

[album.csv](album-csv.md)

[artist.csv](artist-csv.md)

[genre.csv](genre-csv.md)

[subgenre.csv](subgenre-csv.md)

[list.csv](list-csv.md)

[listitem.csv](listitem-csv.md)

[radio.csv](radio-csv.md)

> [!Note]  
> Embora os nomes de arquivo devam ter extensões .csv, os arquivos não estão no formato CSV (valores separados por vírgula). Os arquivos devem estar no formato TSV (valores separados por tabulação).

 

Se a compilação for bem-sucedida, catcomp.exe criará três arquivos de saída.



| Nome do arquivo                   | Descrição                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Catalog. wmdb                | Catálogo compilado não compactado.                                                                                                                                                      |
| Catalog. wmdb. LZ             | Catálogo em formato compactado. seu plug-in pode dar ao local desse arquivo Windows Media Player em [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). |
| \_words.txt exclusivos compilados \_ | Um arquivo de saída intermediário. Não usado pelo Windows Media Player.                                                                                                                      |



 

 

 




