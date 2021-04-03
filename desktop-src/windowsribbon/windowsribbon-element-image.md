---
title: Elemento Image (Windows Ribbon Framework)
description: Representa uma imagem.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Faixa de imagens do elemento Image do Windows
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d33f6710da2261a359aa7fd0a3b493871155cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104084247"
---
# <a name="image-element"></a><span data-ttu-id="538e8-104">Elemento Image</span><span class="sxs-lookup"><span data-stu-id="538e8-104">Image element</span></span>

<span data-ttu-id="538e8-105">Representa uma imagem.</span><span class="sxs-lookup"><span data-stu-id="538e8-105">Represents an image.</span></span>

## <a name="usage"></a><span data-ttu-id="538e8-106">Uso</span><span class="sxs-lookup"><span data-stu-id="538e8-106">Usage</span></span>

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a><span data-ttu-id="538e8-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="538e8-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="538e8-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="538e8-108">Attribute</span></span></th>
<th><span data-ttu-id="538e8-109">Type</span><span class="sxs-lookup"><span data-stu-id="538e8-109">Type</span></span></th>
<th><span data-ttu-id="538e8-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="538e8-110">Required</span></span></th>
<th><span data-ttu-id="538e8-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="538e8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="538e8-112"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="538e8-112"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="538e8-113">xs: positiveInteger Union xs: String</span><span class="sxs-lookup"><span data-stu-id="538e8-113">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="538e8-114">No</span><span class="sxs-lookup"><span data-stu-id="538e8-114">No</span></span><br/></td>
<td><span data-ttu-id="538e8-115">A ID de recurso exclusiva.</span><span class="sxs-lookup"><span data-stu-id="538e8-115">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="538e8-116">
<dt><span></span><span></span><strong></strong> (A União de xs: positiveInteger e xs: String)</span><span class="sxs-lookup"><span data-stu-id="538e8-116">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="538e8-117">Um valor inteiro entre 2 e 59999, inclusivo, ou 0x2 e 0xea5f em hexadecimal, inclusive.</span><span class="sxs-lookup"><span data-stu-id="538e8-117">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="538e8-118">O comprimento máximo é de 10 caracteres, incluindo zeros à esquerda opcionais.</span><span class="sxs-lookup"><span data-stu-id="538e8-118">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="538e8-119"><strong>MinDPI</strong></span><span class="sxs-lookup"><span data-stu-id="538e8-119"><strong>MinDPI</strong></span></span><br/></td>
<td><span data-ttu-id="538e8-120">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="538e8-120">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="538e8-121">No</span><span class="sxs-lookup"><span data-stu-id="538e8-121">No</span></span><br/></td>
<td><span data-ttu-id="538e8-122"><dt><span></span><span></span><strong></strong> (xs: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="538e8-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="538e8-123">Qualquer sequência de dígitos com um valor mínimo de 96.</span><span class="sxs-lookup"><span data-stu-id="538e8-123">Any sequence of digits with a minimum value of 96.</span></span> <br/> <span data-ttu-id="538e8-124">Se MinDPI for omitido, o valor padrão será 96.</span><span class="sxs-lookup"><span data-stu-id="538e8-124">If MinDPI is omitted, the default value is 96.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="538e8-125"><strong>Origem</strong></span><span class="sxs-lookup"><span data-stu-id="538e8-125"><strong>Source</strong></span></span><br/></td>
<td><span data-ttu-id="538e8-126">xs:anyURI</span><span class="sxs-lookup"><span data-stu-id="538e8-126">xs:anyURI</span></span><br/></td>
<td><span data-ttu-id="538e8-127">No</span><span class="sxs-lookup"><span data-stu-id="538e8-127">No</span></span><br/></td>
<td><span data-ttu-id="538e8-128"><dt><span></span><span></span><strong></strong> (xs: anyURI)</span><span class="sxs-lookup"><span data-stu-id="538e8-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span></span><br/> </dt> <dd> <span data-ttu-id="538e8-129">Qualquer sequência de caracteres que representa um URI.</span><span class="sxs-lookup"><span data-stu-id="538e8-129">Any sequence of characters that represents a URI.</span></span> <span data-ttu-id="538e8-130">O valor do URI é um caminho absoluto ou relativo (para o arquivo de marcação da faixa de tipos) para um recurso de imagem do tipo BMP.</span><span class="sxs-lookup"><span data-stu-id="538e8-130">The URI value is an absolute or relative (to the Ribbon markup file) path to an image resource of type BMP.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="538e8-131"><strong>Símbolo</strong></span><span class="sxs-lookup"><span data-stu-id="538e8-131"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="538e8-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="538e8-132">xs:string</span></span><br/></td>
<td><span data-ttu-id="538e8-133">No</span><span class="sxs-lookup"><span data-stu-id="538e8-133">No</span></span><br/></td>
<td><span data-ttu-id="538e8-134">O símbolo de recurso para a imagem.</span><span class="sxs-lookup"><span data-stu-id="538e8-134">The resource symbol for the image.</span></span><br/> <br/><span data-ttu-id="538e8-135">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="538e8-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="538e8-136">Uma cadeia de caracteres composta de uma letra ou sublinhado seguida por qualquer sequência de letras, dígitos ou sublinhados até um máximo de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="538e8-136">A string composed of a letter or underscore followed by any sequence of letters, digits, or underscores up to a maximum of 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="538e8-137">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="538e8-137">Child elements</span></span>



| <span data-ttu-id="538e8-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="538e8-138">Element</span></span>                                                               | <span data-ttu-id="538e8-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="538e8-139">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="538e8-140">**Imagem. origem**</span><span class="sxs-lookup"><span data-stu-id="538e8-140">**Image.Source**</span></span>](windowsribbon-element-image-source.md)<br/> | <span data-ttu-id="538e8-141">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="538e8-141">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="538e8-142">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="538e8-142">Parent elements</span></span>



