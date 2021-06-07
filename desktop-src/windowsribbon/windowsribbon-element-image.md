---
title: Elemento Image (Windows Ribbon Framework)
description: Representa uma imagem.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Faixa de Opções do Windows do elemento Image
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe0b9afb51697d50de9cb80886cf829b90c81262
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442887"
---
# <a name="image-element"></a><span data-ttu-id="41fb1-104">Elemento Image</span><span class="sxs-lookup"><span data-stu-id="41fb1-104">Image element</span></span>

<span data-ttu-id="41fb1-105">Representa uma imagem.</span><span class="sxs-lookup"><span data-stu-id="41fb1-105">Represents an image.</span></span>

## <a name="usage"></a><span data-ttu-id="41fb1-106">Uso</span><span class="sxs-lookup"><span data-stu-id="41fb1-106">Usage</span></span>

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a><span data-ttu-id="41fb1-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="41fb1-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="41fb1-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="41fb1-108">Attribute</span></span></th>
<th><span data-ttu-id="41fb1-109">Type</span><span class="sxs-lookup"><span data-stu-id="41fb1-109">Type</span></span></th>
<th><span data-ttu-id="41fb1-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="41fb1-110">Required</span></span></th>
<th><span data-ttu-id="41fb1-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="41fb1-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41fb1-112"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="41fb1-112"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="41fb1-113">xs:positiveInteger union xs:string</span><span class="sxs-lookup"><span data-stu-id="41fb1-113">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="41fb1-114">Não</span><span class="sxs-lookup"><span data-stu-id="41fb1-114">No</span></span><br/></td>
<td><span data-ttu-id="41fb1-115">A ID de recurso exclusiva.</span><span class="sxs-lookup"><span data-stu-id="41fb1-115">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="41fb1-116">
<dt><span></span><span></span><strong></strong> (A união de xs:positiveInteger e xs:string)</span><span class="sxs-lookup"><span data-stu-id="41fb1-116">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="41fb1-117">Um valor inteiro entre 2 e 59999, inclusive ou 0x2 e 0xea5f em hexadecimal, inclusive.</span><span class="sxs-lookup"><span data-stu-id="41fb1-117">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="41fb1-118">O comprimento máximo é de 10 caracteres, incluindo zeros à esquerda opcionais.</span><span class="sxs-lookup"><span data-stu-id="41fb1-118">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41fb1-119"><strong>MinDPI</strong></span><span class="sxs-lookup"><span data-stu-id="41fb1-119"><strong>MinDPI</strong></span></span><br/></td>
<td><span data-ttu-id="41fb1-120">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="41fb1-120">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="41fb1-121">Não</span><span class="sxs-lookup"><span data-stu-id="41fb1-121">No</span></span><br/></td>
<td><span data-ttu-id="41fb1-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="41fb1-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="41fb1-123">Qualquer sequência de dígitos com um valor mínimo de 96.</span><span class="sxs-lookup"><span data-stu-id="41fb1-123">Any sequence of digits with a minimum value of 96.</span></span> <br/> <span data-ttu-id="41fb1-124">Se MinDPI for omitido, o valor padrão será 96.</span><span class="sxs-lookup"><span data-stu-id="41fb1-124">If MinDPI is omitted, the default value is 96.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41fb1-125"><strong>Origem</strong></span><span class="sxs-lookup"><span data-stu-id="41fb1-125"><strong>Source</strong></span></span><br/></td>
<td><span data-ttu-id="41fb1-126">xs:anyURI</span><span class="sxs-lookup"><span data-stu-id="41fb1-126">xs:anyURI</span></span><br/></td>
<td><span data-ttu-id="41fb1-127">Não</span><span class="sxs-lookup"><span data-stu-id="41fb1-127">No</span></span><br/></td>
<td><span data-ttu-id="41fb1-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span><span class="sxs-lookup"><span data-stu-id="41fb1-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span></span><br/> </dt> <dd> <span data-ttu-id="41fb1-129">Qualquer sequência de caracteres que representa um URI.</span><span class="sxs-lookup"><span data-stu-id="41fb1-129">Any sequence of characters that represents a URI.</span></span> <span data-ttu-id="41fb1-130">O valor de URI é um caminho absoluto ou relativo (para o arquivo de marcação faixa de opções) para um recurso de imagem do tipo BMP.</span><span class="sxs-lookup"><span data-stu-id="41fb1-130">The URI value is an absolute or relative (to the Ribbon markup file) path to an image resource of type BMP.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41fb1-131"><strong>Símbolo</strong></span><span class="sxs-lookup"><span data-stu-id="41fb1-131"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="41fb1-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="41fb1-132">xs:string</span></span><br/></td>
<td><span data-ttu-id="41fb1-133">Não</span><span class="sxs-lookup"><span data-stu-id="41fb1-133">No</span></span><br/></td>
<td><span data-ttu-id="41fb1-134">O símbolo de recurso para a imagem.</span><span class="sxs-lookup"><span data-stu-id="41fb1-134">The resource symbol for the image.</span></span><br/> <br/><span data-ttu-id="41fb1-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="41fb1-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="41fb1-136">Uma cadeia de caracteres composta por uma letra ou sublinhado seguida por qualquer sequência de letras, dígitos ou sublinhados até um máximo de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="41fb1-136">A string composed of a letter or underscore followed by any sequence of letters, digits, or underscores up to a maximum of 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="41fb1-137">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="41fb1-137">Child elements</span></span>



