---
description: Módulos TopoEdit
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Módulos TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010803"
---
# <a name="topoedit-modules"></a><span data-ttu-id="69513-103">Módulos TopoEdit</span><span class="sxs-lookup"><span data-stu-id="69513-103">TopoEdit Modules</span></span>

<span data-ttu-id="69513-104">A ferramenta TopoEdit é fornecida com o SDK do Windows para Windows Server 2008 e posterior.</span><span class="sxs-lookup"><span data-stu-id="69513-104">The TopoEdit tool is provided with the Windows SDK for Windows Server 2008 and later.</span></span> <span data-ttu-id="69513-105">A ferramenta requer o Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="69513-105">The tool requires Windows Vista or later.</span></span>

<span data-ttu-id="69513-106">Os módulos TopoEdit estão localizados na pasta bin do SDK.</span><span class="sxs-lookup"><span data-stu-id="69513-106">The TopoEdit modules are located in the Bin folder of the SDK.</span></span> <span data-ttu-id="69513-107">Esses módulos são:</span><span class="sxs-lookup"><span data-stu-id="69513-107">These modules are:</span></span>

-   <span data-ttu-id="69513-108">TopoEdit.exe — executável do aplicativo</span><span class="sxs-lookup"><span data-stu-id="69513-108">TopoEdit.exe—Application executable</span></span>
-   <span data-ttu-id="69513-109">TEDUTIL.dll — DLL de extensão</span><span class="sxs-lookup"><span data-stu-id="69513-109">TEDUTIL.dll—Extension DLL</span></span>

<span data-ttu-id="69513-110">A instalação do SDK registra a DLL.</span><span class="sxs-lookup"><span data-stu-id="69513-110">The SDK installation registers the DLL.</span></span> <span data-ttu-id="69513-111">No entanto, se isso falhar, em um prompt de comando, execute o seguinte.</span><span class="sxs-lookup"><span data-stu-id="69513-111">However, if this fails, at a command prompt, run the following.</span></span>


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



<span data-ttu-id="69513-112">O código-fonte para TopoEdit também é fornecido como um exemplo na SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="69513-112">Source code for TopoEdit is also provided as a sample in the Windows SDK.</span></span> <span data-ttu-id="69513-113">Ele está localizado no seguinte diretório:</span><span class="sxs-lookup"><span data-stu-id="69513-113">It is located in the following directory:</span></span>

<span data-ttu-id="69513-114"><samples root>\\Multimídia \\ Media Foundation \\ TopoEdit</span><span class="sxs-lookup"><span data-stu-id="69513-114"><samples root>\\Multimedia\\Media Foundation\\TopoEdit</span></span>

## <a name="related-topics"></a><span data-ttu-id="69513-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="69513-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69513-116">Introdução ao TopoEdit</span><span class="sxs-lookup"><span data-stu-id="69513-116">Introduction to TopoEdit</span></span>](introduction-to-topoedit.md)
</dt> <dt>

[<span data-ttu-id="69513-117">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="69513-117">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



