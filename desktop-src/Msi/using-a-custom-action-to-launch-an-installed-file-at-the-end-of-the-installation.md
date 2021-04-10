---
description: O exemplo a seguir ilustra como iniciar um arquivo HTML no final de uma instalação.
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: Usando uma ação personalizada para iniciar um arquivo instalado no final da instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c039d58830ce6a01f76a0946bced474e5091b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170419"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a><span data-ttu-id="2cbdc-103">Usando uma ação personalizada para iniciar um arquivo instalado no final da instalação</span><span class="sxs-lookup"><span data-stu-id="2cbdc-103">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>

<span data-ttu-id="2cbdc-104">O exemplo a seguir ilustra como iniciar um arquivo HTML no final de uma instalação.</span><span class="sxs-lookup"><span data-stu-id="2cbdc-104">The following example illustrates how to launch an HTML file at the end of an installation.</span></span> <span data-ttu-id="2cbdc-105">O instalador instala o componente que contém o arquivo e, em seguida, publica um evento de controle no final da instalação para executar uma ação personalizada que abre o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2cbdc-105">The Installer installs the component that contains the file, and then publishes a control event at the end of the installation to run a custom action that opens the file.</span></span> <span data-ttu-id="2cbdc-106">Essa abordagem pode ser usada para iniciar um tutorial de ajuda no final da primeira instalação de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2cbdc-106">This approach may be used to launch a help tutorial at the end of the first installation of an application.</span></span>

<span data-ttu-id="2cbdc-107">O exemplo deve atender às especificações a seguir.</span><span class="sxs-lookup"><span data-stu-id="2cbdc-107">The sample must meet the following specifications.</span></span>

-   <span data-ttu-id="2cbdc-108">O instalador executará a ação personalizada somente se o nível [*completo da interface do usuário*](f-gly.md) for usado para instalar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2cbdc-108">The Installer executes the custom action only if the [*full UI*](f-gly.md) level is used to install an application.</span></span>
-   <span data-ttu-id="2cbdc-109">O instalador executará a ação personalizada somente se o componente que contém o arquivo HTML for instalado para ser executado localmente no computador.</span><span class="sxs-lookup"><span data-stu-id="2cbdc-109">The Installer executes the custom action only if the component that contains the HTML file is installed to run locally on the computer.</span></span>
-   <span data-ttu-id="2cbdc-110">A ação personalizada só é executada na primeira instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2cbdc-110">The custom action only runs on the first installation of the application.</span></span>
-   <span data-ttu-id="2cbdc-111">A instalação não falhará se a ação personalizada falhar.</span><span class="sxs-lookup"><span data-stu-id="2cbdc-111">The installation does not fail if the custom action fails.</span></span>

<span data-ttu-id="2cbdc-112">O exemplo inclui um componente hipotético chamado tutorial que controla pelo menos um recurso, um arquivo chamado tutorial.htm.</span><span class="sxs-lookup"><span data-stu-id="2cbdc-112">The sample includes a hypothetical component named Tutorial that controls at least one resource, a file named tutorial.htm.</span></span> <span data-ttu-id="2cbdc-113">O identificador para esse arquivo na coluna arquivo da tabela de arquivos é tutorial.</span><span class="sxs-lookup"><span data-stu-id="2cbdc-113">The identifier for this file in the File column of the File table is Tutorial.</span></span> <span data-ttu-id="2cbdc-114">A discussão a seguir pressupõe que você já criou os recursos exigidos pelo tutorial e fez todas as entradas necessárias no [recurso](feature-table.md), [componente](component-table.md), [arquivo](file-table.md), [diretório](directory-table.md)e tabelas [FeatureComponents](featurecomponents-table.md) para instalar esse componente.</span><span class="sxs-lookup"><span data-stu-id="2cbdc-114">The following discussion assumes that you have already created the resources required by Tutorial, and have made all the necessary entries in the [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md), and [FeatureComponents](featurecomponents-table.md) tables to install this component.</span></span> <span data-ttu-id="2cbdc-115">Para obter mais informações, consulte [um exemplo de instalação](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="2cbdc-115">For more information, see [An Installation Example](an-installation-example.md).</span></span>

<span data-ttu-id="2cbdc-116">Os tópicos a seguir contêm informações sobre como criar ações personalizadas necessárias e adicioná-las a um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="2cbdc-116">The following topics contain information about how to create required custom actions and add them to an installation package.</span></span>

-   [<span data-ttu-id="2cbdc-117">Criando a ação personalizada de inicialização</span><span class="sxs-lookup"><span data-stu-id="2cbdc-117">Authoring the Launch Custom Action</span></span>](authoring-the-launch-custom-action.md)
-   [<span data-ttu-id="2cbdc-118">Adicionando inicialização às tabelas CustomAction e binary</span><span class="sxs-lookup"><span data-stu-id="2cbdc-118">Adding Launch to the CustomAction and Binary Tables</span></span>](adding-launch-to-the-customaction-and-binary-tables.md)
-   [<span data-ttu-id="2cbdc-119">Adicionar um evento de controle ao final da instalação para executar a inicialização</span><span class="sxs-lookup"><span data-stu-id="2cbdc-119">Adding a Control Event at the End of the Installation to Run Launch</span></span>](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



