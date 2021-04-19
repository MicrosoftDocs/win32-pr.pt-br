---
description: O Windows Installer mantém todas as informações sobre a instalação em um banco de dados relacional. Você pode modificar esse banco de dados e, portanto, a instalação, usando transformações e mesclagens.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Mesclagens e transformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec6314e81afb5afa9d74346b64fe3129ba5ed30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748152"
---
# <a name="merges-and-transforms"></a><span data-ttu-id="ab595-104">Mesclagens e transformações</span><span class="sxs-lookup"><span data-stu-id="ab595-104">Merges and Transforms</span></span>

<span data-ttu-id="ab595-105">O Windows Installer mantém todas as informações sobre a instalação em um banco de dados relacional.</span><span class="sxs-lookup"><span data-stu-id="ab595-105">The Windows Installer keeps all information about the installation in a relational database.</span></span> <span data-ttu-id="ab595-106">Você pode modificar esse banco de dados e, portanto, a instalação, usando transformações e mesclagens.</span><span class="sxs-lookup"><span data-stu-id="ab595-106">You can modify this database, and therefore the installation, by using transforms and merges.</span></span>

## <a name="transforms"></a><span data-ttu-id="ab595-107">Transformações</span><span class="sxs-lookup"><span data-stu-id="ab595-107">Transforms</span></span>

<span data-ttu-id="ab595-108">Uma [transformação de banco de dados](database-transforms.md) adiciona ou substitui elementos no banco de dados original.</span><span class="sxs-lookup"><span data-stu-id="ab595-108">A [database transform](database-transforms.md) adds or replaces elements in the original database.</span></span> <span data-ttu-id="ab595-109">Por exemplo, uma transformação pode alterar todo o texto na interface do usuário de um aplicativo de francês para inglês.</span><span class="sxs-lookup"><span data-stu-id="ab595-109">For example, a transform can change all of the text in an application's user interface from French to English.</span></span>

<span data-ttu-id="ab595-110">Os usos primários para transformações incluem:</span><span class="sxs-lookup"><span data-stu-id="ab595-110">Primary uses for transforms include:</span></span>

-   <span data-ttu-id="ab595-111">Personalização de pacotes de instalação base para determinados grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="ab595-111">Customization of base installation packages for particular groups of users.</span></span>

    <span data-ttu-id="ab595-112">As transformações podem ser usadas para encapsular as várias personalizações de um único pacote base exigido por diferentes grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="ab595-112">Transforms can be used to encapsulate the various customizations of a single base package that are required by different groups of users.</span></span> <span data-ttu-id="ab595-113">Por exemplo, isso é útil em organizações nas quais os departamentos de suporte da equipe e Finanças exigem diferentes instalações de um produto específico.</span><span class="sxs-lookup"><span data-stu-id="ab595-113">For example, this is useful in organizations where the finance and staff support departments require different installations of a particular product.</span></span> <span data-ttu-id="ab595-114">O pacote base de um produto pode estar disponível para todos em um ponto de instalação administrativa com personalizações apropriadas distribuídas para cada grupo de usuários separadamente.</span><span class="sxs-lookup"><span data-stu-id="ab595-114">A product's base package can be available to everyone at one administrative installation point with appropriate customizations distributed to each group of users separately.</span></span>

-   <span data-ttu-id="ab595-115">Sincronização de aplicativos entre linguagens.</span><span class="sxs-lookup"><span data-stu-id="ab595-115">Synchronization of applications across languages.</span></span>

    <span data-ttu-id="ab595-116">As transformações são úteis para manter os pacotes criados em locais amplamente separados sincronizados durante a criação.</span><span class="sxs-lookup"><span data-stu-id="ab595-116">Transforms are useful for keeping packages authored at widely separated locations synchronized during authoring.</span></span> <span data-ttu-id="ab595-117">Por exemplo, se uma atualização for desenvolvida primeiro para uma versão em inglês de um aplicativo que existe em inglês e francês, uma transformação poderá ser aplicada à versão em inglês atualizada que a converte em uma versão em francês atualizada.</span><span class="sxs-lookup"><span data-stu-id="ab595-117">For example, if an upgrade is first developed for an English version of an application that exists in English and French, a transform can be applied to the upgraded English version that converts it into an upgraded French version.</span></span>

    <span data-ttu-id="ab595-118">Várias transformações podem ser aplicadas a um pacote base e, em seguida, aplicadas imediatamente durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="ab595-118">Multiple transforms can be applied to a base package and then applied on-the-fly during installation.</span></span> <span data-ttu-id="ab595-119">Isso estende os recursos do instalador para criar pacotes personalizados e fornece um mecanismo para atribuir com eficiência as instalações mais apropriadas a diferentes grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="ab595-119">This extends the capabilities of the installer to create custom packages and provides a mechanism for efficiently assigning the most appropriate installations to different groups of users.</span></span>

