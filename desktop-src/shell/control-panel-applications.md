---
description: Os itens do painel de controle são DLLs ou arquivos executáveis (. exe) que permitem aos usuários configurar o ambiente do Windows. Normalmente, eles são acessados clicando em um ícone no painel de controle.
title: Implementando itens do painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2e61cbc0-fbb5-4680-8123-f8ffdcf98210
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 310d01f07d40cef69c6be30231bbf4780a1d8838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967354"
---
# <a name="implementing-control-panel-items"></a><span data-ttu-id="d4295-104">Implementando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="d4295-104">Implementing Control Panel Items</span></span>

<span data-ttu-id="d4295-105">Os itens do painel de controle são DLLs ou arquivos executáveis (. exe) que permitem aos usuários configurar o ambiente do Windows.</span><span class="sxs-lookup"><span data-stu-id="d4295-105">Control Panel items are DLLs or executable (.exe) files that let users configure the environment of Windows.</span></span> <span data-ttu-id="d4295-106">Normalmente, eles são acessados clicando em um ícone no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="d4295-106">They are typically accessed by clicking an icon in the Control Panel.</span></span>

<span data-ttu-id="d4295-107">Esta seção descreve os itens do painel de controle e explica como criá-los e registrá-los para que eles apareçam adequadamente no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="d4295-107">This section describes Control Panel items and explains how to create and register them so that they appear appropriately in the Control Panel.</span></span> <span data-ttu-id="d4295-108">Para o Windows Vista, são incluídas informações que mostram como adicionar links de tarefas que aparecem no item do painel de controle e nos resultados da pesquisa do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="d4295-108">For Windows Vista, information is included that tells you how to add task links that appear under the Control Panel item and in Control Panel search results.</span></span>

-   [<span data-ttu-id="d4295-109">Diretrizes da Experiência do Usuário</span><span class="sxs-lookup"><span data-stu-id="d4295-109">User Experience Guidelines</span></span>](user-experience-guidelines.md)
-   [<span data-ttu-id="d4295-110">Registrando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="d4295-110">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
-   [<span data-ttu-id="d4295-111">Como registrar itens do painel de controle executável</span><span class="sxs-lookup"><span data-stu-id="d4295-111">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="d4295-112">Como registrar itens do painel de controle da DLL</span><span class="sxs-lookup"><span data-stu-id="d4295-112">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
-   [<span data-ttu-id="d4295-113">Usando CPLApplet</span><span class="sxs-lookup"><span data-stu-id="d4295-113">Using CPLApplet</span></span>](using-cplapplet.md)
-   [<span data-ttu-id="d4295-114">Processamento de mensagens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="d4295-114">Control Panel Message Processing</span></span>](message-processing.md)
-   [<span data-ttu-id="d4295-115">Executando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="d4295-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
-   [<span data-ttu-id="d4295-116">Estendendo itens do painel de controle do sistema</span><span class="sxs-lookup"><span data-stu-id="d4295-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
-   [<span data-ttu-id="d4295-117">Atribuindo categorias do painel de controle</span><span class="sxs-lookup"><span data-stu-id="d4295-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
-   [<span data-ttu-id="d4295-118">Criando links de tarefas pesquisáveis para um item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="d4295-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
-   [<span data-ttu-id="d4295-119">Acessando o painel de controle no modo de segurança</span><span class="sxs-lookup"><span data-stu-id="d4295-119">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
-   [<span data-ttu-id="d4295-120">Nomes canônicos de itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="d4295-120">Canonical Names of Control Panel Items</span></span>](controlpanel-canonical-names.md)

 

 



