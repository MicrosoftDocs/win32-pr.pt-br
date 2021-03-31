---
description: Representa a área que o reconhecedor usa no qual a tinta pode ser desenhada. A área é conhecida como o guia de reconhecimento.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: Classe InkRecognizerGuide (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerGuide
- InkRecognizerGuide.IInkRecognizerGuide
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 55729513f748afc87f184b73eaba976184307bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172066"
---
# <a name="inkrecognizerguide-class"></a><span data-ttu-id="4f7f5-104">Classe InkRecognizerGuide</span><span class="sxs-lookup"><span data-stu-id="4f7f5-104">InkRecognizerGuide class</span></span>

<span data-ttu-id="4f7f5-105">Representa a área que o reconhecedor usa no qual a tinta pode ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-105">Represents the area that the recognizer uses in which ink can be drawn.</span></span> <span data-ttu-id="4f7f5-106">A área é conhecida como o guia de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-106">The area is known as the recognition guide.</span></span>

<span data-ttu-id="4f7f5-107">**InkRecognizerGuide** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4f7f5-107">**InkRecognizerGuide** has these types of members:</span></span>

-   [<span data-ttu-id="4f7f5-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="4f7f5-108">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="4f7f5-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4f7f5-109">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="4f7f5-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="4f7f5-110">Interfaces</span></span>

<span data-ttu-id="4f7f5-111">A classe **InkRecognizerGuide** define essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-111">The **InkRecognizerGuide** class defines these interfaces.</span></span>



| <span data-ttu-id="4f7f5-112">Interface</span><span class="sxs-lookup"><span data-stu-id="4f7f5-112">Interface</span></span>               | <span data-ttu-id="4f7f5-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f7f5-113">Description</span></span>                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="4f7f5-114">**IInkRecognizerGuide**</span><span class="sxs-lookup"><span data-stu-id="4f7f5-114">**IInkRecognizerGuide**</span></span> | <span data-ttu-id="4f7f5-115">Esse objeto implementa a interface com do **IInkRecognizerGuide** .</span><span class="sxs-lookup"><span data-stu-id="4f7f5-115">This object implements the **IInkRecognizerGuide** COM interface.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4f7f5-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4f7f5-116">Properties</span></span>

<span data-ttu-id="4f7f5-117">A classe **InkRecognizerGuide** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-117">The **InkRecognizerGuide** class has these properties.</span></span>



| <span data-ttu-id="4f7f5-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4f7f5-118">Property</span></span>                                                       | <span data-ttu-id="4f7f5-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="4f7f5-119">Access type</span></span>           | <span data-ttu-id="4f7f5-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f7f5-120">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f7f5-121">**Colunas**</span><span class="sxs-lookup"><span data-stu-id="4f7f5-121">**Columns**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | <span data-ttu-id="4f7f5-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4f7f5-122">Read/write</span></span><br/> | <span data-ttu-id="4f7f5-123">Obtém ou define o número de colunas na caixa guia.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-123">Gets or sets the number of columns in the guide box.</span></span><br/>                                                                |
| [<span data-ttu-id="4f7f5-124">**DrawnBox**</span><span class="sxs-lookup"><span data-stu-id="4f7f5-124">**DrawnBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | <span data-ttu-id="4f7f5-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4f7f5-125">Read/write</span></span><br/> | <span data-ttu-id="4f7f5-126">Obtém ou define a caixa que é desenhada fisicamente na tela do Tablet e em que ocorre a gravação.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-126">Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place.</span></span><br/>              |
| [<span data-ttu-id="4f7f5-127">**GuideData**</span><span class="sxs-lookup"><span data-stu-id="4f7f5-127">**GuideData**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | <span data-ttu-id="4f7f5-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4f7f5-128">Read/write</span></span><br/> | <span data-ttu-id="4f7f5-129">Obtém ou define os dados do guia para desenvolvedores do C++.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-129">Gets or sets guide data for C++ developers.</span></span><br/>                                                                         |
| [<span data-ttu-id="4f7f5-130">**Tabs no meio**</span><span class="sxs-lookup"><span data-stu-id="4f7f5-130">**Midline**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | <span data-ttu-id="4f7f5-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4f7f5-131">Read/write</span></span><br/> | <span data-ttu-id="4f7f5-132">Obtém ou define a altura de Tabs no meio.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-132">Gets or sets the midline height.</span></span> <span data-ttu-id="4f7f5-133">A altura de Tabs no meio é a distância da linha de base para o Tabs no meio da caixa de desenho.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-133">The midline height is distance from the baseline to the midline, of the drawn box.</span></span><br/> |
| [<span data-ttu-id="4f7f5-134">**As**</span><span class="sxs-lookup"><span data-stu-id="4f7f5-134">**Rows**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | <span data-ttu-id="4f7f5-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4f7f5-135">Read/write</span></span><br/> | <span data-ttu-id="4f7f5-136">Obtém ou define o número de linhas na caixa guia.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-136">Gets or sets the number of rows in the guide box.</span></span><br/>                                                                   |
| [<span data-ttu-id="4f7f5-137">**WritingBox**</span><span class="sxs-lookup"><span data-stu-id="4f7f5-137">**WritingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | <span data-ttu-id="4f7f5-138">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4f7f5-138">Read/write</span></span><br/> | <span data-ttu-id="4f7f5-139">Obtém ou define a área de escrita invisível da caixa guia na qual a gravação pode realmente ocorrer.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-139">Gets or sets the invisible writing area of the guide box in which writing can actually take place.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="4f7f5-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f7f5-140">Remarks</span></span>

<span data-ttu-id="4f7f5-141">Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="4f7f5-141">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method.</span></span>

<span data-ttu-id="4f7f5-142">Por padrão, não há nenhum guia do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-142">By default, there is no recognizer guide.</span></span> <span data-ttu-id="4f7f5-143">Um guia padrão tem todos os valores de propriedade definidos como 0.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-143">A default guide has all property values set to 0.</span></span> <span data-ttu-id="4f7f5-144">Você deve usar as propriedades desse objeto para definir o guia.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-144">You must use the properties of this object to set the guide.</span></span>

<span data-ttu-id="4f7f5-145">Se o aplicativo tiver diretrizes desenhadas na tela em que o usuário deve gravar, o aplicativo deverá definir os valores das propriedades do guia do reconhecedor para informar o reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-145">If the application has drawn guidelines on the screen on which the user is expected to write, the application should set the values of the properties of the recognizer guide to inform the recognizer.</span></span> <span data-ttu-id="4f7f5-146">Essas propriedades são apenas para uso do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-146">These properties are for the recognizer's use only.</span></span> <span data-ttu-id="4f7f5-147">Configurá-las não faz, por si só, desenhar pistas visuais na exibição.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-147">Setting them does not, by itself, draw visual clues on the display.</span></span> <span data-ttu-id="4f7f5-148">O aplicativo ou o controle desenha as pistas visuais.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-148">The application or the control draws the visual clues.</span></span>

<span data-ttu-id="4f7f5-149">O guia do reconhecedor pode consistir em linhas e colunas, e elas dão ao reconhecedor um contexto melhor para executar o reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-149">The recognizer guide can consist of rows and columns, and these give the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="4f7f5-150">Letras como "t" e "I" são mais facilmente reconhecidas quando um guia é usado para dar contexto à tinta.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-150">Letters such as "t" and "I" are more easily recognized when a guide is used to give context to the ink.</span></span> <span data-ttu-id="4f7f5-151">Por exemplo, você pode desenhar linhas horizontais em uma tela, que mostram onde deve ocorrer gravação (esse tipo de guia consistiria apenas em linhas e nenhuma coluna).</span><span class="sxs-lookup"><span data-stu-id="4f7f5-151">For example, you can draw horizontal lines on a screen, that show where writing should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="4f7f5-152">Ao escrever nas linhas, em vez de algum espaço arbitrário, a precisão de reconhecimento melhora.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-152">By writing on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="4f7f5-153">O guia especifica os limites da tinta nas coordenadas de espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-153">The guide specifies the boundaries of the ink in ink space coordinates.</span></span>

<span data-ttu-id="4f7f5-154">A propriedade [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) pode definir uma caixa que é do mesmo tamanho que ou menor que a caixa definida pela propriedade [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) .</span><span class="sxs-lookup"><span data-stu-id="4f7f5-154">The [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) property can define a box which is the same size as or smaller than the box defined by the [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) property.</span></span>

<span data-ttu-id="4f7f5-155">A figura a seguir mostra os elementos de um guia do reconhecedor com duas linhas e nenhuma coluna.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-155">The following figure shows the elements of a recognizer guide with two rows and no columns.</span></span>

![ilustração mostrando elementos do guia do reconhecedor](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

<span data-ttu-id="4f7f5-157">Além de desenhar linhas na tela que mostram os usuários onde escrever, você pode desenhar células na tela em que os caracteres ou palavras são gravados.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-157">In addition to drawing lines on the screen that show users where to write, you can draw cells on the screen in which characters or words are written.</span></span> <span data-ttu-id="4f7f5-158">Isso é chamado de entrada em caixa e é útil em alguns idiomas asiáticos.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-158">This is called boxed input and is useful with some Asian languages.</span></span> <span data-ttu-id="4f7f5-159">Para determinar se o reconhecedor é capaz de entrada em caixa, chame a propriedade [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) do objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) .</span><span class="sxs-lookup"><span data-stu-id="4f7f5-159">To determine if the recognizer is capable of boxed input, call the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object.</span></span>

<span data-ttu-id="4f7f5-160">A figura a seguir mostra um guia do reconhecedor com quatro colunas.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-160">The following figure shows a recognizer guide with four columns.</span></span>

![ilustração mostrando o guia do reconhecedor com quatro colunas](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a><span data-ttu-id="4f7f5-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f7f5-162">Requirements</span></span>



| <span data-ttu-id="4f7f5-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f7f5-163">Requirement</span></span> | <span data-ttu-id="4f7f5-164">Valor</span><span class="sxs-lookup"><span data-stu-id="4f7f5-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f7f5-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f7f5-165">Minimum supported client</span></span><br/> | <span data-ttu-id="4f7f5-166">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4f7f5-166">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4f7f5-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f7f5-167">Minimum supported server</span></span><br/> | <span data-ttu-id="4f7f5-168">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4f7f5-168">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4f7f5-169">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f7f5-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f7f5-170"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4f7f5-170"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4f7f5-171">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f7f5-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="4f7f5-172"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f7f5-172"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4f7f5-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f7f5-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f7f5-174">**Interface IInkRecognizer**</span><span class="sxs-lookup"><span data-stu-id="4f7f5-174">**IInkRecognizer Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[<span data-ttu-id="4f7f5-175">**Classe InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="4f7f5-175">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

