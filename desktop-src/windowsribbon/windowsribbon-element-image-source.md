---
title: Propriedade Image. Source
description: Representa o caminho de diretório de uma imagem.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Ribbon da Propriedade Image. Source do Windows
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ace2a907280a11c54452b54bfb6172539980e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644524"
---
# <a name="imagesource-property"></a><span data-ttu-id="63c38-104">Propriedade Image. Source</span><span class="sxs-lookup"><span data-stu-id="63c38-104">Image.Source property</span></span>

<span data-ttu-id="63c38-105">Representa o caminho de diretório de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="63c38-105">Represents the directory path of an image.</span></span>

## <a name="usage"></a><span data-ttu-id="63c38-106">Uso</span><span class="sxs-lookup"><span data-stu-id="63c38-106">Usage</span></span>

``` syntax
<Image.Source/>
```

## <a name="attributes"></a><span data-ttu-id="63c38-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="63c38-107">Attributes</span></span>

<span data-ttu-id="63c38-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="63c38-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="63c38-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="63c38-109">Child elements</span></span>

<span data-ttu-id="63c38-110">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="63c38-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="63c38-111">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="63c38-111">Parent elements</span></span>



| <span data-ttu-id="63c38-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="63c38-112">Element</span></span>                                                 |
|---------------------------------------------------------|
| [<span data-ttu-id="63c38-113">**Imagem**</span><span class="sxs-lookup"><span data-stu-id="63c38-113">**Image**</span></span>](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="63c38-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="63c38-114">Remarks</span></span>

<span data-ttu-id="63c38-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="63c38-115">Optional.</span></span>

<span data-ttu-id="63c38-116">Pode ocorrer no máximo uma vez para cada [**imagem**](windowsribbon-element-image.md).</span><span class="sxs-lookup"><span data-stu-id="63c38-116">May occur at most once for each [**Image**](windowsribbon-element-image.md).</span></span>

<span data-ttu-id="63c38-117">Esse elemento contém um valor do tipo *xs: anyURI* ou qualquer sequência de caracteres que representa um Uniform Resource Identifier (URI).</span><span class="sxs-lookup"><span data-stu-id="63c38-117">This element contains a value of type *xs:anyURI* or any sequence of characters that represents a Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="63c38-118">O valor do URI é um caminho de diretório absoluto ou relativo (para o arquivo de marcação da faixa de tipos) de um recurso de imagem do tipo bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="63c38-118">The URI value is an absolute or relative (to the Ribbon markup file) directory path of an image resource of type bitmap (BMP).</span></span>

## <a name="examples"></a><span data-ttu-id="63c38-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="63c38-119">Examples</span></span>

<span data-ttu-id="63c38-120">O exemplo de código a seguir mostra a marcação necessária para declarar, por meio de um conjunto de elementos [**Image**](windowsribbon-element-image.md) , uma coleção de recursos de imagem que são projetados para dar suporte a quatro configurações específicas de dpi de tela.</span><span class="sxs-lookup"><span data-stu-id="63c38-120">The following code example shows the markup required to declare, through a set of [**Image**](windowsribbon-element-image.md) elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span> <span data-ttu-id="63c38-121">A propriedade **Image. Source** é usada para especificar o caminho para o recurso de imagem.</span><span class="sxs-lookup"><span data-stu-id="63c38-121">The **Image.Source** property is used to specify the path to the image resource.</span></span>


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="63c38-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63c38-122">Requirements</span></span>



| <span data-ttu-id="63c38-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="63c38-123">Requirement</span></span> | <span data-ttu-id="63c38-124">Valor</span><span class="sxs-lookup"><span data-stu-id="63c38-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="63c38-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63c38-125">Minimum supported client</span></span><br/> | <span data-ttu-id="63c38-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="63c38-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="63c38-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63c38-127">Minimum supported server</span></span><br/> | <span data-ttu-id="63c38-128">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="63c38-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





