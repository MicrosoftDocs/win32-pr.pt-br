---
title: Requisitos para players de áudio portáteis aparecerem no Windows Explorer
description: Requisitos para players de áudio portáteis aparecerem no Windows Explorer
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Media Gerenciador de Dispositivos, players de áudio portáteis
- Gerenciador de Dispositivos, players de áudio portáteis
- Guia de programação, players de áudio portáteis
- provedores de serviços, players de áudio portáteis
- criando provedores de serviços, players de áudio portáteis
- players de áudio portáteis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a163bf04f4185bc1325aa12ea6acddd43191529
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105784929"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a><span data-ttu-id="bdb73-109">Requisitos para players de áudio portáteis aparecerem no Windows Explorer</span><span class="sxs-lookup"><span data-stu-id="bdb73-109">Requirements for Portable Audio Players to Appear in Windows Explorer</span></span>

<span data-ttu-id="bdb73-110">A extensão de namespace do Shell player de áudio portátil fornece aos usuários do Windows uma maneira consistente de gerenciar dispositivos de áudio gerenciados pelo Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="bdb73-110">The portable audio player shell namespace extension provides Windows users with a consistent way to manage audio devices that are managed by Windows Media Device Manager.</span></span> <span data-ttu-id="bdb73-111">Se você criar seu provedor de serviços e componentes de driver de acordo com as diretrizes a seguir, seu dispositivo será exibido no namespace do Shell.</span><span class="sxs-lookup"><span data-stu-id="bdb73-111">If you author your service provider and driver components according to the following guidelines, your device will show up in the shell namespace.</span></span> <span data-ttu-id="bdb73-112">Os usuários poderão interagir com o conteúdo do seu dispositivo de maneira consistente no Windows Explorer para executar operações básicas, como copiar, excluir e renomear.</span><span class="sxs-lookup"><span data-stu-id="bdb73-112">Users will be able to interact with the contents of your device in a consistent manner in Windows Explorer to perform basic operations such as copy, delete, and rename.</span></span>

<span data-ttu-id="bdb73-113">Os seguintes requisitos de Shell para o provedor de serviços e componentes de driver destinam-se a complementar as diretrizes gerais de Gerenciador de Dispositivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="bdb73-113">The following shell requirements for service provider and driver components are intended to supplement the general Windows Media Device Manager guidelines.</span></span>

<span data-ttu-id="bdb73-114">Funcionalidades do dispositivo</span><span class="sxs-lookup"><span data-stu-id="bdb73-114">Device Capabilities</span></span>

<span data-ttu-id="bdb73-115">Os provedores de serviços do Windows Media Gerenciador de Dispositivos devem ser explícitos em seus recursos com suporte.</span><span class="sxs-lookup"><span data-stu-id="bdb73-115">Windows Media Device Manager service providers should be explicit in their supported capabilities.</span></span> <span data-ttu-id="bdb73-116">Se não houver suporte para uma chamada, um código de erro deverá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="bdb73-116">If a call is not supported, an error code must be returned.</span></span> <span data-ttu-id="bdb73-117">Os campos apropriados devem ser definidos para a presença ou ausência de recursos no retorno das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="bdb73-117">The appropriate fields must be set for the presence or absence of capabilities on return from the following functions:</span></span>

