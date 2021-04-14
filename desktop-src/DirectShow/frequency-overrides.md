---
description: Substituições de frequência
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Substituições de frequência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57177e4990cb40be271fc551718964faf1696d2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500202"
---
# <a name="frequency-overrides"></a><span data-ttu-id="0481d-103">Substituições de frequência</span><span class="sxs-lookup"><span data-stu-id="0481d-103">Frequency Overrides</span></span>

<span data-ttu-id="0481d-104">Uma quantidade significativa de esforço foi gasta para garantir que as frequências de difusão e as atribuições padrão de cor estejam corretas para cada país/região.</span><span class="sxs-lookup"><span data-stu-id="0481d-104">A significant amount of effort was spent to ensure that the broadcast frequencies and color standard assignments are correct for each country/region.</span></span> <span data-ttu-id="0481d-105">Mesmo assim, haverá situações em que as tabelas de frequência não são suficientes, contêm erros ou se tornam obsoletas.</span><span class="sxs-lookup"><span data-stu-id="0481d-105">Even so, there will be situations when the frequency tables are not sufficient, contain errors, or become obsolete.</span></span> <span data-ttu-id="0481d-106">Para resolver esse problema, as frequências listadas nas tabelas de frequência do filtro de sintonizador de TV podem ser substituídas seletivamente, usando a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="0481d-106">To address this problem, the frequencies listed in the TV Tuner filter's frequency tables may be selectively overridden, by using the following registry key:</span></span>

<span data-ttu-id="0481d-107">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="0481d-107">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

> [!Note]  
> <span data-ttu-id="0481d-108">A partir do Windows 7, a seguinte chave de registro redirecionada é usada para aplicativos x86 em execução em versões x64 do Windows:</span><span class="sxs-lookup"><span data-stu-id="0481d-108">Starting in Windows 7, the following redirected registry key is used for x86 applications running on x64 versions of Windows:</span></span>

 

<span data-ttu-id="0481d-109">**HKEY \_ \_Computador local** \\ **software** \\ **Wow6432Node** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="0481d-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Wow6432Node**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

<span data-ttu-id="0481d-110">As substituições de frequência são agrupadas em "espaços de ajuste" definidos pelo aplicativo, que são identificadas pelo número.</span><span class="sxs-lookup"><span data-stu-id="0481d-110">Frequency overrides are grouped into application-defined "tuning spaces," which are identified by number.</span></span> <span data-ttu-id="0481d-111">O exemplo a seguir mostra uma substituição de exemplo:</span><span class="sxs-lookup"><span data-stu-id="0481d-111">The following example shows an example override:</span></span>

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

<span data-ttu-id="0481d-112">Nesse caso, "TS0-1" indica o espaço de ajuste 0 para frequências de cabo.</span><span class="sxs-lookup"><span data-stu-id="0481d-112">In this case, "TS0-1" indicates Tuning Space 0 for cable frequencies.</span></span> <span data-ttu-id="0481d-113">O primeiro número identifica o espaço de ajuste.</span><span class="sxs-lookup"><span data-stu-id="0481d-113">The first number identifies the tuning space.</span></span> <span data-ttu-id="0481d-114">O segundo número é 0 para frequências de difusão ou 1 para frequências de cabo.</span><span class="sxs-lookup"><span data-stu-id="0481d-114">The second number is either 0 for broadcast frequencies or 1 for cable frequencies.</span></span>

<span data-ttu-id="0481d-115">A subchave chamada "12" substitui o valor de frequência da frequência no índice 12 da tabela de frequência atual.</span><span class="sxs-lookup"><span data-stu-id="0481d-115">The subkey named "12" overrides the frequency value for the frequency at index 12 in the current frequency table.</span></span> <span data-ttu-id="0481d-116">O valor da subchave é um **DWORD** que especifica a frequência em Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="0481d-116">The value of the subkey is a **DWORD** that specifies the frequency in Hertz (Hz).</span></span> <span data-ttu-id="0481d-117">Neste exemplo, a frequência é definida como 67,25 MHz.</span><span class="sxs-lookup"><span data-stu-id="0481d-117">In this example, the frequency is set to 67.25 MHz.</span></span> <span data-ttu-id="0481d-118">As substituições podem ser definidas para qualquer número de canal no intervalo de 1 a 999, inclusive.</span><span class="sxs-lookup"><span data-stu-id="0481d-118">Overrides can be defined for any channel numbers in the range of 1 to 999, inclusive.</span></span> <span data-ttu-id="0481d-119">Se o hardware de ajuste não oferecer suporte a uma determinada frequência, a solicitação de ajuste falhará.</span><span class="sxs-lookup"><span data-stu-id="0481d-119">If the tuning hardware does not support a given frequency, the tune request will fail.</span></span>

<span data-ttu-id="0481d-120">Esse mecanismo também pode ser usado para criar novos números de canal fora do intervalo existente na tabela de frequência.</span><span class="sxs-lookup"><span data-stu-id="0481d-120">This mechanism can also be used to create new channel numbers outside the existing range in the frequency table.</span></span> <span data-ttu-id="0481d-121">O método [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) retornará o intervalo de canais estendido.</span><span class="sxs-lookup"><span data-stu-id="0481d-121">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method will return the extended channel range.</span></span> <span data-ttu-id="0481d-122">Por exemplo, se o intervalo de canal original era de 1 a 158 e uma substituição de canal de "200" for adicionada ao registro, o método **ChannelMinMax** retornará 200 como o canal máximo.</span><span class="sxs-lookup"><span data-stu-id="0481d-122">For example, if the original channel range was 1 to 158, and a channel override of "200" is added to the registry, the **ChannelMinMax** method will return 200 as the maximum channel.</span></span> <span data-ttu-id="0481d-123">Nesse caso, os números de canal no intervalo de 159 a 199 não terão frequências atribuídas a eles, portanto, quaisquer solicitações de ajuste nesse intervalo falharão automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0481d-123">In this case, channel numbers in the range of 159 to 199 will have no frequencies assigned to them, so any tuning requests in that range will automatically fail.</span></span>

<span data-ttu-id="0481d-124">O método [**IAMTuner::p UT \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) permite que o aplicativo escolha qual conjunto de substituições e informações de ajuste fino a serem usadas.</span><span class="sxs-lookup"><span data-stu-id="0481d-124">The [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method allows the application to choose which set of overrides and fine-tuning information to use.</span></span> <span data-ttu-id="0481d-125">Os números de espaço de ajuste são arbitrários.</span><span class="sxs-lookup"><span data-stu-id="0481d-125">Tuning space numbers are arbitrary.</span></span> <span data-ttu-id="0481d-126">É responsabilidade do aplicativo manter a relação entre o espaço de ajuste e a tabela de frequência.</span><span class="sxs-lookup"><span data-stu-id="0481d-126">It is the application's responsibility to maintain the relationship between the tuning space and the frequency table.</span></span> <span data-ttu-id="0481d-127">A abordagem mais simples é usar o código de país/região como o número de espaço de ajuste.</span><span class="sxs-lookup"><span data-stu-id="0481d-127">The most straightforward approach is to use the country/region code as the tuning space number.</span></span> <span data-ttu-id="0481d-128">Em seguida, sempre que o aplicativo alternar para um novo código de país/região, ele também alternará para o mesmo espaço de ajuste (nessa ordem).</span><span class="sxs-lookup"><span data-stu-id="0481d-128">Then, every time the application switches to a new country/region code, it also switches to the same tuning space (in that order).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0481d-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0481d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0481d-130">Ajuste de TV analógica internacional</span><span class="sxs-lookup"><span data-stu-id="0481d-130">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



