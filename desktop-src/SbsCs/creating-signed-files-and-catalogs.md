---
description: Para assinar um arquivo e criar um catálogo para ele, você deve primeiro ter um processo para assinar arquivos, um certificado e uma chave pública.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Criando arquivos e catálogos assinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1327ed2d64c6f7be9f14acc2c846cf8a887119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169832"
---
# <a name="creating-signed-files-and-catalogs"></a><span data-ttu-id="6957a-103">Criando arquivos e catálogos assinados</span><span class="sxs-lookup"><span data-stu-id="6957a-103">Creating Signed Files and Catalogs</span></span>

<span data-ttu-id="6957a-104">Para assinar um arquivo e criar um catálogo para ele, você deve primeiro ter um processo para assinar arquivos, um certificado e uma chave pública.</span><span class="sxs-lookup"><span data-stu-id="6957a-104">To sign a file and create a catalog for it, you must first have a process for signing files, a certificate, and a public key.</span></span>

<span data-ttu-id="6957a-105">**Para assinar um arquivo e criar um catálogo**</span><span class="sxs-lookup"><span data-stu-id="6957a-105">**To sign a file and a create a catalog**</span></span>

1.  <span data-ttu-id="6957a-106">Use [Pktextract.exe](pktextract-exe.md) para extrair o [*token de chave pública*](p-sbscs-gly.md) do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="6957a-106">Use [Pktextract.exe](pktextract-exe.md) to extract the [*public key token*](p-sbscs-gly.md) from the certificate file.</span></span> <span data-ttu-id="6957a-107">O arquivo de certificado deve estar presente no mesmo diretório que o utilitário.</span><span class="sxs-lookup"><span data-stu-id="6957a-107">The certificate file must be present in the same directory as the utility.</span></span>
2.  <span data-ttu-id="6957a-108">Use o valor do token de chave pública para atualizar o atributo **PublicKeyToken** do elemento **AssemblyIdentity** no arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="6957a-108">Use the public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>
3.  <span data-ttu-id="6957a-109">Use [MT.exe](mt-exe.md) para gerar hashes de arquivos contidos no manifesto do assembly e para criar o arquivo de descrição do catálogo (. CDF).</span><span class="sxs-lookup"><span data-stu-id="6957a-109">Use [MT.exe](mt-exe.md) to generate hashes of files contained in the assembly manifest and to create the catalog description file (.cdf).</span></span>
4.  <span data-ttu-id="6957a-110">Use Makecat.exe com o. CDF gerado para criar o catálogo de segurança para o assembly.</span><span class="sxs-lookup"><span data-stu-id="6957a-110">Use Makecat.exe with the generated .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="6957a-111">Essa ferramenta está incluída no CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="6957a-111">This tool is included in the CryptoAPI.</span></span>
5.  <span data-ttu-id="6957a-112">Use o utilitário [SignTool](/windows/desktop/SecCrypto/signtool) para assinar o catálogo gerado com o certificado usado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="6957a-112">Use the [SignTool](/windows/desktop/SecCrypto/signtool) utility to sign the catalog generated with the certificate used in step 1.</span></span> <span data-ttu-id="6957a-113">O. CDF das etapas 3 e 4 pode ser excluído depois que o catálogo é criado.</span><span class="sxs-lookup"><span data-stu-id="6957a-113">The .cdf from steps 3 and 4 can be deleted once the catalog is created.</span></span>

<span data-ttu-id="6957a-114">Consulte também o [exemplo de assinatura de assembly](assembly-signing-example.md).</span><span class="sxs-lookup"><span data-stu-id="6957a-114">See also, [Assembly Signing Example](assembly-signing-example.md).</span></span>

 

 
