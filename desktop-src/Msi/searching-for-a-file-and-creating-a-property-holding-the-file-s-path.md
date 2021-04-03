---
description: Durante uma instalação de Windows Installer, o instalador pode pesquisar um arquivo e criar uma propriedade que contém o caminho do arquivo.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Procurando um arquivo e criando uma propriedade que contém o caminho do arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed742ee874c2e4b76137e9f17e90fbf54e9729f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828862"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a><span data-ttu-id="3df5e-103">Procurando um arquivo e criando uma propriedade que contém o caminho do arquivo</span><span class="sxs-lookup"><span data-stu-id="3df5e-103">Searching for a File and Creating a Property Holding the File's Path</span></span>

<span data-ttu-id="3df5e-104">**Para pesquisar um arquivo e criar uma propriedade que contém o caminho do arquivo**</span><span class="sxs-lookup"><span data-stu-id="3df5e-104">**To search for a file and create a property holding the path of that file**</span></span>

1.  <span data-ttu-id="3df5e-105">Primeiro, faça uma pesquisa para o arquivo, listando a assinatura e o nome do arquivo na [tabela de assinatura](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="3df5e-105">First do a search for the file by listing the file signature and name in the [Signature Table](signature-table.md).</span></span>

    <span data-ttu-id="3df5e-106">Os campos restantes desse registro podem ser deixados em branco para especificar uma pesquisa de qualquer versão do MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="3df5e-106">The remaining fields of this record can be left empty to specify a search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="3df5e-107">[Tabela de assinatura](signature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="3df5e-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="3df5e-108">Assinatura</span><span class="sxs-lookup"><span data-stu-id="3df5e-108">Signature</span></span>          | <span data-ttu-id="3df5e-109">Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="3df5e-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="3df5e-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="3df5e-110">AppFile</span></span><br/> | <span data-ttu-id="3df5e-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="3df5e-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="3df5e-112">Em seguida, especifique o caminho do arquivo que está sendo pesquisado na [tabela DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="3df5e-112">Next, specify the path of the file that is being searched for in the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="3df5e-113">Como AppFolder não está listado na [tabela de assinatura](signature-table.md), o instalador determina que AppFolder é uma pasta em vez de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3df5e-113">Because AppFolder is not listed in the [Signature Table](signature-table.md), the Installer determines that AppFolder is a folder rather than a file.</span></span>

    [<span data-ttu-id="3df5e-114">Tabela DrLocator</span><span class="sxs-lookup"><span data-stu-id="3df5e-114">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="3df5e-115">Assinatura</span><span class="sxs-lookup"><span data-stu-id="3df5e-115">Signature</span></span>            | <span data-ttu-id="3df5e-116">Pai</span><span class="sxs-lookup"><span data-stu-id="3df5e-116">Parent</span></span>             | <span data-ttu-id="3df5e-117">Caminho</span><span class="sxs-lookup"><span data-stu-id="3df5e-117">Path</span></span> | <span data-ttu-id="3df5e-118">Profundidade</span><span class="sxs-lookup"><span data-stu-id="3df5e-118">Depth</span></span> |
    |----------------------|--------------------|------|-------|
    | <span data-ttu-id="3df5e-119">AppFile</span><span class="sxs-lookup"><span data-stu-id="3df5e-119">AppFile</span></span><br/>   |                    |      |       |
    | <span data-ttu-id="3df5e-120">AppFolder</span><span class="sxs-lookup"><span data-stu-id="3df5e-120">AppFolder</span></span><br/> | <span data-ttu-id="3df5e-121">AppFile</span><span class="sxs-lookup"><span data-stu-id="3df5e-121">AppFile</span></span><br/> |      |       |

    

     

3.  <span data-ttu-id="3df5e-122">Por fim, preencha a [tabela AppSearch](appsearch-table.md) para que a [ação AppSearch](appsearch-action.md) retorne o caminho de AppFolder.</span><span class="sxs-lookup"><span data-stu-id="3df5e-122">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the path of AppFolder.</span></span>

    <span data-ttu-id="3df5e-123">Depois que o instalador executar a ação AppSearch, o valor de MyFolder será o caminho completo de AppFolder.</span><span class="sxs-lookup"><span data-stu-id="3df5e-123">After the Installer executes the AppSearch action, the value of MYFOLDER is the full path of AppFolder.</span></span>

    <span data-ttu-id="3df5e-124">[Tabela AppSearch](appsearch-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="3df5e-124">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="3df5e-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3df5e-125">Property</span></span>            | <span data-ttu-id="3df5e-126">Assinatura</span><span class="sxs-lookup"><span data-stu-id="3df5e-126">Signature</span></span>            |
    |---------------------|----------------------|
    | <span data-ttu-id="3df5e-127">MYFOLDER</span><span class="sxs-lookup"><span data-stu-id="3df5e-127">MYFOLDER</span></span><br/> | <span data-ttu-id="3df5e-128">AppFolder</span><span class="sxs-lookup"><span data-stu-id="3df5e-128">AppFolder</span></span><br/> |

    

     

 

 




