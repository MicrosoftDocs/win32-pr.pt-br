---
description: Um pacote de instalação contém todas as informações que o Windows Installer requer para instalar ou desinstalar um aplicativo ou produto e executar a interface do usuário de instalação.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Pacote de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5e5ff79d0c868036dd12ed533b1cd18f9f70d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748158"
---
# <a name="installation-package"></a><span data-ttu-id="d0008-103">Pacote de instalação</span><span class="sxs-lookup"><span data-stu-id="d0008-103">Installation Package</span></span>

<span data-ttu-id="d0008-104">Um pacote de instalação contém todas as informações que o Windows Installer requer para instalar ou desinstalar um aplicativo ou produto e executar a interface do usuário de instalação.</span><span class="sxs-lookup"><span data-stu-id="d0008-104">An installation package contains all of the information that the Windows Installer requires to install or uninstall an application or product and to run the setup user interface.</span></span> <span data-ttu-id="d0008-105">Cada pacote de instalação inclui um arquivo. msi, que contém um banco de dados de instalação, um fluxo de informações resumido e os data streams para várias partes da instalação.</span><span class="sxs-lookup"><span data-stu-id="d0008-105">Each installation package includes an .msi file, containing an installation database, a summary information stream, and data streams for various parts of the installation.</span></span> <span data-ttu-id="d0008-106">O arquivo. msi também pode conter uma ou mais transformações, arquivos de origem internos e arquivos de origem externos ou arquivos de gabinete exigidos pela instalação.</span><span class="sxs-lookup"><span data-stu-id="d0008-106">The .msi file can also contain one or more transforms, internal source files, and external source files or cabinet files required by the installation.</span></span>

<span data-ttu-id="d0008-107">Os desenvolvedores de aplicativos devem criar uma instalação para usar o instalador.</span><span class="sxs-lookup"><span data-stu-id="d0008-107">Application developers must author an installation to use the installer.</span></span> <span data-ttu-id="d0008-108">Como o instalador organiza as instalações em torno do conceito de [componentes e recursos](components-and-features.md)e armazena todas as informações sobre a instalação em um banco de dados relacional, o processo de criação de um pacote de instalação envolve amplamente as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d0008-108">Because the installer organizes installations around the concept of [components and features](components-and-features.md), and stores all information about the installation in a relational database, the process of authoring an installation package broadly entails the following steps:</span></span>

-   <span data-ttu-id="d0008-109">Identifique os recursos a serem apresentados aos usuários.</span><span class="sxs-lookup"><span data-stu-id="d0008-109">Identify the features to be presented to users.</span></span>
-   <span data-ttu-id="d0008-110">Organize o aplicativo em componentes.</span><span class="sxs-lookup"><span data-stu-id="d0008-110">Organize the application into components.</span></span>
-   <span data-ttu-id="d0008-111">Preencha o banco de dados de instalação com informações.</span><span class="sxs-lookup"><span data-stu-id="d0008-111">Populate the installation database with information.</span></span>
-   <span data-ttu-id="d0008-112">Valide o pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="d0008-112">Validate the installation package.</span></span>

<span data-ttu-id="d0008-113">A próxima seção aborda os componentes e recursos do instalador.</span><span class="sxs-lookup"><span data-stu-id="d0008-113">The next section discusses installer components and features.</span></span> <span data-ttu-id="d0008-114">Para obter mais informações, consulte [componentes e recursos](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="d0008-114">For more information, see [Components and Features](components-and-features.md).</span></span> <span data-ttu-id="d0008-115">A escolha dos recursos é normalmente determinada pela funcionalidade do aplicativo da perspectiva do usuário.</span><span class="sxs-lookup"><span data-stu-id="d0008-115">The choice of features is commonly determined by the application's functionality from the user's perspective.</span></span>

<span data-ttu-id="d0008-116">É recomendável que os desenvolvedores usem um procedimento padrão para escolher componentes.</span><span class="sxs-lookup"><span data-stu-id="d0008-116">It is recommended that developers use a standard procedure for choosing components.</span></span> <span data-ttu-id="d0008-117">Para obter mais informações, consulte [organizando aplicativos em componentes](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="d0008-117">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="d0008-118">Os autores de pacote podem usar ferramentas de criação de pacote de terceiros ou um editor de tabela e o SDK do Windows Installer para preencher o banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="d0008-118">Package authors can use third-party package creation tools, or a table editor and the Windows Installer SDK, to populate the installation database.</span></span> <span data-ttu-id="d0008-119">Todos os pacotes de instalação precisam ser validados para consistência interna.</span><span class="sxs-lookup"><span data-stu-id="d0008-119">All installation packages need to be validated for internal consistency.</span></span> <span data-ttu-id="d0008-120">Para obter mais informações, consulte [validação de pacote](package-validation.md).</span><span class="sxs-lookup"><span data-stu-id="d0008-120">For more information, see [Package Validation](package-validation.md).</span></span>

 

 



