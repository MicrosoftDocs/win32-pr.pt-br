---
title: Trabalhando com níveis de proteção de saída
description: Trabalhando com níveis de proteção de saída
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- SDK do Windows Media Format, níveis de proteção de saída (OPL)
- SDK do Windows Media Format, níveis de proteção
- ASF (Advanced Systems Format), níveis de proteção de saída (OPL)
- ASF (formato de sistemas avançados), níveis de proteção de saída (OPL)
- ASF (Advanced Systems Format), níveis de proteção
- ASF (formato de sistemas avançados), níveis de proteção
- ASF (Advanced Systems Format), várias licenças
- ASF (formato de sistemas avançados), várias licenças
- DRM (gerenciamento de direitos digitais), OPL (níveis de proteção de saída)
- DRM (gerenciamento de direitos digitais), níveis de proteção de saída (OPL)
- DRM (gerenciamento de direitos digitais), níveis de proteção
- DRM (gerenciamento de direitos digitais), níveis de proteção
- DRM (gerenciamento de direitos digitais), avaliando os níveis de proteção de saída (OPL)
- DRM (gerenciamento de direitos digitais), avaliando os níveis de proteção de saída (OPL)
- DRM (gerenciamento de direitos digitais), várias licenças
- DRM (gerenciamento de direitos digitais), várias licenças
- níveis de proteção de saída (OPL)
- OPL (níveis de proteção de saída)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab7023cc8285e5f3993aac69c57deca9675d9dd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293754"
---
# <a name="working-with-output-protection-levels"></a><span data-ttu-id="dec20-121">Trabalhando com níveis de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="dec20-121">Working with Output Protection Levels</span></span>

<span data-ttu-id="dec20-122">As licenças criadas usando o SDK do Windows Media Rights Manager 10 podem especificar restrições de ação usando os níveis de proteção de saída (OPLs).</span><span class="sxs-lookup"><span data-stu-id="dec20-122">Licenses created by using the Windows Media Rights Manager 10 SDK can specify action restrictions using output protection levels (OPLs).</span></span> <span data-ttu-id="dec20-123">OPLs habilite um criador de licença para permitir algumas ações somente em dispositivos com tecnologias específicas.</span><span class="sxs-lookup"><span data-stu-id="dec20-123">OPLs enable a license creator to allow some actions only on devices with specific technologies.</span></span> <span data-ttu-id="dec20-124">Os benefícios de usar o OPLs é que você obtém mais flexibilidade na criação de restrições de licença do que as versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="dec20-124">The benefits of using OPLs is that you get more flexibility in creating license restrictions than previous versions.</span></span> <span data-ttu-id="dec20-125">Além disso, o OPLs é expansível para acomodar tecnologias futuras.</span><span class="sxs-lookup"><span data-stu-id="dec20-125">In addition, OPLs are expandable to accommodate future technologies.</span></span> <span data-ttu-id="dec20-126">Você pode dar suporte a tais licenças em seus aplicativos usando os métodos da interface [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) .</span><span class="sxs-lookup"><span data-stu-id="dec20-126">You can support such licenses in your applications by using the methods of the [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) interface.</span></span>

<span data-ttu-id="dec20-127">Para ler os arquivos que são protegidos por uma licença que especifica OPLs, você deve verificar o OPL para a ação desejada.</span><span class="sxs-lookup"><span data-stu-id="dec20-127">To read files that are protected by a license that specifies OPLs, you must check the OPL for the desired action.</span></span> <span data-ttu-id="dec20-128">A tecnologia de saída que seu aplicativo está usando deve ser permitida pelo OPL na licença.</span><span class="sxs-lookup"><span data-stu-id="dec20-128">The output technology your application is using must be allowed by the OPL in the license.</span></span> <span data-ttu-id="dec20-129">Por exemplo, algumas licenças para áudio protegido podem exigir que você use o caminho de áudio seguro para reproduzi-lo.</span><span class="sxs-lookup"><span data-stu-id="dec20-129">For example, some licenses for protected audio may require that you use secure audio path to play it.</span></span>

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a><span data-ttu-id="dec20-130">Configurando o leitor para avaliar os níveis de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="dec20-130">Configuring the Reader to Evaluate Output Protection Levels</span></span>

