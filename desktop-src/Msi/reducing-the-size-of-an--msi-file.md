---
description: Os desenvolvedores de Windows Installer pacotes podem notar seus arquivos. msi ficando maiores do que o esperado após edições e salvações repetidas.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Reduzindo o tamanho de um arquivo. msi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921640"
---
# <a name="reducing-the-size-of-an-msi-file"></a><span data-ttu-id="2782a-103">Reduzindo o tamanho de um arquivo. msi</span><span class="sxs-lookup"><span data-stu-id="2782a-103">Reducing the Size of an .msi File</span></span>

<span data-ttu-id="2782a-104">Os desenvolvedores de Windows Installer pacotes podem notar seus arquivos. msi ficando maiores do que o esperado após edições e salvações repetidas.</span><span class="sxs-lookup"><span data-stu-id="2782a-104">Developers of Windows Installer packages may notice their .msi files getting larger than expected after repeated edits and saves.</span></span> <span data-ttu-id="2782a-105">Os arquivos. msi do Windows Installer são arquivos compostos que contêm armazenamentos e fluxos e têm algumas das mesmas limitações de armazenamento que os arquivos de documento OLE.</span><span class="sxs-lookup"><span data-stu-id="2782a-105">Windows Installer .msi files are compound files that contain storages and streams, and have some of the same storage limitations as OLE document files.</span></span> <span data-ttu-id="2782a-106">Se você editar e salvar o mesmo arquivo. msi repetidamente, ele criará o espaço de armazenamento desperdiçado no arquivo.</span><span class="sxs-lookup"><span data-stu-id="2782a-106">If you edit and save the same .msi file over and over, it creates wasted storage space in the file.</span></span> <span data-ttu-id="2782a-107">Isso afeta apenas os autores de arquivos. msi e não tem nenhum efeito sobre Windows Installer usuários.</span><span class="sxs-lookup"><span data-stu-id="2782a-107">This only affects authors of .msi files and has no effect on Windows Installer users.</span></span> <span data-ttu-id="2782a-108">Os desenvolvedores podem querer remover esse espaço de armazenamento desperdiçado antes de enviar seu arquivo. msi final.</span><span class="sxs-lookup"><span data-stu-id="2782a-108">Developers may want to remove this wasted storage space before shipping their final .msi file.</span></span>

<span data-ttu-id="2782a-109">Para remover o espaço de armazenamento desperdiçado e reduzir o tamanho final dos arquivos. msi, você tem as seguintes opções.</span><span class="sxs-lookup"><span data-stu-id="2782a-109">To remove wasted storage space and reduce the final size of .msi files, you have the following options.</span></span>

-   <span data-ttu-id="2782a-110">Exporte todas as tabelas no banco de dados para arquivos. IDT e, em seguida, importe-as para um novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2782a-110">Export all of the tables in the database to .idt files, and then import those into a new database.</span></span> <span data-ttu-id="2782a-111">Isso produz o armazenamento mais compacto possível.</span><span class="sxs-lookup"><span data-stu-id="2782a-111">This produces the most compact storage possible.</span></span>
-   <span data-ttu-id="2782a-112">Use um utilitário de software para compactar o espaço de armazenamento de arquivos de documento OLE.</span><span class="sxs-lookup"><span data-stu-id="2782a-112">Use a software utility for compacting the storage space of OLE document files.</span></span>

 

 



