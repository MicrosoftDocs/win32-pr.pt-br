---
description: Um sistema de classificação que usa valores inteiros entre 1 e 99. Esse é o sistema de classificação usado pelo shell do Windows Vista.
ms.assetid: a6288d29-1ef3-4da1-bd30-577336ab6817
title: System. rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e411e313f0fa6042a8cbe3a076a7166928020af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794604"
---
# <a name="systemrating"></a><span data-ttu-id="e3b69-104">System. rating</span><span class="sxs-lookup"><span data-stu-id="e3b69-104">System.Rating</span></span>

<span data-ttu-id="e3b69-105">Um sistema de classificação que usa valores inteiros entre 1 e 99.</span><span class="sxs-lookup"><span data-stu-id="e3b69-105">A rating system that uses integer values between 1 and 99.</span></span> <span data-ttu-id="e3b69-106">Esse é o sistema de classificação usado pelo shell do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e3b69-106">This is the rating system used by the Windows Vista Shell.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="e3b69-107">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="e3b69-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = OneStar
            minValue = 1
            setValue = 1
            defineMaxValue = 12
            text = 1 Star
            defineToken = RATING_ONE_STAR
         enumRange
            name = TwoStars
            minValue = 13
            setValue = 25
            defineMaxValue = 37
            text = 2 Stars
            defineToken = RATING_TWO_STARS
         enumRange
            name = ThreeStars
            minValue = 38
            setValue = 50
            defineMaxValue = 62
            text = 3 Stars
            defineToken = RATING_THREE_STARS
         enumRange
            name = FourStars
            minValue = 63
            setValue = 75
            defineMaxValue = 87
            text = 4 Stars
            defineToken = RATING_FOUR_STARS
         enumRange
            name = FiveStars
            minValue = 88
            setValue = 99
            defineMaxValue = 99
            text = 5 Stars
            defineToken = RATING_FIVE_STARS
         enumRange
            name
            minValue = 100
```

## <a name="windows-vista"></a><span data-ttu-id="e3b69-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3b69-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            defineMinName = RATING_UNRATED_MIN
            setValue = 0
            defineSetName = RATING_UNRATED_SET
            defineMaxValue = 0
            defineMaxName = RATING_UNRATED_MAX
            text = Unrated
         enumRange
            minValue = 1
            defineMinName = RATING_ONE_STAR_MIN
            setValue = 1
            defineSetName = RATING_ONE_STAR_SET
            defineMaxValue = 12
            defineMaxName = RATING_ONE_STAR_MAX
            text = 1 Star
         enumRange
            minValue = 13
            defineMinName = RATING_TWO_STARS_MIN
            setValue = 25
            defineSetName = RATING_TWO_STARS_SET
            defineMaxValue = 37
            defineMaxName = RATING_TWO_STARS_MAX
            text = 2 Stars
         enumRange
            minValue = 38
            defineMinName = RATING_THREE_STARS_MIN
            setValue = 50
            defineSetName = RATING_THREE_STARS_SET
            defineMaxValue = 62
            defineMaxName = RATING_THREE_STARS_MAX
            text = 3 Stars
         enumRange
            minValue = 63
            defineMinName = RATING_FOUR_STARS_MIN
            setValue = 75
            defineSetName = RATING_FOUR_STARS_SET
            defineMaxValue = 87
            defineMaxName = RATING_FOUR_STARS_MAX
            text = 4 Stars
         enumRange
            minValue = 88
            defineMinName = RATING_FIVE_STARS_MIN
            setValue = 99
            defineSetName = RATING_FIVE_STARS_SET
            defineMaxValue = 99
            defineMaxName = RATING_FIVE_STARS_MAX
            text = 5 Stars
         enumRange
            minValue = 100
```

## <a name="remarks"></a><span data-ttu-id="e3b69-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3b69-109">Remarks</span></span>

<span data-ttu-id="e3b69-110">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="e3b69-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="e3b69-111">Para obter compatibilidade com os sistemas de classificação que usam valores entre 1 e 5, consulte a propriedade [System. SimpleRating](./props-system-simplerating.md).</span><span class="sxs-lookup"><span data-stu-id="e3b69-111">For compatibility with ratings systems that use values between 1 and 5, see the property [System.SimpleRating](./props-system-simplerating.md).</span></span> <span data-ttu-id="e3b69-112">No entanto, observe que System. SimpleRating não é usado no Shell do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e3b69-112">Note, however, that System.SimpleRating is not used in the Windows Vista Shell.</span></span>

