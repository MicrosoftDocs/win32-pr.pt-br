---
description: Este exemplo ilustra como localizar o pacote de Windows Installer descrito em um exemplo de instalação. O pacote de instalação original é alterado de uma versão em inglês para o idioma francês.
ms.assetid: b14787fe-3179-47d7-8a15-da45987d613f
title: Um exemplo de localização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5ae0b04e65383d665e2532d45f0cc2eed856a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768490"
---
# <a name="a-localization-example"></a><span data-ttu-id="96a2d-104">Um exemplo de localização</span><span class="sxs-lookup"><span data-stu-id="96a2d-104">A Localization Example</span></span>

<span data-ttu-id="96a2d-105">Este exemplo ilustra como localizar o pacote de Windows Installer descrito em [um exemplo de instalação](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="96a2d-105">This example illustrates how to localize the Windows Installer package described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="96a2d-106">O pacote de instalação original é alterado de uma versão em inglês para o idioma francês.</span><span class="sxs-lookup"><span data-stu-id="96a2d-106">The original installation package is changed from an English into French language version.</span></span>

<span data-ttu-id="96a2d-107">O exemplo de localização tem as seguintes especificações:</span><span class="sxs-lookup"><span data-stu-id="96a2d-107">The localization sample has the following specifications:</span></span>

-   <span data-ttu-id="96a2d-108">A interface do usuário de instalação do aplicativo MNP2000 deve ser alterada de Inglês para francês.</span><span class="sxs-lookup"><span data-stu-id="96a2d-108">The installation UI for the application MNP2000 should be changed from English to French.</span></span>
-   <span data-ttu-id="96a2d-109">A versão em francês do MNP2000 inclui arquivos de Readme.txt e Help.txt escritos no idioma francês.</span><span class="sxs-lookup"><span data-stu-id="96a2d-109">The French version of MNP2000 includes Readme.txt and Help.txt files written in the French language.</span></span>
-   <span data-ttu-id="96a2d-110">A versão em francês inclui uma lista de agentes de viagem na França que podem fornecer tíquetes para a arena do Parque vermelho.</span><span class="sxs-lookup"><span data-stu-id="96a2d-110">The French version includes a list of travel agents in France that can provide tickets to Red Park Arena.</span></span> <span data-ttu-id="96a2d-111">Essa lista (fornecida como um novo arquivo, Fre.txt) não faz parte da versão em inglês.</span><span class="sxs-lookup"><span data-stu-id="96a2d-111">This list (provided as a new file, Fre.txt) is not a part of the English version.</span></span>

<span data-ttu-id="96a2d-112">O procedimento geral para localizar uma instalação é descrito na seção [localizando um pacote de Windows Installer](localizing-a-windows-installer-package.md).</span><span class="sxs-lookup"><span data-stu-id="96a2d-112">The general procedure for localizing an installation is described in the section [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span></span>

<span data-ttu-id="96a2d-113">Copie a versão em inglês do MNP2000.msi e todos os arquivos de origem descritos em [planejando a instalação](planning-the-installation.md) em uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="96a2d-113">Copy the English version of MNP2000.msi and all the source files described in [Planning the Installation](planning-the-installation.md) into a new folder.</span></span> <span data-ttu-id="96a2d-114">Altere o nome do MNP2000.msi na pasta para MNPFren.msi.</span><span class="sxs-lookup"><span data-stu-id="96a2d-114">Change the name of the MNP2000.msi in the folder to MNPFren.msi.</span></span> <span data-ttu-id="96a2d-115">Nas seções a seguir, você modificará essa cópia para localizar o aplicativo em francês.</span><span class="sxs-lookup"><span data-stu-id="96a2d-115">In the following sections you will modify this copy to localize the application into French.</span></span>

[<span data-ttu-id="96a2d-116">Continuar</span><span class="sxs-lookup"><span data-stu-id="96a2d-116">Continue</span></span>](checking-the-installation-database-code-page.md)

 

 



