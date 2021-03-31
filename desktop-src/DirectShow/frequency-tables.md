---
description: Tabelas de frequência
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Tabelas de frequência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933152c7ac38eefe91468aff8bc3a8eb3ced05df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087286"
---
# <a name="frequency-tables"></a><span data-ttu-id="75fa4-103">Tabelas de frequência</span><span class="sxs-lookup"><span data-stu-id="75fa4-103">Frequency Tables</span></span>

<span data-ttu-id="75fa4-104">O filtro de sintonizador de TV (kstvtune.ax) tem uma lista interna de tabelas de frequência.</span><span class="sxs-lookup"><span data-stu-id="75fa4-104">The TV Tuner filter (kstvtune.ax) has an internal list of frequency tables.</span></span> <span data-ttu-id="75fa4-105">Cada tabela de frequência contém uma lista de frequências e corresponde à frequência de transmissão ou de cabo para um determinado país/região.</span><span class="sxs-lookup"><span data-stu-id="75fa4-105">Each frequency table contains a list of frequencies, and corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="75fa4-106">Um aplicativo se ajusta a uma frequência específica chamando o método de [**\_ canal IAMTuner::p UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) com o índice da frequência desejada.</span><span class="sxs-lookup"><span data-stu-id="75fa4-106">An application tunes to a particular frequency by calling the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method with the index of the desired frequency.</span></span>

<span data-ttu-id="75fa4-107">Para alguns países/regiões, os números de índice das tabelas de frequência são mapeados diretamente para números de canal.</span><span class="sxs-lookup"><span data-stu-id="75fa4-107">For some countries/regions, the index numbers of the frequency tables map directly to channel numbers.</span></span> <span data-ttu-id="75fa4-108">No entanto, os números de canal fixos não são apropriados para todos os mercados.</span><span class="sxs-lookup"><span data-stu-id="75fa4-108">Fixed channel numbers are not appropriate for all markets, however.</span></span> <span data-ttu-id="75fa4-109">Por exemplo, os números de canais europeus não são realmente usados pelos consumidores.</span><span class="sxs-lookup"><span data-stu-id="75fa4-109">For instance, the European channel numbers are not actually used by consumers.</span></span> <span data-ttu-id="75fa4-110">Em vez disso, os consumidores esperam escolher e atribuir seus próprios números de canal para as frequências usadas pelos operadores de transmissão ou de cabo em sua área.</span><span class="sxs-lookup"><span data-stu-id="75fa4-110">Instead, consumers expect to choose and assign their own channel numbers for the frequencies that are used by the broadcast or cable operators in their area.</span></span> <span data-ttu-id="75fa4-111">Para esses países/regiões, os aplicativos não devem expor os números de índice diretamente para o usuário.</span><span class="sxs-lookup"><span data-stu-id="75fa4-111">For these countries/regions, applications should not expose the index numbers directly to the user.</span></span> <span data-ttu-id="75fa4-112">Instread, o aplicativo deve manter um mapeamento interno entre os números de canal (apresentados ao usuário) e os índices de frequência (para ajuste).</span><span class="sxs-lookup"><span data-stu-id="75fa4-112">Instread, the application should keep an internal mapping between channel numbers (presented to the user) and frequency indexes (for tuning).</span></span>

<span data-ttu-id="75fa4-113">A maioria dos operadores de cabo não-EUA está livre para transmitir frequências de sua escolha, muitas vezes misturando frequências de diferentes padrões na mesma lista de canais.</span><span class="sxs-lookup"><span data-stu-id="75fa4-113">Most non-US cable operators are free to broadcast on frequencies of their choosing, often mixing frequencies from different standards into the same channel lineup.</span></span> <span data-ttu-id="75fa4-114">Portanto, uma tabela de frequência "unicable" é usada para qualquer país/região que não possua uma autoridade de padrões de canal de cabo padrão.</span><span class="sxs-lookup"><span data-stu-id="75fa4-114">Therefore, a "Unicable" frequency table is used for any country/region that lacks a standard cable channel standards authority.</span></span> <span data-ttu-id="75fa4-115">Além disso, um mecanismo é fornecido para substituir frequências individuais nas tabelas de frequência.</span><span class="sxs-lookup"><span data-stu-id="75fa4-115">Also, a mechanism is provided to override individual frequencies in the frequency tables.</span></span> <span data-ttu-id="75fa4-116">Esse mecanismo é descrito na seção a seguir, [substituições de frequência](frequency-overrides.md).</span><span class="sxs-lookup"><span data-stu-id="75fa4-116">This mechanism is described in the following section, [Frequency Overrides](frequency-overrides.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="75fa4-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75fa4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75fa4-118">Ajuste de TV analógica internacional</span><span class="sxs-lookup"><span data-stu-id="75fa4-118">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



