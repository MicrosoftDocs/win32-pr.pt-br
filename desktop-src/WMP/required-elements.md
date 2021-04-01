---
title: Elementos necessários
description: Elementos necessários
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Capas do Windows Media Player Mobile, elementos
- capas, elementos
- arquivos de definição de capa, elementos
- elementos, arquivos de definição de capa
- elementos, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1f05ba51b83fad6585d24c3ad19830598b8975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636027"
---
# <a name="required-elements"></a><span data-ttu-id="fab5f-108">Elementos necessários</span><span class="sxs-lookup"><span data-stu-id="fab5f-108">Required Elements</span></span>

<span data-ttu-id="fab5f-109">Você deve fornecer os seguintes elementos em seu arquivo de definição de capa:</span><span class="sxs-lookup"><span data-stu-id="fab5f-109">You must provide the following elements in your skin definition file:</span></span>

-   <span data-ttu-id="fab5f-110">**Verga.**</span><span class="sxs-lookup"><span data-stu-id="fab5f-110">**Header.**</span></span> <span data-ttu-id="fab5f-111">O cabeçalho principal do arquivo de definição de capa é necessário.</span><span class="sxs-lookup"><span data-stu-id="fab5f-111">The main skin definition file header is required.</span></span> <span data-ttu-id="fab5f-112">Para obter informações de versão do cabeçalho, consulte a tabela na seção [criando um arquivo de definição de aparência](creating-a-skin-definition-file.md) .</span><span class="sxs-lookup"><span data-stu-id="fab5f-112">For header version information, see the table in the [Creating a Skin Definition File](creating-a-skin-definition-file.md) section.</span></span>
-   <span data-ttu-id="fab5f-113">**Seção de descrição.**</span><span class="sxs-lookup"><span data-stu-id="fab5f-113">**Description section.**</span></span> <span data-ttu-id="fab5f-114">A seção descrição é necessária ao criar capas para o Windows Media Player 9 Series para Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="fab5f-114">The Description section is required when creating skins for Windows Media Player 9 Series for Windows Mobile.</span></span> <span data-ttu-id="fab5f-115">Ele deve ser a primeira seção no arquivo de definição de capa e deve especificar valores válidos para dimensões.</span><span class="sxs-lookup"><span data-stu-id="fab5f-115">It must be the first section in the skin definition file, and it must specify valid values for Dimensions.</span></span> <span data-ttu-id="fab5f-116">A especificação de um valor para a orientação é opcional.</span><span class="sxs-lookup"><span data-stu-id="fab5f-116">Specifying a value for Orientation is optional.</span></span>
-   <span data-ttu-id="fab5f-117">**Seção bitmaps.**</span><span class="sxs-lookup"><span data-stu-id="fab5f-117">**Bitmaps section.**</span></span> <span data-ttu-id="fab5f-118">A seção bitmaps é necessária.</span><span class="sxs-lookup"><span data-stu-id="fab5f-118">The Bitmaps section is required.</span></span> <span data-ttu-id="fab5f-119">Além disso, a seção bitmaps deve especificar nomes válidos para arquivos de plano de fundo, desabilitados, enviados por push, região e super Image.</span><span class="sxs-lookup"><span data-stu-id="fab5f-119">Additionally, the Bitmaps section must specify valid names for Background, Disabled, Pushed, Region, and Super image files.</span></span>
-   <span data-ttu-id="fab5f-120">**Arquivos de imagem.**</span><span class="sxs-lookup"><span data-stu-id="fab5f-120">**Image files.**</span></span> <span data-ttu-id="fab5f-121">Você deve fornecer arquivos de plano de fundo, desabilitados, enviados por push, região e super Image como parte de sua capa.</span><span class="sxs-lookup"><span data-stu-id="fab5f-121">You must provide Background, Disabled, Pushed, Region, and Super image files as part of your skin.</span></span> <span data-ttu-id="fab5f-122">Se você estiver criando capas para o Windows Media Player 10 Mobile ou posterior, não será necessário incluir arquivos de região ou de superimagem.</span><span class="sxs-lookup"><span data-stu-id="fab5f-122">If you are creating skins for Windows Media Player 10 Mobile or later, you do not need to include Region or Super image files.</span></span>

<span data-ttu-id="fab5f-123">Se você criar uma capa com apenas imagens definidas, a capa ficará visível, mas não oferecerá nenhuma funcionalidade significativa para o usuário.</span><span class="sxs-lookup"><span data-stu-id="fab5f-123">If you create a skin with only images defined, the skin will be visible, but will not offer any meaningful functionality to the user.</span></span> <span data-ttu-id="fab5f-124">Se você decidir criar uma capa sem botões, talvez para impedir que o usuário ignore um determinado conteúdo, lembre-se de que ainda pode ser possível mapear a funcionalidade para os botões de hardware no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fab5f-124">If you decide to create a skin without buttons, perhaps to prevent the user from skipping over certain content, be aware that it may still be possible to map functionality to the hardware buttons on the device.</span></span>

<span data-ttu-id="fab5f-125">Os arquivos Thumb são necessários e seu trackbars não pode ser usado sem thumbs.</span><span class="sxs-lookup"><span data-stu-id="fab5f-125">Thumb files are required and your trackbars cannot be used without thumbs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fab5f-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fab5f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fab5f-127">**Arquivo de definição de capa**</span><span class="sxs-lookup"><span data-stu-id="fab5f-127">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 




