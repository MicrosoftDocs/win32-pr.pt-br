---
description: Recupera os resultados da análise do objeto InkDivider.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: Função CallDivideResults
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 11878e6a0ac953b9b7eb27ce21bb67001f9d88d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089706"
---
# <a name="calldivideresults-function"></a><span data-ttu-id="81753-103">Função CallDivideResults</span><span class="sxs-lookup"><span data-stu-id="81753-103">CallDivideResults function</span></span>

<span data-ttu-id="81753-104">Recupera os resultados da análise do objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="81753-104">Retrieves analysis results from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="81753-105">Esta função não se destina a ser usada pelo código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81753-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="81753-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81753-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a><span data-ttu-id="81753-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81753-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81753-108">*hDivider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="81753-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-109">Um identificador para o objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="81753-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="81753-110">*aWordStrokeIds* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="81753-110">*aWordStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-111">Uma matriz de identificadores associada à palavra que é passada para a classe [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="81753-111">An array of identifiers associated with the word that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="81753-112">*aLineStrokeIds* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="81753-112">*aLineStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-113">Uma matriz de propriedades de [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para os objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associados à linha que é passada para a classe [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="81753-113">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the line that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="81753-114">*aParagraphStrokeIds* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="81753-114">*aParagraphStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-115">Uma matriz das propriedades de [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para os objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associados ao parágrafo da classe [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="81753-115">An array of the [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the paragraph from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="81753-116">*aDrawingStrokeIds* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="81753-116">*aDrawingStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-117">Uma matriz de propriedades de [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para os objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associados ao desenho da classe [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="81753-117">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the drawing from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="81753-118">*pastrWords* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="81753-118">*pastrWords* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-119">Uma matriz de palavras retornada da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="81753-119">An array of words returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="81753-120">*pastrLines* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="81753-120">*pastrLines* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-121">Uma matriz de linhas retornadas da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="81753-121">An array of lines returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="81753-122">*pastrParagraphs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="81753-122">*pastrParagraphs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-123">Uma matriz de parágrafos retornada da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="81753-123">An array of paragraphs returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="81753-124">*aWordRotationCenterX* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="81753-124">*aWordRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-125">Uma matriz dos pontos centrais das palavras ao longo do eixo x da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="81753-125">An array of the center points of the words along the x-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="81753-126">*aWordRotationCenterY* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="81753-126">*aWordRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-127">Uma matriz dos pontos centrais das palavras ao longo do eixo y da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="81753-127">An array of the center points of the words along the y-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="81753-128">*aWordAngle* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="81753-128">*aWordAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-129">Uma matriz que contém os ângulos pelos quais girar as palavras para obter melhores resultados de análise.</span><span class="sxs-lookup"><span data-stu-id="81753-129">An array containing the angles by which to rotate the words for best analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="81753-130">*aLineRotationCenterX* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="81753-130">*aLineRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-131">Uma matriz que contém os pontos centrais das linhas ao longo do eixo x.</span><span class="sxs-lookup"><span data-stu-id="81753-131">An array containing the center points of the lines along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="81753-132">*aLineRotationCenterY* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="81753-132">*aLineRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-133">Uma matriz que contém os pontos centrais das linhas ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="81753-133">An array containing the center points of the lines along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="81753-134">*aLineAngle* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="81753-134">*aLineAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81753-135">Uma matriz que contém os ângulos pelos quais girar as linhas para obter melhores resultados de análise.</span><span class="sxs-lookup"><span data-stu-id="81753-135">An array containing the angles by which to rotate the lines for best analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81753-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81753-136">Return value</span></span>

<span data-ttu-id="81753-137">Essa função pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="81753-137">This function can return one of these values.</span></span>



| <span data-ttu-id="81753-138">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="81753-138">Return code</span></span>                                                                                   | <span data-ttu-id="81753-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="81753-139">Description</span></span>                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="81753-140"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="81753-140"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="81753-141">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="81753-141">The function succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="81753-142"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="81753-142"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="81753-143">O parâmetro *hDivider* é inválido.</span><span class="sxs-lookup"><span data-stu-id="81753-143">The *hDivider* parameter is invalid.</span></span><br/>                   |
| <dl> <span data-ttu-id="81753-144"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="81753-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="81753-145">Não foi possível alocar memória suficiente para armazenar os resultados.</span><span class="sxs-lookup"><span data-stu-id="81753-145">Could not allocate enough memory to store the results.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="81753-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="81753-146">Remarks</span></span>

<span data-ttu-id="81753-147">Para evitar vazamentos de memória, você deve liberar os recursos para *pastrWords*, *pastrLines* e *pastrParagraphs*.</span><span class="sxs-lookup"><span data-stu-id="81753-147">To avoid memory leaks you must release the resources for *pastrWords*, *pastrLines*, and *pastrParagraphs*.</span></span>

## <a name="requirements"></a><span data-ttu-id="81753-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81753-148">Requirements</span></span>



| <span data-ttu-id="81753-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="81753-149">Requirement</span></span> | <span data-ttu-id="81753-150">Valor</span><span class="sxs-lookup"><span data-stu-id="81753-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81753-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81753-151">Minimum supported client</span></span><br/> | <span data-ttu-id="81753-152">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="81753-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="81753-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81753-153">Minimum supported server</span></span><br/> | <span data-ttu-id="81753-154">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="81753-154">None supported</span></span><br/>                                                             |
| <span data-ttu-id="81753-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81753-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="81753-156"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81753-156"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




