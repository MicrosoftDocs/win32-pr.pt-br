---
title: PLAYLIST. backgroundImage
description: O atributo backgroundImage especifica ou recupera a imagem de plano de fundo.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- Windows Media Player de PLAYLIST. backgroundImage
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814016"
---
# <a name="playlistbackgroundimage"></a><span data-ttu-id="6931e-104">PLAYLIST. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="6931e-104">PLAYLIST.backgroundImage</span></span>

<span data-ttu-id="6931e-105">O atributo **backgroundImage** especifica ou recupera a imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="6931e-105">The **backgroundImage** attribute specifies or retrieves the background image.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="6931e-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6931e-106">Possible Values</span></span>

<span data-ttu-id="6931e-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="6931e-107">This attribute is a read/write **String** containing the name of an image file.</span></span> <span data-ttu-id="6931e-108">Não tem nenhum valor padrão.</span><span class="sxs-lookup"><span data-stu-id="6931e-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6931e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="6931e-109">Remarks</span></span>

<span data-ttu-id="6931e-110">Se a altura e a largura da imagem forem menores do que a altura e a largura do elemento **playlist** , a imagem será colocada em lado.</span><span class="sxs-lookup"><span data-stu-id="6931e-110">If the image height and width are smaller than the height and width of the **PLAYLIST** element, the image is tiled.</span></span> <span data-ttu-id="6931e-111">Os formatos com suporte são BMP, JPG, GIF e PNG.</span><span class="sxs-lookup"><span data-stu-id="6931e-111">The supported formats are BMP, JPG, GIF and PNG.</span></span>

<span data-ttu-id="6931e-112">A especificação de um valor de "gradação" para a imagem de fundo faz com que o plano de fundo da lista de reprodução seja exibido como um gradiente de cor.</span><span class="sxs-lookup"><span data-stu-id="6931e-112">Specifying a value of "gradient" for the background image causes the background of the playlist to display as a color gradient.</span></span> <span data-ttu-id="6931e-113">Isso significa que a cor do plano de fundo faz a transição gradualmente entre o [playlist. BackgroundColor](playlist-backgroundcolor.md) (na parte superior do plano de fundo) e os valores de [playlist. statusColor](playlist-statuscolor.md) .</span><span class="sxs-lookup"><span data-stu-id="6931e-113">This means the background color gradually transitions between the [PLAYLIST.backgroundColor](playlist-backgroundcolor.md) (at the top of the background) and [PLAYLIST.statusColor](playlist-statuscolor.md) values.</span></span>

## <a name="requirements"></a><span data-ttu-id="6931e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6931e-114">Requirements</span></span>



| <span data-ttu-id="6931e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6931e-115">Requirement</span></span> | <span data-ttu-id="6931e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6931e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6931e-117">Versão</span><span class="sxs-lookup"><span data-stu-id="6931e-117">Version</span></span><br/> | <span data-ttu-id="6931e-118">Windows Media Player versão 7,0 ou posterior, Windows Media Player 10 para o recurso de gradiente</span><span class="sxs-lookup"><span data-stu-id="6931e-118">Windows Media Player version 7.0 or later, Windows Media Player 10 for the gradient feature</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6931e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="6931e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6931e-120">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="6931e-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





