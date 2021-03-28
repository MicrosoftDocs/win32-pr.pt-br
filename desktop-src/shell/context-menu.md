---
description: Esta seção discute a criação de menus de atalho (contexto) e a implementação de manipuladores de menu de atalho (verbo).
title: Menus de atalho (contexto) e manipuladores de menu de atalho
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 286dd9c860ae79e5124439439da97f206b4aa436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164314"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a><span data-ttu-id="92408-103">Menus de atalho (contexto) e manipuladores de menu de atalho</span><span class="sxs-lookup"><span data-stu-id="92408-103">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>

<span data-ttu-id="92408-104">Esta seção discute a criação de menus de atalho (contexto) e a implementação de manipuladores de menu de atalho (verbo).</span><span class="sxs-lookup"><span data-stu-id="92408-104">This section discusses the creation of shortcut (context) menus, and the implementation of shortcut menu (verb) handlers.</span></span>

<span data-ttu-id="92408-105">Esta seção sobre tipos de arquivo e associações de arquivo é organizada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="92408-105">This section on file types and file associations is organized as follows:</span></span>

-   [<span data-ttu-id="92408-106">Verbos e associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="92408-106">Verbs and File Associations</span></span>](fa-verbs.md)
-   [<span data-ttu-id="92408-107">Escolhendo um método de menu de atalho estático ou dinâmico</span><span class="sxs-lookup"><span data-stu-id="92408-107">Choosing a Static or Dynamic Shortcut Menu Method</span></span>](shortcut-choose-method.md)
-   [<span data-ttu-id="92408-108">Práticas recomendadas para manipuladores de menu de atalho e vários verbos</span><span class="sxs-lookup"><span data-stu-id="92408-108">Best Practices for Shortcut Menu Handlers and Multiple Verbs</span></span>](verbs-best-practices.md)
-   [<span data-ttu-id="92408-109">Criando manipuladores de menu de atalho</span><span class="sxs-lookup"><span data-stu-id="92408-109">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
-   [<span data-ttu-id="92408-110">Criando menus em cascata estáticos</span><span class="sxs-lookup"><span data-stu-id="92408-110">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
-   [<span data-ttu-id="92408-111">Como suprimir e controlar a visibilidade de verbo</span><span class="sxs-lookup"><span data-stu-id="92408-111">How to Suppress and Control Verb Visibility</span></span>](how-to-suppress-and-control-visibility.md)
-   [<span data-ttu-id="92408-112">Como empregar o modelo de seleção de verbo</span><span class="sxs-lookup"><span data-stu-id="92408-112">How to Employ the Verb Selection Model</span></span>](how-to-employ-the-verb-selection-model.md)
-   [<span data-ttu-id="92408-113">Como usar atributos de item</span><span class="sxs-lookup"><span data-stu-id="92408-113">How to Use Item Attributes</span></span>](how-to-use-item-attributes.md)
-   [<span data-ttu-id="92408-114">Como implementar verbos personalizados para pastas por meio de Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="92408-114">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [<span data-ttu-id="92408-115">Personalizando um menu de atalho usando verbos dinâmicos</span><span class="sxs-lookup"><span data-stu-id="92408-115">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
-   [<span data-ttu-id="92408-116">Como implementar a interface IContextMenu</span><span class="sxs-lookup"><span data-stu-id="92408-116">How to Implement the IContextMenu Interface</span></span>](how-to-implement-the-icontextmenu-interface.md)
-   [<span data-ttu-id="92408-117">Referência do menu de atalho</span><span class="sxs-lookup"><span data-stu-id="92408-117">Shortcut Menu Reference</span></span>](context-menu-reference.md)

## <a name="additional-resources"></a><span data-ttu-id="92408-118">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="92408-118">Additional Resources</span></span>

<span data-ttu-id="92408-119">Para obter informações conceituais relacionadas, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="92408-119">For related conceptual background, see the following topics:</span></span>

-   <span data-ttu-id="92408-120">[Introdução às associações de arquivo](fa-intro.md).</span><span class="sxs-lookup"><span data-stu-id="92408-120">[Introduction to File Associations](fa-intro.md).</span></span>
-   <span data-ttu-id="92408-121">Para estender o shell com manipuladores de tipo de arquivo, consulte [criando manipuladores de extensão de shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="92408-121">To extend the Shell with file type handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>
-   <span data-ttu-id="92408-122">Para criar um armazenamento de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](nse-implement.md).</span><span class="sxs-lookup"><span data-stu-id="92408-122">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

<span data-ttu-id="92408-123">Para obter documentação de referência relacionada, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="92408-123">For related reference documenation, see the following topics:</span></span>

-   <span data-ttu-id="92408-124">Para executar um verbo em um item de Shell, consulte o método [**InvokeVerb**](folderitem-invokeverb.md) .</span><span class="sxs-lookup"><span data-stu-id="92408-124">To execute a verb on a Shell item, see the [**InvokeVerb**](folderitem-invokeverb.md) method.</span></span>
-   <span data-ttu-id="92408-125">Para recuperar uma coleção de verbos que podem ser executados em um item de Shell, consulte o método [**Verbs**](folderitem-verbs.md) .</span><span class="sxs-lookup"><span data-stu-id="92408-125">To retrieve a collection of verbs that can be executed on a Shell item, see the [**Verbs**](folderitem-verbs.md) method.</span></span>
-   <span data-ttu-id="92408-126">Para executar uma operação em um arquivo especificado, consulte as funções [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="92408-126">To perform an operation on a specified file, see either the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) functions.</span></span>

 

 



