---
description: Por padrão, os itens do painel de controle do Windows Vista não são mostrados quando o Windows é executado no modo de segurança.
title: Acessando o painel de controle no modo de segurança
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0f7a401bbc22a7f8de3618f844bfe463fa3baa50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967366"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a><span data-ttu-id="e1753-103">Acessando o painel de controle no modo de segurança</span><span class="sxs-lookup"><span data-stu-id="e1753-103">Accessing the Control Panel in Safe Mode</span></span>

<span data-ttu-id="e1753-104">Por padrão, os itens do painel de controle do Windows Vista não são mostrados quando o Windows é executado no modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="e1753-104">By default, as of Windows Vista Control Panel items are not shown when Windows is run in safe mode.</span></span> <span data-ttu-id="e1753-105">Para permitir que um novo item do painel de controle seja exibido no modo de segurança, os valores de registro apropriados para o tipo de item podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="e1753-105">To allow a new Control Panel item to be viewed in safe mode, registry values appropriate to the item type can be set.</span></span> <span data-ttu-id="e1753-106">Os valores são interpretados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e1753-106">The values are interpreted as follows:</span></span>



| <span data-ttu-id="e1753-107">Valor</span><span class="sxs-lookup"><span data-stu-id="e1753-107">Value</span></span> | <span data-ttu-id="e1753-108">Significado</span><span class="sxs-lookup"><span data-stu-id="e1753-108">Meaning</span></span>                                                            |
|-------|--------------------------------------------------------------------|
| <span data-ttu-id="e1753-109">1</span><span class="sxs-lookup"><span data-stu-id="e1753-109">1</span></span>     | <span data-ttu-id="e1753-110">O item deve aparecer apenas no modo de segurança mínimo.</span><span class="sxs-lookup"><span data-stu-id="e1753-110">The item should appear in minimal safe mode only.</span></span>                  |
| <span data-ttu-id="e1753-111">2</span><span class="sxs-lookup"><span data-stu-id="e1753-111">2</span></span>     | <span data-ttu-id="e1753-112">O item só deverá aparecer no modo de segurança se a rede estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="e1753-112">The item should appear in safe mode only if networking is enabled.</span></span> |
| <span data-ttu-id="e1753-113">3</span><span class="sxs-lookup"><span data-stu-id="e1753-113">3</span></span>     | <span data-ttu-id="e1753-114">O item sempre deve aparecer em qualquer forma de modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="e1753-114">The item should always appear in any form of safe mode.</span></span>            |



 

<span data-ttu-id="e1753-115">Este exemplo mostra as entradas necessárias para um item implementado como um arquivo. cpl ou. dll.</span><span class="sxs-lookup"><span data-stu-id="e1753-115">This example shows the entries required for an item implemented as a .cpl or .dll file.</span></span> <span data-ttu-id="e1753-116">Ele especifica que o item deve aparecer no modo de segurança com rede.</span><span class="sxs-lookup"><span data-stu-id="e1753-116">It specifies that the item should appear in safe mode with networking.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

<span data-ttu-id="e1753-117">Este exemplo mostra as entradas necessárias para um item implementado como um arquivo. exe.</span><span class="sxs-lookup"><span data-stu-id="e1753-117">This example shows the entries required for an item implemented as a .exe file.</span></span> <span data-ttu-id="e1753-118">Ele especifica que o item deve aparecer em qualquer forma de modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="e1753-118">It specifies that the item should appear in any form of safe mode.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a><span data-ttu-id="e1753-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1753-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1753-120">Itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="e1753-120">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="e1753-121">Diretrizes da Experiência do Usuário</span><span class="sxs-lookup"><span data-stu-id="e1753-121">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="e1753-122">Registrando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="e1753-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="e1753-123">Usando CPLApplet</span><span class="sxs-lookup"><span data-stu-id="e1753-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="e1753-124">Processamento de mensagens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="e1753-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="e1753-125">Executando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="e1753-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="e1753-126">Estendendo itens do painel de controle do sistema</span><span class="sxs-lookup"><span data-stu-id="e1753-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="e1753-127">Atribuindo categorias do painel de controle</span><span class="sxs-lookup"><span data-stu-id="e1753-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="e1753-128">Criando links de tarefas pesquisáveis para um item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="e1753-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> </dl>

 

 



