---
description: O arquivo VBScript WiLstPrd.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. O script de exemplo se conecta a um objeto do instalador e enumera os produtos registrados e as informações do produto.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Listar produtos, propriedades, recursos e componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20d2f563efad42108f763b909e7a1118e255dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789774"
---
# <a name="list-products-properties-features-and-components"></a><span data-ttu-id="820c3-104">Listar produtos, propriedades, recursos e componentes</span><span class="sxs-lookup"><span data-stu-id="820c3-104">List Products, Properties, Features, and Components</span></span>

<span data-ttu-id="820c3-105">O arquivo VBScript WiLstPrd.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="820c3-105">The VBScript file WiLstPrd.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="820c3-106">O script de exemplo se conecta a um objeto do [**instalador**](installer-object.md) e enumera os produtos registrados e as informações do produto.</span><span class="sxs-lookup"><span data-stu-id="820c3-106">The sample script connects to an [**Installer**](installer-object.md) object and enumerates registered products and product information.</span></span>

<span data-ttu-id="820c3-107">Este exemplo demonstra o uso de:</span><span class="sxs-lookup"><span data-stu-id="820c3-107">This sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="820c3-108">**Propriedade ProductInfo**</span><span class="sxs-lookup"><span data-stu-id="820c3-108">**ProductInfo property**</span></span>](installer-productinfo.md)
-   [<span data-ttu-id="820c3-109">**Propriedade productstate (objeto do instalador)**</span><span class="sxs-lookup"><span data-stu-id="820c3-109">**ProductState property (Installer object)**</span></span>](installer-productstate-property.md)
-   [<span data-ttu-id="820c3-110">**Propriedade Products**</span><span class="sxs-lookup"><span data-stu-id="820c3-110">**Products property**</span></span>](installer-products.md)
-   [<span data-ttu-id="820c3-111">**Propriedade Features**</span><span class="sxs-lookup"><span data-stu-id="820c3-111">**Features property**</span></span>](installer-features.md)
-   [<span data-ttu-id="820c3-112">**Propriedade FeatureParent**</span><span class="sxs-lookup"><span data-stu-id="820c3-112">**FeatureParent property**</span></span>](installer-featureparent.md)
-   [<span data-ttu-id="820c3-113">**Propriedade featurestate**</span><span class="sxs-lookup"><span data-stu-id="820c3-113">**FeatureState property**</span></span>](installer-featurestate.md)
-   [<span data-ttu-id="820c3-114">**Propriedade Components**</span><span class="sxs-lookup"><span data-stu-id="820c3-114">**Components property**</span></span>](installer-components.md)
-   [<span data-ttu-id="820c3-115">**Propriedade ComponentClients**</span><span class="sxs-lookup"><span data-stu-id="820c3-115">**ComponentClients property**</span></span>](installer-componentclients.md)
-   [<span data-ttu-id="820c3-116">**Propriedade ComponentPath**</span><span class="sxs-lookup"><span data-stu-id="820c3-116">**ComponentPath property**</span></span>](installer-componentpath.md)
-   [<span data-ttu-id="820c3-117">**Método LastErrorRecord**</span><span class="sxs-lookup"><span data-stu-id="820c3-117">**LastErrorRecord method**</span></span>](installer-lasterrorrecord.md)
-   <span data-ttu-id="820c3-118">[**Método REGISTRYVALUE**](installer-registryvalue.md) do [ **objeto instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="820c3-118">[**RegistryValue method**](installer-registryvalue.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="820c3-119">Você precisará da versão CScript.exe ou WScript.exe do Windows Script Host para usar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="820c3-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="820c3-120">Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="820c3-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="820c3-121">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="820c3-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="820c3-122">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="820c3-122">or if too few arguments are specified.</span></span> <span data-ttu-id="820c3-123">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ caminho para o arquivo \] .</span><span class="sxs-lookup"><span data-stu-id="820c3-123">To redirect the output to a file, end the command line with VBS > \[path to file\].</span></span> <span data-ttu-id="820c3-124">O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="820c3-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="820c3-125">**cscript WiLstPrd.vbs \[ Opções de nome do produto \] \[\]**</span><span class="sxs-lookup"><span data-stu-id="820c3-125">**cscript WiLstPrd.vbs \[Product Name\] \[options\]**</span></span>

<span data-ttu-id="820c3-126">Especifique o nome do produto que não diferencia maiúsculas de minúsculas ou o GUID da ID do produto do produto instalado ou anunciado.</span><span class="sxs-lookup"><span data-stu-id="820c3-126">Specify the case-insensitive product name or the product ID GUID of the installed or advertised product.</span></span> <span data-ttu-id="820c3-127">Se nenhum produto ou opção for especificado, o instalador listará todos os produtos instalados ou anunciados no sistema.</span><span class="sxs-lookup"><span data-stu-id="820c3-127">If no product or options are specified, the installer lists all the products installed or advertised on the system.</span></span>

<span data-ttu-id="820c3-128">Observe que essas opções não são opções, portanto, você não deve prefixar-as com uma barra (/) na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="820c3-128">Note that these options are not switches so you should not prefix them with a slash (/) on the commandline.</span></span> <span data-ttu-id="820c3-129">As opções a seguir podem ser combinadas concatenando as letras.</span><span class="sxs-lookup"><span data-stu-id="820c3-129">The following options may be combined by concatenating the letters.</span></span> <span data-ttu-id="820c3-130">Por exemplo, "PC" para listar as propriedades dos produtos e os componentes instalados.</span><span class="sxs-lookup"><span data-stu-id="820c3-130">For example, "pc" to list both the products' properties and installed components.</span></span>



| <span data-ttu-id="820c3-131">Opção</span><span class="sxs-lookup"><span data-stu-id="820c3-131">Option</span></span>               | <span data-ttu-id="820c3-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="820c3-132">Description</span></span>                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="820c3-133">nenhuma opção especificada</span><span class="sxs-lookup"><span data-stu-id="820c3-133">no options specified</span></span> | <span data-ttu-id="820c3-134">Listar as propriedades dos produtos.</span><span class="sxs-lookup"><span data-stu-id="820c3-134">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="820c3-135">p</span><span class="sxs-lookup"><span data-stu-id="820c3-135">p</span></span>                    | <span data-ttu-id="820c3-136">Listar as propriedades dos produtos.</span><span class="sxs-lookup"><span data-stu-id="820c3-136">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="820c3-137">f</span><span class="sxs-lookup"><span data-stu-id="820c3-137">f</span></span>                    | <span data-ttu-id="820c3-138">Listar os recursos dos produtos, os pais de recursos e os Estados de instalação</span><span class="sxs-lookup"><span data-stu-id="820c3-138">List the products' features, feature parents, and installation states</span></span>                                                                 |
| <span data-ttu-id="820c3-139">c</span><span class="sxs-lookup"><span data-stu-id="820c3-139">c</span></span>                    | <span data-ttu-id="820c3-140">Lista os componentes instalados dos produtos.</span><span class="sxs-lookup"><span data-stu-id="820c3-140">List the products' installed components.</span></span>                                                                                              |
| <span data-ttu-id="820c3-141">d</span><span class="sxs-lookup"><span data-stu-id="820c3-141">d</span></span>                    | <span data-ttu-id="820c3-142">Liste o valor em **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ SharedDlls** para os arquivos de chave do componente Products.</span><span class="sxs-lookup"><span data-stu-id="820c3-142">List the value under **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\SharedDlls** for the key files of the products' component.</span></span> |



 

<span data-ttu-id="820c3-143">Para obter mais informações, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md) para obter exemplos de script adicionais.</span><span class="sxs-lookup"><span data-stu-id="820c3-143">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="820c3-144">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="820c3-144">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



