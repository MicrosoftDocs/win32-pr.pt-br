---
description: O objeto DivisionResult representa um instantâneo da análise de layout dos traços contidos no objeto divisória. Ele contém a classificação de traço e as informações de agrupamento da análise de layout.
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: Trabalhando com o objeto DivisionResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b9874f4a9d2e6bc4390d98803c2344308fc3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501934"
---
# <a name="working-with-the-divisionresult-object"></a><span data-ttu-id="c6cc8-104">Trabalhando com o objeto DivisionResult</span><span class="sxs-lookup"><span data-stu-id="c6cc8-104">Working with the DivisionResult Object</span></span>

<span data-ttu-id="c6cc8-105">O objeto **DivisionResult** representa um instantâneo da análise de layout dos traços contidos no objeto **divisória** .</span><span class="sxs-lookup"><span data-stu-id="c6cc8-105">The **DivisionResult** object represents a snapshot of the layout analysis of the strokes contained by the **Divider** object.</span></span> <span data-ttu-id="c6cc8-106">Ele contém a classificação de traço e as informações de agrupamento da análise de layout.</span><span class="sxs-lookup"><span data-stu-id="c6cc8-106">It contains the stroke classification and grouping information from the layout analysis.</span></span>

<span data-ttu-id="c6cc8-107">Você pode obter informações do objeto **DivisionResult** por tipo de elemento estrutural, como desenho ou linhas de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="c6cc8-107">You can get information from the **DivisionResult** object by structural element type, such as drawing or lines of handwriting.</span></span> <span data-ttu-id="c6cc8-108">O objeto **DivisionResult** pode persistir depois que o objeto **divisória** é destruído.</span><span class="sxs-lookup"><span data-stu-id="c6cc8-108">The **DivisionResult** object can persist after the **Divider** object is destroyed.</span></span> <span data-ttu-id="c6cc8-109">Na automação, esse objeto é chamado de objeto de [**interface IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="c6cc8-109">In Automation, this object is called the [**IInkDivisionResult Interface**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

<span data-ttu-id="c6cc8-110">A propriedade [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) do objeto **DivisionResult** contém uma cópia da coleção **Strokes** no objeto **divisória** no momento em que o objeto **DivisionResult** foi criado.</span><span class="sxs-lookup"><span data-stu-id="c6cc8-110">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property of the **DivisionResult** object contains a copy of the **Strokes** collection in the **Divider** object at the time the **DivisionResult** object was created.</span></span>

<span data-ttu-id="c6cc8-111">A enumeração [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) define os tipos de elementos estruturais que a análise de layout reconhece.</span><span class="sxs-lookup"><span data-stu-id="c6cc8-111">The [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration defines the structural element types that the layout analysis recognizes.</span></span>

<span data-ttu-id="c6cc8-112">O método [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) do objeto **DivisionResult** retorna uma coleção **DivisionUnits** que contém todos os elementos estruturais de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="c6cc8-112">The [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method of the **DivisionResult** object returns a **DivisionUnits** collection that contains all structural elements of a given type.</span></span> <span data-ttu-id="c6cc8-113">Um elemento estrutural individual é representado por um objeto **DivisionUnit** .</span><span class="sxs-lookup"><span data-stu-id="c6cc8-113">An individual structural element is represented by a **DivisionUnit** object.</span></span> <span data-ttu-id="c6cc8-114">Sempre que você chamar o método **ResultByType** , o objeto **DivisionResult** criará uma coleção **DivisionUnits** .</span><span class="sxs-lookup"><span data-stu-id="c6cc8-114">Each time you call the **ResultByType** method, the **DivisionResult** object creates a **DivisionUnits** collection.</span></span> <span data-ttu-id="c6cc8-115">Para obter mais informações sobre o objeto **DivisionUnit** , consulte [trabalhando com o objeto DivisionUnit](working-with-the-divisionunit-object.md).</span><span class="sxs-lookup"><span data-stu-id="c6cc8-115">For more information about the **DivisionUnit** object, see [Working with the DivisionUnit Object](working-with-the-divisionunit-object.md).</span></span>

 

 
