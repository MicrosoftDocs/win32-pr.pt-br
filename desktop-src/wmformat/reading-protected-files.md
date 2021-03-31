---
title: Lendo arquivos protegidos
description: Lendo arquivos protegidos
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows Media Format SDK, lendo arquivos protegidos
- SDK do Windows Media Format, arquivos protegidos
- ASF (Advanced Systems Format), lendo arquivos protegidos
- ASF (formato de sistemas avançados), lendo arquivos protegidos
- ASF (Advanced Systems Format), arquivos protegidos
- ASF (formato de sistemas avançados), arquivos protegidos
- ASF (Advanced Systems Format), WMStubDRM. lib
- ASF (formato de sistemas avançados), WMStubDRM. lib
- WMStubDRM. lib, lendo arquivos protegidos
- WMStubDRM. lib, arquivos protegidos
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b2110708a28daae1e86ba3dac2ea1f18ad16fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640123"
---
# <a name="reading-protected-files"></a><span data-ttu-id="51bbc-115">Lendo arquivos protegidos</span><span class="sxs-lookup"><span data-stu-id="51bbc-115">Reading Protected Files</span></span>

<span data-ttu-id="51bbc-116">Ler um arquivo protegido por DRM ou um fluxo de rede basicamente envolve a tentativa de abrir o arquivo (ou conectar-se ao fluxo) e, em seguida, manipular quaisquer eventos que possam ser enviados dos componentes DRM.</span><span class="sxs-lookup"><span data-stu-id="51bbc-116">Reading a DRM-protected file or network stream basically involves attempting to open the file (or connect to the stream) and then handling any events that might be sent from the DRM components.</span></span>

<span data-ttu-id="51bbc-117">Se um player não estiver habilitado para DRM (não vincula a uma biblioteca wmstubdrm. lib válida), a chamada [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) falhará ao tentar abrir um arquivo protegido e retornará o conteúdo protegido do NS e \_ \_ \_ ou algum erro relacionado.</span><span class="sxs-lookup"><span data-stu-id="51bbc-117">If a player is not DRM-enabled (does not link to a valid wmstubdrm.lib library) the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) call fails when it tries to open a protected file and returns NS\_E\_PROTECTED\_CONTENT or some related error.</span></span>

<span data-ttu-id="51bbc-118">Quando um aplicativo habilitado para DRM tenta abrir um arquivo protegido por DRM, o componente DRM pesquisa automaticamente o sistema local em busca de uma licença válida.</span><span class="sxs-lookup"><span data-stu-id="51bbc-118">When a DRM-enabled application attempts to open a DRM-protected file, the DRM component automatically searches the local system for a valid license.</span></span> <span data-ttu-id="51bbc-119">Se um for encontrado, o componente DRM descriptografará automaticamente o arquivo de forma que seja completamente transparente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="51bbc-119">If one is found, the DRM component automatically decrypts the file in a way that is completely transparent to the application.</span></span> <span data-ttu-id="51bbc-120">A ação que um aplicativo pode executar no arquivo descriptografado depende dos direitos especificados na licença.</span><span class="sxs-lookup"><span data-stu-id="51bbc-120">The action that an application may perform on the decrypted file depends on the rights specified in the license.</span></span> <span data-ttu-id="51bbc-121">Para obter uma descrição completa dos possíveis direitos, consulte a documentação do SDK do Windows Media Rights Manager.</span><span class="sxs-lookup"><span data-stu-id="51bbc-121">For a full description of possible rights, see the Windows Media Rights Manager SDK documentation.</span></span>

<span data-ttu-id="51bbc-122">Se o aplicativo não tiver uma licença válida para um arquivo, o Player receberá uma notificação de status do componente DRM.</span><span class="sxs-lookup"><span data-stu-id="51bbc-122">If the application does not have a valid license for a file, the player receives a status notification from the DRM component.</span></span> <span data-ttu-id="51bbc-123">O aplicativo de player pode iniciar o processo de [*aquisição de licença*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="51bbc-123">The player application can then initiate the [*license acquisition*](wmformat-glossary.md) process.</span></span> <span data-ttu-id="51bbc-124">Depois que uma licença válida tiver sido recebida, o arquivo poderá ser acessado.</span><span class="sxs-lookup"><span data-stu-id="51bbc-124">After a valid license has been received, the file can be accessed.</span></span> <span data-ttu-id="51bbc-125">As seções a seguir descrevem as tarefas básicas que um aplicativo deve executar ao implementar o processo de aquisição de licença:</span><span class="sxs-lookup"><span data-stu-id="51bbc-125">The following sections describe the basic tasks that an application must perform in implementing the license acquisition process:</span></span>

-   [<span data-ttu-id="51bbc-126">Especificando as ações a serem executadas</span><span class="sxs-lookup"><span data-stu-id="51bbc-126">Specifying the Actions To Be Performed</span></span>](specifying-the-actions-to-be-performed.md)
-   [<span data-ttu-id="51bbc-127">Lidando com eventos de aquisição de licença</span><span class="sxs-lookup"><span data-stu-id="51bbc-127">Handling License Acquisition Events</span></span>](handling-license-acquisition-events.md)
-   [<span data-ttu-id="51bbc-128">Individualizando aplicativos DRM</span><span class="sxs-lookup"><span data-stu-id="51bbc-128">Individualizing DRM Applications</span></span>](individualizing-drm-applications.md)
-   [<span data-ttu-id="51bbc-129">Manipulando eventos de individualização</span><span class="sxs-lookup"><span data-stu-id="51bbc-129">Handling Individualization Events</span></span>](handling-individualization-events.md)

> [!Note]  
> <span data-ttu-id="51bbc-130">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="51bbc-130">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="51bbc-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="51bbc-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51bbc-132">**Recursos de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="51bbc-132">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="51bbc-133">**Lista de atributos DRM**</span><span class="sxs-lookup"><span data-stu-id="51bbc-133">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="51bbc-134">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="51bbc-134">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="51bbc-135">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="51bbc-135">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




