---
title: Opções de plug-in da interface do usuário
description: Opções de plug-in da interface do usuário
ms.assetid: 3c188506-865c-4e0c-965d-1429eafd01ef
keywords:
- Plug-ins do Windows Media Player, opções
- plug-ins, opções
- plug-ins de interface do usuário, opções
- Plug-ins de interface do usuário, opções
- plug-ins da área de configurações
- plug-ins em segundo plano
- plug-ins de janela separados
- plug-ins de área de metadados
- Exibir plug-ins de área
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281dd0679e6a975b1c867624f2f652f2b3e6b9ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789329"
---
# <a name="ui-plug-in-options"></a><span data-ttu-id="6d44b-112">Opções de plug-in da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="6d44b-112">UI Plug-in Options</span></span>

<span data-ttu-id="6d44b-113">Qualquer um dos cinco tipos de plug-in da interface do usuário pode ter uma página de propriedades em que o usuário pode modificar as configurações de plug-in.</span><span class="sxs-lookup"><span data-stu-id="6d44b-113">Any of the five UI plug-in types can have a property page where the user can modify plug-in settings.</span></span> <span data-ttu-id="6d44b-114">Essa página de propriedades pode ser definida para ser exibida automaticamente quando um plug-in é carregado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="6d44b-114">This property page can be set to display automatically when a plug-in is loaded for the first time.</span></span> <span data-ttu-id="6d44b-115">Ele também pode ser acessado na guia plug-ins da caixa de diálogo opções.</span><span class="sxs-lookup"><span data-stu-id="6d44b-115">It can also be accessed from the Plug-ins tab of the Options dialog box.</span></span>

<span data-ttu-id="6d44b-116">Um plug-in de interface do usuário pode ser definido para ser carregado automaticamente após a instalação quando o Windows Media Player é iniciado.</span><span class="sxs-lookup"><span data-stu-id="6d44b-116">A UI plug-in can be set to load automatically after installation when Windows Media Player is started.</span></span> <span data-ttu-id="6d44b-117">Se não for iniciado automaticamente, o usuário poderá carregá-lo selecionando-o na lista de **plug-ins** no menu **ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="6d44b-117">If it is not started automatically, the user can load it by selecting it from the **Plug-ins** list on the **Tools** menu.</span></span>

<span data-ttu-id="6d44b-118">Um plug-in de área de exibição pode ter várias predefinições, que são diferentes exibições que o plug-in pode disponibilizar para o usuário.</span><span class="sxs-lookup"><span data-stu-id="6d44b-118">A display area plug-in can have multiple presets, which are different views that the plug-in can make available to the user.</span></span> <span data-ttu-id="6d44b-119">O usuário pode alterar a predefinição selecionando uma entrada diferente na lista **visualizações e exibições** no menu **Exibir** ou usando os botões de seta fornecidos na parte inferior do painel em **execução** logo acima da mensagem de status e dos controles de transporte.</span><span class="sxs-lookup"><span data-stu-id="6d44b-119">The user can change the preset by selecting a different entry from the **Visualizations and Views** list on the **View** menu, or by using the arrow buttons provided at the bottom of the **Now Playing** pane just above the status message and transport controls.</span></span>

<span data-ttu-id="6d44b-120">Os plug-ins de interface do usuário de janela e de plano de fundo podem ser programados para aceitar um item de mídia ou lista de reprodução que o usuário envia a ele.</span><span class="sxs-lookup"><span data-stu-id="6d44b-120">Background and separate window UI plug-ins can be programmed to accept a media item or playlist that the user sends to it.</span></span> <span data-ttu-id="6d44b-121">Se um plug-in der suporte a esse recurso, seu nome aparecerá na lista **Enviar para** disponível no menu de atalho do controle playlist ou na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6d44b-121">If a plug-in supports this feature, its name will appear on the **Send to** list available from the shortcut menu of the playlist control or the library.</span></span>

<span data-ttu-id="6d44b-122">Um plug-in de interface do usuário pode ser programado para interceptar atalhos de teclado quando ele tem o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="6d44b-122">A UI plug-in can be programmed to intercept keyboard shortcuts when it has the keyboard focus.</span></span> <span data-ttu-id="6d44b-123">O foco do teclado é necessário para evitar conflitos quando vários plug-ins de interface do usuário que interceptam o mesmo atalho de teclado são carregados.</span><span class="sxs-lookup"><span data-stu-id="6d44b-123">Keyboard focus is required to prevent conflicts when multiple UI plug-ins that intercept the same keyboard shortcut are loaded.</span></span> <span data-ttu-id="6d44b-124">Embora isso impeça conflitos, ele também pode causar confusão aos usuários finais.</span><span class="sxs-lookup"><span data-stu-id="6d44b-124">Although this prevents conflicts, it can also cause confusion to end users.</span></span> <span data-ttu-id="6d44b-125">Por esse motivo, o uso de atalhos de teclado com plug-ins de interface do usuário não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="6d44b-125">For this reason, the use of keyboard shortcuts with UI plug-ins is not recommended.</span></span> <span data-ttu-id="6d44b-126">No entanto, quando são usados, eles não devem interceptar nenhum atalho de teclado usado pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6d44b-126">When they are used, however, they should not intercept any keyboard shortcuts that are used by Windows Media Player.</span></span> <span data-ttu-id="6d44b-127">Para obter uma lista completa dos atalhos de teclado usados pelo Player, consulte a ajuda do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6d44b-127">For a complete list of keyboard shortcuts used by the Player, see Windows Media Player Help.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d44b-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d44b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d44b-129">**Visão geral do plug-in da interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="6d44b-129">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




