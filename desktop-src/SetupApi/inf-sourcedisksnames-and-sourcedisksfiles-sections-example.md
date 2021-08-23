---
description: A seção SourceDisksNames de um arquivo INF identifica os discos que contêm os arquivos de origem que estão sendo instalados.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: Exemplo de seções SourceDisksNames e SourceDisksFiles do INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00eb8241b8e290f5460cc41b233d3b199df35e709d6e32f2c5a39925a79f851d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739406"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a>Exemplo de seções SourceDisksNames e SourceDisksFiles do INF

A **seção SourceDisksNames** de um arquivo INF identifica os discos que contêm os arquivos de origem que estão sendo instalados. A **seção SourceDisksFiles** identifica os arquivos de origem e os discos de origem que os contêm. Observe que as plataformas MIPS, Alfa e PPC não são suportadas pelo Windows 2000 ou Windows XP.

Começando com Windows XP, uma **seção SourceDisksNames** pode especificar uma marca, bem como um arquivo de gabinete. Por exemplo, a seção **SourceDisksNames** a seguir pode ser usada com mídia removível ou fixa. Se estiver usando mídia removível, a seção de exemplo verificará a presença da mídia verificando primeiro a presença da marca. Se estiver usando mídia fixa, a seção de exemplo verificará a presença da mídia verificando primeiro a presença do gabinete. Depois de verificar a presença de um gabinete, o sistema tenta copiar arquivos do gabinete e solicita todos os arquivos que não pôde copiar.

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

Para obter mais informações sobre **SourceDisksNames** ou **SourceDisksFiles**, consulte as seções "Diretrizes gerais para arquivo INF" e "Seções e diretivas de arquivo INF" do Kit de Desenvolvimento de Driver do Microsoft Windows 2000.

 

 



