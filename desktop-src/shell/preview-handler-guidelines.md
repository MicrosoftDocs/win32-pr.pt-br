---
description: Quando você fornece uma visualização, as diretrizes a seguir devem ser seguidas.
title: Diretrizes do Gerenciador de visualização
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e725d561056e78a88bd9eeabd00d90abda1f0343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828906"
---
# <a name="preview-handler-guidelines"></a><span data-ttu-id="329ba-103">Diretrizes do Gerenciador de visualização</span><span class="sxs-lookup"><span data-stu-id="329ba-103">Preview Handler Guidelines</span></span>

<span data-ttu-id="329ba-104">Quando você fornece uma visualização, as diretrizes a seguir devem ser seguidas.</span><span class="sxs-lookup"><span data-stu-id="329ba-104">When you provide a preview, the following guidelines should be followed.</span></span>

-   <span data-ttu-id="329ba-105">Uma visualização deve conter a interface do usuário mínima — é simplesmente uma visualização.</span><span class="sxs-lookup"><span data-stu-id="329ba-105">A preview should contain minimal UI—it is simply a preview.</span></span> <span data-ttu-id="329ba-106">Ele deve exibir apenas o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="329ba-106">It should display only the file content.</span></span> <span data-ttu-id="329ba-107">Ele não deve exibir caixas de diálogo, telas de abertura, barras de ferramentas ou painéis de tarefas.</span><span class="sxs-lookup"><span data-stu-id="329ba-107">It should not display dialogs, splash screens, toolbars, or task panes.</span></span> <span data-ttu-id="329ba-108">O painel de leitura normalmente será usado em conjunto com a pesquisa para identificar rapidamente um arquivo.</span><span class="sxs-lookup"><span data-stu-id="329ba-108">The reading pane will commonly be used in conjunction with search to quickly identify a file.</span></span> <span data-ttu-id="329ba-109">Tudo que obstrui o painel de leitura ou, de outra forma, reduz o conteúdo do arquivo ou causa atrasos na exibição da visualização.</span><span class="sxs-lookup"><span data-stu-id="329ba-109">Anything that clutters the reading pane or otherwise detracts from file content or causes delays in preview display should be avoided.</span></span>
-   <span data-ttu-id="329ba-110">A visualização deve permitir que o usuário navegue no documento.</span><span class="sxs-lookup"><span data-stu-id="329ba-110">The preview should allow the user to navigate in the document.</span></span> <span data-ttu-id="329ba-111">O usuário também deve ser capaz de selecionar e copiar o texto.</span><span class="sxs-lookup"><span data-stu-id="329ba-111">The user should also be able to select and copy text.</span></span>
-   <span data-ttu-id="329ba-112">A visualização não deve ter uso intensivo de memória, deve consumir recursos mínimos e deve ter um tempo de inicialização rápido.</span><span class="sxs-lookup"><span data-stu-id="329ba-112">The preview should not be memory-intensive, should consume minimal resources, and should have a fast startup time.</span></span>
-   <span data-ttu-id="329ba-113">Todo script e macros no arquivo que está sendo visualizado devem ser impedidos de serem executados para fins de segurança e privacidade.</span><span class="sxs-lookup"><span data-stu-id="329ba-113">All script and macros in the file being previewed should be blocked from running for security and privacy purposes.</span></span>
-   <span data-ttu-id="329ba-114">A visualização deve dar suporte a aceleradores de teclado para navegação e seleção, conforme suportado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="329ba-114">The preview should support keyboard accelerators for navigation and selection as supported by the application.</span></span> <span data-ttu-id="329ba-115">Ele também deve exibir um menu de contexto quando clicado com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="329ba-115">It should also display a context menu when right-clicked.</span></span>
-   <span data-ttu-id="329ba-116">Quando um arquivo é exibido como uma visualização, a visualização não deve bloquear o próprio arquivo.</span><span class="sxs-lookup"><span data-stu-id="329ba-116">When a file is displayed as a preview, the preview should not lock the file itself.</span></span> <span data-ttu-id="329ba-117">Um arquivo pode ser visualizado e aberto em seu aplicativo associado ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="329ba-117">A file can be previewed and opened in its associated application at the same time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="329ba-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="329ba-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="329ba-119">Gerenciadores de visualização e host de visualização do Shell</span><span class="sxs-lookup"><span data-stu-id="329ba-119">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="329ba-120">Criando gerenciadores de visualização</span><span class="sxs-lookup"><span data-stu-id="329ba-120">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> </dl>

 

 