<span data-ttu-id="e3b69-113">A tabela a seguir descreve o que o sistema de classificação por estrelas usou na interface do usuário do shell significa em termos de valor [System. rating]() .</span><span class="sxs-lookup"><span data-stu-id="e3b69-113">The following table describes what the star rating system used in the Shell UI means in terms of the [System.Rating]() value.</span></span>



| <span data-ttu-id="e3b69-114">System. rating</span><span class="sxs-lookup"><span data-stu-id="e3b69-114">System.Rating</span></span> | <span data-ttu-id="e3b69-115">Classificação por Estrelas</span><span class="sxs-lookup"><span data-stu-id="e3b69-115">Star Rating</span></span> |
|---------------|-------------|
| <span data-ttu-id="e3b69-116">1-12</span><span class="sxs-lookup"><span data-stu-id="e3b69-116">1-12</span></span>          | <span data-ttu-id="e3b69-117">1 estrela</span><span class="sxs-lookup"><span data-stu-id="e3b69-117">1 Star</span></span>      |
| <span data-ttu-id="e3b69-118">13-37</span><span class="sxs-lookup"><span data-stu-id="e3b69-118">13-37</span></span>         | <span data-ttu-id="e3b69-119">2 estrelas</span><span class="sxs-lookup"><span data-stu-id="e3b69-119">2 Stars</span></span>     |
| <span data-ttu-id="e3b69-120">38-62</span><span class="sxs-lookup"><span data-stu-id="e3b69-120">38-62</span></span>         | <span data-ttu-id="e3b69-121">3 estrelas</span><span class="sxs-lookup"><span data-stu-id="e3b69-121">3 Stars</span></span>     |
| <span data-ttu-id="e3b69-122">63-87</span><span class="sxs-lookup"><span data-stu-id="e3b69-122">63-87</span></span>         | <span data-ttu-id="e3b69-123">4 estrelas</span><span class="sxs-lookup"><span data-stu-id="e3b69-123">4 Stars</span></span>     |
| <span data-ttu-id="e3b69-124">88-99</span><span class="sxs-lookup"><span data-stu-id="e3b69-124">88-99</span></span>         | <span data-ttu-id="e3b69-125">5 estrelas</span><span class="sxs-lookup"><span data-stu-id="e3b69-125">5 Stars</span></span>     |



 

<span data-ttu-id="e3b69-126">Quando um usuário classifica um item, escolhendo um valor de classificação por estrelas na interface do usuário, os valores reais de [System. rating]() são atribuídos conforme mostrado nesta tabela:</span><span class="sxs-lookup"><span data-stu-id="e3b69-126">When a user rates an item by choosing a star rating value in the UI, actual [System.Rating]() values are assigned as shown in this table:</span></span>



| <span data-ttu-id="e3b69-127">Classificação por Estrelas</span><span class="sxs-lookup"><span data-stu-id="e3b69-127">Star Rating</span></span> | <span data-ttu-id="e3b69-128">Valor atribuído por meio da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="e3b69-128">Value Assigned Through UI</span></span> |
|-------------|---------------------------|
| <span data-ttu-id="e3b69-129">1 estrela</span><span class="sxs-lookup"><span data-stu-id="e3b69-129">1 Star</span></span>      | <span data-ttu-id="e3b69-130">1</span><span class="sxs-lookup"><span data-stu-id="e3b69-130">1</span></span>                         |
| <span data-ttu-id="e3b69-131">2 estrelas</span><span class="sxs-lookup"><span data-stu-id="e3b69-131">2 Stars</span></span>     | <span data-ttu-id="e3b69-132">25</span><span class="sxs-lookup"><span data-stu-id="e3b69-132">25</span></span>                        |
| <span data-ttu-id="e3b69-133">3 estrelas</span><span class="sxs-lookup"><span data-stu-id="e3b69-133">3 Stars</span></span>     | <span data-ttu-id="e3b69-134">50</span><span class="sxs-lookup"><span data-stu-id="e3b69-134">50</span></span>                        |
| <span data-ttu-id="e3b69-135">4 estrelas</span><span class="sxs-lookup"><span data-stu-id="e3b69-135">4 Stars</span></span>     | <span data-ttu-id="e3b69-136">75</span><span class="sxs-lookup"><span data-stu-id="e3b69-136">75</span></span>                        |
| <span data-ttu-id="e3b69-137">5 estrelas</span><span class="sxs-lookup"><span data-stu-id="e3b69-137">5 Stars</span></span>     | <span data-ttu-id="e3b69-138">99</span><span class="sxs-lookup"><span data-stu-id="e3b69-138">99</span></span>                        |



 

