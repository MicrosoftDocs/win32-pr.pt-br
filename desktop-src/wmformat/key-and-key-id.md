---
title: Chave e ID da chave
description: Chave e ID da chave
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- DRM (gerenciamento de direitos digitais), chaves
- DRM (gerenciamento de direitos digitais), chaves
- DRM (gerenciamento de direitos digitais), criança
- DRM (gerenciamento de direitos digitais), KID
- ID da chave (KID)
- KID (ID da chave)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f74521fdf0f6cc268b8af1259f8468087f45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765664"
---
# <a name="key-and-key-id"></a><span data-ttu-id="74d92-110">Chave e ID da chave</span><span class="sxs-lookup"><span data-stu-id="74d92-110">Key and Key ID</span></span>

<span data-ttu-id="74d92-111">Ao empacotar um arquivo, você usa uma chave.</span><span class="sxs-lookup"><span data-stu-id="74d92-111">When you package a file, you use a key.</span></span> <span data-ttu-id="74d92-112">Uma chave é uma parte dos dados usados nos algoritmos de criptografia que protegem o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="74d92-112">A key is a piece of data used in the encryption algorithms that protect the content.</span></span> <span data-ttu-id="74d92-113">Há duas partes para cada chave: uma semente de chave de licença e uma ID de chave (muitas vezes abreviadas como KID).</span><span class="sxs-lookup"><span data-stu-id="74d92-113">There are two parts to each key: a license key seed and a key ID (often abbreviated as KID).</span></span> <span data-ttu-id="74d92-114">A ID da chave é pública e é armazenada no cabeçalho do arquivo como uma maneira de identificar a chave necessária para descriptografar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="74d92-114">The key ID is public, and is stored in the file header as a way to identify the key required to decrypt the file.</span></span> <span data-ttu-id="74d92-115">A semente da chave de licença é um valor secreto que deve ser compartilhado pelo empacotador de conteúdo e pelo emissor da licença.</span><span class="sxs-lookup"><span data-stu-id="74d92-115">The license key seed is a secret value that must be shared by the content packager and the license issuer.</span></span>

<span data-ttu-id="74d92-116">Uma ID de chave identifica o conteúdo protegido da perspectiva da licença.</span><span class="sxs-lookup"><span data-stu-id="74d92-116">A key ID identifies protected content from the perspective of the license.</span></span> <span data-ttu-id="74d92-117">Embora você possa usar a mesma ID de chave para vários arquivos, é recomendável usar sempre uma ID de chave exclusiva para cada parte do conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="74d92-117">Although you can use the same key ID for multiple files, it is recommended that you always use a unique key ID for each piece of protected content.</span></span>

<span data-ttu-id="74d92-118">Muitos dos métodos descritos nesta documentação usam cadeias de caracteres de ID de chave para selecionar licenças.</span><span class="sxs-lookup"><span data-stu-id="74d92-118">Many of the methods described in this documentation use key ID strings to select licenses.</span></span> <span data-ttu-id="74d92-119">Essas cadeias de caracteres contêm a ID de chave codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="74d92-119">These strings contain the key ID encoded in base64.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74d92-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74d92-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74d92-121">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="74d92-121">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