-   <span data-ttu-id="ab595-120">Aplicação de patches em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ab595-120">Patching applications.</span></span>

    <span data-ttu-id="ab595-121">As transformações podem ser usadas para aplicar uma correção secundária a um aplicativo que não garante uma atualização importante.</span><span class="sxs-lookup"><span data-stu-id="ab595-121">Transforms can be used to apply a minor fix to an application that does not warrant a major upgrade.</span></span> <span data-ttu-id="ab595-122">Para obter mais informações sobre patches, consulte [pacotes de patches](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="ab595-122">For more information about patches, see [Patch Packages](patch-packages.md).</span></span>

## <a name="merges"></a><span data-ttu-id="ab595-123">Mesclagens</span><span class="sxs-lookup"><span data-stu-id="ab595-123">Merges</span></span>

<span data-ttu-id="ab595-124">Uma mesclagem combina dois bancos de dados em um único e adiciona, em vez de substituir, informações.</span><span class="sxs-lookup"><span data-stu-id="ab595-124">A merge combines two databases into one database, and adds, rather than replaces, information.</span></span> <span data-ttu-id="ab595-125">Se as mesmas informações existirem em ambos os bancos de dados, ocorrerá um conflito de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="ab595-125">If the same information exists in both databases, a merge conflict occurs.</span></span> <span data-ttu-id="ab595-126">As mesclagens são úteis para as equipes de desenvolvimento porque permitem que um aplicativo grande seja dividido em partes que podem ser recombinadas mais tarde.</span><span class="sxs-lookup"><span data-stu-id="ab595-126">Merges are useful to development teams because they allow a large application to be divided into parts that can be recombined later.</span></span> <span data-ttu-id="ab595-127">Por exemplo, os elementos de banco de dados para a instalação de um novo componente podem ser desenvolvidos separadamente e posteriormente mesclados no banco de dados de instalação principal.</span><span class="sxs-lookup"><span data-stu-id="ab595-127">For example, the database elements for the installation of a new component can be developed separately and later merged into the main installation database.</span></span> <span data-ttu-id="ab595-128">Para obter mais informações, consulte [Mesclar módulos](merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="ab595-128">For more information, see [Merge Modules](merge-modules.md).</span></span>

<span data-ttu-id="ab595-129">Uma equipe de desenvolvimento pode aplicar uma operação de mesclagem da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ab595-129">A development team might apply a merge operation in the following way:</span></span>

1.  <span data-ttu-id="ab595-130">Separe em grupos e trabalhe simultaneamente em diferentes componentes de um aplicativo grande.</span><span class="sxs-lookup"><span data-stu-id="ab595-130">Separate into groups and work simultaneously on different components of a large application.</span></span>
2.  <span data-ttu-id="ab595-131">Em seguida, cada grupo de desenvolvimento popula um banco de dados com informações de instalação para seu próprio componente, sem se preocupar com os outros componentes do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ab595-131">Each development group then populates a database with installation information for its own component, without being concerned with the other components of the application.</span></span>
3.  <span data-ttu-id="ab595-132">Após a conclusão do desenvolvimento de um componente, o banco de dados desse componente poderá ser mesclado no banco de dados de instalação principal do aplicativo inteiro.</span><span class="sxs-lookup"><span data-stu-id="ab595-132">After the development of a component is complete, that component's database can be merged into the main installation database for the entire application.</span></span>

 

 