<span data-ttu-id="e3b69-139">Se o arquivo tiver um valor [System. SimpleRating](./props-system-simplerating.md) em vez de um valor [System. rating]() , use a tabela abaixo para converter e especificar valores para System. rating.</span><span class="sxs-lookup"><span data-stu-id="e3b69-139">If your file has a [System.SimpleRating](./props-system-simplerating.md) value rather than a [System.Rating]() value, use the table below to convert and specify values for System.Rating.</span></span>



| <span data-ttu-id="e3b69-140">System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="e3b69-140">System.SimpleRating</span></span> | <span data-ttu-id="e3b69-141">System. rating</span><span class="sxs-lookup"><span data-stu-id="e3b69-141">System.Rating</span></span> |
|---------------------|---------------|
| <span data-ttu-id="e3b69-142">1</span><span class="sxs-lookup"><span data-stu-id="e3b69-142">1</span></span>                   | <span data-ttu-id="e3b69-143">1</span><span class="sxs-lookup"><span data-stu-id="e3b69-143">1</span></span>             |
| <span data-ttu-id="e3b69-144">2</span><span class="sxs-lookup"><span data-stu-id="e3b69-144">2</span></span>                   | <span data-ttu-id="e3b69-145">25</span><span class="sxs-lookup"><span data-stu-id="e3b69-145">25</span></span>            |
| <span data-ttu-id="e3b69-146">3</span><span class="sxs-lookup"><span data-stu-id="e3b69-146">3</span></span>                   | <span data-ttu-id="e3b69-147">50</span><span class="sxs-lookup"><span data-stu-id="e3b69-147">50</span></span>            |
| <span data-ttu-id="e3b69-148">4</span><span class="sxs-lookup"><span data-stu-id="e3b69-148">4</span></span>                   | <span data-ttu-id="e3b69-149">75</span><span class="sxs-lookup"><span data-stu-id="e3b69-149">75</span></span>            |
| <span data-ttu-id="e3b69-150">5</span><span class="sxs-lookup"><span data-stu-id="e3b69-150">5</span></span>                   | <span data-ttu-id="e3b69-151">99</span><span class="sxs-lookup"><span data-stu-id="e3b69-151">99</span></span>            |



 

<span data-ttu-id="e3b69-152">Se o arquivo tiver os valores [System. rating]() e [System. SimpleRating](./props-system-simplerating.md) persistentes, sempre use o valor System. rating quando ele for solicitado diretamente, sem referência a System. SimpleRating.</span><span class="sxs-lookup"><span data-stu-id="e3b69-152">If your file has both [System.Rating]() and [System.SimpleRating](./props-system-simplerating.md) persisted values, always use the System.Rating value when it is directly requested, without reference to System.SimpleRating.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3b69-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3b69-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3b69-154">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e3b69-154">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e3b69-155">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e3b69-155">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e3b69-156">labelInfo</span><span class="sxs-lookup"><span data-stu-id="e3b69-156">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e3b69-157">typeInfo</span><span class="sxs-lookup"><span data-stu-id="e3b69-157">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e3b69-158">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e3b69-158">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e3b69-159">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e3b69-159">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e3b69-160">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="e3b69-160">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e3b69-161">numberFormat</span><span class="sxs-lookup"><span data-stu-id="e3b69-161">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e3b69-162">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e3b69-162">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e3b69-163">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="e3b69-163">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e3b69-164">drawControl</span><span class="sxs-lookup"><span data-stu-id="e3b69-164">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e3b69-165">editControl</span><span class="sxs-lookup"><span data-stu-id="e3b69-165">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e3b69-166">filterControl</span><span class="sxs-lookup"><span data-stu-id="e3b69-166">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e3b69-167">queryControl</span><span class="sxs-lookup"><span data-stu-id="e3b69-167">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
