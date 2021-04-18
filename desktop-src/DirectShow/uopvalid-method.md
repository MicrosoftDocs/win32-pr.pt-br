---
description: O método UOPValid recupera um valor que indica se a operação de usuário especificada (UOP) é válida no momento.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Método UOPValid (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3051ad20c496713880407270c7054839520ce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810929"
---
# <a name="uopvalid-method"></a><span data-ttu-id="b90b6-103">Método UOPValid</span><span class="sxs-lookup"><span data-stu-id="b90b6-103">UOPValid Method</span></span>

> [!Note]  
> <span data-ttu-id="b90b6-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b90b6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b90b6-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b90b6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b90b6-106">O `UOPValid` método recupera um valor que indica se a operação de usuário especificada (UOP) é válida no momento.</span><span class="sxs-lookup"><span data-stu-id="b90b6-106">The `UOPValid` method retrieves a value that indicates whether the specified user operation (UOP) is currently valid.</span></span>

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a><span data-ttu-id="b90b6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b90b6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b90b6-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*</span><span class="sxs-lookup"><span data-stu-id="b90b6-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*</span></span>
</dt> <dd>

<span data-ttu-id="b90b6-109">Especifica a operação do usuário (UOP) como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="b90b6-109">Specifies the user operation (UOP) as an Integer.</span></span>



| <span data-ttu-id="b90b6-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b90b6-110">Value</span></span> | <span data-ttu-id="b90b6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="b90b6-111">Description</span></span>                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b90b6-112">0</span><span class="sxs-lookup"><span data-stu-id="b90b6-112">0</span></span>     | <span data-ttu-id="b90b6-113">[**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)</span><span class="sxs-lookup"><span data-stu-id="b90b6-113">[**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)</span></span>                                                                                      |
| <span data-ttu-id="b90b6-114">1</span><span class="sxs-lookup"><span data-stu-id="b90b6-114">1</span></span>     | [<span data-ttu-id="b90b6-115">**PlayChapter**</span><span class="sxs-lookup"><span data-stu-id="b90b6-115">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="b90b6-116">2</span><span class="sxs-lookup"><span data-stu-id="b90b6-116">2</span></span>     | [<span data-ttu-id="b90b6-117">**PlayTitle**</span><span class="sxs-lookup"><span data-stu-id="b90b6-117">**PlayTitle**</span></span>](playtitle-method.md)                                                                                                                                                                                    |
| <span data-ttu-id="b90b6-118">3</span><span class="sxs-lookup"><span data-stu-id="b90b6-118">3</span></span>     | [<span data-ttu-id="b90b6-119">**Stop**</span><span class="sxs-lookup"><span data-stu-id="b90b6-119">**Stop**</span></span>](stop-method.md)                                                                                                                                                                                              |
| <span data-ttu-id="b90b6-120">4</span><span class="sxs-lookup"><span data-stu-id="b90b6-120">4</span></span>     | [<span data-ttu-id="b90b6-121">**ReturnFromSubmenu**</span><span class="sxs-lookup"><span data-stu-id="b90b6-121">**ReturnFromSubmenu**</span></span>](returnfromsubmenu-method.md)                                                                                                                                                                    |
| <span data-ttu-id="b90b6-122">5</span><span class="sxs-lookup"><span data-stu-id="b90b6-122">5</span></span>     | [<span data-ttu-id="b90b6-123">**PlayChapter**</span><span class="sxs-lookup"><span data-stu-id="b90b6-123">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="b90b6-124">6</span><span class="sxs-lookup"><span data-stu-id="b90b6-124">6</span></span>     | <span data-ttu-id="b90b6-125">[**PlayPrevChapter**](playprevchapter-method.md), [ **ReplayChapter**](replaychapter-method.md)</span><span class="sxs-lookup"><span data-stu-id="b90b6-125">[**PlayPrevChapter**](playprevchapter-method.md), [**ReplayChapter**](replaychapter-method.md)</span></span>                                                                                                                         |
| <span data-ttu-id="b90b6-126">7</span><span class="sxs-lookup"><span data-stu-id="b90b6-126">7</span></span>     | [<span data-ttu-id="b90b6-127">**PlayNextChapter**</span><span class="sxs-lookup"><span data-stu-id="b90b6-127">**PlayNextChapter**</span></span>](playnextchapter-method.md)                                                                                                                                                                        |
| <span data-ttu-id="b90b6-128">8</span><span class="sxs-lookup"><span data-stu-id="b90b6-128">8</span></span>     | [<span data-ttu-id="b90b6-129">**PlayForwards**</span><span class="sxs-lookup"><span data-stu-id="b90b6-129">**PlayForwards**</span></span>](playforwards-method.md)                                                                                                                                                                              |
| <span data-ttu-id="b90b6-130">9</span><span class="sxs-lookup"><span data-stu-id="b90b6-130">9</span></span>     | [<span data-ttu-id="b90b6-131">**PlayBackwards**</span><span class="sxs-lookup"><span data-stu-id="b90b6-131">**PlayBackwards**</span></span>](playbackwards-method.md)                                                                                                                                                                            |
| <span data-ttu-id="b90b6-132">10</span><span class="sxs-lookup"><span data-stu-id="b90b6-132">10</span></span>    | <span data-ttu-id="b90b6-133">[**Menu**](showmenu-method.md) de propriedade com um valor de parâmetro 2 ( \_ título de menu de DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="b90b6-133">[**ShowMenu**](showmenu-method.md) with a parameter value of 2 (DVD\_MENU\_Title)</span></span>                                                                                                                                       |
| <span data-ttu-id="b90b6-134">11</span><span class="sxs-lookup"><span data-stu-id="b90b6-134">11</span></span>    | <span data-ttu-id="b90b6-135">[**Menu de atalho**](showmenu-method.md) com um valor de parâmetro de 3 (raiz do menu do DVD \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="b90b6-135">[**ShowMenu**](showmenu-method.md) with a parameter value of 3 (DVD\_MENU\_Root)</span></span>                                                                                                                                        |
| <span data-ttu-id="b90b6-136">12</span><span class="sxs-lookup"><span data-stu-id="b90b6-136">12</span></span>    | <span data-ttu-id="b90b6-137">[**Menu de menus**](showmenu-method.md) com um valor de parâmetro 4 ( \_ subimagem do menu DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="b90b6-137">[**ShowMenu**](showmenu-method.md) with a parameter value of 4 (DVD\_MENU\_Subpicture)</span></span>                                                                                                                                  |
| <span data-ttu-id="b90b6-138">13</span><span class="sxs-lookup"><span data-stu-id="b90b6-138">13</span></span>    | <span data-ttu-id="b90b6-139">[**Menu de atalho**](showmenu-method.md) com um valor de parâmetro de 5 (áudio de menu de DVD \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="b90b6-139">[**ShowMenu**](showmenu-method.md) with a parameter value of 5 (DVD\_MENU\_Audio)</span></span>                                                                                                                                       |
| <span data-ttu-id="b90b6-140">14</span><span class="sxs-lookup"><span data-stu-id="b90b6-140">14</span></span>    | <span data-ttu-id="b90b6-141">[**Menu de atalho**](showmenu-method.md) com um valor de parâmetro 6 ( \_ ângulo de menu de DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="b90b6-141">[**ShowMenu**](showmenu-method.md) with a parameter value of 6 (DVD\_MENU\_Angle)</span></span>                                                                                                                                       |
| <span data-ttu-id="b90b6-142">15</span><span class="sxs-lookup"><span data-stu-id="b90b6-142">15</span></span>    | <span data-ttu-id="b90b6-143">[**Menu de atalho**](showmenu-method.md) com um valor de parâmetro de 7 (capítulo de menu do DVD \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="b90b6-143">[**ShowMenu**](showmenu-method.md) with a parameter value of 7 (DVD\_MENU\_Chapter)</span></span>                                                                                                                                     |
| <span data-ttu-id="b90b6-144">16</span><span class="sxs-lookup"><span data-stu-id="b90b6-144">16</span></span>    | [<span data-ttu-id="b90b6-145">**Retomar**</span><span class="sxs-lookup"><span data-stu-id="b90b6-145">**Resume**</span></span>](resume-method.md)                                                                                                                                                                                          |
| <span data-ttu-id="b90b6-146">17</span><span class="sxs-lookup"><span data-stu-id="b90b6-146">17</span></span>    | <span data-ttu-id="b90b6-147">[**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md)</span><span class="sxs-lookup"><span data-stu-id="b90b6-147">[**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md)</span></span> |
| <span data-ttu-id="b90b6-148">18</span><span class="sxs-lookup"><span data-stu-id="b90b6-148">18</span></span>    | [<span data-ttu-id="b90b6-149">**StillOff**</span><span class="sxs-lookup"><span data-stu-id="b90b6-149">**StillOff**</span></span>](stilloff-method.md)                                                                                                                                                                                      |
| <span data-ttu-id="b90b6-150">19</span><span class="sxs-lookup"><span data-stu-id="b90b6-150">19</span></span>    | [<span data-ttu-id="b90b6-151">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="b90b6-151">**Pause**</span></span>](pause-method.md)                                                                                                                                                                                            |
| <span data-ttu-id="b90b6-152">20</span><span class="sxs-lookup"><span data-stu-id="b90b6-152">20</span></span>    | [<span data-ttu-id="b90b6-153">**CurrentAudioStream**</span><span class="sxs-lookup"><span data-stu-id="b90b6-153">**CurrentAudioStream**</span></span>](currentaudiostream-property.md)                                                                                                                                                                |
| <span data-ttu-id="b90b6-154">21</span><span class="sxs-lookup"><span data-stu-id="b90b6-154">21</span></span>    | [<span data-ttu-id="b90b6-155">**CurrentSubpictureStream**</span><span class="sxs-lookup"><span data-stu-id="b90b6-155">**CurrentSubpictureStream**</span></span>](currentsubpicturestream-property.md)                                                                                                                                                      |
| <span data-ttu-id="b90b6-156">22</span><span class="sxs-lookup"><span data-stu-id="b90b6-156">22</span></span>    | <span data-ttu-id="b90b6-157">[**CurrentAngle**](currentangle-property.md), [ **SelectParentalLevel**](selectparentallevel-method.md)</span><span class="sxs-lookup"><span data-stu-id="b90b6-157">[**CurrentAngle**](currentangle-property.md), [**SelectParentalLevel**](selectparentallevel-method.md)</span></span>                                                                                                                 |
| <span data-ttu-id="b90b6-158">23</span><span class="sxs-lookup"><span data-stu-id="b90b6-158">23</span></span>    | [<span data-ttu-id="b90b6-159">**KaraokeAudioPresentationMode**</span><span class="sxs-lookup"><span data-stu-id="b90b6-159">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| <span data-ttu-id="b90b6-160">24</span><span class="sxs-lookup"><span data-stu-id="b90b6-160">24</span></span>    | <span data-ttu-id="b90b6-161">Selecione preferência de modo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b90b6-161">Select video mode preference.</span></span>                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b90b6-162">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b90b6-162">Return Value</span></span>

<span data-ttu-id="b90b6-163">Retorna um valor booliano que indica se a operação especificada é permitida pelo controle UOP.</span><span class="sxs-lookup"><span data-stu-id="b90b6-163">Returns a Boolean value indicating whether the specified operation is permitted by UOP control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b90b6-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b90b6-164">Requirements</span></span>



| <span data-ttu-id="b90b6-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="b90b6-165">Requirement</span></span> | <span data-ttu-id="b90b6-166">Valor</span><span class="sxs-lookup"><span data-stu-id="b90b6-166">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b90b6-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b90b6-167">Header</span></span><br/> | <dl> <span data-ttu-id="b90b6-168"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="b90b6-168"><dt>Segment.h</dt></span></span> </dl> |



 

 




