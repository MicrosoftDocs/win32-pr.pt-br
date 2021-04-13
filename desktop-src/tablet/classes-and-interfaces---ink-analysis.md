---
description: Esta seção contém informações sobre as interfaces e classes usadas na análise de tinta. As classes e interfaces de análise de tinta não são compatíveis com a automação.
ms.assetid: 712908e1-2d1d-4e42-8c80-71354b03d318
title: Classes e interfaces de análise de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1c157a08a4b7366c20a712c120265320ab4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501283"
---
# <a name="ink-analysis-classes-and-interfaces"></a><span data-ttu-id="723e1-104">Classes e interfaces de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="723e1-104">Ink Analysis Classes and Interfaces</span></span>

<span data-ttu-id="723e1-105">Esta seção contém informações sobre as interfaces e classes usadas na análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="723e1-105">This section contains information about the interfaces and classes used in ink analysis.</span></span> <span data-ttu-id="723e1-106">As classes e interfaces de análise de tinta não são compatíveis com a automação.</span><span class="sxs-lookup"><span data-stu-id="723e1-106">The ink analysis classes and interfaces are not Automation-compliant.</span></span>

## <a name="classes"></a><span data-ttu-id="723e1-107">Classes</span><span class="sxs-lookup"><span data-stu-id="723e1-107">Classes</span></span>



