---
description: Como determinar as taxas com suporte
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Como determinar as taxas com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f67e9753604f51e85c641e616e8b69944b96618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164841"
---
# <a name="how-to-determine-supported-rates"></a><span data-ttu-id="236b0-103">Como determinar as taxas com suporte</span><span class="sxs-lookup"><span data-stu-id="236b0-103">How to Determine Supported Rates</span></span>

<span data-ttu-id="236b0-104">Antes de alterar a taxa de reprodução, um aplicativo deve verificar se a taxa de reprodução é suportada pelos objetos no pipeline.</span><span class="sxs-lookup"><span data-stu-id="236b0-104">Before changing the playback rate, an application should check whether the playback rate is supported by the objects in the pipeline.</span></span> <span data-ttu-id="236b0-105">A interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) fornece métodos para obter as taxas máximas de avanço e reversão, a taxa com suporte mais próxima a uma taxa solicitada e a taxa mais lenta.</span><span class="sxs-lookup"><span data-stu-id="236b0-105">The [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface provides methods to get the maximum forward and reverse rates, the supported rate nearest to a requested rate, and the slowest rate.</span></span> <span data-ttu-id="236b0-106">Cada uma dessas consultas de taxa pode especificar a direção da reprodução e se deseja usar a fina.</span><span class="sxs-lookup"><span data-stu-id="236b0-106">Each of these rate queries can specify the playback direction and whether to use thinning.</span></span> <span data-ttu-id="236b0-107">A taxa de reprodução exata é consultada usando a interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .</span><span class="sxs-lookup"><span data-stu-id="236b0-107">The exact playback rate is queried by using the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface.</span></span>

<span data-ttu-id="236b0-108">Para obter informações sobre como alterar as taxas de reprodução, consulte [como definir a taxa de reprodução na sessão de mídia](how-to-set-the-playback-rate-on-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="236b0-108">For information about changing playback rates, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>

<span data-ttu-id="236b0-109">Para obter informações gerais sobre taxas de reprodução, consulte [sobre o controle de taxa](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="236b0-109">For general information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-determine-the-current-playback-rate"></a><span data-ttu-id="236b0-110">Para determinar a taxa de reprodução atual</span><span class="sxs-lookup"><span data-stu-id="236b0-110">To determine the current playback rate</span></span>

1.  <span data-ttu-id="236b0-111">Obtenha o serviço de controle de taxa da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="236b0-111">Get the rate control service from the Media Session.</span></span>

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    <span data-ttu-id="236b0-112">Passe um ponteiro de interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado no parâmetro *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="236b0-112">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

    <span data-ttu-id="236b0-113">O aplicativo deve consultar o serviço de controle de taxa por meio da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="236b0-113">The application must query for the rate control service through the Media Session.</span></span> <span data-ttu-id="236b0-114">Internamente, a sessão de mídia consulta os objetos na topologia.</span><span class="sxs-lookup"><span data-stu-id="236b0-114">Internally, the Media Session queries the objects in the topology.</span></span>

2.  <span data-ttu-id="236b0-115">Chame o método [**IMFRateControl:: GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) para obter a taxa de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="236b0-115">Call the [**IMFRateControl::GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) method to get the current playback rate.</span></span>

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    <span data-ttu-id="236b0-116">O parâmetro *pfThin* de [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) recebe um valor **bool** que indica se o fluxo está sendo fino no momento.</span><span class="sxs-lookup"><span data-stu-id="236b0-116">The *pfThin* parameter of [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) receives a **BOOL** value that indicates whether the stream is currently being thinned.</span></span> <span data-ttu-id="236b0-117">O aplicativo deve passar **nulo** se não quiser consultar o suporte de finamento para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="236b0-117">The application must pass **NULL** if it does not want to query thinning support for the stream.</span></span> <span data-ttu-id="236b0-118">O parâmetro *pflRate* recebe a taxa de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="236b0-118">The *pflRate* parameter receives the current playback rate.</span></span>

## <a name="to-determine-the-nearest-supported-rate"></a><span data-ttu-id="236b0-119">Para determinar a taxa mais próxima com suporte</span><span class="sxs-lookup"><span data-stu-id="236b0-119">To determine the nearest supported rate</span></span>

1.  <span data-ttu-id="236b0-120">Obtenha a taxa de serviço de suporte da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="236b0-120">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="236b0-121">Passe um ponteiro de interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado no parâmetro *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="236b0-121">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="236b0-122">Chame o método [**IMFRateSupport:: IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) para recuperar a taxa com suporte mais próxima de uma taxa de reprodução solicitada.</span><span class="sxs-lookup"><span data-stu-id="236b0-122">Call the [**IMFRateSupport::IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method to retrieve the supported rate nearest to a requested playback rate.</span></span>

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    <span data-ttu-id="236b0-123">O exemplo consulta se uma taxa de reprodução de 4,0 tem suporte com finamento.</span><span class="sxs-lookup"><span data-stu-id="236b0-123">The example queries whether a playback rate of 4.0 is supported with thinning.</span></span> <span data-ttu-id="236b0-124">Isso é indicado passando **true** no parâmetro *fThin* de [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported).</span><span class="sxs-lookup"><span data-stu-id="236b0-124">This is indicated by passing **TRUE** in the *fThin* parameter of [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported).</span></span> <span data-ttu-id="236b0-125">Se essa taxa for suportada, *actualRate* conterá a taxa de reprodução de 4,0 e a chamada terá um valor de retorno de S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="236b0-125">If this rate is supported, *actualRate* contains the playback rate of 4.0, and the call succeeds with a return value of S\_OK.</span></span> <span data-ttu-id="236b0-126">Se a taxa de reprodução exata não for suportada, a taxa com suporte mais próxima será recebida em *actualRate*.</span><span class="sxs-lookup"><span data-stu-id="236b0-126">If the exact playback rate is not supported, the nearest supported rate is received in *actualRate*.</span></span> <span data-ttu-id="236b0-127">Se a taxa não for suportada e não houver uma taxa de reprodução mais próxima disponível, a chamada retornará um código de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="236b0-127">If the rate is not supported and there is no available nearest playback rate, the call returns an appropriate error code.</span></span>

    <span data-ttu-id="236b0-128">Esses valores podem ser alterados dependendo de quais componentes de pipeline são carregados.</span><span class="sxs-lookup"><span data-stu-id="236b0-128">These values can change depending on which pipeline components are loaded.</span></span> <span data-ttu-id="236b0-129">Portanto, você deve consultar os valores novamente sempre que carregar um novo topololgy.</span><span class="sxs-lookup"><span data-stu-id="236b0-129">Therefore, you should query the values again whenever you load a new topololgy.</span></span>

    <span data-ttu-id="236b0-130">Se a taxa de reprodução desejada não for suportada, uma opção é consultar cada objeto na topologia individualmente para descobrir se um componente específico não oferece suporte à taxa.</span><span class="sxs-lookup"><span data-stu-id="236b0-130">If the desired playback rate is not supported, one option is to query each object in the topology individually, to find out if a particular component does not support the rate.</span></span> <span data-ttu-id="236b0-131">Talvez seja possível recriar a topologia sem esse componente e, em seguida, reproduzir a taxa desejada.</span><span class="sxs-lookup"><span data-stu-id="236b0-131">You might be able to rebuild the topology without this component and then play at the desired rate.</span></span> <span data-ttu-id="236b0-132">Por exemplo, se cada componente, exceto o processador de áudio, der suporte a uma determinada taxa, você poderá recriar a topologia sem a ramificação de áudio e tocar na taxa desejada sem áudio.</span><span class="sxs-lookup"><span data-stu-id="236b0-132">For example, if every component except the audio renderer supports a given rate, you could rebuild the topology without the audio branch and play at the desired rate without audio.</span></span>

## <a name="to-determine-the-slowest-supported-rate"></a><span data-ttu-id="236b0-133">Para determinar a taxa com suporte mais lenta</span><span class="sxs-lookup"><span data-stu-id="236b0-133">To determine the slowest supported rate</span></span>

1.  <span data-ttu-id="236b0-134">Obtenha a taxa de serviço de suporte da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="236b0-134">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="236b0-135">Passe um ponteiro de interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado no parâmetro *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="236b0-135">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="236b0-136">Chame o método [**IMFRateSupport:: GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) para recuperar a taxa com suporte mais lenta.</span><span class="sxs-lookup"><span data-stu-id="236b0-136">Call the [**IMFRateSupport::GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) method to retrieve the slowest supported rate.</span></span>

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    <span data-ttu-id="236b0-137">O exemplo consulta a taxa de reprodução inversa mais lenta com finamento.</span><span class="sxs-lookup"><span data-stu-id="236b0-137">The example queries for the slowest reverse playback rate with thinning.</span></span> <span data-ttu-id="236b0-138">A taxa de limite inferior é recebida no parâmetro *slowestRate* de [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).</span><span class="sxs-lookup"><span data-stu-id="236b0-138">The lower bound rate is received in *slowestRate* parameter of [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).</span></span>

    <span data-ttu-id="236b0-139">Se a reprodução reversa ou a fina não for suportada, a chamada retornará um código de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="236b0-139">If reverse playback or thinning is not supported, the call returns an appropriate error code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="236b0-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="236b0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="236b0-141">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="236b0-141">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="236b0-142">Controle de taxa</span><span class="sxs-lookup"><span data-stu-id="236b0-142">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="236b0-143">Busca, avanço rápido e reprodução reversa</span><span class="sxs-lookup"><span data-stu-id="236b0-143">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



