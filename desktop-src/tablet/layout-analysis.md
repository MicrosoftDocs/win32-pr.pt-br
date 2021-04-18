---
description: A análise de layout opera em uma coleção de traços e classifica os traços em elementos manuscritos e de desenho. O objeto divisória fornece acesso aos recursos de análise de layout do Tablet PC.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Análise de layout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0901e7c7df96bec5ea3972f643469033fbb22ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793737"
---
# <a name="layout-analysis"></a><span data-ttu-id="2a69a-104">Análise de layout</span><span class="sxs-lookup"><span data-stu-id="2a69a-104">Layout Analysis</span></span>

<span data-ttu-id="2a69a-105">A análise de layout opera em uma coleção de [**traços**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) e classifica os traços em elementos manuscritos e de desenho.</span><span class="sxs-lookup"><span data-stu-id="2a69a-105">Layout analysis operates on a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection and classifies the strokes into handwriting and drawing elements.</span></span> <span data-ttu-id="2a69a-106">O objeto [**divisória**](inkdivider-class.md) fornece acesso aos recursos de análise de layout do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="2a69a-106">The [**Divider**](inkdivider-class.md) object provides access to the Tablet PC layout analysis features.</span></span>

<span data-ttu-id="2a69a-107">A tabela a seguir descreve os tipos de elementos estruturais da enumeração [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) em que o objeto [**divisória**](inkdivider-class.md) classifica os traços.</span><span class="sxs-lookup"><span data-stu-id="2a69a-107">The following table describes the structural element types of the [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration into which the [**Divider**](inkdivider-class.md) object classifies strokes.</span></span>



| <span data-ttu-id="2a69a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a69a-108">Type</span></span>          | <span data-ttu-id="2a69a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a69a-109">Description</span></span>                                                                      |
|---------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2a69a-110">**Segment**</span><span class="sxs-lookup"><span data-stu-id="2a69a-110">**Segment**</span></span>   | <span data-ttu-id="2a69a-111">Um segmento de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="2a69a-111">A recognition segment.</span></span><br/>                                                |
| <span data-ttu-id="2a69a-112">**Linha**</span><span class="sxs-lookup"><span data-stu-id="2a69a-112">**Line**</span></span>      | <span data-ttu-id="2a69a-113">Uma linha de manuscrito que contém um ou mais segmentos de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="2a69a-113">A line of handwriting that contains one or more recognition segments.</span></span><br/> |
| <span data-ttu-id="2a69a-114">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="2a69a-114">**Paragraph**</span></span> | <span data-ttu-id="2a69a-115">Um bloco de traços que contém uma ou mais linhas de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="2a69a-115">A block of strokes that contains one or more lines of handwriting.</span></span><br/>    |
| <span data-ttu-id="2a69a-116">**Senha**</span><span class="sxs-lookup"><span data-stu-id="2a69a-116">**Drawing**</span></span>   | <span data-ttu-id="2a69a-117">Tinta que não é manuscrito.</span><span class="sxs-lookup"><span data-stu-id="2a69a-117">Ink that is not handwriting.</span></span><br/>                                          |



 

<span data-ttu-id="2a69a-118">O objeto [**divisória**](inkdivider-class.md) tem uma coleção [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , que o objeto **divisória** analisa dinamicamente cada vez que você adiciona ou exclui da coleção.</span><span class="sxs-lookup"><span data-stu-id="2a69a-118">The [**Divider**](inkdivider-class.md) object has a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection, which the **Divider** object dynamically analyzes each time you add to or delete from the collection.</span></span> <span data-ttu-id="2a69a-119">O objeto **divisória** não é serializável e você não pode salvar seu estado de análise.</span><span class="sxs-lookup"><span data-stu-id="2a69a-119">The **Divider** object is not serializable, and you cannot save its analysis state.</span></span> <span data-ttu-id="2a69a-120">Portanto, o objeto **divisória** é projetado para aplicativos que devem diferenciar a entrada de desenho e de manuscrito misturada, mas não precisam reanalisar grandes quantidades de tinta entre sessões.</span><span class="sxs-lookup"><span data-stu-id="2a69a-120">Thus the **Divider** object is designed for applications that must differentiate between mixed handwriting and drawing input, but do not need to reanalyze large amounts of ink between sessions.</span></span>

<span data-ttu-id="2a69a-121">Você pode obter um instantâneo estático do resultado da análise atual, que é retornado em um objeto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="2a69a-121">You can obtain a static snapshot of the current analysis result, which is returned in a [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span> <span data-ttu-id="2a69a-122">Você pode obter objetos [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) , cada um representando um único elemento estrutural de um objeto **DivisionResult** .</span><span class="sxs-lookup"><span data-stu-id="2a69a-122">You can obtain [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) objects, each which represents a single structural element of a **DivisionResult** object.</span></span> <span data-ttu-id="2a69a-123">Os objetos **DivisionResult** e **DivisionUnit** não são serializáveis.</span><span class="sxs-lookup"><span data-stu-id="2a69a-123">The **DivisionResult** and **DivisionUnit** objects are not serializable.</span></span> <span data-ttu-id="2a69a-124">No entanto, as informações de estado desses objetos estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2a69a-124">However, state information from these objects is available.</span></span>

<span data-ttu-id="2a69a-125">O objeto [**divisória**](inkdivider-class.md) funciona apenas com manuscrito da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="2a69a-125">The [**Divider**](inkdivider-class.md) object works only with left-to-right handwriting.</span></span> <span data-ttu-id="2a69a-126">Para que o objeto **divisória** analise idiomas verticais, como chinês corretamente, os caracteres devem ser desenhados da esquerda para a direita em vez de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="2a69a-126">For the **Divider** object to analyze vertical languages such as Chinese correctly, the characters must be drawn left-to-right instead of top-to-bottom.</span></span>

 

