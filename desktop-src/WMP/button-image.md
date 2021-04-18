---
title: BOTÃO. imagem
description: O atributo Image especifica ou recupera a imagem padrão do botão.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- BUTTON. Image Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27363383d72110ebe7b3e94187013ab701a6a3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763369"
---
# <a name="buttonimage"></a><span data-ttu-id="0cb49-104">BOTÃO. imagem</span><span class="sxs-lookup"><span data-stu-id="0cb49-104">BUTTON.image</span></span>

<span data-ttu-id="0cb49-105">O atributo **Image** especifica ou recupera a imagem padrão do **botão**.</span><span class="sxs-lookup"><span data-stu-id="0cb49-105">The **image** attribute specifies or retrieves the default image of the **BUTTON**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="0cb49-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0cb49-106">Possible Values</span></span>

<span data-ttu-id="0cb49-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="0cb49-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cb49-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cb49-108">Remarks</span></span>

<span data-ttu-id="0cb49-109">Os formatos de imagem com suporte são BMP, JPG, PNG e GIF (incluindo GIFs animados).</span><span class="sxs-lookup"><span data-stu-id="0cb49-109">The supported image formats are BMP, JPG, PNG, and GIF (including animated GIFs).</span></span>

<span data-ttu-id="0cb49-110">Se a imagem do **botão** for maior do que a região definida pelos atributos **Width** e **Height** , a imagem será cortada.</span><span class="sxs-lookup"><span data-stu-id="0cb49-110">If the **BUTTON** image is larger than the region defined by the **width** and **height** attributes, the image will be cropped.</span></span>

<span data-ttu-id="0cb49-111">Se a imagem não for especificada, mas a **altura** e a **largura** forem, a imagem diretamente atrás desse controle será exibida.</span><span class="sxs-lookup"><span data-stu-id="0cb49-111">If the image is not specified but the **height** and **width** are, then the image directly behind this control is displayed.</span></span> <span data-ttu-id="0cb49-112">Isso pode facilitar o desenho da imagem na própria **exibição** , reduzindo o número de arquivos de imagem separados necessários.</span><span class="sxs-lookup"><span data-stu-id="0cb49-112">This can facilitate drawing the image on the **VIEW** itself, reducing the number of separate image files needed.</span></span>

<span data-ttu-id="0cb49-113">Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.</span><span class="sxs-lookup"><span data-stu-id="0cb49-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb49-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cb49-114">Requirements</span></span>



| <span data-ttu-id="0cb49-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb49-115">Requirement</span></span> | <span data-ttu-id="0cb49-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0cb49-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0cb49-117">Versão</span><span class="sxs-lookup"><span data-stu-id="0cb49-117">Version</span></span><br/> | <span data-ttu-id="0cb49-118">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0cb49-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0cb49-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cb49-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb49-120">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="0cb49-120">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





