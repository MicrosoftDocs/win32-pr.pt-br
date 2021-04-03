---
title: Aquisição de licença silenciosa
description: Aquisição de licença silenciosa
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- SDK do Windows Media Format, aquisição de licença silenciosa
- SDK do Windows Media Format, licenças
- DRM (gerenciamento de direitos digitais), aquisição de licença silenciosa
- DRM (gerenciamento de direitos digitais), aquisição de licença silenciosa
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- APIs estendidas do cliente DRM, aquisição de licença silenciosa
- APIs estendidas do cliente, aquisição de licença silenciosa
- aquisição de licença silenciosa
- licenças, aquisição de licença silenciosa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ef92eaf4e347e8eb30f56c1111ec5b27f1e62d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005806"
---
# <a name="silent-license-acquisition"></a><span data-ttu-id="44664-113">Aquisição de licença silenciosa</span><span class="sxs-lookup"><span data-stu-id="44664-113">Silent License Acquisition</span></span>

<span data-ttu-id="44664-114">A aquisição de licença silenciosa requer apenas uma chamada de método única que manipule todas as comunicações de rede com o servidor de licença de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="44664-114">Silent license acquisition requires only a single method call that handles all of the network communications with the license server asynchronously.</span></span>

<span data-ttu-id="44664-115">Esse tipo de aquisição de licença geralmente é usado como uma resposta ao usuário final que está tentando acessar o conteúdo protegido — por exemplo, tentar reproduzir um arquivo protegido em um aplicativo de player de mídia.</span><span class="sxs-lookup"><span data-stu-id="44664-115">This type of license acquisition is usually used as a response to the end user trying to access protected content—for example, trying to play a protected file in a media player application.</span></span> <span data-ttu-id="44664-116">Como a aquisição de licença silenciosa Obtém a licença com uma única chamada, ela não pode ser usada se forem necessárias entradas adicionais do usuário, como o pagamento do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="44664-116">Because silent license acquisition gets the license with a single call, it cannot be used if additional input from the user, such as payment for the content, is required.</span></span>

<span data-ttu-id="44664-117">Para executar a aquisição de licença silenciosa, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="44664-117">To perform silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="44664-118">Chame o método [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="44664-118">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="44664-119">Passe o cabeçalho DRM do arquivo protegido como o parâmetro *bstrHeaderData* .</span><span class="sxs-lookup"><span data-stu-id="44664-119">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="44664-120">Especifique quais direitos você deseja que a licença conceda no parâmetro *bstrActions* .</span><span class="sxs-lookup"><span data-stu-id="44664-120">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="44664-121">Por fim, defina o parâmetro *dwFlags* como WMDRM \_ adquirir \_ licença \_ silenciosa.</span><span class="sxs-lookup"><span data-stu-id="44664-121">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_SILENT.</span></span>
2.  <span data-ttu-id="44664-122">Interceptar eventos para a interface [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) .</span><span class="sxs-lookup"><span data-stu-id="44664-122">Trap events for the [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span> <span data-ttu-id="44664-123">Ao receber o evento **MEWMDRMLicenseAcquisitionCompleted** , verifique seu código de retorno chamando o método **IMFMediaEvent:: GetStatus** , que está documentado na documentação do Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="44664-123">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, check its return code by calling the **IMFMediaEvent::GetStatus** method, which is documented in the Media Foundation documentation.</span></span> <span data-ttu-id="44664-124">Se o valor **HRESULT** recuperado for um código de êxito, a licença foi baixada com êxito e estará no repositório de licenças local pronto para uso.</span><span class="sxs-lookup"><span data-stu-id="44664-124">If the retrieved **HRESULT** value is a success code, then the license was successfully downloaded and is in the local license store ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44664-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44664-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44664-126">**Adquirindo licenças**</span><span class="sxs-lookup"><span data-stu-id="44664-126">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="44664-127">**Usando o modelo de evento Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="44664-127">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 




