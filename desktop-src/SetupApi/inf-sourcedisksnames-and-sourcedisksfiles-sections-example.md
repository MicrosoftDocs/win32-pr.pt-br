---
description: A seção SourceDisksNames de um arquivo INF identifica os discos que contêm os arquivos de origem que estão sendo instalados.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: Exemplo das seções SourceDisksNames e SourceDisksFiles do INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f991727a8a2ca9cce2bd2d7161dfbf27b62ce74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749199"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a>Exemplo das seções SourceDisksNames e SourceDisksFiles do INF

A seção **SourceDisksNames** de um arquivo inf identifica os discos que contêm os arquivos de origem que estão sendo instalados. A seção **SourceDisksFiles** identifica os arquivos de origem e os discos de origem que os contêm. Observe que as plataformas MIPS, Alpha e PPC não têm suporte no Windows 2000 ou no Windows XP.

A partir do Windows XP, uma seção **SourceDisksNames** pode especificar uma marca, bem como um arquivo de gabinete. Por exemplo, a seguinte seção **SourceDisksNames** pode ser usada com mídia removível ou fixa. Se estiver usando mídia removível, a seção de exemplo verifica a presença da mídia verificando primeiro a presença da marca. Se estiver usando mídia fixa, a seção de exemplo verifica a presença da mídia verificando primeiro a presença do gabinete. Depois de verificar a presença de um gabinete, o sistema tenta copiar arquivos do gabinete e solicita os arquivos que não puderam ser copiados.

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

Para obter mais informações sobre **SourceDisksNames** ou **SourceDisksFiles**, consulte as seções "diretrizes gerais para arquivo inf" e "seções e diretivas de arquivo inf" do Microsoft Windows 2000 Driver Development Kit.

 

 



