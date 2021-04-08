---
description: Um componente é uma parte do aplicativo ou produto a ser instalado.
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Componentes do Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad90f2fb576d0333a26fc92f9cf951e4da06bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922012"
---
# <a name="windows-installer-components"></a><span data-ttu-id="c0ccb-103">Componentes do Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c0ccb-103">Windows Installer Components</span></span>

<span data-ttu-id="c0ccb-104">Um componente é uma parte do aplicativo ou produto a ser instalado.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-104">A component is a piece of the application or product to be installed.</span></span> <span data-ttu-id="c0ccb-105">Exemplos de componentes incluem arquivos únicos, um grupo de arquivos relacionados, objetos COM, registro, chaves do registro, atalhos, recursos, bibliotecas agrupadas em um diretório ou partes compartilhadas de código como MFC ou DAO.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-105">Examples of components include single files, a group of related files, COM objects, registration, registry keys, shortcuts, resources, libraries grouped into a directory, or shared pieces of code such as MFC or DAO.</span></span>

<span data-ttu-id="c0ccb-106">O serviço instalador instala ou remove um componente como uma única parte coerente.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-106">The installer service installs or removes a component as a single coherent piece.</span></span> <span data-ttu-id="c0ccb-107">Ele controla cada componente pelo respectivo GUID de ID de componente especificado na coluna ComponentID da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="c0ccb-107">It tracks every component by the respective component ID GUID specified in the ComponentId column of the [Component table](component-table.md).</span></span>

> [!Note]  
> <span data-ttu-id="c0ccb-108">Dois componentes que compartilham a mesma ID de componente são tratados como várias instâncias do mesmo componente, independentemente de seu conteúdo real.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-108">Two components that share the same component ID are treated as multiple instances of the same component regardless of their actual content.</span></span> <span data-ttu-id="c0ccb-109">Apenas uma única instância de qualquer componente é instalada no computador de um usuário.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-109">Only a single instance of any component is installed on a user's computer.</span></span> <span data-ttu-id="c0ccb-110">Por isso, vários recursos ou aplicativos podem compartilhar alguns componentes.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-110">Several features or applications may therefore share some components.</span></span>

 

<span data-ttu-id="c0ccb-111">Como os componentes são normalmente compartilhados, o autor de um pacote de instalação deve seguir regras estritas ao especificar os componentes de um recurso ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-111">Because components are commonly shared, the author of an installation package must follow strict rules when specifying the components of a feature or application.</span></span> <span data-ttu-id="c0ccb-112">Isso é essencial para a operação correta do mecanismo de contagem de referência Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-112">This is essential for the correct operation of the Windows Installer reference-counting mechanism.</span></span> <span data-ttu-id="c0ccb-113">Para obter mais informações, consulte [organizando aplicativos em componentes](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="c0ccb-113">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="c0ccb-114">Em resumo, essas regras são:</span><span class="sxs-lookup"><span data-stu-id="c0ccb-114">In brief, these rules are:</span></span>

-   <span data-ttu-id="c0ccb-115">Cada componente deve ser armazenado em uma única pasta.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-115">Each component must be stored in a single folder.</span></span>
-   <span data-ttu-id="c0ccb-116">Nenhum arquivo, entrada de registro, atalho ou outros recursos já devem ser enviados como um membro de mais de um componente.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-116">No file, registry entry, shortcut, or other resources should ever be shipped as a member of more than one component.</span></span> <span data-ttu-id="c0ccb-117">Isso se aplica a produtos, versões de produtos e empresas.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-117">This applies across products, product versions, and companies.</span></span>

<span data-ttu-id="c0ccb-118">Para obter mais informações sobre como usar componentes, consulte</span><span class="sxs-lookup"><span data-stu-id="c0ccb-118">For more information about using components, see</span></span>

-   [<span data-ttu-id="c0ccb-119">Instalando um componente ausente</span><span class="sxs-lookup"><span data-stu-id="c0ccb-119">Installing a Missing Component</span></span>](installing-a-missing-component.md)
-   [<span data-ttu-id="c0ccb-120">Instalando componentes, arquivos, fontes e chaves do registro permanentes</span><span class="sxs-lookup"><span data-stu-id="c0ccb-120">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
-   [<span data-ttu-id="c0ccb-121">Usando componentes qualificados</span><span class="sxs-lookup"><span data-stu-id="c0ccb-121">Using Qualified Components</span></span>](using-qualified-components.md)
-   [<span data-ttu-id="c0ccb-122">Usando componentes transitivos</span><span class="sxs-lookup"><span data-stu-id="c0ccb-122">Using Transitive Components</span></span>](using-transitive-components.md)
-   [<span data-ttu-id="c0ccb-123">Trabalhando com recursos e componentes</span><span class="sxs-lookup"><span data-stu-id="c0ccb-123">Working with Features and Components</span></span>](working-with-features-and-components.md)
-   [<span data-ttu-id="c0ccb-124">Criando um pacote grande</span><span class="sxs-lookup"><span data-stu-id="c0ccb-124">Authoring a Large Package</span></span>](authoring-a-large-package.md)
-   [<span data-ttu-id="c0ccb-125">Verificando a instalação de recursos, componentes, arquivos</span><span class="sxs-lookup"><span data-stu-id="c0ccb-125">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
-   [<span data-ttu-id="c0ccb-126">Pesquisando um componente ou recurso desfeito</span><span class="sxs-lookup"><span data-stu-id="c0ccb-126">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
-   [<span data-ttu-id="c0ccb-127">Publicando produtos, recursos e componentes</span><span class="sxs-lookup"><span data-stu-id="c0ccb-127">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)

 

 



