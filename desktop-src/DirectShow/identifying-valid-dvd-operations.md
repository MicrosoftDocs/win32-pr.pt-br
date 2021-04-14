---
description: Identificando operações de DVD válidas
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identificando operações de DVD válidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444595e402dc73a3468946b820f031dabaecc2f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370275"
---
# <a name="identifying-valid-dvd-operations"></a><span data-ttu-id="e7d37-103">Identificando operações de DVD válidas</span><span class="sxs-lookup"><span data-stu-id="e7d37-103">Identifying Valid DVD Operations</span></span>

<span data-ttu-id="e7d37-104">Vários fatores determinam se você pode executar uma determinada operação de DVD:</span><span class="sxs-lookup"><span data-stu-id="e7d37-104">Several factors determine whether you can perform a given DVD operation:</span></span>

-   <span data-ttu-id="e7d37-105">O domínio atual.</span><span class="sxs-lookup"><span data-stu-id="e7d37-105">The current domain.</span></span> <span data-ttu-id="e7d37-106">Alguns comandos são válidos somente em determinados domínios.</span><span class="sxs-lookup"><span data-stu-id="e7d37-106">Some commands are only valid in certain domains.</span></span> <span data-ttu-id="e7d37-107">Quando o domínio é alterado, o navegador envia um \_ evento de alteração de domínio de DVD do EC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e7d37-107">When the domain changes, the navigator sends an EC\_DVD\_DOMAIN\_CHANGE event.</span></span> <span data-ttu-id="e7d37-108">Você também pode chamar [**IDvdInfo2:: GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) para obter o domínio atual.</span><span class="sxs-lookup"><span data-stu-id="e7d37-108">You can also call [**IDvdInfo2::GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) to get the current domain.</span></span>
-   <span data-ttu-id="e7d37-109">Sinalizadores UOPS.</span><span class="sxs-lookup"><span data-stu-id="e7d37-109">UOPS flags.</span></span> <span data-ttu-id="e7d37-110">Esses são sinalizadores gravados no disco que indicam quais operações são permitidas.</span><span class="sxs-lookup"><span data-stu-id="e7d37-110">These are flags written onto the disc that indicate which operations are permitted.</span></span> <span data-ttu-id="e7d37-111">Sempre que os sinalizadores são alterados, o navegador envia \_ um \_ evento de alteração UOPS válido de DVD do EC \_ \_ com os novos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="e7d37-111">Whenever the flags change, the navigator sends a EC\_DVD\_VALID\_UOPS\_CHANGE event with the new flags.</span></span> <span data-ttu-id="e7d37-112">Você também pode chamar [**IDvdInfo2:: GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) para obter os sinalizadores UOPS atuais.</span><span class="sxs-lookup"><span data-stu-id="e7d37-112">You can also call [**IDvdInfo2::GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) to get the current UOPS flags.</span></span>
-   <span data-ttu-id="e7d37-113">Conteúdo do DVD.</span><span class="sxs-lookup"><span data-stu-id="e7d37-113">DVD content.</span></span> <span data-ttu-id="e7d37-114">Alguns comandos podem não ser relevantes com base no conteúdo do DVD.</span><span class="sxs-lookup"><span data-stu-id="e7d37-114">Some commands may not be relevant based on the content of the DVD.</span></span> <span data-ttu-id="e7d37-115">Por exemplo, o método [**IDvdControl2:: SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) pode ser permitido de acordo com os sinalizadores de domínio e UOPS atuais, mas o vídeo pode ter apenas um ângulo.</span><span class="sxs-lookup"><span data-stu-id="e7d37-115">For example, the [**IDvdControl2::SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) method might be permitted according to the current domain and UOPS flags, yet the video might have only one angle.</span></span> <span data-ttu-id="e7d37-116">Nesse caso, a chamada **SelectAngle** é permitida, mas não é uma opção significativa.</span><span class="sxs-lookup"><span data-stu-id="e7d37-116">In that case, the **SelectAngle** call is permitted but is not a meaningful option.</span></span>

<span data-ttu-id="e7d37-117">Em caso de dúvida, permita uma ação.</span><span class="sxs-lookup"><span data-stu-id="e7d37-117">When in doubt, permit an action.</span></span> <span data-ttu-id="e7d37-118">No pior, o método [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) falhará e você poderá fornecer comentários ao usuário.</span><span class="sxs-lookup"><span data-stu-id="e7d37-118">At worst, the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method will fail and you can give feedback to the user.</span></span> <span data-ttu-id="e7d37-119">Os comentários devem ser relativamente discretos.</span><span class="sxs-lookup"><span data-stu-id="e7d37-119">The feedback should be relatively unobtrusive.</span></span> <span data-ttu-id="e7d37-120">Por exemplo, você pode piscar um pequeno X vermelho para alertar o usuário.</span><span class="sxs-lookup"><span data-stu-id="e7d37-120">For example, you might flash a small red X to alert the user.</span></span> <span data-ttu-id="e7d37-121">O navegador de DVD retorna VFW \_ e \_ DVD \_ INVALIDDOMAIN quando o domínio proíbe uma operação e \_ \_ a operação de VFW e DVD é \_ \_ inibida quando os sinalizadores de UOPS proíbem uma operação.</span><span class="sxs-lookup"><span data-stu-id="e7d37-121">The DVD Navigator returns VFW\_E\_DVD\_INVALIDDOMAIN when the domain prohibits an operation, and VFW\_E\_DVD\_OPERATION\_INHIBITED when the UOPS flags prohibit an operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7d37-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7d37-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7d37-123">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="e7d37-123">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