-   [<span data-ttu-id="bdb73-118">**IMDSPStorageGlobals:: GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bdb73-118">**IMDSPStorageGlobals::GetCapabilities**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [<span data-ttu-id="bdb73-119">**IMDSPStorage:: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="bdb73-119">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [<span data-ttu-id="bdb73-120">**IMDSPDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="bdb73-120">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

<span data-ttu-id="bdb73-121">Os provedores de serviços devem dar suporte aos seguintes recursos para serem compatíveis com o Shell:</span><span class="sxs-lookup"><span data-stu-id="bdb73-121">Service providers must support the following capabilities to be compatible with the shell:</span></span>

-   <span data-ttu-id="bdb73-122">Copiar para o dispositivo (com suporte para retornos de chamada de cancelamento e progresso)</span><span class="sxs-lookup"><span data-stu-id="bdb73-122">Copy to device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="bdb73-123">Excluir arquivo do dispositivo (com suporte para retornos de chamada de cancelamento e progresso)</span><span class="sxs-lookup"><span data-stu-id="bdb73-123">Delete file from device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="bdb73-124">Renomear arquivo no dispositivo</span><span class="sxs-lookup"><span data-stu-id="bdb73-124">Rename file on device</span></span>
-   <span data-ttu-id="bdb73-125">Relatório de espaço (espaço total, espaço livre, espaço inutilizável)</span><span class="sxs-lookup"><span data-stu-id="bdb73-125">Space reporting (total space, free space, unusable space)</span></span>
-   <span data-ttu-id="bdb73-126">Plug and Play (consulte [habilitando PNP para dispositivos](enabling-pnp-for-devices.md))</span><span class="sxs-lookup"><span data-stu-id="bdb73-126">Plug and Play (see [Enabling PnP for Devices](enabling-pnp-for-devices.md))</span></span>
-   <span data-ttu-id="bdb73-127">Formato (preferencialmente com suporte para retornos de chamada de cancelamento e progresso)</span><span class="sxs-lookup"><span data-stu-id="bdb73-127">Format (preferably with support for cancel and progress callbacks)</span></span>

<span data-ttu-id="bdb73-128">Se houver suporte para metadados, os campos a seguir deverão ter suporte para arquivos individuais.</span><span class="sxs-lookup"><span data-stu-id="bdb73-128">If metadata is supported, the following fields must be supported for individual files.</span></span> <span data-ttu-id="bdb73-129">Se nenhum dado estiver disponível, o campo deverá ser inicializado como uma cadeia de caracteres vazia:</span><span class="sxs-lookup"><span data-stu-id="bdb73-129">If no data is available, the field should be initialized as an empty string:</span></span>



| <span data-ttu-id="bdb73-130">Campo</span><span class="sxs-lookup"><span data-stu-id="bdb73-130">Field</span></span>        | <span data-ttu-id="bdb73-131">Constante (definida em WMDM. idl)</span><span class="sxs-lookup"><span data-stu-id="bdb73-131">Constant (defined in WMDM.idl)</span></span> | <span data-ttu-id="bdb73-132">Marca de metadados</span><span class="sxs-lookup"><span data-stu-id="bdb73-132">Metadata tag</span></span>    |
|--------------|--------------------------------|-----------------|
| <span data-ttu-id="bdb73-133">Título da música</span><span class="sxs-lookup"><span data-stu-id="bdb73-133">Song Title</span></span>   | <span data-ttu-id="bdb73-134">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="bdb73-134">g\_wszWMDMTitle</span></span>                | <span data-ttu-id="bdb73-135">WMDM/título</span><span class="sxs-lookup"><span data-stu-id="bdb73-135">WMDM/Title</span></span>      |
| <span data-ttu-id="bdb73-136">Número da faixa</span><span class="sxs-lookup"><span data-stu-id="bdb73-136">Track Number</span></span> | <span data-ttu-id="bdb73-137">g \_ wszWMDMTrack</span><span class="sxs-lookup"><span data-stu-id="bdb73-137">g\_wszWMDMTrack</span></span>                | <span data-ttu-id="bdb73-138">WMDM/faixa</span><span class="sxs-lookup"><span data-stu-id="bdb73-138">WMDM/Track</span></span>      |
| <span data-ttu-id="bdb73-139">Autor</span><span class="sxs-lookup"><span data-stu-id="bdb73-139">Artist</span></span>       | <span data-ttu-id="bdb73-140">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="bdb73-140">g\_wszWMDMAuthor</span></span>               | <span data-ttu-id="bdb73-141">WMDM/autor</span><span class="sxs-lookup"><span data-stu-id="bdb73-141">WMDM/Author</span></span>     |
| <span data-ttu-id="bdb73-142">Álbuns</span><span class="sxs-lookup"><span data-stu-id="bdb73-142">Album</span></span>        | <span data-ttu-id="bdb73-143">g \_ wszWMDMAlbumTitle</span><span class="sxs-lookup"><span data-stu-id="bdb73-143">g\_wszWMDMAlbumTitle</span></span>           | <span data-ttu-id="bdb73-144">WMDM/campos AlbumTitle</span><span class="sxs-lookup"><span data-stu-id="bdb73-144">WMDM/AlbumTitle</span></span> |
| <span data-ttu-id="bdb73-145">Year</span><span class="sxs-lookup"><span data-stu-id="bdb73-145">Year</span></span>         | <span data-ttu-id="bdb73-146">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="bdb73-146">g\_wszWMDMYear</span></span>                 | <span data-ttu-id="bdb73-147">WMDM/ano</span><span class="sxs-lookup"><span data-stu-id="bdb73-147">WMDM/Year</span></span>       |
| <span data-ttu-id="bdb73-148">Gênero</span><span class="sxs-lookup"><span data-stu-id="bdb73-148">Genre</span></span>        | <span data-ttu-id="bdb73-149">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="bdb73-149">g\_wszWMDMGenre</span></span>                | <span data-ttu-id="bdb73-150">WMDM/gênero</span><span class="sxs-lookup"><span data-stu-id="bdb73-150">WMDM/Genre</span></span>      |



 

<span data-ttu-id="bdb73-151">Simultaneidade</span><span class="sxs-lookup"><span data-stu-id="bdb73-151">Concurrency</span></span>

<span data-ttu-id="bdb73-152">Os drivers de modo kernel para Windows Media Gerenciador de Dispositivos precisam ser robustos para lidar com o acesso simultâneo.</span><span class="sxs-lookup"><span data-stu-id="bdb73-152">Kernel mode drivers for Windows Media Device Manager need to be robust in handling concurrent access.</span></span> <span data-ttu-id="bdb73-153">Por exemplo, um usuário pode acessar simultaneamente o dispositivo por meio do Shell e do Media Player ou simplesmente por meio de várias janelas no Shell.</span><span class="sxs-lookup"><span data-stu-id="bdb73-153">For example, a user can be concurrently accessing the device through both the shell and media player or simply through multiple windows in the shell.</span></span> <span data-ttu-id="bdb73-154">Como parte do tratamento de simultaneidade, os drivers não devem assumir, apenas porque o provedor de serviços está carregado, se o dispositivo está em uso.</span><span class="sxs-lookup"><span data-stu-id="bdb73-154">As part of handling concurrency, drivers should not assume, just because the service provider is loaded, that the device is in use.</span></span> <span data-ttu-id="bdb73-155">Em vez disso, eles devem implementar um mecanismo de bloqueio para serializar o acesso ao dispositivo, conforme necessário, para operações individuais.</span><span class="sxs-lookup"><span data-stu-id="bdb73-155">Instead, they should implement a locking mechanism to serialize access to the device as needed for individual operations.</span></span>

<span data-ttu-id="bdb73-156">Interface do usuário</span><span class="sxs-lookup"><span data-stu-id="bdb73-156">UI</span></span>

<span data-ttu-id="bdb73-157">Os provedores de serviço para Windows Media Gerenciador de Dispositivos não devem mostrar nenhuma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="bdb73-157">Service providers for Windows Media Device Manager should not show any user interface.</span></span> <span data-ttu-id="bdb73-158">Todos os erros devem ser retornados de chamadas de método como códigos de erro específicos do Windows Media Gerenciador de Dispositivos sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="bdb73-158">Any errors should be returned from method calls as specific Windows Media Device Manager error codes whenever possible.</span></span>

<span data-ttu-id="bdb73-159">Habilitando no Shell</span><span class="sxs-lookup"><span data-stu-id="bdb73-159">Enabling in the Shell</span></span>

<span data-ttu-id="bdb73-160">Se o pacote atender a todos os requisitos de Shell, você poderá habilitar seu dispositivo para ser mostrado no Shell definindo o valor *ShowInShell* como 1 nos parâmetros do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bdb73-160">If your package meets all of the shell requirements, you can enable your device to be shown in the shell by setting the *ShowInShell* value to 1 under the device parameters.</span></span> <span data-ttu-id="bdb73-161">Para obter mais informações, consulte [parâmetros do dispositivo](device-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bdb73-161">For more information, see [Device Parameters](device-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdb73-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bdb73-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdb73-163">**Criando um provedor de serviços**</span><span class="sxs-lookup"><span data-stu-id="bdb73-163">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




