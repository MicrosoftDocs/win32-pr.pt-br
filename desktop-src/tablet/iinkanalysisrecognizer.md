---
description: Fornece acesso a reconhecedores de manuscrito para uso com a análise de tinta.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Interface IInkAnalysisRecognizer (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b091b47d14929e155548dc057ef0fdb1731133a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813573"
---
# <a name="iinkanalysisrecognizer-interface"></a><span data-ttu-id="12f43-103">Interface IInkAnalysisRecognizer</span><span class="sxs-lookup"><span data-stu-id="12f43-103">IInkAnalysisRecognizer interface</span></span>

<span data-ttu-id="12f43-104">Fornece acesso a reconhecedores de manuscrito para uso com a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="12f43-104">Provides access to handwriting recognizers for use with ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="12f43-105">Membros</span><span class="sxs-lookup"><span data-stu-id="12f43-105">Members</span></span>

<span data-ttu-id="12f43-106">A interface **IInkAnalysisRecognizer** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="12f43-106">The **IInkAnalysisRecognizer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="12f43-107">**IInkAnalysisRecognizer** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="12f43-107">**IInkAnalysisRecognizer** also has these types of members:</span></span>

-   [<span data-ttu-id="12f43-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="12f43-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="12f43-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="12f43-109">Methods</span></span>

<span data-ttu-id="12f43-110">A interface **IInkAnalysisRecognizer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="12f43-110">The **IInkAnalysisRecognizer** interface has these methods.</span></span>



| <span data-ttu-id="12f43-111">Método</span><span class="sxs-lookup"><span data-stu-id="12f43-111">Method</span></span>                                                                          | <span data-ttu-id="12f43-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="12f43-112">Description</span></span>                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12f43-113">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="12f43-113">**GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)               | <span data-ttu-id="12f43-114">Recupera os recursos do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="12f43-114">Retrieves the capabilities of the recognizer.</span></span><br/>                                                                       |
| [<span data-ttu-id="12f43-115">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="12f43-115">**GetGuid**</span></span>](iinkanalysisrecognizer-getguid.md)                               | <span data-ttu-id="12f43-116">Recupera o identificador global exclusivo (GUID) do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="12f43-116">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span><br/>                                                  |
| [<span data-ttu-id="12f43-117">**GetLanguages**</span><span class="sxs-lookup"><span data-stu-id="12f43-117">**GetLanguages**</span></span>](iinkanalysisrecognizer-getlanguages.md)                     | <span data-ttu-id="12f43-118">Recupera os identificadores para as localidades às quais esse **IInkAnalysisRecognizer** dá suporte.</span><span class="sxs-lookup"><span data-stu-id="12f43-118">Retrieves the identifiers for the locales that this **IInkAnalysisRecognizer** supports.</span></span><br/>                            |
| [<span data-ttu-id="12f43-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="12f43-119">**GetName**</span></span>](iinkanalysisrecognizer-getname.md)                               | <span data-ttu-id="12f43-120">Recupera o nome do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="12f43-120">Retrieves the name of the recognizer.</span></span><br/>                                                                               |
| [<span data-ttu-id="12f43-121">**GetSupportedProperties**</span><span class="sxs-lookup"><span data-stu-id="12f43-121">**GetSupportedProperties**</span></span>](iinkanalysisrecognizer-getsupportedproperties.md) | <span data-ttu-id="12f43-122">Recupera os identificadores globalmente exclusivos (GUIDs) para as propriedades às quais esse **IInkAnalysisRecognizer** dá suporte.</span><span class="sxs-lookup"><span data-stu-id="12f43-122">Retrieves the globally unique identifiers (GUIDs) for the properties that this **IInkAnalysisRecognizer** supports.</span></span><br/> |
| [<span data-ttu-id="12f43-123">**Getvendor**</span><span class="sxs-lookup"><span data-stu-id="12f43-123">**GetVendor**</span></span>](iinkanalysisrecognizer-getvendor.md)                           | <span data-ttu-id="12f43-124">Recupera o nome do fornecedor do **IInkAnalysisRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="12f43-124">Retrieves the vendor name of the **IInkAnalysisRecognizer**.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="12f43-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="12f43-125">Remarks</span></span>

<span data-ttu-id="12f43-126">Um reconhecedor tem atributos e propriedades específicos que permitem que ele execute o reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="12f43-126">A recognizer has specific attributes and properties that allow it to perform recognition.</span></span> <span data-ttu-id="12f43-127">As propriedades de um reconhecedor devem ser determinadas antes que o reconhecimento possa ocorrer.</span><span class="sxs-lookup"><span data-stu-id="12f43-127">The properties of a recognizer must be determined before recognition can occur.</span></span> <span data-ttu-id="12f43-128">Os tipos de propriedades que um reconhecedor dá suporte determinam os tipos de reconhecimento que ele pode executar.</span><span class="sxs-lookup"><span data-stu-id="12f43-128">The types of properties that a recognizer supports determine the types of recognition that it can perform.</span></span> <span data-ttu-id="12f43-129">Por exemplo, se um reconhecedor não oferecer suporte a manuscritos cursivos, ele retornará resultados imprecisos quando um usuário gravar em letra cursiva.</span><span class="sxs-lookup"><span data-stu-id="12f43-129">For instance, if a recognizer does not support cursive handwriting, it returns inaccurate results when a user writes in cursive.</span></span>

<span data-ttu-id="12f43-130">Um reconhecedor também tem uma funcionalidade interna que gerencia automaticamente muitos aspectos do manuscrito.</span><span class="sxs-lookup"><span data-stu-id="12f43-130">A recognizer also has built-in functionality that automatically manages many aspects of handwriting.</span></span> <span data-ttu-id="12f43-131">Por exemplo, ele determina as métricas para as linhas nas quais os traços são desenhados.</span><span class="sxs-lookup"><span data-stu-id="12f43-131">For instance, it determines the metrics for the lines on which strokes are drawn.</span></span> <span data-ttu-id="12f43-132">Você pode retornar o número de linha de um traço, mas nunca precisa especificar como essas métricas de linha são determinadas devido à funcionalidade interna do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="12f43-132">You can return the line number of a stroke, but you never need to specify how those line metrics are determined because of the built-in functionality of the recognizer.</span></span>

<span data-ttu-id="12f43-133">O [**IInkAnalyzer**](iinkanalyzer.md) mantém uma lista de reconhecedores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="12f43-133">The [**IInkAnalyzer**](iinkanalyzer.md) maintains a list of available recognizers.</span></span> <span data-ttu-id="12f43-134">Para acessar essa lista, use o método do [**método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) .</span><span class="sxs-lookup"><span data-stu-id="12f43-134">To access this list, use the [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="12f43-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12f43-135">Requirements</span></span>



| <span data-ttu-id="12f43-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="12f43-136">Requirement</span></span> | <span data-ttu-id="12f43-137">Valor</span><span class="sxs-lookup"><span data-stu-id="12f43-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f43-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12f43-138">Minimum supported client</span></span><br/> | <span data-ttu-id="12f43-139">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="12f43-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="12f43-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12f43-140">Minimum supported server</span></span><br/> | <span data-ttu-id="12f43-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="12f43-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="12f43-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12f43-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="12f43-143"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="12f43-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="12f43-144">DLL</span><span class="sxs-lookup"><span data-stu-id="12f43-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12f43-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12f43-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="12f43-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="12f43-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f43-147">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="12f43-147">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="12f43-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="12f43-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="12f43-149">**Método IInkAnalyzer:: CreateCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="12f43-149">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="12f43-150">Tipos de nó de contexto</span><span class="sxs-lookup"><span data-stu-id="12f43-150">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="12f43-151">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="12f43-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

