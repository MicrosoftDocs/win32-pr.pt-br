---
title: Texto (SDK do Windows Media Player)
description: Texto
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Aparências móveis do Windows Media Player, texto
- capas, texto
- referência de capas, texto
- texto em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801d93698bc7a17eea34df71514dd88b485f0d9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103824128"
---
# <a name="text-windows-media-player-sdk"></a><span data-ttu-id="aa17c-107">Texto (SDK do Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="aa17c-107">Text (Windows Media Player SDK)</span></span>

<span data-ttu-id="aa17c-108">Talvez você queira usar uma ou mais caixas de exibição de texto em sua capa.</span><span class="sxs-lookup"><span data-stu-id="aa17c-108">You may want to use one or more text display boxes in your skin.</span></span> <span data-ttu-id="aa17c-109">Cada caixa de exibição de texto que você usa deve ser definida no arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="aa17c-109">Each text display box you use must be defined in the skin definition file.</span></span> <span data-ttu-id="aa17c-110">Se você não definir uma caixa de exibição de texto nesta seção, sua capa não será capaz de usá-la.</span><span class="sxs-lookup"><span data-stu-id="aa17c-110">If you do not define a text display box in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="aa17c-111">A seção de texto do arquivo de definição de capa começa com esta linha:</span><span class="sxs-lookup"><span data-stu-id="aa17c-111">The Text section of the skin definition file begins with this line:</span></span>


```C++
[ Text ]

```



<span data-ttu-id="aa17c-112">Em seguida, você deve adicionar uma ou mais linhas que contêm informações sobre cada uma das caixas de exibição de texto em sua capa</span><span class="sxs-lookup"><span data-stu-id="aa17c-112">You then must add one or more lines that contain information about each of the text display boxes in your skin</span></span>


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



<span data-ttu-id="aa17c-113">Você pode usar o modelo a seguir para a seção de texto do arquivo de definição de capa:</span><span class="sxs-lookup"><span data-stu-id="aa17c-113">You can use the following template for the Text section of your skin definition file:</span></span>


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



<span data-ttu-id="aa17c-114">Você deve usar a ordem mostrada no modelo anterior para informações da caixa de exibição de texto para cada linha na seção de texto.</span><span class="sxs-lookup"><span data-stu-id="aa17c-114">You must use the order shown in the preceding template for text display box information for each line in the Text section.</span></span> <span data-ttu-id="aa17c-115">Cada parte da linha é necessária.</span><span class="sxs-lookup"><span data-stu-id="aa17c-115">Each part of the line is required.</span></span> <span data-ttu-id="aa17c-116">As seções a seguir descrevem cada item em detalhes.</span><span class="sxs-lookup"><span data-stu-id="aa17c-116">The following sections describe each item in detail.</span></span>

1.  [<span data-ttu-id="aa17c-117">Tipo de texto</span><span class="sxs-lookup"><span data-stu-id="aa17c-117">Text Type</span></span>](text-type.md)
2.  [<span data-ttu-id="aa17c-118">Local do texto</span><span class="sxs-lookup"><span data-stu-id="aa17c-118">Text Location</span></span>](text-location.md)
3.  [<span data-ttu-id="aa17c-119">Alinhamento de texto</span><span class="sxs-lookup"><span data-stu-id="aa17c-119">Text Alignment</span></span>](text-alignment.md)
4.  [<span data-ttu-id="aa17c-120">Fonte do texto</span><span class="sxs-lookup"><span data-stu-id="aa17c-120">Text Font</span></span>](text-font.md)
5.  [<span data-ttu-id="aa17c-121">Cor do texto</span><span class="sxs-lookup"><span data-stu-id="aa17c-121">Text Color</span></span>](text-color.md)

<span data-ttu-id="aa17c-122">Para obter um exemplo de código de texto, consulte a [seção texto de exemplo](sample-text-section.md).</span><span class="sxs-lookup"><span data-stu-id="aa17c-122">For an example of Text code, see [Sample Text Section](sample-text-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa17c-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa17c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa17c-124">**Referência de capa**</span><span class="sxs-lookup"><span data-stu-id="aa17c-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




