---
description: Clicar em executar especialistas na janela especialistas da interface do usuário do Monitor de Rede inicia os especialistas selecionados para o arquivo de captura e chama a função executar. Quando iniciado, o especialista analisa o arquivo de captura usando várias funções de quadro de especialista.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Iniciar e executar especialistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bd41472d286727541d26bade1942eb3b6b5c593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788125"
---
# <a name="starting-and-running-experts"></a><span data-ttu-id="d7921-104">Iniciar e executar especialistas</span><span class="sxs-lookup"><span data-stu-id="d7921-104">Starting and Running Experts</span></span>

<span data-ttu-id="d7921-105">Clicar em **executar especialistas** na janela especialistas da interface do usuário do monitor de rede inicia os especialistas selecionados para o arquivo de captura e chama a função [**executar**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="d7921-105">Clicking **Run Experts** from the Experts window of the Network Monitor UI starts the experts selected for the capture file and calls the [**Run**](run.md) function.</span></span> <span data-ttu-id="d7921-106">Quando iniciado, o especialista analisa o arquivo de captura usando várias funções de quadro de especialista.</span><span class="sxs-lookup"><span data-stu-id="d7921-106">When started, the expert analyzes the capture file by using several expert frame functions.</span></span>

<span data-ttu-id="d7921-107">A função [**ExpertIndicateStatus**](expertindicatestatus.md) fornece informações de status do especialista.</span><span class="sxs-lookup"><span data-stu-id="d7921-107">The [**ExpertIndicateStatus**](expertindicatestatus.md) function provides status information from the expert.</span></span> <span data-ttu-id="d7921-108">Quando você executa um especialista com Monitor de Rede, a janela de exibição de status de especialista exibe informações de status atualizadas periodicamente (de 0 a 100 por cento de conclusão).</span><span class="sxs-lookup"><span data-stu-id="d7921-108">When you run an expert with Network Monitor, the Expert Status View window displays periodically updated status information (from 0 to 100 percent completion).</span></span>

![janela de exibição de status de especialista](images/exview.png)

<span data-ttu-id="d7921-110">O especialista está ativo até que os dados concluam sua passagem por meio do arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="d7921-110">The expert is active until the data completes its pass though the capture file.</span></span> <span data-ttu-id="d7921-111">Quando a passagem for concluída, uma janela de Visualizador de Eventos será exibida.</span><span class="sxs-lookup"><span data-stu-id="d7921-111">When the pass is complete, an Event Viewer window appears.</span></span> <span data-ttu-id="d7921-112">As informações nessa janela dependem do tipo de especialista que analisou os dados.</span><span class="sxs-lookup"><span data-stu-id="d7921-112">The information in this window depends on the type of expert that analyzed the data.</span></span> <span data-ttu-id="d7921-113">A ilustração a seguir mostra uma exibição de especialista em distribuição de propriedade, que resume os dados de quadro analisados pelo especialista.</span><span class="sxs-lookup"><span data-stu-id="d7921-113">The following illustration shows a Property Distribution Expert view, which summarizes the frame data that the expert analyzed.</span></span>

![exibição do especialista de distribuição de propriedade](images/exview1.png)

<span data-ttu-id="d7921-115">Um segundo relatório (não mostrado), resume os resultados do especialista de retransmissão do protocolo TCP.</span><span class="sxs-lookup"><span data-stu-id="d7921-115">A second report (not shown), summarizes the results of the Transmission Control Protocol (TCP) Retransmit expert.</span></span>

<span data-ttu-id="d7921-116">Também é possível:</span><span class="sxs-lookup"><span data-stu-id="d7921-116">You can also:</span></span>

-   <span data-ttu-id="d7921-117">Crie uma entrada para uma página de referência de evento (ERP) que aconselha o usuário de condições ou problemas detectados (conforme mostrado na janela de análise).</span><span class="sxs-lookup"><span data-stu-id="d7921-117">Create an entry for an event reference page (ERP) that advises the user of detected conditions or problems (as shown in the Analysis window).</span></span>
-   <span data-ttu-id="d7921-118">Crie entradas para correções sugeridas ou dados explicativos que forneçam informações adicionais (conforme mostrado na janela de resolução).</span><span class="sxs-lookup"><span data-stu-id="d7921-118">Create entries for suggested fixes or explanatory data that provide additional information (as shown in the Resolution window).</span></span>

<span data-ttu-id="d7921-119">Depois que o especialista concluir sua tarefa, Monitor de Rede removerá o especialista da memória ativa.</span><span class="sxs-lookup"><span data-stu-id="d7921-119">After the expert completes its task, Network Monitor removes the expert from active memory.</span></span> <span data-ttu-id="d7921-120">Os especialistas devem usar as funções de memória protegida incluídas no SDK (Software Development Kit) da plataforma. essas funções limpam a memória se os especialistas falharem durante o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d7921-120">Experts should use the protected memory functions included in the Platform Software Development Kit (SDK); these functions clean up memory if the experts fail during run time.</span></span>

 

 



