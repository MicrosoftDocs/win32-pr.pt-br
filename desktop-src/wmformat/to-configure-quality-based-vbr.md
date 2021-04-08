---
title: Para configurar Quality-Based VBR
description: Para configurar Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- fluxos, configurando fluxos de VBR
- fluxos, taxa de bits variável (VBR)
- taxa de bits variável (VBR), fluxos
- VBR (taxa de bits variável), fluxos
- fluxos, configurando a taxa de bits baseada em qualidade
- taxa de bits variável (VBR), configurando com base na qualidade
- VBR (taxa de bits variável), configurando com base na qualidade
- perfis, configurando a taxa de bits baseada em qualidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0b7a6ecb83c7242f82f5626a086c8aba23881f
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103917064"
---
# <a name="to-configure-quality-based-vbr"></a><span data-ttu-id="5ed3c-111">Para configurar Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="5ed3c-111">To Configure Quality-Based VBR</span></span>

<span data-ttu-id="5ed3c-112">Você pode usar a codificação de taxa de bits variável (VBR) com base em qualidade em um fluxo para especificar um nível de qualidade que será mantido para todo o fluxo, independentemente dos requisitos de taxa de bits resultantes.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-112">You can use quality-based variable bit rate (VBR) encoding on a stream to specify a quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>

<span data-ttu-id="5ed3c-113">Para fluxos de vídeo de taxa de bits VBR com base na qualidade, você deve especificar um nível de qualidade de 1 a 100, com 100 representando a qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-113">For quality-based VBR video streams, you must specify a quality level from 1 to 100, with 100 representing the highest quality.</span></span> <span data-ttu-id="5ed3c-114">No momento, há apenas 30 configurações de qualidade discretas.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-114">At present there are only 30 discrete quality settings.</span></span> <span data-ttu-id="5ed3c-115">Os níveis de qualidade a seguir correspondem a configurações de qualidade discretas: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-115">The following quality levels equate to discrete quality settings: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100.</span></span> <span data-ttu-id="5ed3c-116">Os números entre dois valores consecutivos na lista anterior equivalem à mesma configuração de qualidade que o número mais baixo.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-116">Numbers between two consecutive values in the preceding list equate to the same quality setting as the lower number.</span></span> <span data-ttu-id="5ed3c-117">Por exemplo, 1 e 4 são listados, portanto 2 e 3 resultam na mesma configuração de qualidade que 1.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-117">For example, 1 and 4 are listed, so 2 and 3 both result in the same quality setting as 1.</span></span>

<span data-ttu-id="5ed3c-118">Para fluxos de áudio, você pode enumerar os modos disponíveis e recuperar um objeto de configuração de fluxo.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-118">For audio streams, you can enumerate the available modes and retrieve a stream configuration object.</span></span> <span data-ttu-id="5ed3c-119">Para obter mais informações, consulte [para enumerar formatos de codec](to-enumerate-codec-formats.md).</span><span class="sxs-lookup"><span data-stu-id="5ed3c-119">For more information, see [To Enumerate Codec Formats](to-enumerate-codec-formats.md).</span></span>

<span data-ttu-id="5ed3c-120">Ao usar o vídeo VBR com base na qualidade, você deve definir o membro **dwBitrate** da estrutura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) para um valor positivo.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-120">When using quality-based VBR video, you must set the **dwBitrate** member of the [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure to a positive value.</span></span> <span data-ttu-id="5ed3c-121">Esse valor não é usado pelo gravador, mas passar zero ou um número negativo pode causar erros durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-121">This value is not used by the writer, but passing zero or a negative number can cause errors when writing.</span></span>

<span data-ttu-id="5ed3c-122">Para configurar um fluxo em um perfil a ser codificado com a VBR com base em qualidade, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-122">To configure a stream in a profile to be encoded with quality-based VBR, perform the following steps.</span></span>

1.  <span data-ttu-id="5ed3c-123">Crie um objeto do Gerenciador de perfis chamando a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="5ed3c-123">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="5ed3c-124">Abra um perfil existente ao qual você deseja adicionar suporte a VBR.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-124">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="5ed3c-125">Para obter mais informações sobre como abrir perfis, consulte [trabalhando com perfis](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="5ed3c-125">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="5ed3c-126">Obtenha um objeto de configuração de fluxo para o fluxo que você deseja usar chamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) ou [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="5ed3c-126">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="5ed3c-127">Obtenha um ponteiro para a interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) do objeto de configuração de fluxo chamando **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-127">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="5ed3c-128">Habilite a VBR para o fluxo chamando [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para a propriedade **g \_ wszVBREnabled** .</span><span class="sxs-lookup"><span data-stu-id="5ed3c-128">Enable VBR for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="5ed3c-129">Defina o nível de qualidade para o fluxo de VBR chamando **IWMPropertyVault:: SetProperty** para a propriedade **g \_ wszVBRQuality** .</span><span class="sxs-lookup"><span data-stu-id="5ed3c-129">Set the quality level for the VBR stream by calling **IWMPropertyVault::SetProperty** for the **g\_wszVBRQuality** property.</span></span>
7.  <span data-ttu-id="5ed3c-130">Defina **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** para zero com **IWMPropertyVault:: SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-130">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
8.  <span data-ttu-id="5ed3c-131">Salve as alterações feitas no fluxo chamando [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="5ed3c-131">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
9.  <span data-ttu-id="5ed3c-132">Salve o perfil ou passe-o para o objeto gravador e comece a escrever.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-132">Save the profile, or pass it to the writer object and start writing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ed3c-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ed3c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ed3c-134">**Configurando fluxos de VBR**</span><span class="sxs-lookup"><span data-stu-id="5ed3c-134">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




