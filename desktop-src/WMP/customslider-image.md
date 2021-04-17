---
title: CUSTOMSLIDER. Image
description: O atributo Image especifica ou recupera o nome do arquivo que contém as imagens correspondentes aos vários Estados do controle deslizante personalizado.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- CUSTOMSLIDER. Image Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f425ce138b2a11d2be834f39603ecc295c52c706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762087"
---
# <a name="customsliderimage"></a><span data-ttu-id="fcc7a-104">CUSTOMSLIDER. Image</span><span class="sxs-lookup"><span data-stu-id="fcc7a-104">CUSTOMSLIDER.image</span></span>

<span data-ttu-id="fcc7a-105">O atributo **Image** especifica ou recupera o nome do arquivo que contém as imagens correspondentes aos vários Estados do controle deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="fcc7a-105">The **image** attribute specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="fcc7a-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="fcc7a-106">Possible Values</span></span>

<span data-ttu-id="fcc7a-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="fcc7a-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcc7a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcc7a-108">Remarks</span></span>

<span data-ttu-id="fcc7a-109">O atributo **Image** é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="fcc7a-109">The **image** attribute is required.</span></span> <span data-ttu-id="fcc7a-110">Ele especifica um arquivo de imagem que consiste em uma ou mais subimagems, organizadas horizontal ou verticalmente, representando os vários Estados do controle deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="fcc7a-110">It specifies an image file that consists of one or more sub-images, arranged either horizontally or vertically, representing the various states of the custom slider.</span></span> <span data-ttu-id="fcc7a-111">Cada subimagem deve ter as mesmas dimensões que o **positionImage** ou o controle deslizante personalizado não funcionará corretamente.</span><span class="sxs-lookup"><span data-stu-id="fcc7a-111">Each sub-image must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span> <span data-ttu-id="fcc7a-112">A altura ou a largura da imagem geral deve, portanto, ser um múltiplo par da altura ou largura do **positionImage**.</span><span class="sxs-lookup"><span data-stu-id="fcc7a-112">The height or width of the overall image must therefore be an even multiple of the height or width of the **positionImage**.</span></span>

<span data-ttu-id="fcc7a-113">Os tipos de arquivo de imagem com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).</span><span class="sxs-lookup"><span data-stu-id="fcc7a-113">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="fcc7a-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fcc7a-114">Examples</span></span>

<span data-ttu-id="fcc7a-115">Veja a seguir um exemplo de uma imagem de controle deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="fcc7a-115">The following is an example of a custom slider image.</span></span> <span data-ttu-id="fcc7a-116">O **positionImage** correspondente é mostrado na seção de exemplo da propriedade **positionImage** .</span><span class="sxs-lookup"><span data-stu-id="fcc7a-116">The corresponding **positionImage** is shown in the example section of the **positionImage** property.</span></span>

![imagem customslider de exemplo](images/dial.png)

<span data-ttu-id="fcc7a-118">O atributo **positionImage** também contém um exemplo de código que ilustra como os atributos do elemento **CUSTOMSLIDER** são usados.</span><span class="sxs-lookup"><span data-stu-id="fcc7a-118">The **positionImage** attribute also contains a code sample illustrating how the attributes of the **CUSTOMSLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcc7a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcc7a-119">Requirements</span></span>



| <span data-ttu-id="fcc7a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcc7a-120">Requirement</span></span> | <span data-ttu-id="fcc7a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fcc7a-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fcc7a-122">Versão</span><span class="sxs-lookup"><span data-stu-id="fcc7a-122">Version</span></span><br/> | <span data-ttu-id="fcc7a-123">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="fcc7a-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fcc7a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcc7a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc7a-125">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="fcc7a-125">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="fcc7a-126">**CUSTOMSLIDER.positionImage**</span><span class="sxs-lookup"><span data-stu-id="fcc7a-126">**CUSTOMSLIDER.positionImage**</span></span>](customslider-positionimage.md)
</dt> </dl>

 

 





