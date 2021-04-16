---
description: Obtenha um banco de dados de módulo de mesclagem em branco. Você pode usar o arquivo Schema. msm fornecido com o SDK do Windows Installer como um banco de dados inicial para o módulo de mesclagem. Para obter mais informações, consulte SDK do Windows components for Windows Installer Developers.
ms.assetid: 8408e892-adc6-4ef5-ad36-4d04c021c899
title: Obtendo bancos de dados de módulo de mesclagem em branco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba75d55763d30b0ab545d2dbddbc19c1b0c279d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757790"
---
# <a name="obtaining-blank-merge-module-databases"></a><span data-ttu-id="b8ff5-105">Obtendo bancos de dados de módulo de mesclagem em branco</span><span class="sxs-lookup"><span data-stu-id="b8ff5-105">Obtaining Blank Merge Module Databases</span></span>

<span data-ttu-id="b8ff5-106">Obtenha um banco de dados de módulo de mesclagem em branco.</span><span class="sxs-lookup"><span data-stu-id="b8ff5-106">Obtain a blank merge module database.</span></span> <span data-ttu-id="b8ff5-107">Você pode usar o arquivo Schema. msm fornecido com o SDK do Windows Installer como um banco de dados inicial para o módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="b8ff5-107">You can use the file Schema.msm provided with the Windows Installer SDK as a starting database for your merge module.</span></span> <span data-ttu-id="b8ff5-108">Para obter mais informações, consulte [SDK do Windows components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="b8ff5-108">For more information, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="b8ff5-109">Os desenvolvedores devem criar módulos de mesclagem usando o esquema de banco de dados mais simples que instala seus componentes.</span><span class="sxs-lookup"><span data-stu-id="b8ff5-109">Developers should author merge modules using the simplest database schema that installs their components.</span></span> <span data-ttu-id="b8ff5-110">O uso de um esquema simples garante a maior compatibilidade para o módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="b8ff5-110">The use of a simple schema ensures the greatest compatibility for the merge module.</span></span> <span data-ttu-id="b8ff5-111">A mesclagem de um módulo de mesclagem em um pacote de instalação com um esquema de banco de dados diferente geralmente resulta em conflitos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="b8ff5-111">Merging a merge module into an installation package with a different database schema usually results in merge conflicts.</span></span>

<span data-ttu-id="b8ff5-112">Para obter uma lista completa de todas as tabelas obrigatórias e opcionais em módulos de mesclagem, consulte [mesclar tabelas de banco de dados do módulo](merge-module-database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b8ff5-112">For a complete list of all the required and optional tables in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span>

 

 



