---
title: Manipulando eventos de individualização
description: Manipulando eventos de individualização
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- SDK do Windows Media Format, tratando eventos de individualização
- SDK do Windows Media Format, eventos de individualização
- ASF (Advanced Systems Format), tratando eventos de individualização
- ASF (formato de sistemas avançados), tratando eventos de individualização
- ASF (Advanced Systems Format), eventos de individualização
- ASF (formato de sistemas avançados), eventos de individualização
- DRM (gerenciamento de direitos digitais), tratando eventos de individualização
- DRM (gerenciamento de direitos digitais), manipulação de eventos de individualização
- DRM (gerenciamento de direitos digitais), eventos de individualização
- DRM (gerenciamento de direitos digitais), eventos de individualização
- eventos de individualização
- eventos, eventos de individualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e74df94bf871ec62ec2acb94658785969812640
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105761047"
---
# <a name="handling-individualization-events"></a><span data-ttu-id="3dd40-115">Manipulando eventos de individualização</span><span class="sxs-lookup"><span data-stu-id="3dd40-115">Handling Individualization Events</span></span>

<span data-ttu-id="3dd40-116">Quando um aplicativo habilitado para DRM tenta abrir um arquivo protegido, o componente DRM examina o atributo [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) no arquivo, que especifica o nível mínimo de versão necessário para acessar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3dd40-116">When a DRM-enabled application attempts to open a protected file, the DRM component examines the [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md) attribute in the file, which specifies the minimum version level required to access the content.</span></span> <span data-ttu-id="3dd40-117">Todos os níveis do componente DRM funcionam com todas as versões 7,0 e posteriores do Windows Media Player e do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="3dd40-117">All levels of the DRM component work with all 7.0 and later versions of Windows Media Player and the Windows Media Format SDK.</span></span> <span data-ttu-id="3dd40-118">Se o nível de versão individual do componente DRM for menor do que a versão necessária, o componente DRM enviará um evento de **\_ \_ individualização de WMT precisará** para o método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3dd40-118">If the DRM component's individualized version level is lower than the required version, the DRM component will send a **WMT\_NEEDS\_INDIVIDUALIZATION** event to the application's [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="3dd40-119">O aplicativo deve exibir uma mensagem ou caixa de diálogo solicitando que os usuários iniciem ou cancelem a atualização de segurança.</span><span class="sxs-lookup"><span data-stu-id="3dd40-119">The application must then display a message or dialog box prompting users to either start or cancel the security upgrade.</span></span> <span data-ttu-id="3dd40-120">Esse prompt é necessário porque, por motivos de privacidade, os usuários devem conceder sua permissão antes que uma atualização de segurança seja instalada em seu computador.</span><span class="sxs-lookup"><span data-stu-id="3dd40-120">This prompt is necessary because, for privacy reasons, users must give their permission before a security upgrade is installed on their computer.</span></span>

> [!Note]  
> <span data-ttu-id="3dd40-121">O cabeçalho do conteúdo especifica apenas os dois primeiros dígitos para DRM \_ DRMVersion \_ IndividualizedVersion.</span><span class="sxs-lookup"><span data-stu-id="3dd40-121">The header of the content specifies only the first two digits for DRM\_DRMVersion\_IndividualizedVersion.</span></span> <span data-ttu-id="3dd40-122">Em outras palavras, para exigir um componente 2.2.0.1 DRM de nível, o cabeçalho conterá "2,2".</span><span class="sxs-lookup"><span data-stu-id="3dd40-122">In other words, to require a level 2.2.0.1 DRM component, the header would contain "2.2".</span></span>

 

<span data-ttu-id="3dd40-123">Para iniciar a atualização de segurança e/ou disparar a individualização, chame o método [**IWMDRMReader:: individual**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) com o parâmetro *dwFlags* definido como 1.</span><span class="sxs-lookup"><span data-stu-id="3dd40-123">To start the security upgrade and/or trigger individualization, call the [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) method with the *dwFlags* parameter set to 1.</span></span>

<span data-ttu-id="3dd40-124">Você deve manipular o **evento \_ individual WMT** em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3dd40-124">You must handle the **WMT\_INDIVIDUALIZE** event in your application.</span></span> <span data-ttu-id="3dd40-125">Esse evento será acionado várias vezes pelo componente DRM com o status do processo de individualização indicado *no parâmetro atingir* , que é convertido em um ponteiro para uma estrutura de [**\_ \_ status individual do WM**](wm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="3dd40-125">This event will be fired multiple times by the DRM component with the status of the individualization process indicated in the *pValue* parameter, which is cast to a pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

<span data-ttu-id="3dd40-126">Depois que o componente DRM for individualizado com êxito, o aplicativo receberá um evento **WMT \_ no \_ Rights \_ ex** , indicando que o aplicativo agora pode continuar a adquirir uma licença para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3dd40-126">After the DRM component is successfully individualized, the application will receive a **WMT\_NO\_RIGHTS\_EX** event, indicating that the application can now proceed to acquire a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="3dd40-127">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="3dd40-127">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3dd40-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3dd40-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dd40-129">**Lidando com eventos de aquisição de licença**</span><span class="sxs-lookup"><span data-stu-id="3dd40-129">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> <dt>

[<span data-ttu-id="3dd40-130">**Individualizando aplicativos DRM**</span><span class="sxs-lookup"><span data-stu-id="3dd40-130">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> <dt>

[<span data-ttu-id="3dd40-131">**Interface IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="3dd40-131">**IWMDRMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




