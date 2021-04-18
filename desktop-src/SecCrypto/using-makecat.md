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
# <a name="using-makecat"></a><span data-ttu-id="0732d-104">Usando MakeCat</span><span class="sxs-lookup"><span data-stu-id="0732d-104">Using MakeCat</span></span>

<span data-ttu-id="0732d-105">A ferramenta [MakeCat](makecat.md) cria um arquivo de catálogo não assinado, que contém os [*hashes*](../secgloss/h-gly.md) de um conjunto de arquivos junto com os atributos associados de cada arquivo no conjunto.</span><span class="sxs-lookup"><span data-stu-id="0732d-105">The [MakeCat](makecat.md) tool makes an unsigned catalog file, which contains the [*hashes*](../secgloss/h-gly.md) of a set of files along with associated attributes of each file in the set.</span></span> <span data-ttu-id="0732d-106">Um arquivo de catálogo permite que o usuário assine um arquivo (o catálogo) em vez de assinar vários arquivos individuais.</span><span class="sxs-lookup"><span data-stu-id="0732d-106">A catalog file allows the user to sign one file (the catalog) instead of signing numerous individual files.</span></span>

<span data-ttu-id="0732d-107">Depois que o arquivo de catálogo não assinado for assinado e transmitido, o receptor poderá comparar os hashes dos arquivos originais com os hashes contidos no arquivo de catálogo e verificar se os arquivos estão livres de violação.</span><span class="sxs-lookup"><span data-stu-id="0732d-107">After the unsigned catalog file is signed and transmitted, the receiver can compare the hashes of the original files to the hashes contained within the catalog file and verify that the files are free of tampering.</span></span>

<span data-ttu-id="0732d-108">Antes de usar a ferramenta [MakeCat](makecat.md) , o usuário deve preparar um arquivo de definição de catálogo (. CDF) usando qualquer editor de texto.</span><span class="sxs-lookup"><span data-stu-id="0732d-108">Prior to using the [MakeCat](makecat.md) tool, the user must prepare a Catalog Definition File (.cdf), by using any text editor.</span></span> <span data-ttu-id="0732d-109">O arquivo. CDF contém a lista de arquivos e os atributos dos arquivos a serem catalogados (as especificações são listadas abaixo).</span><span class="sxs-lookup"><span data-stu-id="0732d-109">The .cdf file contains the list of files and the attributes of the files to be cataloged (the specifications are listed below).</span></span> <span data-ttu-id="0732d-110">A ferramenta MakeCat verifica o arquivo. CDF, verifica a lista de atributos de cada arquivo listado, adiciona os atributos listados ao próprio catálogo, aplica hash a cada um dos arquivos listados e armazena os hashes de cada arquivo no arquivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="0732d-110">The MakeCat tool scans the .cdf file, verifies the list of attributes of each listed file, adds the listed attributes to the catalog itself, hashes each of the listed files, and stores the hashes of each file into the catalog file.</span></span> <span data-ttu-id="0732d-111">Cada arquivo tem seu hash e seus atributos armazenados separadamente no catálogo.</span><span class="sxs-lookup"><span data-stu-id="0732d-111">Each file has its hash and attributes stored separately within the catalog.</span></span> <span data-ttu-id="0732d-112">Esse arquivo de catálogo pode então ser assinado e transmitido.</span><span class="sxs-lookup"><span data-stu-id="0732d-112">This catalog file can then be signed and transmitted.</span></span> <span data-ttu-id="0732d-113">O receptor pode posteriormente comparar o hash de cada arquivo dentro do catálogo com o hash dos arquivos originais para provar que o conteúdo original está livre de violação.</span><span class="sxs-lookup"><span data-stu-id="0732d-113">The receiver can subsequently compare the hash of each file within the catalog with the hash of the original files to prove that the original content is free of tampering.</span></span> <span data-ttu-id="0732d-114">MakeCat não modifica o arquivo. CDF.</span><span class="sxs-lookup"><span data-stu-id="0732d-114">MakeCat does not modify the .cdf file.</span></span>

<span data-ttu-id="0732d-115">Os exemplos a seguir usam comandos [MakeCat](makecat.md) .</span><span class="sxs-lookup"><span data-stu-id="0732d-115">The following examples use [MakeCat](makecat.md) commands.</span></span>

-   <span data-ttu-id="0732d-116">Gere um arquivo de catálogo a partir do arquivo Good. CDF.</span><span class="sxs-lookup"><span data-stu-id="0732d-116">Generate a catalog file from the file Good.cdf.</span></span>

    <span data-ttu-id="0732d-117">**MakeCat-v Good. CDF**</span><span class="sxs-lookup"><span data-stu-id="0732d-117">**MakeCat -v good.cdf**</span></span>

<span data-ttu-id="0732d-118">Um arquivo, um bom. CDF, produz um arquivo de catálogo, Good.cat, analisando os arquivos UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, não assinados. class e SignedPE.exe.</span><span class="sxs-lookup"><span data-stu-id="0732d-118">A file, Good.cdf, produces a catalog file, Good.cat, by parsing the files UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, Unsigned.Class, and SignedPE.exe.</span></span> <span data-ttu-id="0732d-119">Os arquivos analisados, juntamente com bons. CDF e o Good.cat recém-gerado, estão todos no mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="0732d-119">The parsed files, along with Good.cdf and the newly generated Good.cat, are all in the same directory.</span></span>

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
> <span data-ttu-id="0732d-120">A última entrada no arquivo. CDF sempre deve ter um caractere de nova linha explícito no final da linha.</span><span class="sxs-lookup"><span data-stu-id="0732d-120">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

 

 
