---
description: Cria um arquivo de catálogo não assinado, que contém os hashes de um conjunto de arquivos junto com os atributos associados de cada arquivo no conjunto. Um arquivo de catálogo permite que o usuário assine um arquivo (o catálogo) em vez de assinar vários arquivos individuais.
ms.assetid: 0a6ce2cd-db1f-4b47-990c-36fa87c28a60
title: Usando MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36c83531df38b95bde03edd719d98be325dbeac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767817"
---
# <a name="using-makecat"></a>Usando MakeCat

A ferramenta [MakeCat](makecat.md) cria um arquivo de catálogo não assinado, que contém os [*hashes*](../secgloss/h-gly.md) de um conjunto de arquivos junto com os atributos associados de cada arquivo no conjunto. Um arquivo de catálogo permite que o usuário assine um arquivo (o catálogo) em vez de assinar vários arquivos individuais.

Depois que o arquivo de catálogo não assinado for assinado e transmitido, o receptor poderá comparar os hashes dos arquivos originais com os hashes contidos no arquivo de catálogo e verificar se os arquivos estão livres de violação.

Antes de usar a ferramenta [MakeCat](makecat.md) , o usuário deve preparar um arquivo de definição de catálogo (. CDF) usando qualquer editor de texto. O arquivo. CDF contém a lista de arquivos e os atributos dos arquivos a serem catalogados (as especificações são listadas abaixo). A ferramenta MakeCat verifica o arquivo. CDF, verifica a lista de atributos de cada arquivo listado, adiciona os atributos listados ao próprio catálogo, aplica hash a cada um dos arquivos listados e armazena os hashes de cada arquivo no arquivo de catálogo. Cada arquivo tem seu hash e seus atributos armazenados separadamente no catálogo. Esse arquivo de catálogo pode então ser assinado e transmitido. O receptor pode posteriormente comparar o hash de cada arquivo dentro do catálogo com o hash dos arquivos originais para provar que o conteúdo original está livre de violação. MakeCat não modifica o arquivo. CDF.

Os exemplos a seguir usam comandos [MakeCat](makecat.md) .

-   Gere um arquivo de catálogo a partir do arquivo Good. CDF.

    **MakeCat-v Good. CDF**

Um arquivo, um bom. CDF, produz um arquivo de catálogo, Good.cat, analisando os arquivos UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, não assinados. class e SignedPE.exe. Os arquivos analisados, juntamente com bons. CDF e o Good.cat recém-gerado, estão todos no mesmo diretório.

``` syntax
[CatalogHeader]
Name=Good.cat
ResultDir=.\
PublicVersion=0x00000001
EncodingType=
CATATTR1=0x10010001:Movie1:FirstMovie
CATATTR2=0x10010001:Movie2:SecondMovie
CATATTR3=0x10010001:Movie3:ThirdMovie

[CatalogFiles]
UnsignedPE=.\UnsignedPE.EXE
UnsignedDOS=.\UnsignedDOS.EXE
<HASH>UnsignedCAB=.\Unsigned.CAB
UnsignedClass=.\Unsigned.Class
SignedPE=.\SignedPE.EXE
```

> [!Note]  
> A última entrada no arquivo. CDF sempre deve ter um caractere de nova linha explícito no final da linha.

 

 

 