<span data-ttu-id="dec20-131">Antes de poder verificar OPLs para arquivos carregados no leitor, você deve chamar o método [**IWMDRMReader2:: SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) , passando **true** para o parâmetro *fEvaluate* .</span><span class="sxs-lookup"><span data-stu-id="dec20-131">Before you can check OPLs for files loaded in the reader, you must call the [**IWMDRMReader2::SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) method, passing **TRUE** for the *fEvaluate* parameter.</span></span> <span data-ttu-id="dec20-132">Se você não chamar esse método, as licenças que exigem OPLs não serão visíveis para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dec20-132">If you do not call this method, licenses that require OPLs are not visible to your application.</span></span>

## <a name="evaluating-copy-output-protection-levels"></a><span data-ttu-id="dec20-133">Avaliando níveis de proteção de saída de cópia</span><span class="sxs-lookup"><span data-stu-id="dec20-133">Evaluating Copy Output Protection Levels</span></span>

<span data-ttu-id="dec20-134">Para obter os níveis de proteção de saída para a ação de cópia, chame o método [**IWMDRMReader2:: GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) .</span><span class="sxs-lookup"><span data-stu-id="dec20-134">To get output protection levels for the copy action, call the [**IWMDRMReader2::GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) method.</span></span> <span data-ttu-id="dec20-135">Os dados recebidos da chamada são armazenados em uma estrutura [**OPL de \_ cópia \_ do DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) .</span><span class="sxs-lookup"><span data-stu-id="dec20-135">The data you receive from the call is stored in a [**DRM\_COPY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) structure.</span></span> <span data-ttu-id="dec20-136">A estrutura contém um nível de proteção de saída base, que especifica o nível de saída mínimo para a ação de cópia na licença.</span><span class="sxs-lookup"><span data-stu-id="dec20-136">The structure contains a base output protection level, which specifies the minimum output level for the copy action in the license.</span></span> <span data-ttu-id="dec20-137">No entanto, \_ a \_ estrutura OPL de cópia do DRM também contém duas listas de identificadores de tecnologia: uma para tecnologias permitidas que são classificadas em um OPL mais baixo do que a base e outra para tecnologias que são classificadas de forma igual ou superior à OPL base, mas que são restritas pela licença.</span><span class="sxs-lookup"><span data-stu-id="dec20-137">However, the DRM\_COPY\_OPL structure also contains two lists of technology identifiers: one for allowed technologies that are rated at a lower OPL than the base, and one for technologies that are rated equal to or higher than the base OPL but that are restricted by the license.</span></span> <span data-ttu-id="dec20-138">Você deve verificar as inclusões e exclusões para garantir que a tecnologia que seu aplicativo está usando seja permitida pela licença.</span><span class="sxs-lookup"><span data-stu-id="dec20-138">You must check the inclusions and exclusions to ensure that the technology your application is using is allowed by the license.</span></span>

## <a name="evaluating-play-output-protection-levels"></a><span data-ttu-id="dec20-139">Avaliando níveis de proteção de saída de reprodução</span><span class="sxs-lookup"><span data-stu-id="dec20-139">Evaluating Play Output Protection Levels</span></span>

<span data-ttu-id="dec20-140">Para obter os níveis de proteção de saída para a ação de reprodução, chame o método [**IWMDRMReader2:: GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) .</span><span class="sxs-lookup"><span data-stu-id="dec20-140">To get output protection levels for the play action, call the [**IWMDRMReader2::GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) method.</span></span> <span data-ttu-id="dec20-141">Os dados recebidos da chamada são armazenados em uma estrutura [**OPL de \_ reprodução \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) .</span><span class="sxs-lookup"><span data-stu-id="dec20-141">The data you receive from the call is stored in a [**DRM\_PLAY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) structure.</span></span> <span data-ttu-id="dec20-142">A estrutura contém várias outras estruturas.</span><span class="sxs-lookup"><span data-stu-id="dec20-142">The structure contains several other structures.</span></span> <span data-ttu-id="dec20-143">Os níveis de proteção de saída de base para a ação de reprodução são armazenados em uma estrutura de níveis de  [**\_ \_ \_ proteção \_ de saída mínima de DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) (o membro minOPL do **DRM \_ Play \_ OPL**), que define o mínimo de OPL necessário para reproduzir conteúdo em uma variedade de formatos.</span><span class="sxs-lookup"><span data-stu-id="dec20-143">The base output protection levels for the play action are stored in a [**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) structure (the **minOPL** member of **DRM\_PLAY\_OPL**), which defines the minimum OPL required to play content in a variety of formats.</span></span> <span data-ttu-id="dec20-144">Você deve verificar o membro para o tipo de formatos de saída que seu aplicativo fornece.</span><span class="sxs-lookup"><span data-stu-id="dec20-144">You must check the member for the type of output formats that your application delivers.</span></span>

