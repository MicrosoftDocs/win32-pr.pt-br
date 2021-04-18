---
title: Classificações
description: Classificações
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Aparências móveis do Windows Media Player, classificações
- capas, classificações
- referência para capas, classificações
- classificações em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105791575"
---
# <a name="ratings"></a><span data-ttu-id="3bc99-107">Classificações</span><span class="sxs-lookup"><span data-stu-id="3bc99-107">Ratings</span></span>

<span data-ttu-id="3bc99-108">Ao criar uma capa para o Windows Media Player 10,1 Mobile, você pode exibir a classificação associada ao conteúdo baseado em áudio do Windows Media que está sendo executado no momento.</span><span class="sxs-lookup"><span data-stu-id="3bc99-108">When you create a skin for Windows Media Player 10.1 Mobile, you can display the rating associated with Windows Media Audio-based content that is currently playing.</span></span> <span data-ttu-id="3bc99-109">A classificação é exibida como uma estrela com um número.</span><span class="sxs-lookup"><span data-stu-id="3bc99-109">The rating is displayed as a star with a number on it.</span></span> <span data-ttu-id="3bc99-110">A estrela será numerada uma a cinco, denotando a classificação atual desse conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3bc99-110">The star will be numbered one through five, denoting the current rating for that content.</span></span> <span data-ttu-id="3bc99-111">Se o conteúdo não for classificado, a estrela será numerada como zero.</span><span class="sxs-lookup"><span data-stu-id="3bc99-111">If the content is not rated, the star will be numbered zero.</span></span>

<span data-ttu-id="3bc99-112">A seção ratings do arquivo de definição de capa começa com esta linha:</span><span class="sxs-lookup"><span data-stu-id="3bc99-112">The Ratings section of the skin definition file begins with this line:</span></span>


```C++
[ Ratings ]

```



<span data-ttu-id="3bc99-113">Em seguida, você deve adicionar uma linha que contém informações sobre o tamanho e o local do ícone de classificações em sua capa.</span><span class="sxs-lookup"><span data-stu-id="3bc99-113">You then must add a line that contains information about the size and location of your ratings icon in your skin.</span></span>


```C++
147, 3, 22, 21       ratings96S.gif

```



<span data-ttu-id="3bc99-114">Você pode usar o modelo a seguir para a seção de classificações do arquivo de definição de capa:</span><span class="sxs-lookup"><span data-stu-id="3bc99-114">You can use the following template for the Ratings section of your skin definition file:</span></span>


```C++
// <Location>           <Image>
// ---------------      --------------------
```



<span data-ttu-id="3bc99-115">Você também pode atribuir um valor de classificações a um item de mídia por meio da interface do usuário no Windows Media Player 10,1 Mobile e, na próxima vez em que o dispositivo for sincronizado com o computador, o novo valor de classificações será propagado para esse item de mídia se ele residir na biblioteca do Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="3bc99-115">You can also assign a ratings value to a media item through the user interface in Windows Media Player 10.1 Mobile, and the next time the device synchronizes with the a computer, the new ratings value will be propagated to that media item if it resides in the Windows Media Player 10 library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bc99-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3bc99-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bc99-117">**Referência de capa**</span><span class="sxs-lookup"><span data-stu-id="3bc99-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




