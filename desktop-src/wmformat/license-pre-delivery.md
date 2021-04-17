---
title: Pré-entrega de licença
description: Pré-entrega de licença
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- SDK do Windows Media Format, pré-entrega de licenças
- SDK do Windows Media Format, licenças
- DRM (gerenciamento de direitos digitais), pré-entrega de licenças
- DRM (gerenciamento de direitos digitais), pré-entrega de licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- APIs estendidas do cliente DRM, pré-entrega de licenças
- APIs estendidas do cliente, pré-entrega de licenças
- pré-entrega de licenças
- licenças, pré-entrega de licenças
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105755907"
---
# <a name="license-pre-delivery"></a><span data-ttu-id="7dc40-113">Pré-entrega de licença</span><span class="sxs-lookup"><span data-stu-id="7dc40-113">License Pre-Delivery</span></span>

<span data-ttu-id="7dc40-114">A pré-entrega de licença é o processo usado para efetuar pull de licenças para um computador cliente preemptivo.</span><span class="sxs-lookup"><span data-stu-id="7dc40-114">License pre-delivery is the process used to pull licenses to a client computer preemptively.</span></span> <span data-ttu-id="7dc40-115">Um cenário comum para usar a pré-entrega é quando um usuário assina um serviço de música.</span><span class="sxs-lookup"><span data-stu-id="7dc40-115">A common scenario for using pre-delivery is when a user subscribes to a music service.</span></span> <span data-ttu-id="7dc40-116">Sem o fornecimento de licenças antes que elas sejam necessárias, o usuário precisa aguardar a aquisição de licença para cada nova música.</span><span class="sxs-lookup"><span data-stu-id="7dc40-116">Without delivering licenses before they are needed, the user would have to wait for license acquisition for each new song.</span></span>

<span data-ttu-id="7dc40-117">Como a pré-entrega não é feita como uma resposta à tentativa de acesso, ela normalmente é executada apenas pelo proprietário do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7dc40-117">Because pre-delivery is not done as a response to attempted access, it is typically performed only by the content owner.</span></span> <span data-ttu-id="7dc40-118">Ou seja, você só pode entregar licenças previamente para o conteúdo que você controla.</span><span class="sxs-lookup"><span data-stu-id="7dc40-118">That is, you can only pre-deliver licenses for content that you control.</span></span> <span data-ttu-id="7dc40-119">O processo de pré-entrega é uma coordenação entre um componente de cliente e um servidor de licença criado usando os objetos do SDK do Windows Media Digital Rights Management.</span><span class="sxs-lookup"><span data-stu-id="7dc40-119">The pre-delivery process is a coordination between a client component and a license server built by using the objects of the Windows Media Digital Rights Management SDK.</span></span>

<span data-ttu-id="7dc40-120">A pré-entrega de licença é semelhante à [aquisição de licença não silenciosa](non-silent-license-acquisition.md).</span><span class="sxs-lookup"><span data-stu-id="7dc40-120">License pre-delivery is similar to [Non-Silent License Acquisition](non-silent-license-acquisition.md).</span></span> <span data-ttu-id="7dc40-121">Siga as mesmas etapas, exceto que você não tem um cabeçalho DRM para passar para [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md).</span><span class="sxs-lookup"><span data-stu-id="7dc40-121">Follow the same steps, except that you don't have a DRM header to pass to [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md).</span></span> <span data-ttu-id="7dc40-122">O método gerará um desafio que não é específico de conteúdo que você pode enviar para o servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="7dc40-122">The method will generate a challenge that is not content-specific that you can send to your license server.</span></span>

<span data-ttu-id="7dc40-123">Como alternativa, você pode usar o [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) para entregar licenças previamente.</span><span class="sxs-lookup"><span data-stu-id="7dc40-123">Alternatively you can use the [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) to pre-deliver licenses.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7dc40-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7dc40-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dc40-125">**Adquirindo licenças**</span><span class="sxs-lookup"><span data-stu-id="7dc40-125">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="7dc40-126">**Usando o modelo de evento Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="7dc40-126">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 