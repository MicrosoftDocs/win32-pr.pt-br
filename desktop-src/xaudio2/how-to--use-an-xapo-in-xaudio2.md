---
description: Este tópico mostra como usar um efeito criado com a API XAPO em uma cadeia de efeitos XAudio2.
ms.assetid: d4d24177-25eb-13ca-0e38-0c876a273e0d
title: 'Como: Usar um XAPO no XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780e0ba59b5032ddc01b2709f1f3e9c5a0fcce1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779248"
---
# <a name="how-to-use-an-xapo-in-xaudio2"></a><span data-ttu-id="844f1-103">Como: Usar um XAPO no XAudio2</span><span class="sxs-lookup"><span data-stu-id="844f1-103">How to: Use an XAPO in XAudio2</span></span>

<span data-ttu-id="844f1-104">Este tópico mostra como usar um efeito criado com a API XAPO em uma cadeia de efeitos XAudio2.</span><span class="sxs-lookup"><span data-stu-id="844f1-104">This topic shows you how to use an effect created with the XAPO API in an XAudio2 effect chain.</span></span>

1.  <span data-ttu-id="844f1-105">Crie o XAPO conforme descrito em [como: criar um XAPO](how-to--create-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="844f1-105">Create the XAPO as described in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>

    <span data-ttu-id="844f1-106">Você também pode implementar a funcionalidade de parâmetro de tempo de execução conforme descrito em [como adicionar suporte a parâmetros de tempo de execução a um XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="844f1-106">You can also implement run-time parameter functionality as described in [How to: Add Run-time Parameter Support to an XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).</span></span>

2.  <span data-ttu-id="844f1-107">Crie uma instância do XAPO.</span><span class="sxs-lookup"><span data-stu-id="844f1-107">Create an instance of the XAPO.</span></span>

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  <span data-ttu-id="844f1-108">Popular uma estrutura de [**\_ \_ descritor de efeito XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) com dados.</span><span class="sxs-lookup"><span data-stu-id="844f1-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  <span data-ttu-id="844f1-109">Preencha uma estrutura de [**\_ \_ cadeia de efeito de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) com dados.</span><span class="sxs-lookup"><span data-stu-id="844f1-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  <span data-ttu-id="844f1-110">Aplique a cadeia de efeito a uma voz XAudio2 com a função [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="844f1-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="844f1-111">Uma cadeia de efeitos também pode ser aplicada a uma voz quando a voz é criada passando a cadeia como um parâmetro para [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)ou [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span><span class="sxs-lookup"><span data-stu-id="844f1-111">An effect chain can also be applied to a voice when the voice is created by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

6.  <span data-ttu-id="844f1-112">Libere o efeito com IUnknown:: Release.</span><span class="sxs-lookup"><span data-stu-id="844f1-112">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="844f1-113">Quando você cria um XAPO, ele terá uma contagem de referência de 1.</span><span class="sxs-lookup"><span data-stu-id="844f1-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="844f1-114">Quando XAPO é passado para XAudio2 com [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa a contagem de referência no XAPO.</span><span class="sxs-lookup"><span data-stu-id="844f1-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="844f1-115">Liberar a referência do cliente para o XAPO permite que o XAudio2 assuma a propriedade do XAPO.</span><span class="sxs-lookup"><span data-stu-id="844f1-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="844f1-116">Se XAudio2 tiver a única referência para o XAPO, ele será Descartado quando não estiver mais sendo usado pelo XAudio2.</span><span class="sxs-lookup"><span data-stu-id="844f1-116">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="844f1-117">Se o código do cliente precisar manter uma referência para o XAPO para reutilização posterior, por exemplo, você deve ignorar esta etapa.</span><span class="sxs-lookup"><span data-stu-id="844f1-117">If the client code needs to maintain a reference to the XAPO for later reuse, for example, you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

7.  <span data-ttu-id="844f1-118">Preencha a estrutura do parâmetro, se houver, associada ao efeito.</span><span class="sxs-lookup"><span data-stu-id="844f1-118">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="844f1-119">Nesse caso, a porcentagem de força total na qual o efeito deve ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="844f1-119">In this case, the percentage of full strength at which the effect should be applied.</span></span>

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  <span data-ttu-id="844f1-120">Passe a estrutura do parâmetro de efeito para o efeito chamando a função [**Seteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) na voz à qual o efeito está anexado.</span><span class="sxs-lookup"><span data-stu-id="844f1-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="844f1-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="844f1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="844f1-122">Efeitos de áudio</span><span class="sxs-lookup"><span data-stu-id="844f1-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="844f1-123">Visão geral do XAPO</span><span class="sxs-lookup"><span data-stu-id="844f1-123">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="844f1-124">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="844f1-124">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
