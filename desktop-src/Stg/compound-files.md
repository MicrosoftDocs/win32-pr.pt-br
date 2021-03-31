---
title: arquivos compostos
description: Embora você possa implementar seus próprios objetos e interfaces de armazenamento estruturado, o COM fornece uma implementação padrão chamada arquivos compostos.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62be79f09afd23e53a569b76ad3e0af46cae2f9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159428"
---
# <a name="compound-files"></a><span data-ttu-id="84190-103">arquivos compostos</span><span class="sxs-lookup"><span data-stu-id="84190-103">Compound Files</span></span>

<span data-ttu-id="84190-104">Embora você possa implementar seus próprios objetos e interfaces de armazenamento estruturado, o COM fornece uma implementação padrão chamada arquivos compostos.</span><span class="sxs-lookup"><span data-stu-id="84190-104">Although you can implement your own structured storage objects and interfaces, COM provides a standard implementation called Compound Files.</span></span> <span data-ttu-id="84190-105">O uso de arquivos compostos poupa o trabalho de codificar sua própria implementação de armazenamento estruturado e confere vários benefícios adicionais derivados de aderir a um padrão definido.</span><span class="sxs-lookup"><span data-stu-id="84190-105">Using Compound Files saves you the work of coding your own implementation of structured storage and confers several additional benefits derived from adhering to a defined standard.</span></span> <span data-ttu-id="84190-106">Esses benefícios incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="84190-106">These benefits include the following:</span></span>

-   <span data-ttu-id="84190-107">**Independência de plataforma e sistema de arquivos**.</span><span class="sxs-lookup"><span data-stu-id="84190-107">**File-system and platform independence**.</span></span> <span data-ttu-id="84190-108">Como a implementação dos arquivos compostos do COM é executada na parte superior dos sistemas de arquivos simples existentes, os arquivos compostos armazenados no sistema de arquivos FAT, no sistema de arquivos NTFS ou nos sistemas de arquivos do Macintosh podem ser abertos por aplicativos que usam qualquer um dos outros sistemas de arquivos.</span><span class="sxs-lookup"><span data-stu-id="84190-108">Because COM's Compound Files implementation runs on top of existing flat-file systems, compound files stored in the FAT file system, NTFS file system, or Macintosh file systems can be opened by applications using any one of the other file systems.</span></span>
-   <span data-ttu-id="84190-109">**Pesquisável**.</span><span class="sxs-lookup"><span data-stu-id="84190-109">**Searchable**.</span></span> <span data-ttu-id="84190-110">Como os objetos separados em um arquivo composto são salvos em um formato padrão e podem ser acessados usando interfaces COM e APIs padrão, qualquer utilitário de navegador usando essas interfaces e APIs pode listar os objetos no arquivo, mesmo que os dados dentro de um determinado objeto possam estar em um formato proprietário.</span><span class="sxs-lookup"><span data-stu-id="84190-110">Because the separate objects in a compound file are saved in a standard format and can be accessed using standard COM interfaces and APIs, any browser utility using these interfaces and APIs can list the objects in the file, even though data within a given object may be in a proprietary format.</span></span>
-   <span data-ttu-id="84190-111">**Acesso a determinados dados internos**.</span><span class="sxs-lookup"><span data-stu-id="84190-111">**Access to certain internal data**.</span></span> <span data-ttu-id="84190-112">Como a implementação dos arquivos compostos fornece maneiras padrão de gravar determinados tipos de dados — informações de resumo, por exemplo — os aplicativos podem ler esses dados usando interfaces e APIs COM.</span><span class="sxs-lookup"><span data-stu-id="84190-112">Because the Compound Files implementation provides standard ways of writing certain types of data—summary information, for example—applications can read this data using COM interfaces and APIs.</span></span>

 

 




