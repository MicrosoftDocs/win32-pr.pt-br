---
description: Durante uma instalação de Windows Installer, o instalador pode pesquisar por um arquivo em todas as unidades fixas.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Pesquisando todas as unidades fixas de um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b79c7f2999d4ee7937790dc68470210f1d4b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758765"
---
# <a name="searching-all-fixed-drives-for-a-file"></a><span data-ttu-id="a1c0e-103">Pesquisando todas as unidades fixas de um arquivo</span><span class="sxs-lookup"><span data-stu-id="a1c0e-103">Searching All Fixed Drives for a File</span></span>

<span data-ttu-id="a1c0e-104">**Para pesquisar todas as unidades fixas de um arquivo**</span><span class="sxs-lookup"><span data-stu-id="a1c0e-104">**To search all fixed drives for a file**</span></span>

1.  <span data-ttu-id="a1c0e-105">Insira a assinatura e o nome do arquivo na [tabela de assinatura](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="a1c0e-105">Enter the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="a1c0e-106">Os campos restantes nesse registro podem ser nulos para pesquisar qualquer versão do MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="a1c0e-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="a1c0e-107">[Tabela de assinatura](signature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="a1c0e-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="a1c0e-108">Assinatura</span><span class="sxs-lookup"><span data-stu-id="a1c0e-108">Signature</span></span>          | <span data-ttu-id="a1c0e-109">Nome do Arquivo</span><span class="sxs-lookup"><span data-stu-id="a1c0e-109">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="a1c0e-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="a1c0e-110">AppFile</span></span><br/> | <span data-ttu-id="a1c0e-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="a1c0e-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="a1c0e-112">Insira a propriedade que o instalador deve definir se MyApp.exe estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="a1c0e-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    [<span data-ttu-id="a1c0e-113">Tabela AppSearch</span><span class="sxs-lookup"><span data-stu-id="a1c0e-113">AppSearch Table</span></span>](appsearch-table.md)

    

    | <span data-ttu-id="a1c0e-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a1c0e-114">Property</span></span>         | <span data-ttu-id="a1c0e-115">Assinatura</span><span class="sxs-lookup"><span data-stu-id="a1c0e-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="a1c0e-116">MYAPP</span><span class="sxs-lookup"><span data-stu-id="a1c0e-116">MYAPP</span></span><br/> | <span data-ttu-id="a1c0e-117">AppFile</span><span class="sxs-lookup"><span data-stu-id="a1c0e-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="a1c0e-118">Use a [tabela DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="a1c0e-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="a1c0e-119">Deixe os campos pai e caminho vazios para pesquisar todas as unidades fixas do sistema de usuário.</span><span class="sxs-lookup"><span data-stu-id="a1c0e-119">Leave the Parent and Path fields empty to search all fixed drives of the user system.</span></span> <span data-ttu-id="a1c0e-120">Especifique na coluna profundidade o número de níveis de subdiretório a serem pesquisados.</span><span class="sxs-lookup"><span data-stu-id="a1c0e-120">Specify in the Depth column the number of subdirectory levels to search.</span></span> <span data-ttu-id="a1c0e-121">Por exemplo, a definição de profundidade como 0 detecta c: \\MyApp.exe, mas não detecta o arquivo em uma profundidade de 2, por exemplo: c: \\ arquivos de programas \\ myapps \\MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="a1c0e-121">For example, setting Depth to 0 detects c:\\MyApp.exe, but does not detect the file at a depth of 2, for example: c:\\Program Files\\MyApps\\MyApp.exe.</span></span>

    [<span data-ttu-id="a1c0e-122">Tabela DrLocator</span><span class="sxs-lookup"><span data-stu-id="a1c0e-122">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="a1c0e-123">Assinatura</span><span class="sxs-lookup"><span data-stu-id="a1c0e-123">Signature</span></span>          | <span data-ttu-id="a1c0e-124">Pai</span><span class="sxs-lookup"><span data-stu-id="a1c0e-124">Parent</span></span> | <span data-ttu-id="a1c0e-125">Caminho</span><span class="sxs-lookup"><span data-stu-id="a1c0e-125">Path</span></span> | <span data-ttu-id="a1c0e-126">Profundidade</span><span class="sxs-lookup"><span data-stu-id="a1c0e-126">Depth</span></span>        |
    |--------------------|--------|------|--------------|
    | <span data-ttu-id="a1c0e-127">AppFile</span><span class="sxs-lookup"><span data-stu-id="a1c0e-127">AppFile</span></span><br/> |        |      | <span data-ttu-id="a1c0e-128">3</span><span class="sxs-lookup"><span data-stu-id="a1c0e-128">3</span></span><br/> |

    

     

4.  <span data-ttu-id="a1c0e-129">Inclua a ação AppSearch na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="a1c0e-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="a1c0e-130">Se MyApp.exe estiver instalado, o instalador definirá a propriedade MYAPP para o local do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a1c0e-130">If MyApp.exe is installed, the Installer sets the property MYAPP to the location of the file.</span></span> <span data-ttu-id="a1c0e-131">Se o arquivo estiver instalado, MYAPP será avaliado como true em uma expressão condicional.</span><span class="sxs-lookup"><span data-stu-id="a1c0e-131">If the file is installed, MYAPP evaluates as True in a conditional expression.</span></span>

 

 




