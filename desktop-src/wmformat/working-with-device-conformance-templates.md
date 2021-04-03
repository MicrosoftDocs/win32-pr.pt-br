---
title: Trabalhando com modelos de conformidade do dispositivo
description: Trabalhando com modelos de conformidade do dispositivo
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- perfis, modelos de conformidade do dispositivo
- perfis, modelos de conformidade
- codecs, modelos de conformidade do dispositivo
- codecs, modelos de conformidade
- modelos de conformidade do dispositivo, sobre
- modelos de conformidade
- modelos, modelos de conformidade do dispositivo
- ASF (Advanced Systems Format), modelos de conformidade do dispositivo
- ASF (formato de sistemas avançados), modelos de conformidade do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036d304aa43c0dce5fe4d5302dccc32484657155
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084348"
---
# <a name="working-with-device-conformance-templates"></a><span data-ttu-id="6393e-112">Trabalhando com modelos de conformidade do dispositivo</span><span class="sxs-lookup"><span data-stu-id="6393e-112">Working with Device Conformance Templates</span></span>

<span data-ttu-id="6393e-113">Devido à grande flexibilidade dos arquivos ASF, muitas vezes é difícil determinar se um arquivo é apropriado para reprodução em um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="6393e-113">Because of the great flexibility of ASF files, it is often difficult to determine whether a file is appropriate for playback on a specific device.</span></span> <span data-ttu-id="6393e-114">Por exemplo, os arquivos escritos para reprodução local em computadores desktop não são ideais para uso em dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="6393e-114">For example, files written for local playback on desktop computers are not optimal for use on handheld devices.</span></span> <span data-ttu-id="6393e-115">Os modelos de conformidade do dispositivo permitem que os aplicativos identifiquem rapidamente o tipo de dispositivo de reprodução para o qual um arquivo foi projetado.</span><span class="sxs-lookup"><span data-stu-id="6393e-115">Device conformance templates enable applications to quickly identify the type of playback device for which a file was intended.</span></span> <span data-ttu-id="6393e-116">Se o modelo de conformidade do dispositivo não corresponder ao dispositivo, o aplicativo poderá informar ao usuário que o arquivo não é apropriado para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6393e-116">If the device conformance template does not match the device, the application can inform the user that the file is inappropriate for the device.</span></span> <span data-ttu-id="6393e-117">Dessa forma, o usuário pode ter a garantia de uma melhor experiência de reprodução.</span><span class="sxs-lookup"><span data-stu-id="6393e-117">In this way, the user can be assured of a better playback experience.</span></span>

<span data-ttu-id="6393e-118">Se você estiver gravando arquivos exclusivamente para uso em computadores pessoais, os modelos de conformidade do dispositivo não serão tão de um fator na criação de perfis.</span><span class="sxs-lookup"><span data-stu-id="6393e-118">If you are writing files exclusively for use on personal computers, device conformance templates will not be as much of a factor in creating profiles.</span></span> <span data-ttu-id="6393e-119">A principal finalidade desses modelos é garantir que os arquivos criados para uso com hardware especial sejam compatíveis com uma gama completa de dispositivos, e não apenas um único dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6393e-119">The main purpose of these templates is to ensure that files created for use with special hardware are compatible with a whole range of devices and not just a single device.</span></span>

<span data-ttu-id="6393e-120">Um modelo de conformidade do dispositivo é uma asserção de que um arquivo ASF contém dados codificados dentro de determinados parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6393e-120">A device conformance template is an assertion that an ASF file contains data encoded within certain parameters.</span></span> <span data-ttu-id="6393e-121">Para obter mais informações sobre as configurações apropriadas para os modelos individuais, consulte [parâmetros de modelo de conformidade do dispositivo](device-conformance-template-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6393e-121">For more information about the settings appropriate to the individual templates, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="6393e-122">Os seguintes codecs dão suporte a modelos de conformidade do dispositivo:</span><span class="sxs-lookup"><span data-stu-id="6393e-122">The following codecs support device conformance templates:</span></span>

-   <span data-ttu-id="6393e-123">Vídeo do Windows Media 9</span><span class="sxs-lookup"><span data-stu-id="6393e-123">Windows Media Video 9</span></span>
-   <span data-ttu-id="6393e-124">Windows Media Audio 9 e posterior</span><span class="sxs-lookup"><span data-stu-id="6393e-124">Windows Media Audio 9 and later</span></span>
-   <span data-ttu-id="6393e-125">Windows Media Audio 9 Professional e posterior</span><span class="sxs-lookup"><span data-stu-id="6393e-125">Windows Media Audio 9 Professional and later</span></span>
-   <span data-ttu-id="6393e-126">Voz do Windows Media Audio 9</span><span class="sxs-lookup"><span data-stu-id="6393e-126">Windows Media Audio 9 Voice</span></span>

<span data-ttu-id="6393e-127">Você não precisa executar nenhuma etapa especial para usar modelos de conformidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6393e-127">You do not need to take any special steps to use device conformance templates.</span></span> <span data-ttu-id="6393e-128">O codec grava automaticamente uma cadeia de caracteres de modelo para cada fluxo apropriado no arquivo.</span><span class="sxs-lookup"><span data-stu-id="6393e-128">The codec automatically writes a template string for each appropriate stream in the file.</span></span> <span data-ttu-id="6393e-129">O codec decidirá qual modelo usar, com base nas definições de configuração de fluxo no perfil.</span><span class="sxs-lookup"><span data-stu-id="6393e-129">The codec will decide which template to use, based on the stream configuration settings in the profile.</span></span> <span data-ttu-id="6393e-130">Há alguma sobreposição nos parâmetros do modelo de conformidade do dispositivo, portanto, convém solicitar um modelo específico em vez de permitir que o codec atribua um para você.</span><span class="sxs-lookup"><span data-stu-id="6393e-130">There is some overlap in device conformance template parameters, so you may want to request a specific template instead of letting the codec assign one for you.</span></span> <span data-ttu-id="6393e-131">Você pode especificar qual modelo deseja definindo a \_ Propriedade g wszDecoderComplexityRequested com os métodos da interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) do objeto de configuração de fluxo apropriado.</span><span class="sxs-lookup"><span data-stu-id="6393e-131">You can specify which template you want by setting the g\_wszDecoderComplexityRequested property with the methods of the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the appropriate stream configuration object.</span></span>

<span data-ttu-id="6393e-132">Quando um arquivo ASF é gravado, o modelo de conformidade do dispositivo real para cada fluxo é definido como o valor passado ao gravador pelo codec.</span><span class="sxs-lookup"><span data-stu-id="6393e-132">When an ASF file is written, the actual device conformance template for each stream is set to the value passed to the writer by the codec.</span></span> <span data-ttu-id="6393e-133">Ao abrir um arquivo para leitura, você pode descobrir em qual modelo os fluxos do arquivo estão em conformidade usando os métodos da interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) para recuperar o \_ atributo de nível de fluxo g wszDeviceConformanceTemplate.</span><span class="sxs-lookup"><span data-stu-id="6393e-133">When opening a file for reading, you can find out which template the streams of the file conform to by using the methods of the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface to retrieve the g\_wszDeviceConformanceTemplate stream-level attribute.</span></span> <span data-ttu-id="6393e-134">Para obter mais informações sobre atributos, consulte [trabalhando com metadados](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="6393e-134">For more information about attributes, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6393e-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6393e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6393e-136">**Criando perfis**</span><span class="sxs-lookup"><span data-stu-id="6393e-136">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="6393e-137">**Parâmetros do modelo de conformidade do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="6393e-137">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> </dl>

 

 




