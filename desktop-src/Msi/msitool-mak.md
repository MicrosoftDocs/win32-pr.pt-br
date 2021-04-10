---
description: Msitool. Mak é um makefile que você pode usar para criar ferramentas e ações personalizadas.
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: Msitool. Mak
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3dad9fd65aaa880e9fdb38369843907104dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091450"
---
# <a name="msitoolmak"></a><span data-ttu-id="2d2f2-103">Msitool. Mak</span><span class="sxs-lookup"><span data-stu-id="2d2f2-103">Msitool.mak</span></span>

<span data-ttu-id="2d2f2-104">Msitool. Mak é um makefile que você pode usar para criar ferramentas e ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2d2f2-104">Msitool.mak is a makefile that you can use to build tools and custom actions.</span></span> <span data-ttu-id="2d2f2-105">Ele pode ser usado com Visual C++ versão 4,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2d2f2-105">It may be used with Visual C++ version 4.0 or later.</span></span> <span data-ttu-id="2d2f2-106">Para obter mais informações, consulte o arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="2d2f2-106">For more information, see the header file.</span></span> <span data-ttu-id="2d2f2-107">Ele requer um conjunto de valores a serem definidos antes de incluir esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d2f2-107">It requires a set of values to be defined before including this file.</span></span> <span data-ttu-id="2d2f2-108">Normalmente, os desenvolvedores colocam esses no início do. cpp, ifdef deve ser ignorado pelo compilador do C.</span><span class="sxs-lookup"><span data-stu-id="2d2f2-108">Typically developers put those at the start of the .cpp, ifdef'd to be skipped by the C compiler.</span></span> <span data-ttu-id="2d2f2-109">Da mesma forma, os recursos são adicionados ao final do arquivo. cpp.</span><span class="sxs-lookup"><span data-stu-id="2d2f2-109">Likewise resources are added to the end of the .cpp file.</span></span> <span data-ttu-id="2d2f2-110">Consulte os exemplos para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="2d2f2-110">See samples for details.</span></span>

<span data-ttu-id="2d2f2-111">VCBIN pode ser definido para o diretório onde as ferramentas de Visual C++ são encontradas ou o makefile usa MSVCDIR e MSDEVDIR.</span><span class="sxs-lookup"><span data-stu-id="2d2f2-111">VCBIN can be defined to the directory where the Visual C++ tools are found or the makefile uses MSVCDIR and MSDEVDIR.</span></span> <span data-ttu-id="2d2f2-112">Se eles não estiverem definidos, ele não especificará um local, supondo que as ferramentas estejam no caminho.</span><span class="sxs-lookup"><span data-stu-id="2d2f2-112">If those are not defined, it does not specify a location, assuming the tools to be on the PATH.</span></span> <span data-ttu-id="2d2f2-113">Um problema com as variáveis de ambiente no Visual C++ versão 5,0 é que, se ambos não estiverem no caminho, o vinculador não poderá encontrar Msdis100.dll.</span><span class="sxs-lookup"><span data-stu-id="2d2f2-113">An issue with the environment variables in Visual C++ version 5.0 is that if both are not on you path, the linker cannot find Msdis100.dll.</span></span> <span data-ttu-id="2d2f2-114">Se você copiá-lo de MSDEVDIR para MSVCDIR, ele funcionará.</span><span class="sxs-lookup"><span data-stu-id="2d2f2-114">If you copy that from MSDEVDIR to MSVCDIR, it works.</span></span> <span data-ttu-id="2d2f2-115">A outra opção é copiar Msdis100.dll e Rc.exe e Rcdll.dll para MSVCDIR e definir VCBIN para isso.</span><span class="sxs-lookup"><span data-stu-id="2d2f2-115">The other option is to copy Msdis100.dll and Rc.exe and Rcdll.dll to MSVCDIR, and set VCBIN to that.</span></span>

<span data-ttu-id="2d2f2-116">Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="2d2f2-116">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d2f2-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d2f2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d2f2-118">Ferramentas de desenvolvimento Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2d2f2-118">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="2d2f2-119">Versões, ferramentas e redistribuíveis liberados</span><span class="sxs-lookup"><span data-stu-id="2d2f2-119">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



