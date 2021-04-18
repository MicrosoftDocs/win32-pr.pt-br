---
title: Resposta do leitor para recursos do ASF
description: Resposta do leitor para recursos do ASF
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- SDK do Windows Media Format, respostas do leitor para recursos do ASF
- ASF (Advanced Systems Format), respostas de leitor para recursos
- ASF (formato de sistemas avançados), respostas de leitor para recursos
- respostas do leitor para recursos do ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291752d2d011fbc8b0a3e5211c5d8926f94b1cbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105814086"
---
# <a name="reader-response-to-asf-features"></a><span data-ttu-id="e97ee-107">Resposta do leitor para recursos do ASF</span><span class="sxs-lookup"><span data-stu-id="e97ee-107">Reader Response to ASF Features</span></span>

<span data-ttu-id="e97ee-108">A maioria dos recursos de arquivo ASF especiais pode ser definida em arquivos para interagir com aplicativos de reprodução personalizados projetados para tratá-los.</span><span class="sxs-lookup"><span data-stu-id="e97ee-108">Most of the special ASF file features can be set in files to interact with custom playing applications designed to handle them.</span></span> <span data-ttu-id="e97ee-109">No entanto, alguns dos recursos têm suporte interno no objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="e97ee-109">However, some of the features have built-in support in the reader object.</span></span>

<span data-ttu-id="e97ee-110">O objeto leitor selecionará automaticamente fluxos de conjuntos que são mutuamente exclusivos por taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="e97ee-110">The reader object will automatically select streams from sets that are mutually exclusive by bit rate.</span></span> <span data-ttu-id="e97ee-111">Esse caso especial é chamado de taxa de bits múltipla (MBR).</span><span class="sxs-lookup"><span data-stu-id="e97ee-111">This special case is referred to as multiple bit rate (MBR).</span></span> <span data-ttu-id="e97ee-112">O fluxo que o leitor seleciona é baseado na taxa de bits do fluxo.</span><span class="sxs-lookup"><span data-stu-id="e97ee-112">The stream the reader selects is based on the bit rate of the stream.</span></span> <span data-ttu-id="e97ee-113">O número do fluxo e a ordem em que ele foi adicionado ao objeto de exclusão mútua são irrelevantes para a seleção automática.</span><span class="sxs-lookup"><span data-stu-id="e97ee-113">The stream number and the order in which it was added to the mutual exclusion object are irrelevant to the automatic selection.</span></span> <span data-ttu-id="e97ee-114">Se um arquivo incluir mais de um conjunto de fluxos mutuamente exclusivos por taxa de bits, o leitor selecionará fluxos com base no cálculo do melhor uso da largura de banda disponível.</span><span class="sxs-lookup"><span data-stu-id="e97ee-114">If a file includes more than one set of streams mutually exclusive by bit rate, the reader will select streams based on calculating the best use of the available bandwidth.</span></span>

<span data-ttu-id="e97ee-115">A exclusão mútua baseada em linguagem é definida usando uma configuração de saída, antes da reprodução.</span><span class="sxs-lookup"><span data-stu-id="e97ee-115">Language-based mutual exclusion is set using an output setting, before playback.</span></span> <span data-ttu-id="e97ee-116">Se você combinar o idioma e a exclusão mútua baseada em taxa de bits, deverá agrupar os fluxos mutuamente exclusivos baseados em taxa de bits por idioma e, em seguida, tornar os grupos mutuamente exclusivos por idioma.</span><span class="sxs-lookup"><span data-stu-id="e97ee-116">If you combine both language and bit-rate-based mutual exclusion, you should group the bit-rate-based mutually exclusive streams by language and then make the groups mutually exclusive by language.</span></span> <span data-ttu-id="e97ee-117">O leitor verificará o idioma primeiro e, em seguida, determinará qual taxa de bits usar.</span><span class="sxs-lookup"><span data-stu-id="e97ee-117">The reader will check the language first, and then determine which bit rate to use.</span></span>

<span data-ttu-id="e97ee-118">A priorização de fluxo é definida usando uma matriz de registros.</span><span class="sxs-lookup"><span data-stu-id="e97ee-118">Stream prioritization is set using an array of records.</span></span> <span data-ttu-id="e97ee-119">Os registros na matriz estão em ordem decrescente de prioridade.</span><span class="sxs-lookup"><span data-stu-id="e97ee-119">The records in the array are in descending order of priority.</span></span> <span data-ttu-id="e97ee-120">O último fluxo na matriz é o primeiro que será Descartado pelo leitor.</span><span class="sxs-lookup"><span data-stu-id="e97ee-120">The last stream in the array is the first that will be dropped by the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e97ee-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e97ee-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e97ee-122">**Recursos de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="e97ee-122">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="e97ee-123">**Exclusão mútua**</span><span class="sxs-lookup"><span data-stu-id="e97ee-123">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="e97ee-124">**Priorização de fluxo**</span><span class="sxs-lookup"><span data-stu-id="e97ee-124">**Stream Prioritization**</span></span>](stream-prioritization.md)
</dt> </dl>

 

 