| <span data-ttu-id="538e8-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="538e8-143">Element</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="538e8-144">**Comando. LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="538e8-144">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [<span data-ttu-id="538e8-145">**Comando. LargeImages**</span><span class="sxs-lookup"><span data-stu-id="538e8-145">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         |
| [<span data-ttu-id="538e8-146">**Comando. SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="538e8-146">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [<span data-ttu-id="538e8-147">**Comando. SmallImages**</span><span class="sxs-lookup"><span data-stu-id="538e8-147">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a><span data-ttu-id="538e8-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="538e8-148">Remarks</span></span>

<span data-ttu-id="538e8-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="538e8-149">Optional.</span></span>

<span data-ttu-id="538e8-150">Pode ocorrer uma ou mais vezes para cada [**comando. SmallImages**](windowsribbon-element-command-smallimages.md), [**Command. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command. LargeImages**](windowsribbon-element-command-largeimages.md)ou [**Command. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) elemento.</span><span class="sxs-lookup"><span data-stu-id="538e8-150">May occur one or more times for each [**Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command.LargeImages**](windowsribbon-element-command-largeimages.md), or [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) element.</span></span>

<span data-ttu-id="538e8-151">Quando uma coleção de recursos de imagem que são projetados para dar suporte a configurações de pontos de tela específicos por polegada (DPI) é fornecida à estrutura da faixa de opções por meio de um conjunto de elementos **Image** , a estrutura usa a **imagem** com um valor de atributo *MinDPI* que corresponde à configuração de dpi de tela atual.</span><span class="sxs-lookup"><span data-stu-id="538e8-151">When a collection of image resources that are designed to support specific screen dots per inch (dpi) settings is supplied to the Ribbon framework through a set of **Image** elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>

<span data-ttu-id="538e8-152">Se nenhum elemento **Image** for declarado com um valor *MinDPI* que corresponda à configuração de dpi de tela atual, a estrutura selecionará a **imagem** que tem o valor de *MinDPI* mais próximo menor que a configuração de dpi de tela atual e dimensionará o recurso de imagem para cima.</span><span class="sxs-lookup"><span data-stu-id="538e8-152">If no **Image** element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="538e8-153">Caso contrário, se nenhum elemento **Image** for declarado com um valor de atributo *MinDPI* menor que a configuração de dpi de tela atual, a estrutura escolherá o valor de *MinDPI* mais próximo maior que a configuração de dpi de tela atual e dimensionará o recurso de imagem para baixo.</span><span class="sxs-lookup"><span data-stu-id="538e8-153">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

## <a name="examples"></a><span data-ttu-id="538e8-154">Exemplos</span><span class="sxs-lookup"><span data-stu-id="538e8-154">Examples</span></span>

<span data-ttu-id="538e8-155">O exemplo de código a seguir mostra a marcação necessária para declarar, por meio de um conjunto de elementos **Image** , uma coleção de recursos de imagem que são projetados para dar suporte a quatro configurações específicas de dpi de tela.</span><span class="sxs-lookup"><span data-stu-id="538e8-155">The following code example shows the markup required to declare, through a set of **Image** elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="538e8-156">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="538e8-156">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="538e8-157">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="538e8-157">Minimum supported system</span></span><br/> | <span data-ttu-id="538e8-158">Windows 7</span><span class="sxs-lookup"><span data-stu-id="538e8-158">Windows 7</span></span> |
| <span data-ttu-id="538e8-159">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="538e8-159">Can be empty</span></span>                        | <span data-ttu-id="538e8-160">Não</span><span class="sxs-lookup"><span data-stu-id="538e8-160">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="538e8-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="538e8-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="538e8-162">Especificando recursos de imagem da faixa de uma</span><span class="sxs-lookup"><span data-stu-id="538e8-162">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 





