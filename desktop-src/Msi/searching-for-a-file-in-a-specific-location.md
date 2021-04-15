---
description: Durante uma instalação de Windows Installer, o instalador pode pesquisar um arquivo em um local específico no sistema do usuário.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Procurando um arquivo em um local específico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ad4e456d331119b698d8e6e696e86b953006eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506009"
---
# <a name="searching-for-a-file-in-a-specific-location"></a><span data-ttu-id="46b7d-103">Procurando um arquivo em um local específico</span><span class="sxs-lookup"><span data-stu-id="46b7d-103">Searching for a File in a Specific Location</span></span>

<span data-ttu-id="46b7d-104">**Para procurar um arquivo em um local específico em um sistema de usuário**</span><span class="sxs-lookup"><span data-stu-id="46b7d-104">**To search for a file in a specific location on a user system**</span></span>

1.  <span data-ttu-id="46b7d-105">Liste a assinatura e o nome do arquivo na [tabela de assinatura](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="46b7d-105">List the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="46b7d-106">Os campos restantes nesse registro podem ser nulos para pesquisar qualquer versão do MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="46b7d-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    [<span data-ttu-id="46b7d-107">Tabela de assinatura</span><span class="sxs-lookup"><span data-stu-id="46b7d-107">Signature Table</span></span>](signature-table.md)

    

    | <span data-ttu-id="46b7d-108">Assinatura</span><span class="sxs-lookup"><span data-stu-id="46b7d-108">Signature</span></span>          | <span data-ttu-id="46b7d-109">Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="46b7d-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="46b7d-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="46b7d-110">AppFile</span></span><br/> | <span data-ttu-id="46b7d-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="46b7d-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="46b7d-112">Insira a propriedade que o instalador deve definir se MyApp.exe estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="46b7d-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="46b7d-113">[Tabela AppSearch](appsearch-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="46b7d-113">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="46b7d-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="46b7d-114">Property</span></span>         | <span data-ttu-id="46b7d-115">Assinatura</span><span class="sxs-lookup"><span data-stu-id="46b7d-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="46b7d-116">MYAPP</span><span class="sxs-lookup"><span data-stu-id="46b7d-116">MYAPP</span></span><br/> | <span data-ttu-id="46b7d-117">AppFile</span><span class="sxs-lookup"><span data-stu-id="46b7d-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="46b7d-118">Use a [tabela DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="46b7d-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="46b7d-119">Insira o caminho completo para o arquivo no sistema do usuário no campo caminho.</span><span class="sxs-lookup"><span data-stu-id="46b7d-119">Enter the full path to the file on the user system in the Path field.</span></span> <span data-ttu-id="46b7d-120">Insira um valor de 0 na coluna profundidade para pesquisar a pasta bin.</span><span class="sxs-lookup"><span data-stu-id="46b7d-120">Enter a value of 0 into the Depth column to search the bin folder.</span></span>

    [<span data-ttu-id="46b7d-121">Tabela DrLocator</span><span class="sxs-lookup"><span data-stu-id="46b7d-121">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="46b7d-122">Assinatura</span><span class="sxs-lookup"><span data-stu-id="46b7d-122">Signature</span></span>          | <span data-ttu-id="46b7d-123">Pai</span><span class="sxs-lookup"><span data-stu-id="46b7d-123">Parent</span></span> | <span data-ttu-id="46b7d-124">Caminho</span><span class="sxs-lookup"><span data-stu-id="46b7d-124">Path</span></span>                                                    | <span data-ttu-id="46b7d-125">Profundidade</span><span class="sxs-lookup"><span data-stu-id="46b7d-125">Depth</span></span>        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | <span data-ttu-id="46b7d-126">AppFile</span><span class="sxs-lookup"><span data-stu-id="46b7d-126">AppFile</span></span><br/> |        | <span data-ttu-id="46b7d-127">C: \\ arquivos de programas \\ MyProducts \\ projetos \\ bin</span><span class="sxs-lookup"><span data-stu-id="46b7d-127">C:\\Program Files\\MyProducts\\Projects\\bin</span></span><br/> | <span data-ttu-id="46b7d-128">0</span><span class="sxs-lookup"><span data-stu-id="46b7d-128">0</span></span><br/> |

    

     

4.  <span data-ttu-id="46b7d-129">Inclua a ação AppSearch na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="46b7d-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="46b7d-130">Se MyApp.exe estiver instalado em C: \\ arquivos de programas \\ MyProducts \\ Projects \\ bin, o instalador definirá a propriedade MyApp para o local do arquivo.</span><span class="sxs-lookup"><span data-stu-id="46b7d-130">If MyApp.exe is installed in C:\\Program Files\\MyProducts\\Projects\\bin, the Installer sets the property MYAPP to the location of file.</span></span>

 

 