<span data-ttu-id="dec20-145">A **estrutura \_ \_ OPL de reprodução do DRM** define dois tipos de restrições: os identificadores de proteção de saída de vídeo permitidos e de amostragem necessários.</span><span class="sxs-lookup"><span data-stu-id="dec20-145">The **DRM\_PLAY\_OPL** structure defines two kinds of restrictions: required down-sampling and allowed video output protection identifiers.</span></span>

<span data-ttu-id="dec20-146">Requerido-a amostragem é definida como uma lista de identificadores de tecnologia de saída (o membro **oplIdDownsample** do **\_ \_ OPL de reprodução DRM**) que, se usado, pode receber o conteúdo para reprodução somente se o conteúdo estiver primeiro abaixo de amostra para uma taxa de bits inferior.</span><span class="sxs-lookup"><span data-stu-id="dec20-146">Required down-sampling is defined as a list of output technology identifiers (the **oplIdDownsample** member of **DRM\_PLAY\_OPL**) that, if used, can receive the content for playback only if the content is first down-sampled to a lower bit rate.</span></span>

<span data-ttu-id="dec20-147">Os identificadores de proteção de saída de vídeo permitidos são definidos como uma lista de tecnologias de saída de vídeo com informações de configuração para cada uma.</span><span class="sxs-lookup"><span data-stu-id="dec20-147">Allowed video output protection identifiers are defined as a list of video output technologies with configuration information for each.</span></span>

## <a name="handling-multiple-licenses"></a><span data-ttu-id="dec20-148">Lidando com várias licenças</span><span class="sxs-lookup"><span data-stu-id="dec20-148">Handling Multiple Licenses</span></span>

<span data-ttu-id="dec20-149">Alguns arquivos podem ter várias licenças associadas a eles no repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="dec20-149">Some files may have multiple licenses associated with them in the local license store.</span></span> <span data-ttu-id="dec20-150">Ao avaliar OPLs para um arquivo que você está lendo, você pode verificar licenças adicionais chamando o método [**IWMDRMReader2:: TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) .</span><span class="sxs-lookup"><span data-stu-id="dec20-150">When you evaluate OPLs for a file that you are reading, you can check for additional licenses by calling the [**IWMDRMReader2::TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) method.</span></span> <span data-ttu-id="dec20-151">Você deve continuar tentando as licenças até encontrar uma que permita a ação que deseja executar ou até que TryNextLicense retorne o DRM \_ S \_ false, o que indica que não há mais licenças.</span><span class="sxs-lookup"><span data-stu-id="dec20-151">You should continue trying licenses until you find one that allows the action you want to perform or until TryNextLicense returns DRM\_S\_FALSE, which indicates that there are no more licenses.</span></span>

<span data-ttu-id="dec20-152">Em alguns casos, um arquivo pode ter uma licença associada que exige um OPL para o qual seu aplicativo não possa dar suporte.</span><span class="sxs-lookup"><span data-stu-id="dec20-152">In some cases, a file might have an associated license that requires an OPL that your application cannot support.</span></span> <span data-ttu-id="dec20-153">Nesse caso, é importante verificar licenças adicionais, pois pode haver uma licença que não especifique OPLs.</span><span class="sxs-lookup"><span data-stu-id="dec20-153">In such a case it is important to check for additional licenses because a license may exist that does not specify OPLs.</span></span>

<span data-ttu-id="dec20-154">**Observação** O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="dec20-154">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dec20-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dec20-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dec20-156">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="dec20-156">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="dec20-157">**Interface IWMDRMReader2**</span><span class="sxs-lookup"><span data-stu-id="dec20-157">**IWMDRMReader2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