| <span data-ttu-id="723e1-108">Classe</span><span class="sxs-lookup"><span data-stu-id="723e1-108">Class</span></span>                                    | <span data-ttu-id="723e1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="723e1-109">Description</span></span>                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="723e1-110">**AnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="723e1-110">**AnalysisRegion**</span></span>](analysisregion.md) | <span data-ttu-id="723e1-111">Implementa a interface [**IAnalysisRegion**](ianalysisregion.md) .</span><span class="sxs-lookup"><span data-stu-id="723e1-111">Implements the [**IAnalysisRegion**](ianalysisregion.md) interface.</span></span><br/> |
| [<span data-ttu-id="723e1-112">**InkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="723e1-112">**InkAnalyzer**</span></span>](inkanalyzer.md)       | <span data-ttu-id="723e1-113">Implementa a interface [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="723e1-113">Implements the [**IInkAnalyzer**](iinkanalyzer.md) interface.</span></span><br/>       |



 

## <a name="interfaces"></a><span data-ttu-id="723e1-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="723e1-114">Interfaces</span></span>



| <span data-ttu-id="723e1-115">Interface</span><span class="sxs-lookup"><span data-stu-id="723e1-115">Interface</span></span>                                                    | <span data-ttu-id="723e1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="723e1-116">Description</span></span>                                                                                                                                                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="723e1-117">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="723e1-117">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)             | <span data-ttu-id="723e1-118">Representa as correspondências de palavras de reconhecimento de manuscrito possíveis para objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="723e1-118">Represents the possible handwriting recognition word matches for [**IContextNode**](icontextnode.md) objects.</span></span><br/>                                                                                        |
| [<span data-ttu-id="723e1-119">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="723e1-119">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)           | <span data-ttu-id="723e1-120">Contém uma coleção de objetos que implementam a interface [**IAnalysisAlternate**](ianalysisalternate.md) e que são o resultado da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="723e1-120">Contains a collection of objects that implement the [**IAnalysisAlternate**](ianalysisalternate.md) interface and that are the result of ink analysis.</span></span><br/>                                               |
| [<span data-ttu-id="723e1-121">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="723e1-121">**IAnalysisRegion**</span></span>](ianalysisregion.md)                   | <span data-ttu-id="723e1-122">Expõe métodos e propriedades para uma região que representa uma área de um documento.</span><span class="sxs-lookup"><span data-stu-id="723e1-122">Exposes methods and properties for a region that represents an area of a document.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="723e1-123">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="723e1-123">**IAnalysisStatus**</span></span>](ianalysisstatus.md)                   | <span data-ttu-id="723e1-124">Representa o status da operação de análise de tinta descrevendo se a análise foi concluída com êxito e se ocorreu algum aviso.</span><span class="sxs-lookup"><span data-stu-id="723e1-124">Represents the status of the ink analysis operation by describing whether the analysis was completed successfully and whether any warnings occurred.</span></span><br/>                                                  |
| [<span data-ttu-id="723e1-125">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="723e1-125">**IAnalysisWarning**</span></span>](ianalysiswarning.md)                 | <span data-ttu-id="723e1-126">Representa um aviso ou erro que ocorre durante uma operação de análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="723e1-126">Represents a warning or error that occurs during an ink analysis operation.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="723e1-127">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="723e1-127">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)               | <span data-ttu-id="723e1-128">Contém uma coleção de objetos que implementam a interface [**IAnalysisWarning**](ianalysiswarning.md) e que são o resultado de uma operação de análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="723e1-128">Contains a collection of objects that implement the [**IAnalysisWarning**](ianalysiswarning.md) interface and that are the result of an ink analysis operation.</span></span><br/>                                      |
| [<span data-ttu-id="723e1-129">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="723e1-129">**IContextLink**</span></span>](icontextlink.md)                         | <span data-ttu-id="723e1-130">Representa uma relação entre dois objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="723e1-130">Represents a relationship between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="723e1-131">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="723e1-131">**IContextLinks**</span></span>](icontextlinks.md)                       | <span data-ttu-id="723e1-132">Contém uma coleção de objetos que implementam a interface [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="723e1-132">Contains a collection of objects that implement the [**IContextLink**](icontextlink.md) interface.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="723e1-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="723e1-133">**IContextNode**</span></span>](icontextnode.md)                         | <span data-ttu-id="723e1-134">Representa um nó em uma árvore de objetos que são criados como parte da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="723e1-134">Represents a node in a tree of objects that are created as part of ink analysis.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="723e1-135">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="723e1-135">**IContextNodes**</span></span>](icontextnodes.md)                       | <span data-ttu-id="723e1-136">Contém uma coleção de objetos que implementam a interface [**IContextNode**](icontextnode.md) e que são o resultado de uma operação de análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="723e1-136">Contains a collection of objects that implement the [**IContextNode**](icontextnode.md) interface and that are the result of an ink analysis operation.</span></span><br/>                                              |
| [<span data-ttu-id="723e1-137">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="723e1-137">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)     | <span data-ttu-id="723e1-138">Fornece acesso a reconhecedores de manuscrito para uso com a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="723e1-138">Provides access to handwriting recognizers for use with ink analysis.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="723e1-139">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="723e1-139">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)   | <span data-ttu-id="723e1-140">Contém uma coleção de objetos que implementam a interface [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) e que representam a capacidade de reconhecer manuscritos, objetos ou gestos.</span><span class="sxs-lookup"><span data-stu-id="723e1-140">Contains a collection of objects that implement the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) interface and that represent the ability to recognize handwriting, objects, or gestures.</span></span><br/> |
| [<span data-ttu-id="723e1-141">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="723e1-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)                         | <span data-ttu-id="723e1-142">Fornece acesso à análise de layout, escrita e classificação de desenho e reconhecimento de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="723e1-142">Provides access to layout analysis, writing and drawing classification, and handwriting recognition.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="723e1-143">**IMatchesCriteriaCallBack**</span><span class="sxs-lookup"><span data-stu-id="723e1-143">**IMatchesCriteriaCallBack**</span></span>](imatchescriteriacallback.md) | <span data-ttu-id="723e1-144">Expõe um método para avaliar se um objeto [**IContextNode**](icontextnode.md) atende ou falha em um critério especificado.</span><span class="sxs-lookup"><span data-stu-id="723e1-144">Exposes a method to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails a specified criteria.</span></span><br/>                                                                              |



 

## <a name="return-values"></a><span data-ttu-id="723e1-145">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="723e1-145">Return Values</span></span>

<span data-ttu-id="723e1-146">Os métodos na biblioteca COM do Tablet PC retornam valores de **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="723e1-146">Methods in the Tablet PC COM Library return values of **HRESULT**.</span></span> <span data-ttu-id="723e1-147">Salvo indicação em contrário, os significados dos valores **HRESULT** são descritos nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="723e1-147">Unless otherwise noted, the meanings of the **HRESULT** values are described in this table.</span></span>



| <span data-ttu-id="723e1-148">Valor HRESULT</span><span class="sxs-lookup"><span data-stu-id="723e1-148">HRESULT value</span></span>                                   | <span data-ttu-id="723e1-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="723e1-149">Description</span></span>                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="723e1-150">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="723e1-150">S\_OK</span></span><br/>                                | <span data-ttu-id="723e1-151">Êxito.</span><span class="sxs-lookup"><span data-stu-id="723e1-151">Success.</span></span><br/>                                                                      |
| <span data-ttu-id="723e1-152">\_ponteiro E</span><span class="sxs-lookup"><span data-stu-id="723e1-152">E\_POINTER</span></span><br/>                           | <span data-ttu-id="723e1-153">Pelo menos um ponteiro (para um parâmetro de entrada ou de saída) é inválido.</span><span class="sxs-lookup"><span data-stu-id="723e1-153">At least one pointer (for either an input or an output parameter) is invalid.</span></span><br/> |
| <span data-ttu-id="723e1-154">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="723e1-154">E\_INVALIDARG</span></span><br/>                        | <span data-ttu-id="723e1-155">O membro tentou passar um argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="723e1-155">Member attempted to pass in an invalid argument.</span></span><br/>                              |
| <span data-ttu-id="723e1-156">\_exceção de tinta E \_</span><span class="sxs-lookup"><span data-stu-id="723e1-156">E\_INK\_EXCEPTION</span></span><br/>                    | <span data-ttu-id="723e1-157">Exceção ocorreu.</span><span class="sxs-lookup"><span data-stu-id="723e1-157">Exception occurred.</span></span><br/>                                                           |
| <span data-ttu-id="723e1-158">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="723e1-158">E\_OUTOFMEMORY</span></span><br/>                       | <span data-ttu-id="723e1-159">O sistema não pode alocar memória para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="723e1-159">System cannot allocate memory to complete the operation.</span></span><br/>                      |
| <span data-ttu-id="723e1-160">E \_ falha</span><span class="sxs-lookup"><span data-stu-id="723e1-160">E\_FAIL</span></span><br/>                              | <span data-ttu-id="723e1-161">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="723e1-161">Unspecified failure occurred.</span></span><br/>                                                 |
| <span data-ttu-id="723e1-162">E \_ INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="723e1-162">E\_INVALIDOPERATION</span></span><br/>                  | <span data-ttu-id="723e1-163">O membro tentou usar uma operação inválida.</span><span class="sxs-lookup"><span data-stu-id="723e1-163">Member attempted to use an invalid operation.</span></span><br/>                                 |
| <span data-ttu-id="723e1-164">modo do TPC \_ E \_ inválido \_</span><span class="sxs-lookup"><span data-stu-id="723e1-164">TPC\_E\_INVALID\_MODE</span></span><br/>                | <span data-ttu-id="723e1-165">O membro tentou usar um modo inválido.</span><span class="sxs-lookup"><span data-stu-id="723e1-165">Member attempted to use an invalid mode.</span></span><br/>                                      |
| <span data-ttu-id="723e1-166">configuração de TPC \_ E \_ inválido \_</span><span class="sxs-lookup"><span data-stu-id="723e1-166">TPC\_E\_INVALID\_CONFIGURATION</span></span><br/>       | <span data-ttu-id="723e1-167">O membro tentou usar uma configuração inválida.</span><span class="sxs-lookup"><span data-stu-id="723e1-167">Member attempted to use an invalid configuration.</span></span><br/>                             |
| <span data-ttu-id="723e1-168">\_Descrição do pacote TPC E \_ inválido \_ \_</span><span class="sxs-lookup"><span data-stu-id="723e1-168">TPC\_E\_INVALID\_PACKET\_DESCRIPTION</span></span><br/> | <span data-ttu-id="723e1-169">O membro tentou usar uma descrição de pacote inválida.</span><span class="sxs-lookup"><span data-stu-id="723e1-169">Member attempted to use an invalid packet description.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="723e1-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="723e1-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="723e1-171">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="723e1-171">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




