---
description: Um pacote de 64 bits consiste parcialmente ou totalmente em componentes de Windows Installer de 64 bits.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: Pacotes de Windows Installer de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b34c8ff7ce4809dc44932cc8a5daa978b6ff66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828100"
---
# <a name="64-bit-windows-installer-packages"></a><span data-ttu-id="d0cd7-103">Pacotes de Windows Installer de 64 bits</span><span class="sxs-lookup"><span data-stu-id="d0cd7-103">64-bit Windows Installer Packages</span></span>

<span data-ttu-id="d0cd7-104">Um pacote de 64 bits consiste parcialmente ou totalmente em componentes de [Windows Installer](windows-installer-components.md) de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d0cd7-104">A 64-bit package consists partially or entirely of 64-bit [Windows Installer](windows-installer-components.md) components.</span></span> <span data-ttu-id="d0cd7-105">A lista a seguir identifica os requisitos para cada pacote de Windows Installer de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="d0cd7-105">The following list identifies the requirements for every 64-bit Windows Installer package:</span></span>

-   <span data-ttu-id="d0cd7-106">O valor "Intel64" deve ser inserido no campo plataforma da propriedade [**Resumo do modelo**](template-summary.md) se e somente se o pacote for executado em um processador Intel64 (Itanium).</span><span class="sxs-lookup"><span data-stu-id="d0cd7-106">The value "Intel64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Intel64 (Itanium) processor.</span></span>
-   <span data-ttu-id="d0cd7-107">O valor "x64" deve ser inserido no campo plataforma da propriedade [**Resumo do modelo**](template-summary.md) se e somente se o pacote for executado em um processador x64.</span><span class="sxs-lookup"><span data-stu-id="d0cd7-107">The value "x64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an x64 processor.</span></span>
-   <span data-ttu-id="d0cd7-108">O valor "Arm64" deve ser inserido no campo plataforma da propriedade [**Resumo do modelo**](template-summary.md) se e somente se o pacote for executado em um processador Arm64.</span><span class="sxs-lookup"><span data-stu-id="d0cd7-108">The value "Arm64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Arm64 processor.</span></span>
-   <span data-ttu-id="d0cd7-109">A propriedade de [**Resumo contagem de páginas**](page-count-summary.md) deve ser definida como o número inteiro 200 ou maior, porque Windows Installer 2,0 é a versão mínima que é capaz de instalar os componentes da 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d0cd7-109">The [**Page Count Summary**](page-count-summary.md) property must be set to the integer 200 or greater, because Windows Installer 2.0 is the minimum version that is capable of installing 64-bit components.</span></span> <span data-ttu-id="d0cd7-110">Os pacotes para a plataforma Arm64 exigem um valor de 500 ou superior.</span><span class="sxs-lookup"><span data-stu-id="d0cd7-110">Packages for the Arm64 platform require a value of 500 or greater.</span></span>
-   <span data-ttu-id="d0cd7-111">Cada componente de Windows Installer de 64 bits no pacote deve incluir o bit **msidbComponentAttributes64bit** na coluna Attributes da [tabela Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d0cd7-111">Each 64-bit Windows Installer component in the package must include the **msidbComponentAttributes64bit** bit in the Attributes column of the [Component Table](component-table.md).</span></span>

<span data-ttu-id="d0cd7-112">Para obter mais informações, consulte [Windows Installer em sistemas operacionais de 64 bits](windows-installer-on-64-bit-operating-systems.md) e [pacotes de Windows Installer de 32 bits](32-bit-windows-installer-packages.md).</span><span class="sxs-lookup"><span data-stu-id="d0cd7-112">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md) and [32-bit Windows Installer Packages](32-bit-windows-installer-packages.md).</span></span>

 

 



