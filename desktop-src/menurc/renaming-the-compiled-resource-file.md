---
title: Renomeando o arquivo de recurso compilado
description: Por padrão, ao compilar recursos, o RC nomeia o arquivo de recurso compilado (. res) com o nome base do arquivo. rc e o coloca no mesmo diretório que o arquivo. rc.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c54e22cff753dbc59cbce61cd71874c8fe77a85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159368"
---
# <a name="renaming-the-compiled-resource-file"></a><span data-ttu-id="da024-103">Renomeando o arquivo de recurso compilado</span><span class="sxs-lookup"><span data-stu-id="da024-103">Renaming the Compiled Resource File</span></span>

<span data-ttu-id="da024-104">Por padrão, ao compilar recursos, o RC nomeia o arquivo de recurso compilado (. res) com o nome base do arquivo. rc e o coloca no mesmo diretório que o arquivo. rc.</span><span class="sxs-lookup"><span data-stu-id="da024-104">By default, when compiling resources, RC names the compiled resource (.res) file with the base name of the .rc file and places it in the same directory as the .rc file.</span></span> <span data-ttu-id="da024-105">CVTRES deve ser chamado para converter o arquivo. res em um formato de recurso binário (. RBJ) que pode ser compreendido pelo vinculador.</span><span class="sxs-lookup"><span data-stu-id="da024-105">CVTRES must then be invoked to convert the .res file to a binary resource (.rbj) format which can be understood by the linker.</span></span> <span data-ttu-id="da024-106">O exemplo a seguir compila MyApp. rc e cria um arquivo de recurso compilado chamado MyApp. res no mesmo diretório que MyApp. rc:</span><span class="sxs-lookup"><span data-stu-id="da024-106">The following example compiles MyApp.rc and creates a compiled resource file named MyApp.res in the same directory as MyApp.rc:</span></span>

<span data-ttu-id="da024-107">**RC MyApp. rc**</span><span class="sxs-lookup"><span data-stu-id="da024-107">**rc myapp.rc**</span></span>

<span data-ttu-id="da024-108">A opção **/fo** dá ao arquivo. res resultante um nome que difere do nome do arquivo. rc correspondente.</span><span class="sxs-lookup"><span data-stu-id="da024-108">The **/fo** option gives the resulting .res file a name that differs from the name of the corresponding .rc file.</span></span> <span data-ttu-id="da024-109">Por exemplo, para nomear o arquivo. res NewFile. res, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="da024-109">For example, to name the resulting .res file NewFile.res, use the following command:</span></span>

<span data-ttu-id="da024-110">**RC-fo newfile. res MyApp. rc**</span><span class="sxs-lookup"><span data-stu-id="da024-110">**rc -fo newfile.res myapp.rc**</span></span>

<span data-ttu-id="da024-111">A opção **/fo** também pode posicionar o arquivo. res em um diretório diferente.</span><span class="sxs-lookup"><span data-stu-id="da024-111">The **/fo** option can also place the .res file in a different directory.</span></span> <span data-ttu-id="da024-112">Por exemplo, o comando a seguir coloca o arquivo de recurso compilado MyApp. res no diretório C \\ : \\ recurso de origem:</span><span class="sxs-lookup"><span data-stu-id="da024-112">For example, the following command places the compiled resource file MyApp.res in the directory C:\\Source\\Resource:</span></span>

<span data-ttu-id="da024-113">**RC-fo c: \\ recurso de origem \\ \\ MyApp. res MyApp. rc**</span><span class="sxs-lookup"><span data-stu-id="da024-113">**rc -fo c:\\source\\resource\\myapp.res myapp.rc**</span></span>

 

 




