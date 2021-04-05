---
description: Siga estas diretrizes ao criar um módulo de mesclagem de 64 bits.
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: Usando módulos de mesclagem de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662590"
---
# <a name="using-64-bit-merge-modules"></a><span data-ttu-id="87241-103">Usando módulos de mesclagem de 64 bits</span><span class="sxs-lookup"><span data-stu-id="87241-103">Using 64-bit Merge Modules</span></span>

<span data-ttu-id="87241-104">Um módulo de mesclagem de 64 bits tem qualquer uma das características identificadas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="87241-104">A 64-bit merge module has any of the characteristics identified in this this topic.</span></span>

-   <span data-ttu-id="87241-105">O módulo de mesclagem contém pelo menos um componente que foi compilado para sistemas operacionais de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="87241-105">The merge module contains at least one component that has been compiled for 64-bit operating systems.</span></span>
-   <span data-ttu-id="87241-106">O módulo de mesclagem não contém nenhum componente de 64 bits, mas destina-se ao uso somente com pacotes [de Windows Installer de 64 bits](64-bit-windows-installer-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="87241-106">The merge module contains no 64-bit components, but is intended for use only with [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>

<span data-ttu-id="87241-107">Os módulos de mesclagem podem ser usados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="87241-107">Merge modules can be used as follows:</span></span>

-   <span data-ttu-id="87241-108">Um módulo de mesclagem de 64 bits pode ser mesclado em um pacote de [Windows Installer de 64 bits](64-bit-windows-installer-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="87241-108">A 64-bit merge module can be merged into a [64-bit Windows Installer](64-bit-windows-installer-packages.md) package.</span></span> <span data-ttu-id="87241-109">As propriedades de [**Resumo do modelo**](template-summary.md) no módulo de mesclagem e no pacote de Windows Installer devem ser definidas para o mesmo tipo de processador de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="87241-109">The [**Template Summary**](template-summary.md) properties in the merge module and in the Windows Installer package must be set to the same type of 64-bit processor.</span></span> <span data-ttu-id="87241-110">Um módulo de mesclagem x64 pode ser mesclado somente em pacotes x64 e um módulo de mesclagem Intel64 pode ser mesclado somente em pacotes Intel64.</span><span class="sxs-lookup"><span data-stu-id="87241-110">A x64 merge module can be merged only into x64 packages and an Intel64 merge module can be merged only into Intel64 packages.</span></span>
-   <span data-ttu-id="87241-111">Um módulo de mesclagem de 32 bits pode ser mesclado em pacotes de Windows Installer de 32 bits ou [64 bits](64-bit-windows-installer-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="87241-111">A 32-bit merge module can be merged into 32-bit or [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>
-   <span data-ttu-id="87241-112">Um módulo de mesclagem de 64 bits pode ser mesclado em um pacote de 64 bits em um sistema operacional de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="87241-112">A 64-bit merge module can be merged into a 64-bit package on a 32-bit operating system.</span></span>

<span data-ttu-id="87241-113">Siga o seguinte ao criar um módulo de mesclagem de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="87241-113">Adhere to the following when authoring a 64-bit merge module:</span></span>

-   <span data-ttu-id="87241-114">Use o mesmo procedimento geral de criação de módulos de mesclagem de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="87241-114">Use the same general procedure as when authoring 32-bit merge modules.</span></span> <span data-ttu-id="87241-115">Para obter informações, consulte [sobre módulos de mesclagem](about-merge-modules.md) e [criação de módulos de mesclagem](authoring-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="87241-115">For information, see [About Merge Modules](about-merge-modules.md) and [Authoring Merge Modules](authoring-merge-modules.md).</span></span>
-   <span data-ttu-id="87241-116">Você deve definir a propriedade de [**Resumo do modelo**](template-summary.md) com o valor Intel64 se estiver executando um sistema Intel64.</span><span class="sxs-lookup"><span data-stu-id="87241-116">You must set the [**Template Summary**](template-summary.md) property with the Intel64 value if running an Intel64 system.</span></span> <span data-ttu-id="87241-117">Você deve definir a propriedade de **Resumo do modelo** com o valor x64 se estiver executando um sistema x64.</span><span class="sxs-lookup"><span data-stu-id="87241-117">You must set the **Template Summary** property with the x64 value if running an x64 system.</span></span> <span data-ttu-id="87241-118">Para obter informações, consulte [referência de fluxo de informações de resumo do módulo de mesclagem](merge-module-summary-information-stream-reference.md).</span><span class="sxs-lookup"><span data-stu-id="87241-118">For information see [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md).</span></span>
-   <span data-ttu-id="87241-119">Quando existirem módulos de mesclagem de 32 bits e 64 bits para o mesmo componente, é recomendável que os módulos tenham assinaturas diferentes.</span><span class="sxs-lookup"><span data-stu-id="87241-119">When both 32-bit and 64-bit merge modules exist for the same component, it is recommended that the modules have different signatures.</span></span> <span data-ttu-id="87241-120">Isso permitirá que um pacote contenha as duas versões do componente.</span><span class="sxs-lookup"><span data-stu-id="87241-120">This will enable a package to contain both versions of the component.</span></span>

<span data-ttu-id="87241-121">Para obter mais informações, consulte [Windows Installer em sistemas operacionais de 64 bits](windows-installer-on-64-bit-operating-systems.md).</span><span class="sxs-lookup"><span data-stu-id="87241-121">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md).</span></span>

 

 



