---
description: O arquivo VBScript WiGenXfm.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este script de exemplo pode gerar uma transformação de dois bancos de dados Windows Installer. Para obter mais informações, consulte transformações de banco de dados.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Gerar uma transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92617c2e007b9deb01685679d4940095285b8218
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662536"
---
# <a name="generate-a-transform"></a><span data-ttu-id="c0ade-105">Gerar uma transformação</span><span class="sxs-lookup"><span data-stu-id="c0ade-105">Generate a Transform</span></span>

<span data-ttu-id="c0ade-106">O arquivo VBScript WiGenXfm.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="c0ade-106">The VBScript file WiGenXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="c0ade-107">Este script de exemplo pode gerar uma transformação de dois bancos de dados Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c0ade-107">This sample script can generate a transform from two Windows Installer databases.</span></span> <span data-ttu-id="c0ade-108">Para obter mais informações, consulte [transformações de banco de dados](database-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="c0ade-108">For more information see [Database Transforms](database-transforms.md).</span></span>

<span data-ttu-id="c0ade-109">O exemplo demonstra o uso de:</span><span class="sxs-lookup"><span data-stu-id="c0ade-109">The sample demonstrates the use of:</span></span>

[<span data-ttu-id="c0ade-110">**Método OpenDatabase (objeto instalador)**</span><span class="sxs-lookup"><span data-stu-id="c0ade-110">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)

<span data-ttu-id="c0ade-111">[**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="c0ade-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="c0ade-112">[**Método GenerateTransform**](database-generatetransform.md) do [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="c0ade-112">[**GenerateTransform method**](database-generatetransform.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="c0ade-113">Você precisará da versão CScript.exe ou WScript.exe do Windows Script Host para usar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="c0ade-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="c0ade-114">Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0ade-114">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="c0ade-115">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="c0ade-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="c0ade-116">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="c0ade-116">or if too few arguments are specified.</span></span> <span data-ttu-id="c0ade-117">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .</span><span class="sxs-lookup"><span data-stu-id="c0ade-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="c0ade-118">O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="c0ade-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="c0ade-119">**cscript WiGenXfm.vbs \[ caminho para o caminho do banco de dados original \] \[ para o caminho do banco de dados revisado \] \[ para transformar\]**</span><span class="sxs-lookup"><span data-stu-id="c0ade-119">**cscript WiGenXfm.vbs \[path to original database\]\[path to revised database\]\[path to transform file\]**</span></span>

<span data-ttu-id="c0ade-120">Especifique o caminho para o banco de dados de Windows Installer original.</span><span class="sxs-lookup"><span data-stu-id="c0ade-120">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="c0ade-121">Especifique o caminho para o banco de dados revisado.</span><span class="sxs-lookup"><span data-stu-id="c0ade-121">Specify the path to the revised database.</span></span> <span data-ttu-id="c0ade-122">Especifique o caminho para o arquivo de transformação a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c0ade-122">Specify the path to the transform file to be created.</span></span> <span data-ttu-id="c0ade-123">Se o caminho para o arquivo de transformação for omitido, os dois bancos de dados serão comparados apenas.</span><span class="sxs-lookup"><span data-stu-id="c0ade-123">If the path to the transform file is omitted, the two databases are only compared.</span></span>

<span data-ttu-id="c0ade-124">Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="c0ade-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="c0ade-125">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="c0ade-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="c0ade-126">Observe que [um exemplo de localização](a-localization-example.md) demonstra [a geração de uma transformação de personalização](generating-a-customization-transform.md).</span><span class="sxs-lookup"><span data-stu-id="c0ade-126">Note that [A Localization Example](a-localization-example.md) demonstrates [Generating a Customization Transform](generating-a-customization-transform.md).</span></span>

 

 



