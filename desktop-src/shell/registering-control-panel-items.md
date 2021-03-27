---
description: Os itens do painel de controle devem ser registrados para que apareçam na janela do painel de controle.
title: Registrando itens do painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05c2a652314babc212e17b48198e9441f4d3465d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091718"
---
# <a name="registering-control-panel-items"></a><span data-ttu-id="3f5b3-103">Registrando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="3f5b3-103">Registering Control Panel Items</span></span>

<span data-ttu-id="3f5b3-104">Os itens do painel de controle devem ser registrados para que apareçam na janela do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="3f5b3-104">Control Panel items must be registered in order to appear in the Control Panel window.</span></span> <span data-ttu-id="3f5b3-105">Se o item do painel de controle for implementado como parte de um arquivo. exe, ele será registrado como um objeto de comando.</span><span class="sxs-lookup"><span data-stu-id="3f5b3-105">If the Control Panel item is implemented as part of a .exe file then it is registered as a command object.</span></span> <span data-ttu-id="3f5b3-106">O registro difere se o item for implementado como um arquivo. dll que exporta a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) .</span><span class="sxs-lookup"><span data-stu-id="3f5b3-106">Registration differs if the item is implemented as a .dll file that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function.</span></span>

<span data-ttu-id="3f5b3-107">Requisitos específicos são discutidos nestes tópicos:</span><span class="sxs-lookup"><span data-stu-id="3f5b3-107">Specific requirements are discussed in these topics:</span></span>

-   [<span data-ttu-id="3f5b3-108">Como registrar itens do painel de controle executável</span><span class="sxs-lookup"><span data-stu-id="3f5b3-108">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="3f5b3-109">Como registrar itens do painel de controle da DLL</span><span class="sxs-lookup"><span data-stu-id="3f5b3-109">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a><span data-ttu-id="3f5b3-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f5b3-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f5b3-111">Itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="3f5b3-111">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="3f5b3-112">Diretrizes da Experiência do Usuário</span><span class="sxs-lookup"><span data-stu-id="3f5b3-112">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="3f5b3-113">Usando CPLApplet</span><span class="sxs-lookup"><span data-stu-id="3f5b3-113">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="3f5b3-114">Processamento de mensagens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="3f5b3-114">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="3f5b3-115">Executando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="3f5b3-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="3f5b3-116">Estendendo itens do painel de controle do sistema</span><span class="sxs-lookup"><span data-stu-id="3f5b3-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="3f5b3-117">Atribuindo categorias do painel de controle</span><span class="sxs-lookup"><span data-stu-id="3f5b3-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="3f5b3-118">Criando links de tarefas pesquisáveis para um item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="3f5b3-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="3f5b3-119">Acessando o painel de controle no modo de segurança no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f5b3-119">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
