---
title: Métodos (IInertiaProcessor)
description: Esta seção contém os métodos para a interface IInertiaProcessor.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows Touch, interface IInertiaProcessor
- Windows Touch, métodos de interface
- inércia, interface IInertiaProcessor
- Interface IInertiaProcessor, métodos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105771378"
---
# <a name="methods-iinertiaprocessor"></a><span data-ttu-id="08e98-107">Métodos (IInertiaProcessor)</span><span class="sxs-lookup"><span data-stu-id="08e98-107">Methods (IInertiaProcessor)</span></span>

<span data-ttu-id="08e98-108">Esta seção contém os métodos para a interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="08e98-108">This section contains the methods for the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface.</span></span>



| <span data-ttu-id="08e98-109">Método</span><span class="sxs-lookup"><span data-stu-id="08e98-109">Method</span></span>                                                 | <span data-ttu-id="08e98-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="08e98-110">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08e98-111">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="08e98-111">**Reset**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | <span data-ttu-id="08e98-112">Inicializa o processador com o carimbo de data/hora inicial e reinicia o inércia.</span><span class="sxs-lookup"><span data-stu-id="08e98-112">Initializes the processor with initial time stamp and restarts inertia.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="08e98-113">**Processar**</span><span class="sxs-lookup"><span data-stu-id="08e98-113">**Process**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | <span data-ttu-id="08e98-114">Executa cálculos para o tique atual e pode gerar o **Delta** ou o evento **concluído** dependendo se a extrapolação está concluída ou não.</span><span class="sxs-lookup"><span data-stu-id="08e98-114">Performs calculations for the current tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span> <span data-ttu-id="08e98-115">Se a extrapolação terminar no tique anterior, o método será no-op.</span><span class="sxs-lookup"><span data-stu-id="08e98-115">If extrapolation finished at the previous tick, the method is no-op.</span></span> |
| [<span data-ttu-id="08e98-116">**Processtime**</span><span class="sxs-lookup"><span data-stu-id="08e98-116">**ProcessTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | <span data-ttu-id="08e98-117">Executa cálculos para a marcação especificada e pode gerar o evento **Delta** ou **Completed** dependendo se a extrapolação está concluída ou não.</span><span class="sxs-lookup"><span data-stu-id="08e98-117">Performs calculations for the given tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span>                                                                        |
| [<span data-ttu-id="08e98-118">**Concluir**</span><span class="sxs-lookup"><span data-stu-id="08e98-118">**Complete**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | <span data-ttu-id="08e98-119">Conclui a manipulação atual e para o inércia no processador inércia.</span><span class="sxs-lookup"><span data-stu-id="08e98-119">Finishes the current manipulation and stops inertia on the inertia processor.</span></span>                                                                                                                                              |
| [<span data-ttu-id="08e98-120">**Concluído**</span><span class="sxs-lookup"><span data-stu-id="08e98-120">**CompleteTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | <span data-ttu-id="08e98-121">Conclui a manipulação atual no tique especificado, interrompe o inércia no processador inércia e gera o evento ManipulationCompleted.</span><span class="sxs-lookup"><span data-stu-id="08e98-121">Finishes the current manipulation at the given tick, stops inertia on the inertia processor, and raises the ManipulationCompleted event.</span></span>                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="08e98-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08e98-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08e98-123">**IInertiaProcessor**</span><span class="sxs-lookup"><span data-stu-id="08e98-123">**IInertiaProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




