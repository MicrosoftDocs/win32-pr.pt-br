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
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a><span data-ttu-id="b83a1-103">Exemplo das seções SourceDisksNames e SourceDisksFiles do INF</span><span class="sxs-lookup"><span data-stu-id="b83a1-103">INF SourceDisksNames and SourceDisksFiles Sections Example</span></span>

<span data-ttu-id="b83a1-104">A seção **SourceDisksNames** de um arquivo inf identifica os discos que contêm os arquivos de origem que estão sendo instalados.</span><span class="sxs-lookup"><span data-stu-id="b83a1-104">The **SourceDisksNames** section of an INF file identifies the disks that contain the source files being installed.</span></span> <span data-ttu-id="b83a1-105">A seção **SourceDisksFiles** identifica os arquivos de origem e os discos de origem que os contêm.</span><span class="sxs-lookup"><span data-stu-id="b83a1-105">The **SourceDisksFiles** section identifies the source files and the source disks that contain them.</span></span> <span data-ttu-id="b83a1-106">Observe que as plataformas MIPS, Alpha e PPC não têm suporte no Windows 2000 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b83a1-106">Note that MIPS, Alpha, and PPC platforms are not supported by Windows 2000 or Windows XP.</span></span>

<span data-ttu-id="b83a1-107">A partir do Windows XP, uma seção **SourceDisksNames** pode especificar uma marca, bem como um arquivo de gabinete.</span><span class="sxs-lookup"><span data-stu-id="b83a1-107">Beginning with Windows XP, a **SourceDisksNames** section may specify a tag as well as cabinet file.</span></span> <span data-ttu-id="b83a1-108">Por exemplo, a seguinte seção **SourceDisksNames** pode ser usada com mídia removível ou fixa.</span><span class="sxs-lookup"><span data-stu-id="b83a1-108">For example, the following **SourceDisksNames** section may be used with removable or fixed media.</span></span> <span data-ttu-id="b83a1-109">Se estiver usando mídia removível, a seção de exemplo verifica a presença da mídia verificando primeiro a presença da marca.</span><span class="sxs-lookup"><span data-stu-id="b83a1-109">If using removable media, the example section verifies the presence of the media by first checking for the presence of the tag.</span></span> <span data-ttu-id="b83a1-110">Se estiver usando mídia fixa, a seção de exemplo verifica a presença da mídia verificando primeiro a presença do gabinete.</span><span class="sxs-lookup"><span data-stu-id="b83a1-110">If using fixed media, the example section verifies the presence of the media by first checking for the presence of the cabinet.</span></span> <span data-ttu-id="b83a1-111">Depois de verificar a presença de um gabinete, o sistema tenta copiar arquivos do gabinete e solicita os arquivos que não puderam ser copiados.</span><span class="sxs-lookup"><span data-stu-id="b83a1-111">After verifying the presence of a cabinet, the system attempts to copy files out of the cabinet and prompts for any files it was unable to copy.</span></span>

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

<span data-ttu-id="b83a1-112">Para obter mais informações sobre **SourceDisksNames** ou **SourceDisksFiles**, consulte as seções "diretrizes gerais para arquivo inf" e "seções e diretivas de arquivo inf" do Microsoft Windows 2000 Driver Development Kit.</span><span class="sxs-lookup"><span data-stu-id="b83a1-112">For more information about **SourceDisksNames** or **SourceDisksFiles**, see the "General Guidelines for INF File" and "INF File Sections and Directives" sections of the Microsoft Windows 2000 Driver Development Kit.</span></span>

 

 



