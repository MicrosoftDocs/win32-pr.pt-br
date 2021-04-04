---
title: Para configurar a VBR não restringida
description: Para configurar a VBR não restringida
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- fluxos, configurando fluxos de VBR
- fluxos, taxa de bits variável (VBR)
- taxa de bits variável (VBR), fluxos
- VBR (taxa de bits variável), fluxos
- fluxos, configurando a VBR não restringida
- taxa de bits variável (VBR), configurando irrestrito
- VBR (taxa de bits variável), configurando irrestrito
- perfis, configurando a VBR não restringida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c022c79bb38414ab201db11abd0cf260dfafe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104084393"
---
# <a name="to-configure-unconstrained-vbr"></a><span data-ttu-id="fc112-111">Para configurar a VBR não restringida</span><span class="sxs-lookup"><span data-stu-id="fc112-111">To Configure Unconstrained VBR</span></span>

<span data-ttu-id="fc112-112">Você pode usar a codificação de taxa de bits variável (VBR) irrestrita em um fluxo para especificar uma taxa média de bits que será mantida no conteúdo codificado.</span><span class="sxs-lookup"><span data-stu-id="fc112-112">You can use unconstrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="fc112-113">A VBR não restringida difere da CBR normal, pois a variação em taxa de bits em todo o fluxo pode ser maior.</span><span class="sxs-lookup"><span data-stu-id="fc112-113">Unconstrained VBR differs from normal CBR in that the variance in bit rate throughout the stream can be greater.</span></span>

<span data-ttu-id="fc112-114">A taxa de bits do fluxo, definida com [**IWMStreamConfig::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)setaverage, é usada como a taxa de bits média desejada.</span><span class="sxs-lookup"><span data-stu-id="fc112-114">The bit rate of the stream, set with [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), is used as the desired average bit rate.</span></span> <span data-ttu-id="fc112-115">Quando a codificação do fluxo estiver concluída, você poderá usar [**IWMPropertyVault:: GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) para recuperar duas propriedades adicionais: **g \_ wszVBRPeak** e **g \_ wszBufferAverage**.</span><span class="sxs-lookup"><span data-stu-id="fc112-115">When encoding of the stream is complete, you can use [**IWMPropertyVault::GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) to retrieve two additional properties: **g\_wszVBRPeak** and **g\_wszBufferAverage**.</span></span> <span data-ttu-id="fc112-116">Essas propriedades descrevem a taxa de bits de pico do conteúdo codificado e a janela de buffer médio do conteúdo, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fc112-116">These properties describe the peak bit rate of the encoded content and the average buffer window of the content, respectively.</span></span>

<span data-ttu-id="fc112-117">A VBR não restringida deve ser usada em conjunto com codificação de duas passagens.</span><span class="sxs-lookup"><span data-stu-id="fc112-117">Unconstrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="fc112-118">A codificação de duas passagens não está definida no perfil.</span><span class="sxs-lookup"><span data-stu-id="fc112-118">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="fc112-119">Você deve configurar o gravador para executar uma passagem de pré-processamento antes de gravar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="fc112-119">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="fc112-120">Para obter mais informações sobre como usar a codificação de duas passagens, consulte [usando a codificação Two-Pass](using-two-pass-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="fc112-120">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="fc112-121">Para configurar um fluxo em um perfil a ser codificado com uma VBR não restringida, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="fc112-121">To configure a stream in a profile to be encoded with unconstrained VBR, perform the following steps:</span></span>

1.  <span data-ttu-id="fc112-122">Crie um objeto do Gerenciador de perfis chamando a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="fc112-122">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="fc112-123">Abra um perfil existente ao qual você deseja adicionar suporte a VBR.</span><span class="sxs-lookup"><span data-stu-id="fc112-123">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="fc112-124">Para obter mais informações sobre como abrir perfis, consulte [trabalhando com perfis](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="fc112-124">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="fc112-125">Obtenha um objeto de configuração de fluxo para o fluxo que você deseja usar chamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) ou [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="fc112-125">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="fc112-126">Obtenha um ponteiro para a interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) do objeto de configuração de fluxo chamando **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="fc112-126">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="fc112-127">Habilite a codificação de VBR para o fluxo chamando [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para a propriedade **g \_ wszVBREnabled** .</span><span class="sxs-lookup"><span data-stu-id="fc112-127">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="fc112-128">Defina **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** para zero com **IWMPropertyVault:: SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="fc112-128">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
7.  <span data-ttu-id="fc112-129">Salve as alterações feitas no fluxo chamando [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="fc112-129">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="fc112-130">Salve o perfil ou passe-o para o objeto gravador.</span><span class="sxs-lookup"><span data-stu-id="fc112-130">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="fc112-131">Configure o gravador para executar uma passagem de pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="fc112-131">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc112-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc112-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc112-133">**Configurando fluxos de VBR**</span><span class="sxs-lookup"><span data-stu-id="fc112-133">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




