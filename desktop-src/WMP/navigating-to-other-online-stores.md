---
title: Navegando para outras lojas online
description: Navegando para outras lojas online
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Lojas online do Windows Media Player, navegando
- lojas online, navegando
- Digite 2 lojas online, navegando
- navegando no tipo 2 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8456954d5a7197a054098320b35fb38409ba62
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291762"
---
# <a name="navigating-to-other-online-stores"></a><span data-ttu-id="fe68a-107">Navegando para outras lojas online</span><span class="sxs-lookup"><span data-stu-id="fe68a-107">Navigating to Other Online Stores</span></span>

<span data-ttu-id="fe68a-108">Você pode criar links para outras lojas online que você possui ou entre links para lojas online fornecidas por outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="fe68a-108">You can create links to other online stores you own or cross-link to online stores provided by others.</span></span> <span data-ttu-id="fe68a-109">Para fazer isso, você precisa saber o nome da chave para a loja online na qual deseja navegar.</span><span class="sxs-lookup"><span data-stu-id="fe68a-109">To do this, you need to know the key name for the online store to which you want to navigate.</span></span>

<span data-ttu-id="fe68a-110">O código de exemplo a seguir mostra o HTML que cria um link para alternar da loja online da Proseware para o recurso "ServiceTask2" da loja online de vídeo Southridge:</span><span class="sxs-lookup"><span data-stu-id="fe68a-110">The following example code shows HTML that creates a link to switch from the Proseware online store to the "ServiceTask2" feature of the Southridge Video online store:</span></span>


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



<span data-ttu-id="fe68a-111">Quando o usuário clica no link, o Windows Media Player solicita que o usuário alterne para o armazenamento de vídeo Southridge.</span><span class="sxs-lookup"><span data-stu-id="fe68a-111">When the user clicks the link, Windows Media Player prompts the user to switch to the Southridge Video store.</span></span> <span data-ttu-id="fe68a-112">Se o usuário permitir, o Player alternará os armazenamentos e navegará até o painel de tarefas especificado, acrescentando os parâmetros da cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="fe68a-112">If the user permits it, the Player then switches stores and navigates to the specified task pane, appending the query string parameters.</span></span> <span data-ttu-id="fe68a-113">Os parâmetros de cadeia de caracteres de consulta mostrados no exemplo anterior são parâmetros personalizados.</span><span class="sxs-lookup"><span data-stu-id="fe68a-113">The query string parameters shown in the preceding example are custom parameters.</span></span> <span data-ttu-id="fe68a-114">Isso significa que a loja online que você alterna para deve esperar esses valores e tratá-los.</span><span class="sxs-lookup"><span data-stu-id="fe68a-114">This means that the online store you switch to must expect these values and handle them.</span></span> <span data-ttu-id="fe68a-115">Sua loja online (e qualquer loja que você alternar para) pode usar parâmetros de cadeia de caracteres de consulta da maneira que você escolher.</span><span class="sxs-lookup"><span data-stu-id="fe68a-115">Your online store (and any store you switch to) can use query string parameters any way you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe68a-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe68a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe68a-117">**Navegando entre os painéis de tarefas de serviço**</span><span class="sxs-lookup"><span data-stu-id="fe68a-117">**Navigating between Service Task Panes**</span></span>](navigating-between-service-task-panes.md)
</dt> <dt>

[<span data-ttu-id="fe68a-118">**Navegação para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="fe68a-118">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




