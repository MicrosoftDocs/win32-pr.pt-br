---
description: Representa a capacidade de analisar o layout de uma coleção de traços e dividi-los em texto e gráficos.
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: Classe InkDivider (Msinkaut15. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDivider
- InkDivider.IInkDivider
api_type:
- COM
api_location:
- Inkdiv.dll
- Inkdiv.dll.dll
ms.openlocfilehash: c0658504303968803bd2abff063694701d121390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762054"
---
# <a name="inkdivider-class"></a><span data-ttu-id="58a9e-103">Classe InkDivider</span><span class="sxs-lookup"><span data-stu-id="58a9e-103">InkDivider class</span></span>

<span data-ttu-id="58a9e-104">Representa a capacidade de analisar o layout de uma coleção de traços e dividi-los em texto e gráficos.</span><span class="sxs-lookup"><span data-stu-id="58a9e-104">Represents the ability to analyze the layout of a collection of strokes and divide them into text and graphics.</span></span>

<span data-ttu-id="58a9e-105">**InkDivider** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="58a9e-105">**InkDivider** has these types of members:</span></span>

-   [<span data-ttu-id="58a9e-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="58a9e-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="58a9e-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="58a9e-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="58a9e-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58a9e-108">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="58a9e-109">Interfaces</span><span class="sxs-lookup"><span data-stu-id="58a9e-109">Interfaces</span></span>

<span data-ttu-id="58a9e-110">A classe **InkDivider** define essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="58a9e-110">The **InkDivider** class defines these interfaces.</span></span>



| <span data-ttu-id="58a9e-111">Interface</span><span class="sxs-lookup"><span data-stu-id="58a9e-111">Interface</span></span>       | <span data-ttu-id="58a9e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="58a9e-112">Description</span></span>                                                          |
|:----------------|:---------------------------------------------------------------------|
| <span data-ttu-id="58a9e-113">**IInkDivider**</span><span class="sxs-lookup"><span data-stu-id="58a9e-113">**IInkDivider**</span></span> | <span data-ttu-id="58a9e-114">Esse objeto implementa a interface com do **IInkDivider** .</span><span class="sxs-lookup"><span data-stu-id="58a9e-114">This object implements the **IInkDivider** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="58a9e-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="58a9e-115">Methods</span></span>

<span data-ttu-id="58a9e-116">A classe **InkDivider** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="58a9e-116">The **InkDivider** class has these methods.</span></span>



| <span data-ttu-id="58a9e-117">Método</span><span class="sxs-lookup"><span data-stu-id="58a9e-117">Method</span></span>                              | <span data-ttu-id="58a9e-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="58a9e-118">Description</span></span>                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58a9e-119">**Dividir**</span><span class="sxs-lookup"><span data-stu-id="58a9e-119">**Divide**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | <span data-ttu-id="58a9e-120">Retorna um objeto [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) que contém informações estruturais sobre os traços no objeto **InkDivider** .</span><span class="sxs-lookup"><span data-stu-id="58a9e-120">Returns an [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object that contains structural information about the strokes in the **InkDivider** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="58a9e-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58a9e-121">Properties</span></span>

<span data-ttu-id="58a9e-122">A classe **InkDivider** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="58a9e-122">The **InkDivider** class has these properties.</span></span>



| <span data-ttu-id="58a9e-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="58a9e-123">Property</span></span>                                                             | <span data-ttu-id="58a9e-124">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="58a9e-124">Access type</span></span>           | <span data-ttu-id="58a9e-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="58a9e-125">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58a9e-126">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="58a9e-126">**LineHeight**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | <span data-ttu-id="58a9e-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="58a9e-127">Read/write</span></span><br/> | <span data-ttu-id="58a9e-128">Obtém ou define a altura de manuscrito esperada em unidades HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="58a9e-128">Gets or sets the expected handwriting height in HIMETRIC units.</span></span><br/>                                                      |
| [<span data-ttu-id="58a9e-129">**RecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="58a9e-129">**RecognizerContext**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | <span data-ttu-id="58a9e-130">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="58a9e-130">Read/write</span></span><br/> | <span data-ttu-id="58a9e-131">Obtém ou define o objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) usado para reconhecimento de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="58a9e-131">Gets or sets the [**InkRecognizerContext**](inkrecognizercontext-class.md) object used for handwriting recognition.</span></span><br/> |
| [<span data-ttu-id="58a9e-132">**Traços**</span><span class="sxs-lookup"><span data-stu-id="58a9e-132">**Strokes**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | <span data-ttu-id="58a9e-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="58a9e-133">Read/write</span></span><br/> | <span data-ttu-id="58a9e-134">Obtém ou define a coleção [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contida pelo objeto **InkDivider** .</span><span class="sxs-lookup"><span data-stu-id="58a9e-134">Gets or sets the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained by the **InkDivider** object.</span></span> <br/>     |



 

## <a name="remarks"></a><span data-ttu-id="58a9e-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="58a9e-135">Remarks</span></span>

<span data-ttu-id="58a9e-136">Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.</span><span class="sxs-lookup"><span data-stu-id="58a9e-136">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="58a9e-137">O objeto **InkDivider** usa o layout dos traços, a ordem na qual os traços são adicionados, a direção na qual os traços são desenhados e outros fatores para executar a análise da tinta.</span><span class="sxs-lookup"><span data-stu-id="58a9e-137">The **InkDivider** object uses the layout of the strokes, the order in which the strokes are added, the direction in which the strokes are drawn, and other factors to perform the analysis of the ink.</span></span> <span data-ttu-id="58a9e-138">A coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que o objeto **InkDivider** analisa está contida na propriedade [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) do objeto **InkDivider** .</span><span class="sxs-lookup"><span data-stu-id="58a9e-138">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the **InkDivider** object analyzes is contained in the [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) property of the **InkDivider** object.</span></span> <span data-ttu-id="58a9e-139">O objeto **InkDivider** analisa dinamicamente a coleção InkStrokes à medida que você adiciona ou exclui da coleção, mas não executa nenhuma modificação dos traços.</span><span class="sxs-lookup"><span data-stu-id="58a9e-139">The **InkDivider** object dynamically analyzes the InkStrokes collection as you add to or delete from the collection, but it performs no modification of the strokes.</span></span>

<span data-ttu-id="58a9e-140">Os resultados da análise são retornados em um objeto [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="58a9e-140">The analysis results are returned in an [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

<span data-ttu-id="58a9e-141">O objeto **InkDivider** usa um objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) para dividir com mais precisão os traços e atribuir uma cadeia de caracteres de reconhecimento aos resultados.</span><span class="sxs-lookup"><span data-stu-id="58a9e-141">The **InkDivider** object uses an [**InkRecognizerContext**](inkrecognizercontext-class.md) object to more accurately divide the strokes and to assign a recognition string to the results.</span></span>

> [!Note]  
> <span data-ttu-id="58a9e-142">O objeto **InkDivider** usa as configurações de propriedade padrão do objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="58a9e-142">The **InkDivider** object uses the default property settings of the [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

 

<span data-ttu-id="58a9e-143">Se você não atribuir um contexto de reconhecedor ao objeto **InkDivider** , o objeto **InkDivider** ainda analisará a tinta, mas dividirá os traços menos precisamente e não associará o texto aos resultados da divisão.</span><span class="sxs-lookup"><span data-stu-id="58a9e-143">If you do not assign a recognizer context to the **InkDivider** object, the **InkDivider** object still analyzes the ink, but it divides the strokes less accurately and does not associate text with the division results.</span></span>

> [!Note]  
> <span data-ttu-id="58a9e-144">A propriedade [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) deve ser definida antes da adição de traços à propriedade [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) .</span><span class="sxs-lookup"><span data-stu-id="58a9e-144">The [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property should be set before adding strokes to the [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) property.</span></span> <span data-ttu-id="58a9e-145">Depois que os traços tiverem sido adicionados ao objeto **InkDivider** , a propriedade **RecognizerContext** não poderá ser alterada.</span><span class="sxs-lookup"><span data-stu-id="58a9e-145">After strokes have been added to the **InkDivider** object, the **RecognizerContext** property cannot be changed.</span></span>

 

<span data-ttu-id="58a9e-146">Atualmente, o **InkDivider** não dá suporte a idiomas verticais.</span><span class="sxs-lookup"><span data-stu-id="58a9e-146">The **InkDivider** does not currently support vertical languages.</span></span> <span data-ttu-id="58a9e-147">Para o objeto **InkDivider** reconhecer esses idiomas corretamente, o objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) para o idioma deve dar suporte à funcionalidade de entrada gratuita e os caracteres devem ser gravados da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="58a9e-147">For the **InkDivider** object to recognize these languages properly the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object for the language must support the free input capability and the characters must be written from left to right.</span></span>

## <a name="requirements"></a><span data-ttu-id="58a9e-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58a9e-148">Requirements</span></span>



| <span data-ttu-id="58a9e-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="58a9e-149">Requirement</span></span> | <span data-ttu-id="58a9e-150">Valor</span><span class="sxs-lookup"><span data-stu-id="58a9e-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58a9e-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58a9e-151">Minimum supported client</span></span><br/> | <span data-ttu-id="58a9e-152">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="58a9e-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="58a9e-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58a9e-153">Minimum supported server</span></span><br/> | <span data-ttu-id="58a9e-154">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="58a9e-154">None supported</span></span><br/>                                                                                               |
| <span data-ttu-id="58a9e-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="58a9e-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="58a9e-156"><dt>Msinkaut15. h (também requer Msinkaut15 \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="58a9e-156"><dt>Msinkaut15.h (also requires Msinkaut15\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="58a9e-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58a9e-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="58a9e-158"><dt>Inkdiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58a9e-158"><dt>Inkdiv.dll</dt></span></span> </dl>                                   |



## <a name="see-also"></a><span data-ttu-id="58a9e-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="58a9e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58a9e-160">**Interface IInkDivisionResult**</span><span class="sxs-lookup"><span data-stu-id="58a9e-160">**IInkDivisionResult Interface**</span></span>](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[<span data-ttu-id="58a9e-161">**Classe InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="58a9e-161">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

<span data-ttu-id="58a9e-162">[Coleção InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="58a9e-162">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 