| <span data-ttu-id="41fb1-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="41fb1-138">Element</span></span>                                                               | <span data-ttu-id="41fb1-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="41fb1-139">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="41fb1-140">**Image.Source**</span><span class="sxs-lookup"><span data-stu-id="41fb1-140">**Image.Source**</span></span>](windowsribbon-element-image-source.md)<br/> | <span data-ttu-id="41fb1-141">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="41fb1-141">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="41fb1-142">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="41fb1-142">Parent elements</span></span>



| <span data-ttu-id="41fb1-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="41fb1-143">Element</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41fb1-144">**Command.LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="41fb1-144">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [<span data-ttu-id="41fb1-145">**Command.LargeImages**</span><span class="sxs-lookup"><span data-stu-id="41fb1-145">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         |
| [<span data-ttu-id="41fb1-146">**Command.SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="41fb1-146">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [<span data-ttu-id="41fb1-147">**Command.SmallImages**</span><span class="sxs-lookup"><span data-stu-id="41fb1-147">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a><span data-ttu-id="41fb1-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="41fb1-148">Remarks</span></span>

<span data-ttu-id="41fb1-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="41fb1-149">Optional.</span></span>

<span data-ttu-id="41fb1-150">Pode ocorrer uma ou mais vezes para cada [**elemento Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)ou [**Command.LargeHighContrastImages.**](windowsribbon-element-command-largehighcontrastimages.md)</span><span class="sxs-lookup"><span data-stu-id="41fb1-150">May occur one or more times for each [**Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command.LargeImages**](windowsribbon-element-command-largeimages.md), or [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) element.</span></span>

<span data-ttu-id="41fb1-151">Quando uma coleção de recursos de imagem projetados para dar suporte a configurações específicas de dpi (pontos de  tela por polegada) é fornecida à estrutura de Faixa de Opções por meio de um conjunto de elementos Image, a estrutura usa a Imagem com um valor de atributo *MinDPI* que corresponde à configuração de dpi da tela atual. </span><span class="sxs-lookup"><span data-stu-id="41fb1-151">When a collection of image resources that are designed to support specific screen dots per inch (dpi) settings is supplied to the Ribbon framework through a set of **Image** elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>

<span data-ttu-id="41fb1-152">Se nenhum elemento **Image** for declarado com um valor *MinDPI* que corresponde à  configuração de dpi da tela atual, a estrutura escolherá a Imagem que tem o valor *minDPI* mais próximo menor que a configuração de dpi da tela atual e escalará o recurso de imagem para cima.</span><span class="sxs-lookup"><span data-stu-id="41fb1-152">If no **Image** element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="41fb1-153">Caso contrário, se nenhum elemento **Image** for declarado com um valor de atributo *MinDPI* menor que a configuração de dpi da tela atual, a estrutura escolherá o valor *minDPI* mais próximo maior que a configuração de dpi da tela atual e dimensiona o recurso de imagem para baixo.</span><span class="sxs-lookup"><span data-stu-id="41fb1-153">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

## <a name="examples"></a><span data-ttu-id="41fb1-154">Exemplos</span><span class="sxs-lookup"><span data-stu-id="41fb1-154">Examples</span></span>

<span data-ttu-id="41fb1-155">O exemplo de código a seguir mostra a marcação necessária para declarar, por meio de um conjunto de elementos **Image,** uma coleção de recursos de imagem projetados para dar suporte a quatro configurações específicas de dpi de tela.</span><span class="sxs-lookup"><span data-stu-id="41fb1-155">The following code example shows the markup required to declare, through a set of **Image** elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span>


```XML
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">res/sizeAndColor_96.bmp</Image>
    <Image Id="252" MinDPI="120">res/sizeAndColor_120.bmp</Image>
    <Image Id="253" MinDPI="144">res/sizeAndColor_144.bmp</Image>
    <Image Id="254" MinDPI="192">res/sizeAndColor_192.bmp</Image>
  </Command.LargeImages>
</Command>
```



## <a name="element-information"></a><span data-ttu-id="41fb1-156">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="41fb1-156">Element information</span></span>

* <span data-ttu-id="41fb1-157">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="41fb1-157">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="41fb1-158">**Pode estar vazio:** Não</span><span class="sxs-lookup"><span data-stu-id="41fb1-158">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="41fb1-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="41fb1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41fb1-160">Especificando recursos de imagem da faixa de opções</span><span class="sxs-lookup"><span data-stu-id="41fb1-160">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 





