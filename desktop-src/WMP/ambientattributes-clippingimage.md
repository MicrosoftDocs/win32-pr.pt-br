---
title: Ambienteattributes. clippingImage
description: O atributo clippingImage especifica ou recupera a região para a qual o controle será recortado.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- ClippingImage do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781467"
---
# <a name="ambientattributesclippingimage"></a><span data-ttu-id="6f47f-104">Ambienteattributes. clippingImage</span><span class="sxs-lookup"><span data-stu-id="6f47f-104">AmbientAttributes.clippingImage</span></span>

<span data-ttu-id="6f47f-105">O atributo **clippingImage** especifica ou recupera a região para a qual o controle será recortado.</span><span class="sxs-lookup"><span data-stu-id="6f47f-105">The **clippingImage** attribute specifies or retrieves the region to clip the control to.</span></span>

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a><span data-ttu-id="6f47f-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6f47f-106">Possible Values</span></span>

<span data-ttu-id="6f47f-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que indica o nome do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="6f47f-107">This attribute is a read/write **String** indicating the image file name.</span></span> <span data-ttu-id="6f47f-108">Não tem nenhum valor padrão.</span><span class="sxs-lookup"><span data-stu-id="6f47f-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f47f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f47f-109">Remarks</span></span>

<span data-ttu-id="6f47f-110">O atributo **clippingImage** dá suporte a arquivos PNG, jpg, BMP e gif (não incluindo gifs animados).</span><span class="sxs-lookup"><span data-stu-id="6f47f-110">The **clippingImage** attribute supports PNG, JPG, BMP, and GIF files (not including animated GIFs).</span></span> <span data-ttu-id="6f47f-111">Como JPGs são derrotas e, portanto, sujeitos à alteração de cor inesperada, eles não são recomendados para imagens de recorte.</span><span class="sxs-lookup"><span data-stu-id="6f47f-111">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for clipping images.</span></span>

<span data-ttu-id="6f47f-112">Esse atributo é útil quando você deseja exibir apenas uma parte da imagem de controle e não a área retangular inteira.</span><span class="sxs-lookup"><span data-stu-id="6f47f-112">This attribute is useful when you want to display only a part of the control image and not the entire rectangular area.</span></span> <span data-ttu-id="6f47f-113">O atributo **clippingColor** indica as regiões da imagem de recorte que correspondem a partes transparentes e não clicáveis do controle.</span><span class="sxs-lookup"><span data-stu-id="6f47f-113">The **clippingColor** attribute indicates the regions of the clipping image that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="6f47f-114">Portanto, o controle pode ser de qualquer forma.</span><span class="sxs-lookup"><span data-stu-id="6f47f-114">The control can therefore be of any shape.</span></span> <span data-ttu-id="6f47f-115">Para obter melhores resultados, a imagem de recorte deve ter o mesmo tamanho da imagem de controle.</span><span class="sxs-lookup"><span data-stu-id="6f47f-115">For best results, the clipping image should be the same size as the control image.</span></span>

<span data-ttu-id="6f47f-116">Não há suporte para o atributo **clippingImage** nos elementos **playlist**, **View** e **subview** .</span><span class="sxs-lookup"><span data-stu-id="6f47f-116">The **clippingImage** attribute is not supported by the **PLAYLIST**, **VIEW**, and **SUBVIEW** elements.</span></span> <span data-ttu-id="6f47f-117">Uma imagem de recorte não funcionará com o elemento de **vídeo** se houver *vídeo*. **sem janela** é definido como false, nem com o elemento **Effects** , se houver *efeitos*. em **janela** é definido como true.</span><span class="sxs-lookup"><span data-stu-id="6f47f-117">A clipping image will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

<span data-ttu-id="6f47f-118">Como o uso de imagens de recorte impõe uma penalidade de desempenho, elas não devem ser usadas quando a eficiência é um problema.</span><span class="sxs-lookup"><span data-stu-id="6f47f-118">Because the use of clipping images imposes a performance penalty, they should not be used when efficiency is an issue.</span></span>

## <a name="examples"></a><span data-ttu-id="6f47f-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6f47f-119">Examples</span></span>

<span data-ttu-id="6f47f-120">Consulte o atributo [buttonelement. mappingColor](buttonelement-mappingcolor.md) para obter um exemplo ilustrando o uso desse atributo.</span><span class="sxs-lookup"><span data-stu-id="6f47f-120">See the [BUTTONELEMENT.mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f47f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f47f-121">Requirements</span></span>



| <span data-ttu-id="6f47f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f47f-122">Requirement</span></span> | <span data-ttu-id="6f47f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6f47f-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6f47f-124">Versão</span><span class="sxs-lookup"><span data-stu-id="6f47f-124">Version</span></span><br/> | <span data-ttu-id="6f47f-125">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6f47f-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6f47f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f47f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f47f-127">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="6f47f-127">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="6f47f-128">**Ambienteattributes. clippingColor**</span><span class="sxs-lookup"><span data-stu-id="6f47f-128">**AmbientAttributes.clippingColor**</span></span>](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





