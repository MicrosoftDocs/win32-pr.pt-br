---
title: Exportando conteúdo compactado
description: Exportando conteúdo compactado
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- SDK do Windows Media Format, exportação de DRM
- SDK do Windows Media Format, exportar
- SDK do Windows Media Format, conteúdo compactado
- DRM (gerenciamento de direitos digitais), exportar
- DRM (gerenciamento de direitos digitais), exportar
- DRM (gerenciamento de direitos digitais), conteúdo compactado
- DRM (gerenciamento de direitos digitais), conteúdo compactado
- APIs estendidas do cliente DRM, conteúdo compactado
- APIs estendidas do cliente, conteúdo compactado
- APIs estendidas do cliente DRM, exportar
- APIs estendidas do cliente, exportar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37781d5575dbffb7103f07307a149f4bd5e9e4fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822519"
---
# <a name="exporting-compressed-content"></a><span data-ttu-id="d5de9-114">Exportando conteúdo compactado</span><span class="sxs-lookup"><span data-stu-id="d5de9-114">Exporting Compressed Content</span></span>

<span data-ttu-id="d5de9-115">Esta seção descreve como exportar mídia protegida por DRM do Windows Media em um arquivo do Windows Media onde o aplicativo recebe dados de mídia digital compactados.</span><span class="sxs-lookup"><span data-stu-id="d5de9-115">This section describes exporting Windows Media DRM protected media on a Windows Media file where the application receives compressed digital media data.</span></span> <span data-ttu-id="d5de9-116">Para fazer isso, seu aplicativo deve executar a descriptografia embutida de todos os conteúdos criptografados do DRM do Windows Media em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="d5de9-116">To do this, your application must perform inline decryption of all Windows Media DRM encrypted payloads in an ASF file.</span></span>

> [!Note]  
> <span data-ttu-id="d5de9-117">Uma biblioteca de análise de ASF é fornecida a você como parte do contrato de exportação do DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d5de9-117">An ASF parsing library is supplied to you as part of the Windows Media DRM Export agreement.</span></span>

 

<span data-ttu-id="d5de9-118">As principais etapas envolvidas na exportação de conteúdo compactado são:</span><span class="sxs-lookup"><span data-stu-id="d5de9-118">The primary steps involved in exporting compressed content are:</span></span>

1.  <span data-ttu-id="d5de9-119">Execute a individualização de DRM, se necessário.</span><span class="sxs-lookup"><span data-stu-id="d5de9-119">Perform DRM individualization, if needed.</span></span>
2.  <span data-ttu-id="d5de9-120">Verifique se o esquema de proteção de conteúdo de destino é explicitamente permitido.</span><span class="sxs-lookup"><span data-stu-id="d5de9-120">Verify that the target content protection scheme is explicitly permitted.</span></span>
3.  <span data-ttu-id="d5de9-121">Crie um objeto de descriptografia para descriptografar cada carga de ASF.</span><span class="sxs-lookup"><span data-stu-id="d5de9-121">Create a decryptor object to decrypt each ASF payload.</span></span>
4.  <span data-ttu-id="d5de9-122">O sistema DRM criptografa cada carga ASF do Windows Media DRM em RC4 antes de passá-la para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5de9-122">The DRM system transcrypts each ASF payload from Windows Media DRM into RC4 before passing it to your application.</span></span>

<span data-ttu-id="d5de9-123">Se o seu aplicativo alterar o tamanho de uma carga ASF durante a transformação, você também deverá remultiplexar o arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="d5de9-123">If your application changes the size of an ASF payload during transcryption, you must also remultiplex the ASF file.</span></span>

<span data-ttu-id="d5de9-124">Passe para a biblioteca de stub um certificado de aplicativo de exportação do Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="d5de9-124">Pass to the stub library a Windows Media DRM Export Application Certificate.</span></span> <span data-ttu-id="d5de9-125">O certificado é verificado e, se for válido, o sistema DRM gerará um vetor de inicialização e o criptografará usando o RSA OAEP.</span><span class="sxs-lookup"><span data-stu-id="d5de9-125">The certificate is verified, and if it is valid, the DRM system generates an initialization vector and encrypts it using RSA OAEP.</span></span>

-   <span data-ttu-id="d5de9-126">Uma chave de sessão RC4 é criada para cada carga concatenando o vetor de inicialização e um valor Salt.</span><span class="sxs-lookup"><span data-stu-id="d5de9-126">An RC4 session key is created for each payload by concatenating the initialization vector and a salt value.</span></span> <span data-ttu-id="d5de9-127">Você fornece o valor salt para a API de descriptografia, e você deve incrementar isso por um valor inteiro positivo diferente de zero para cada carga.</span><span class="sxs-lookup"><span data-stu-id="d5de9-127">You supply the salt value to the decryption API, and you must increment it by a positive non-zero integer value for each payload.</span></span>

<span data-ttu-id="d5de9-128">Você receberá uma ferramenta da Microsoft como parte do contrato de exportação do DRM do Windows Media que lhe permitirá gerar seu próprio par de chaves pública/privada RSA.</span><span class="sxs-lookup"><span data-stu-id="d5de9-128">You will be provided a tool by Microsoft as part of the Windows Media DRM export agreement that will enable you to generate your own RSA public/private key pair.</span></span> <span data-ttu-id="d5de9-129">Você enviará a chave pública para a Microsoft, na qual a Microsoft irá incorporá-la em um certificado de aplicativo DRM do Windows Media assinado e retorná-la.</span><span class="sxs-lookup"><span data-stu-id="d5de9-129">You will send the public key to Microsoft, where Microsoft will incorporate it into a signed Windows Media DRM Application Certificate, and return it.</span></span>

<span data-ttu-id="d5de9-130">Cada carga, depois de ser descriptografada usando a chave de descriptografia RC4, deve ser imediatamente criptografada no CPS de saída.</span><span class="sxs-lookup"><span data-stu-id="d5de9-130">Each payload, after it is decrypted using the RC4 decryption key, must be immediately encrypted into the output CPS.</span></span> <span data-ttu-id="d5de9-131">Há outras restrições sobre o tratamento de cargas não criptografadas que são descritas nas regras de robustez e de conformidade, que acompanham o contrato de exportação do DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d5de9-131">There are other restrictions on handling of unencrypted payloads that are outlined in the robustness and compliance rules, which accompany the Windows Media DRM Export agreement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5de9-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5de9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5de9-133">**Descriptografia de carga ASF e recriptografação**</span><span class="sxs-lookup"><span data-stu-id="d5de9-133">**ASF Payload Decryption and Re-encryption**</span></span>](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[<span data-ttu-id="d5de9-134">**Exportação de DRM**</span><span class="sxs-lookup"><span data-stu-id="d5de9-134">**DRM Export**</span></span>](drm-export.md)
</dt> <dt>

[<span data-ttu-id="d5de9-135">**Executando individualização de DRM**</span><span class="sxs-lookup"><span data-stu-id="d5de9-135">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> <dt>

[<span data-ttu-id="d5de9-136">**Verificação e inicialização**</span><span class="sxs-lookup"><span data-stu-id="d5de9-136">**Verification and Initialization**</span></span>](verification-and-initialization.md)
</dt> </dl>

 

 




