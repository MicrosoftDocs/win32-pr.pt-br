---
description: Use comandos MakeCert para criar certificados de teste usando as opções disponíveis com o Internet Explorer versão 4,0 ou posterior.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Usando MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068b10d5ce50141ff657379f9c5106cf2733d969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647636"
---
# <a name="using-makecert"></a><span data-ttu-id="45ad4-103">Usando MakeCert</span><span class="sxs-lookup"><span data-stu-id="45ad4-103">Using MakeCert</span></span>

<span data-ttu-id="45ad4-104">Os exemplos a seguir usam comandos [MakeCert](makecert.md) para criar certificados de teste usando opções disponíveis com o Internet Explorer versão 4,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="45ad4-104">The following examples use [MakeCert](makecert.md) commands to create test certificates using options available with Internet Explorer version 4.0 or later.</span></span>

-   <span data-ttu-id="45ad4-105">Faça um certificado emitido pela raiz de teste padrão.</span><span class="sxs-lookup"><span data-stu-id="45ad4-105">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="45ad4-106">Salve o certificado em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="45ad4-106">Save the certificate to a file.</span></span>

    <span data-ttu-id="45ad4-107">**MakeCert** *MyNew. cer*</span><span class="sxs-lookup"><span data-stu-id="45ad4-107">**MakeCert** *MyNew.cer*</span></span>

-   <span data-ttu-id="45ad4-108">Faça um certificado emitido pela raiz de teste padrão.</span><span class="sxs-lookup"><span data-stu-id="45ad4-108">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="45ad4-109">Salve-o em um repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="45ad4-109">Save it to a certificate store.</span></span>

    <span data-ttu-id="45ad4-110">**MakeCert-SS** *MyNewStore*</span><span class="sxs-lookup"><span data-stu-id="45ad4-110">**MakeCert -ss** *MyNewStore*</span></span>

-   <span data-ttu-id="45ad4-111">Faça um certificado emitido pela raiz de teste padrão.</span><span class="sxs-lookup"><span data-stu-id="45ad4-111">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="45ad4-112">Crie um contêiner de chave e salve o certificado em um repositório e em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="45ad4-112">Create a key container and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="45ad4-113">**Makecert-sk** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer*</span><span class="sxs-lookup"><span data-stu-id="45ad4-113">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="45ad4-114">Faça um certificado emitido pela raiz de teste padrão.</span><span class="sxs-lookup"><span data-stu-id="45ad4-114">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="45ad4-115">Crie um arquivo de chave privada e salve o certificado em um repositório e em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="45ad4-115">Create a private key file and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="45ad4-116">**MakeCert-VA** *mykeyfile* **-SS** *MyNewStore* *MyNew. cer*</span><span class="sxs-lookup"><span data-stu-id="45ad4-116">**MakeCert -sv** *MyKeyFile* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="45ad4-117">Faça um certificado emitido pela raiz de teste padrão.</span><span class="sxs-lookup"><span data-stu-id="45ad4-117">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="45ad4-118">Crie um contêiner de chave, salve o certificado em um repositório e em um arquivo e torne a chave privada exportável.</span><span class="sxs-lookup"><span data-stu-id="45ad4-118">Create a key container, save the certificate to both a store and a file, and make the private key exportable.</span></span>

    <span data-ttu-id="45ad4-119">**Makecert-sk** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer* **-PE**</span><span class="sxs-lookup"><span data-stu-id="45ad4-119">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer* **-pe**</span></span>

-   <span data-ttu-id="45ad4-120">Faça um certificado usando a raiz de teste padrão.</span><span class="sxs-lookup"><span data-stu-id="45ad4-120">Make a certificate by using the default test root.</span></span> <span data-ttu-id="45ad4-121">Salve o certificado em um repositório.</span><span class="sxs-lookup"><span data-stu-id="45ad4-121">Save the certificate to a store.</span></span> <span data-ttu-id="45ad4-122">Em seguida, faça outro certificado emitido pelo certificado recém-criado.</span><span class="sxs-lookup"><span data-stu-id="45ad4-122">Then make another certificate issued by the newly created certificate.</span></span> <span data-ttu-id="45ad4-123">Salve o segundo certificado em outro repositório.</span><span class="sxs-lookup"><span data-stu-id="45ad4-123">Save the second certificate to another store.</span></span>

    <span data-ttu-id="45ad4-124">**Makecert-sk** *MyNewKey* **-SS** *MyNewStore* **MakeCert-is** *MyNewStore* **-SS** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="45ad4-124">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* **MakeCert -is** *MyNewStore* **-ss** *AnotherStore*</span></span>

-   <span data-ttu-id="45ad4-125">Faça um certificado usando a raiz de teste padrão.</span><span class="sxs-lookup"><span data-stu-id="45ad4-125">Make a certificate by using the default test root.</span></span> <span data-ttu-id="45ad4-126">Salve o certificado no meu repositório.</span><span class="sxs-lookup"><span data-stu-id="45ad4-126">Save the certificate to the MY store.</span></span> <span data-ttu-id="45ad4-127">Em seguida, faça outro certificado usando o certificado recém-criado.</span><span class="sxs-lookup"><span data-stu-id="45ad4-127">Then make another certificate by using the newly created certificate.</span></span> <span data-ttu-id="45ad4-128">Se houver mais de um certificado no meu repositório, o certificado deverá ser identificado usando seu nome comum.</span><span class="sxs-lookup"><span data-stu-id="45ad4-128">If there is more than one certificate in the MY store, the certificate must be identified by using its common name.</span></span>

    <span data-ttu-id="45ad4-129">**Makecert-sk** *MyNewKey* **-n "CN = XXZZYY"-SS meu MakeCert-is my-in "XXZZYY"-SS** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="45ad4-129">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my MakeCert -is my -in "XXZZYY" -ss** *AnotherStore*</span></span>

-   <span data-ttu-id="45ad4-130">Faça um certificado usando a raiz de teste padrão.</span><span class="sxs-lookup"><span data-stu-id="45ad4-130">Make a certificate by using the default test root.</span></span> <span data-ttu-id="45ad4-131">Salve o certificado no meu repositório e em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="45ad4-131">Save the certificate to the MY store and to a file.</span></span> <span data-ttu-id="45ad4-132">Em seguida, faça outro certificado usando o certificado *MyNew* recém-criado.</span><span class="sxs-lookup"><span data-stu-id="45ad4-132">Then make another certificate by using the newly created *MyNew* certificate.</span></span> <span data-ttu-id="45ad4-133">Se houver mais de um certificado no meu repositório, identifique exclusivamente o primeiro certificado usando o nome do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="45ad4-133">If there is more than one certificate in the MY store, uniquely identify the first certificate by using the certificate file name.</span></span>

    <span data-ttu-id="45ad4-134">**Makecert-sk** *MyNewKey* **-n "CN = XXZZYY"-SS meu** *MyNew. cer* **MakeCert-is my-IC** *MyNew. cer* **-SS** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="45ad4-134">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my** *MyNew.cer* **MakeCert -is my -ic** *MyNew.cer* **-ss** *AnotherStore*</span></span>

 

 



