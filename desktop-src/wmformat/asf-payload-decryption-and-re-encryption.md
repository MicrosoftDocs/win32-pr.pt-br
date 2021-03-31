---
title: Descriptografia de carga ASF e recriptografação
description: Descriptografia de carga ASF e recriptografação
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- SDK do Windows Media Format, descriptografia e recriptografia de conteúdo ASF
- Windows Media Format SDK, descriptografia de carga e nova criptografia
- SDK do Windows Media Format, descriptografia
- SDK do Windows Media Format, nova criptografia
- DRM (gerenciamento de direitos digitais), descriptografia de conteúdo ASF e nova criptografia
- DRM (gerenciamento de direitos digitais), descriptografia e descriptografia de conteúdo ASF
- DRM (gerenciamento de direitos digitais), descriptografia de carga e nova criptografia
- DRM (gerenciamento de direitos digitais), descriptografia de carga e nova criptografia
- DRM (gerenciamento de direitos digitais), descriptografia
- DRM (gerenciamento de direitos digitais), descriptografia
- DRM (gerenciamento de direitos digitais), nova criptografia
- DRM (gerenciamento de direitos digitais), nova criptografia
- APIs estendidas do cliente DRM, descriptografia e descriptografia de carga ASF
- APIs estendidas do cliente, descriptografia de carga ASF e recriptografia
- APIs estendidas do cliente DRM, descriptografia de carga e nova criptografia
- APIs estendidas do cliente, descriptografia de carga e nova criptografia
- APIs estendidas do cliente DRM, descriptografia
- APIs estendidas do cliente, descriptografia
- APIs estendidas do cliente DRM, nova criptografia
- APIs estendidas do cliente, nova criptografia
- ASF (Advanced Systems Format), nova criptografia
- ASF (formato de sistemas avançados), nova criptografia
- ASF (Advanced Systems Format), descriptografia
- ASF (formato de sistemas avançados), descriptografia
- ASF (Advanced Systems Format), descriptografia de carga e nova criptografia
- ASF (formato de sistemas avançados), descriptografia de carga e nova criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c6dcab1d483b737b6b05636b51b8af0502350
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635024"
---
# <a name="asf-payload-decryption-and-re-encryption"></a><span data-ttu-id="4a479-129">Descriptografia de carga ASF e recriptografação</span><span class="sxs-lookup"><span data-stu-id="4a479-129">ASF Payload Decryption and Re-encryption</span></span>

<span data-ttu-id="4a479-130">As etapas a seguir descrevem as ações que um aplicativo deve concluir para descriptografar e criptografar novamente cada carga:</span><span class="sxs-lookup"><span data-stu-id="4a479-130">The steps below describe the actions that an application must complete to decrypt and re-encrypt each payload:</span></span>

1.  <span data-ttu-id="4a479-131">Incrementar o valor de Salt.</span><span class="sxs-lookup"><span data-stu-id="4a479-131">Increment the salt value.</span></span>
2.  <span data-ttu-id="4a479-132">Passe a carga (criptografada com o DRM do Windows Media) e o valor de Salt para a função de descriptografia, [**IWMDRMDecrypt::D ecrypt**](iwmdrmdecrypt-decrypt.md), que retornará a carga, criptografada usando a chave pública RC4.</span><span class="sxs-lookup"><span data-stu-id="4a479-132">Pass the payload (encrypted with Windows Media DRM) and the salt value to the decryption function, [**IWMDRMDecrypt::Decrypt**](iwmdrmdecrypt-decrypt.md), which will return the payload, encrypted using the RC4 public key.</span></span>
3.  <span data-ttu-id="4a479-133">Derive uma chave RC4 transitória aplicando um hash SHA-1 do vetor de inicialização concatenado com o valor Salt.</span><span class="sxs-lookup"><span data-stu-id="4a479-133">Derive a transitory RC4 key by applying an SHA-1 hash of the initialization vector concatenated with the salt value.</span></span>
4.  <span data-ttu-id="4a479-134">Use sua chave transitória para descriptografar a carga.</span><span class="sxs-lookup"><span data-stu-id="4a479-134">Use your transitory key to decrypt the payload.</span></span>
5.  <span data-ttu-id="4a479-135">Criptografar imediatamente a carga com o esquema de proteção de conteúdo autorizado de acordo com as regras de conformidade e de robustez de exportação do Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="4a479-135">Immediately re-encrypt the payload with the authorized content protection scheme according to the Windows Media DRM export compliance and robustness rules.</span></span>
6.  <span data-ttu-id="4a479-136">Localize a carga seguinte.</span><span class="sxs-lookup"><span data-stu-id="4a479-136">Locate the next payload.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a479-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a479-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a479-138">**Exportando conteúdo compactado**</span><span class="sxs-lookup"><span data-stu-id="4a479-138">**Exporting Compressed Content**</span></span>](exporting-compressed-content.md)
</dt> </dl>

 

 




