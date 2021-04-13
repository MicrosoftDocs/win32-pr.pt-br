---
title: Criptografando e importando amostras de mídia
description: Criptografando e importando amostras de mídia
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- SDK do Windows Media Format, importação de DRM
- SDK do Windows Media Format, importar
- SDK do Windows Media Format, criptografando amostras de mídia
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), criptografia de amostras de mídia
- DRM (gerenciamento de direitos digitais), criptografia de amostras de mídia
- APIs estendidas do cliente DRM, importar
- APIs estendidas do cliente, importar
- APIs estendidas do cliente DRM, criptografando amostras de mídia
- APIs estendidas do cliente, criptografando amostras de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473db9580990b62818842aaa5eeea3e82f38c5ad
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365556"
---
# <a name="encrypting-and-importing-media-samples"></a><span data-ttu-id="36a5d-114">Criptografando e importando amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="36a5d-114">Encrypting and Importing Media Samples</span></span>

<span data-ttu-id="36a5d-115">Para cada exemplo de mídia criptografada usando o DRM do Windows Media, você deve gerar um valor salt que seja estritamente maior do que o anterior (monotônico aumentando).</span><span class="sxs-lookup"><span data-stu-id="36a5d-115">For each media sample that you encrypt using Windows Media DRM, you must generate a salt value that is strictly bigger than the previous one (monotonically increasing).</span></span> <span data-ttu-id="36a5d-116">Use o novo valor de Salt para criar uma chave de criptografia transitória aplicando o algoritmo de criptografia SHA-1 ao vetor de inicialização concatenado com o valor de Salt.</span><span class="sxs-lookup"><span data-stu-id="36a5d-116">Use the new salt value to create a transitory encryption key by applying the SHA-1 encryption algorithm to the initialization vector concatenated with the salt value.</span></span>

<span data-ttu-id="36a5d-117">Em seguida, criptografe o exemplo de acordo com o algoritmo RC4 usando a chave transitória gerada.</span><span class="sxs-lookup"><span data-stu-id="36a5d-117">Next, encrypt the sample according to the RC4 algorithm using the generated transitory key.</span></span> <span data-ttu-id="36a5d-118">Antes que o exemplo seja passado para o SDK, seu aplicativo deve associar o valor de Salt ao exemplo definindo um atributo de extensão.</span><span class="sxs-lookup"><span data-stu-id="36a5d-118">Before the sample is passed to the SDK, your application must associate the salt value with the sample by setting an extension attribute.</span></span>

<span data-ttu-id="36a5d-119">Aqui estão as etapas para criptografar amostras de mídia:</span><span class="sxs-lookup"><span data-stu-id="36a5d-119">Here are the steps for encrypting media samples:</span></span>

1.  <span data-ttu-id="36a5d-120">Chame o método **QueryInterface** do objeto de exemplo para obter a interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .</span><span class="sxs-lookup"><span data-stu-id="36a5d-120">Call the **QueryInterface** method of the sample object to get the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface.</span></span>
2.  <span data-ttu-id="36a5d-121">Incrementar o valor de Salt.</span><span class="sxs-lookup"><span data-stu-id="36a5d-121">Increment the salt value.</span></span>
3.  <span data-ttu-id="36a5d-122">Criptografe o exemplo usando um algoritmo de criptografia RC1.</span><span class="sxs-lookup"><span data-stu-id="36a5d-122">Encrypt the sample using an RC1 encryption algorithm.</span></span> <span data-ttu-id="36a5d-123">Para a criptografia, você cria uma chave concatenando o vetor de inicialização e o valor de Salt.</span><span class="sxs-lookup"><span data-stu-id="36a5d-123">For the encryption you create a key by concatenating the initialization vector and the salt value.</span></span>
4.  <span data-ttu-id="36a5d-124">Forneça o valor de Salt para o SDK chamando [**INSSBuffer:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).</span><span class="sxs-lookup"><span data-stu-id="36a5d-124">Provide the salt value to the SDK by calling [**INSSBuffer::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="36a5d-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="36a5d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36a5d-126">**Importação de DRM**</span><span class="sxs-lookup"><span data-stu-id="36a5d-126">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="36a5d-127">**Exemplo de criptografia de exemplo de mídia**</span><span class="sxs-lookup"><span data-stu-id="36a5d-127">**Media Sample Encryption Example**</span></span>](media-sample-encryption-example.md)
</dt> </dl>

 

 




