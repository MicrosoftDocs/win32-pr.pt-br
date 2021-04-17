---
title: Adicionando um botão
description: Adicionando um botão
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- Criando capas, elemento de botão
- Capas do Windows Media Player, elemento de botão
- capas, elemento de botão
- arquivos de definição de capa, elemento de botão
- Elemento de botão
- elementos, um botão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90659a2e867a65d2751532701b71810a532c8ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291959"
---
# <a name="adding-buttongroup"></a><span data-ttu-id="235e8-109">Adicionando um botão</span><span class="sxs-lookup"><span data-stu-id="235e8-109">Adding BUTTONGROUP</span></span>

<span data-ttu-id="235e8-110">Este exemplo usa o elemento de grupo de **botões** para a codificação no arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="235e8-110">This example uses the **BUTTONGROUP** element for the coding in the skin definition file.</span></span> <span data-ttu-id="235e8-111">O tipo de **botão** cria uma maneira fácil de processar eventos de mouse sem a necessidade de calcular os locais exatos na tela e usa a cor em vez das coordenadas x e y.</span><span class="sxs-lookup"><span data-stu-id="235e8-111">**BUTTONGROUP** creates an easy way to process mouse events without having to calculate exact locations on the screen and uses color instead of x and y-coordinates.</span></span>

<span data-ttu-id="235e8-112">Primeiro, você deve adicionar as marcas de grupo de **botões** ao arquivo de definição de capa que você criou.</span><span class="sxs-lookup"><span data-stu-id="235e8-112">First you must add the **BUTTONGROUP** tags to the skin definition file you created.</span></span> <span data-ttu-id="235e8-113">Coloque-os após os atributos de marca de **tema** .</span><span class="sxs-lookup"><span data-stu-id="235e8-113">Put them after the **THEME** tag attributes.</span></span>


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



<span data-ttu-id="235e8-114">Deixe algumas linhas em branco acima da marca do **botão** de fechamento para os botões que serão adicionados a seguir.</span><span class="sxs-lookup"><span data-stu-id="235e8-114">Leave a few blank lines above the closing **BUTTONGROUP** tag for the buttons you will add next.</span></span>

<span data-ttu-id="235e8-115">Os seguintes atributos são usados para definir o **botão**:</span><span class="sxs-lookup"><span data-stu-id="235e8-115">The following attributes are used to define **BUTTONGROUP**:</span></span>

<span data-ttu-id="235e8-116">**mappingImage**</span><span class="sxs-lookup"><span data-stu-id="235e8-116">**mappingImage**</span></span>

<span data-ttu-id="235e8-117">Esse é o nome de arquivo do arquivo de arte de mapeamento criado anteriormente, aquele com os círculos vermelho e verde.</span><span class="sxs-lookup"><span data-stu-id="235e8-117">This is the file name of the mapping art file you created before, the one with the red and green circles.</span></span> <span data-ttu-id="235e8-118">Esse atributo é necessário para qualquer um dos **botões**.</span><span class="sxs-lookup"><span data-stu-id="235e8-118">This attribute is required for any **BUTTONGROUP**.</span></span>

<span data-ttu-id="235e8-119">**hoverImage**</span><span class="sxs-lookup"><span data-stu-id="235e8-119">**hoverImage**</span></span>

<span data-ttu-id="235e8-120">Esse é o nome do arquivo Art que você criou anteriormente, aquele com os dois botões amarelos que lêem "Play" e "Close".</span><span class="sxs-lookup"><span data-stu-id="235e8-120">This is the file name of the hover art file you created before, the one with the two yellow buttons that read "Play" and "Close".</span></span> <span data-ttu-id="235e8-121">Isso não é necessário, mas uma imagem em foco ajuda a fornecer comentários para o usuário.</span><span class="sxs-lookup"><span data-stu-id="235e8-121">This is not required, but a hover image helps to provide feedback to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="235e8-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="235e8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="235e8-123">**Criando o arquivo de definição de capa**</span><span class="sxs-lookup"><span data-stu-id="235e8-123">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




