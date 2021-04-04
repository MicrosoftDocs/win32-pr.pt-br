---
title: Para configurar a VBR restrita
description: Para configurar a VBR restrita
ms.assetid: a39e7628-0211-48ad-94e5-5003203f30be
keywords:
- fluxos, configurando fluxos de VBR
- fluxos, taxa de bits variável (VBR)
- taxa de bits variável (VBR), fluxos
- VBR (taxa de bits variável), fluxos
- fluxos, configurando a taxa de bits restrita
- taxa de bits variável (VBR), configurando a restrição
- VBR (taxa de bits variável), configurando a restrição
- perfis, configurando a VBR restrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d4e2a1bbea1b724fdde1cc820f19caf9dd77be
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007236"
---
# <a name="to-configure-constrained-vbr"></a><span data-ttu-id="9e569-111">Para configurar a VBR restrita</span><span class="sxs-lookup"><span data-stu-id="9e569-111">To Configure Constrained VBR</span></span>

<span data-ttu-id="9e569-112">Você pode usar a codificação de taxa de bits variável restrita (VBR) em um fluxo para especificar uma taxa média de bits que será mantida no conteúdo codificado.</span><span class="sxs-lookup"><span data-stu-id="9e569-112">You can use constrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="9e569-113">Você também especifica a taxa de bits máxima do fluxo e a janela de buffer máxima necessária.</span><span class="sxs-lookup"><span data-stu-id="9e569-113">You also specify the maximum bit rate of the stream and the maximum required buffer window.</span></span>

<span data-ttu-id="9e569-114">Você não pode saber qual será a taxa de bits média para um fluxo de VBR restrita antes da codificação, mas você pode usar uma estimativa aproximada.</span><span class="sxs-lookup"><span data-stu-id="9e569-114">You cannot know what the average bit rate will be for a constrained VBR stream before encoding, but you can use a rough estimate.</span></span> <span data-ttu-id="9e569-115">Como regra geral, a taxa de bits máxima especificada acabará sendo de duas a três vezes a taxa média de bits.</span><span class="sxs-lookup"><span data-stu-id="9e569-115">As a general rule, the maximum bit rate you specify will end up being two to three times the average bit rate.</span></span>

<span data-ttu-id="9e569-116">A taxa de bits restrita deve ser usada em conjunto com codificação de duas passagens.</span><span class="sxs-lookup"><span data-stu-id="9e569-116">Constrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="9e569-117">A codificação de duas passagens não está definida no perfil.</span><span class="sxs-lookup"><span data-stu-id="9e569-117">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="9e569-118">Você deve configurar o gravador para executar uma passagem de pré-processamento antes de gravar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="9e569-118">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="9e569-119">Para obter mais informações sobre como usar a codificação de duas passagens, consulte [usando a codificação Two-Pass](using-two-pass-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="9e569-119">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="9e569-120">Para configurar um fluxo em um perfil para usar a codificação de VBR restrita, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9e569-120">To configure a stream in a profile to use constrained VBR encoding, perform the following steps.</span></span>

1.  <span data-ttu-id="9e569-121">Crie um objeto do Gerenciador de perfis chamando a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="9e569-121">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="9e569-122">Abra um perfil existente ao qual você deseja adicionar suporte a VBR.</span><span class="sxs-lookup"><span data-stu-id="9e569-122">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="9e569-123">Para obter mais informações sobre como abrir perfis, consulte [trabalhando com perfis](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="9e569-123">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="9e569-124">Obtenha um objeto de configuração de fluxo para o fluxo que você deseja usar chamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) ou [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="9e569-124">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="9e569-125">Obtenha um ponteiro para a interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) do objeto de configuração de fluxo chamando **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="9e569-125">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="9e569-126">Habilite a codificação de VBR para o fluxo chamando [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para a propriedade **g \_ wszVBREnabled** .</span><span class="sxs-lookup"><span data-stu-id="9e569-126">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="9e569-127">Use chamadas para **IWMPropertyVault:: SetProperty** para definir os valores máximos desejados para as propriedades **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** .</span><span class="sxs-lookup"><span data-stu-id="9e569-127">Use calls to **IWMPropertyVault::SetProperty** to set the desired maximum values for the **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** properties.</span></span>
7.  <span data-ttu-id="9e569-128">Salve as alterações feitas no fluxo chamando [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="9e569-128">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="9e569-129">Salve o perfil ou passe-o para o objeto gravador.</span><span class="sxs-lookup"><span data-stu-id="9e569-129">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="9e569-130">Configure o gravador para executar uma passagem de pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="9e569-130">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e569-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9e569-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e569-132">**Configurando fluxos de VBR**</span><span class="sxs-lookup"><span data-stu-id="9e569-132">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




