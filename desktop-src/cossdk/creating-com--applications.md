---
description: Criando aplicativos COM+
ms.assetid: 32828d4d-aa98-4e6a-b7de-2ec832024517
title: Criando aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42a4b7ad18dab3f7163f527626322e05671e7be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793234"
---
# <a name="creating-com-applications"></a><span data-ttu-id="46c69-103">Criando aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="46c69-103">Creating COM+ Applications</span></span>

<span data-ttu-id="46c69-104">Esta seção descreve como criar um novo aplicativo COM+ (vazio) e, em seguida, adicionar componentes a esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46c69-104">This section describes how to create a new (empty) COM+ application and then add components to that application.</span></span> <span data-ttu-id="46c69-105">Ele também descreve como adicionar componentes COM e removê-los de aplicativos COM+ existentes e como mover e copiar componentes de um aplicativo COM+ para outro.</span><span class="sxs-lookup"><span data-stu-id="46c69-105">It also describes how to add COM components to, and remove them from, existing COM+ applications, and how to move and copy components from one COM+ application to another.</span></span>



| <span data-ttu-id="46c69-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="46c69-106">Topic</span></span>                                                                                                       | <span data-ttu-id="46c69-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="46c69-107">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="46c69-108">Criando um novo aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="46c69-108">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)<br/>                           | <span data-ttu-id="46c69-109">Descreve como criar um novo aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="46c69-109">Describes how to create a new COM+ application.</span></span><br/>                         |
| [<span data-ttu-id="46c69-110">Instalando novos componentes</span><span class="sxs-lookup"><span data-stu-id="46c69-110">Installing New Components</span></span>](installing-new-components.md)<br/>                                       | <span data-ttu-id="46c69-111">Descreve como instalar novos componentes do.</span><span class="sxs-lookup"><span data-stu-id="46c69-111">Describes how to install new components.</span></span><br/>                                |
| [<span data-ttu-id="46c69-112">Importando componentes</span><span class="sxs-lookup"><span data-stu-id="46c69-112">Importing Components</span></span>](importing-components.md)<br/>                                                 | <span data-ttu-id="46c69-113">Descreve como importar componentes do.</span><span class="sxs-lookup"><span data-stu-id="46c69-113">Describes how to import components.</span></span><br/>                                     |
| [<span data-ttu-id="46c69-114">Removendo um componente de um aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="46c69-114">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)<br/> | <span data-ttu-id="46c69-115">Descreve como excluir um componente de um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="46c69-115">Describes how to delete a component from a COM+ application.</span></span><br/>            |
| [<span data-ttu-id="46c69-116">Movendo componentes</span><span class="sxs-lookup"><span data-stu-id="46c69-116">Moving Components</span></span>](moving-components.md)<br/>                                                       | <span data-ttu-id="46c69-117">Descreve como mover um componente de um aplicativo COM+ para outro.</span><span class="sxs-lookup"><span data-stu-id="46c69-117">Describes how to move a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="46c69-118">Copiando componentes</span><span class="sxs-lookup"><span data-stu-id="46c69-118">Copying Components</span></span>](copying-components.md)<br/>                                                     | <span data-ttu-id="46c69-119">Descreve como copiar um componente de um aplicativo COM+ para outro.</span><span class="sxs-lookup"><span data-stu-id="46c69-119">Describes how to copy a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="46c69-120">Excluindo um aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="46c69-120">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)<br/>                                   | <span data-ttu-id="46c69-121">Descreve como excluir um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="46c69-121">Describes how to delete a COM+ application.</span></span><br/>                             |



 

<span data-ttu-id="46c69-122">Para obter informações conceituais sobre os procedimentos descritos nesta seção, consulte [visão geral do aplicativo com+](com--application-overview.md) e [Implantando aplicativos com+](deploying-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="46c69-122">For conceptual information on the procedures described in this section, see [COM+ Application Overview](com--application-overview.md) and [Deploying COM+ Applications](deploying-com--applications.md).</span></span>

<span data-ttu-id="46c69-123">Para obter informações de procedimento sobre as tarefas administrativas envolvidas na exportação e instalação de aplicativos COM+, consulte "Instalando aplicativos COM+" no guia do administrador de serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="46c69-123">For procedural information on the administrative tasks involved in exporting and installing COM+ applications, see "Installing COM+ Applications" in the Component Services Administrator's Guide.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46c69-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="46c69-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46c69-125">Automatizando a administração do COM+</span><span class="sxs-lookup"><span data-stu-id="46c69-125">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="46c69-126">Configurando aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="46c69-126">Configuring COM+ Applications</span></span>](configuring-com--applications.md)
</dt> <dt>

[<span data-ttu-id="46c69-127">Conversão de pacotes MTS em aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="46c69-127">Conversion of MTS Packages to COM+ Applications</span></span>](conversion-of-mts-packages-to-com--applications.md)
</dt> </dl>

 

 




