---
title: Manipulando conteúdo protegido no provedor de serviços
description: Manipulando conteúdo protegido no provedor de serviços
ms.assetid: 5c18c8ec-d579-41df-8c25-c143fb9cdbef
keywords:
- Gerenciador de Dispositivos de mídia do Windows, certificados
- Gerenciador de Dispositivos, certificados
- Guia de programação, certificados
- provedores de serviços, certificados
- criando provedores de serviços, certificados
- certificates
- Windows Media Gerenciador de Dispositivos, conteúdo protegido por DRM
- Gerenciador de Dispositivos, conteúdo protegido por DRM
- Guia de programação, conteúdo protegido por DRM
- provedores de serviços, conteúdo protegido por DRM
- criando provedores de serviços, conteúdo protegido por DRM
- Conteúdo protegido por DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d10cf9078cf9aaf631b65de968f01491a97781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105770536"
---
# <a name="handling-protected-content-in-the-service-provider"></a><span data-ttu-id="a31af-115">Manipulando conteúdo protegido no provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="a31af-115">Handling Protected Content in the Service Provider</span></span>

<span data-ttu-id="a31af-116">Você pode criar um provedor de serviços que possa enviar conteúdo protegido por DRM para um dispositivo criado em DRM (PDDRM) de dispositivo portátil, mas não é possível criar um provedor de serviços que possa enviar conteúdo protegido por DRM para dispositivos criados no Windows Media DRM 10 para dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="a31af-116">You can build a service provider that can send DRM-protected content to a device built on Portable Device DRM (PDDRM), but you cannot build a service provider that can send DRM-protected content to devices built on Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="a31af-117">Esses dispositivos usam MTP e você não pode criar seu próprio provedor de serviços do MTP.</span><span class="sxs-lookup"><span data-stu-id="a31af-117">These devices use MTP, and you cannot build your own MTP service provider.</span></span>

<span data-ttu-id="a31af-118">A única etapa extra que um provedor de serviços deve executar para enviar material DRM para um dispositivo PDDRM é obter um par certificado/chave emitido pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a31af-118">The only extra step that a service provider must take to send DRM material to a PDDRM device is to get a Microsoft-issued certificate/key pair.</span></span> <span data-ttu-id="a31af-119">Consulte [ferramentas para desenvolvimento](tools-for-development.md) para saber onde obter esse certificado/chave.</span><span class="sxs-lookup"><span data-stu-id="a31af-119">See [Tools for Development](tools-for-development.md) to learn where to get this certificate/key.</span></span> <span data-ttu-id="a31af-120">As licenças emitidas para esses dispositivos serão licenças simplificadas que oferecem suporte apenas à reprodução simples de conteúdo comprado; Eles não oferecerão suporte a licenças de expiração de tempo.</span><span class="sxs-lookup"><span data-stu-id="a31af-120">The licenses issued to these devices will be simplified licenses that only support simple playback of purchased content; they will not support time-expiring licenses.</span></span> <span data-ttu-id="a31af-121">Essa licença será criada para você pelo provedor de conteúdo seguro (fornecido pela Microsoft para arquivos WMA/WMV) e armazenada no cabeçalho do arquivo enviado para o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="a31af-121">This license will be created for you by the secure content provider (provided by Microsoft for WMA/WMV files) and stored in the header of the file sent to the service provider.</span></span> <span data-ttu-id="a31af-122">Você não precisará executar nenhuma etapa especial para arquivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="a31af-122">You will not have to take any special steps for protected files.</span></span>

<span data-ttu-id="a31af-123">Depois de enviar o arquivo protegido, o Windows Media Gerenciador de Dispositivos chamará o provedor de serviços para solicitar um arquivo de armazenamento de licença especial do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a31af-123">After sending the protected file, Windows Media Device Manager will call the service provider to request a special license storage file from the device.</span></span> <span data-ttu-id="a31af-124">O Windows Media Gerenciador de Dispositivos adicionará uma cópia da nova licença a esse arquivo e a retornará ao provedor de serviços para enviar de volta para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a31af-124">Windows Media Device Manager will add a copy of the new license to this file, and return it to the service provider to send back to the device.</span></span> <span data-ttu-id="a31af-125">No entanto, mesmo que o provedor de serviços não consiga localizar ou retornar esse arquivo, o dispositivo ainda deve ser capaz de reproduzir o arquivo protegido usando a cópia de licença no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a31af-125">However, even if the service provider fails to find or return this file, the device should still be able to play the protected file by using the license copy in the file header.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a31af-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a31af-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a31af-127">**Criando um provedor de serviços**</span><span class="sxs-lookup"><span data-stu-id="a31af-127">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="a31af-128">**Lidando com conteúdo protegido**</span><span class="sxs-lookup"><span data-stu-id="a31af-128">**Handling Protected Content**</span></span>](handling-protected-content.md)
</dt> </dl>

 

 




