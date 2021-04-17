---
description: Fornece a funcionalidade para assinar arquivos executáveis com uma assinatura digital Authenticode.
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: Objeto SignedCode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08648c8b941874a6d1e1ed97d49f510694b998b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769272"
---
# <a name="signedcode-object"></a><span data-ttu-id="82e4e-103">Objeto SignedCode</span><span class="sxs-lookup"><span data-stu-id="82e4e-103">SignedCode object</span></span>

<span data-ttu-id="82e4e-104">\[O objeto **SignedCode** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="82e4e-104">\[The **SignedCode** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="82e4e-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="82e4e-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="82e4e-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="82e4e-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="82e4e-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="82e4e-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="82e4e-108">O objeto **SignedCode** fornece funcionalidade para assinar arquivos executáveis com uma assinatura digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="82e4e-108">The **SignedCode** object provides functionality for signing executable files with an Authenticode digital signature.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="82e4e-109">Quando usar</span><span class="sxs-lookup"><span data-stu-id="82e4e-109">When to use</span></span>

<span data-ttu-id="82e4e-110">O objeto **SignedCode** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="82e4e-110">The **SignedCode** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="82e4e-111">Assinar arquivos executáveis.</span><span class="sxs-lookup"><span data-stu-id="82e4e-111">Sign executable files.</span></span>
-   <span data-ttu-id="82e4e-112">Arquivos executáveis de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="82e4e-112">Time stamp executable files.</span></span>
-   <span data-ttu-id="82e4e-113">Determine se a assinatura do arquivo executável é válida.</span><span class="sxs-lookup"><span data-stu-id="82e4e-113">Determine whether the signature of the executable file is valid.</span></span>
-   <span data-ttu-id="82e4e-114">Defina ou recupere o caminho para o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="82e4e-114">Set or retrieve the path to the executable file.</span></span>
-   <span data-ttu-id="82e4e-115">Recupere o signatário e a hora Stamper do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="82e4e-115">Retrieve the signer and time stamper of the executable file.</span></span>
-   <span data-ttu-id="82e4e-116">Recupere uma coleção de certificados para o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="82e4e-116">Retrieve a collection of the certificates for the executable file.</span></span>
-   <span data-ttu-id="82e4e-117">Recupere uma descrição ou a URL para a descrição do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="82e4e-117">Retrieve a description or the URL to the description of the executable file.</span></span>

## <a name="members"></a><span data-ttu-id="82e4e-118">Membros</span><span class="sxs-lookup"><span data-stu-id="82e4e-118">Members</span></span>

<span data-ttu-id="82e4e-119">O objeto **SignedCode** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="82e4e-119">The **SignedCode** object has these types of members:</span></span>

-   [<span data-ttu-id="82e4e-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="82e4e-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="82e4e-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82e4e-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="82e4e-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="82e4e-122">Methods</span></span>

<span data-ttu-id="82e4e-123">O objeto **SignedCode** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="82e4e-123">The **SignedCode** object has these methods.</span></span>



| <span data-ttu-id="82e4e-124">Método</span><span class="sxs-lookup"><span data-stu-id="82e4e-124">Method</span></span>                                    | <span data-ttu-id="82e4e-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="82e4e-125">Description</span></span>                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82e4e-126">**Assine**</span><span class="sxs-lookup"><span data-stu-id="82e4e-126">**Sign**</span></span>](signedcode-sign.md)           | <span data-ttu-id="82e4e-127">Cria uma assinatura digital Authenticode e assina o arquivo executável especificado na propriedade [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="82e4e-127">Creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>    |
| [<span data-ttu-id="82e4e-128">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="82e4e-128">**Timestamp**</span></span>](signedcode-timestamp.md) | <span data-ttu-id="82e4e-129">Cria uma assinatura de carimbo de data/hora Authenticode no arquivo executável assinado especificado na propriedade [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="82e4e-129">Creates an Authenticode time stamp signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/> |
| [<span data-ttu-id="82e4e-130">**Verificar**</span><span class="sxs-lookup"><span data-stu-id="82e4e-130">**Verify**</span></span>](signedcode-verify.md)       | <span data-ttu-id="82e4e-131">Verifica a assinatura Authenticode no arquivo executável assinado especificado na propriedade [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="82e4e-131">Verifies the Authenticode signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="82e4e-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82e4e-132">Properties</span></span>

<span data-ttu-id="82e4e-133">O objeto **SignedCode** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="82e4e-133">The **SignedCode** object has these properties.</span></span>



| <span data-ttu-id="82e4e-134">Propriedade</span><span class="sxs-lookup"><span data-stu-id="82e4e-134">Property</span></span>                                                       | <span data-ttu-id="82e4e-135">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="82e4e-135">Access type</span></span>           | <span data-ttu-id="82e4e-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="82e4e-136">Description</span></span>                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82e4e-137">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="82e4e-137">**Certificates**</span></span>](signedcode-certificates.md)<br/>     | <span data-ttu-id="82e4e-138">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82e4e-138">Read-only</span></span><br/>  | <span data-ttu-id="82e4e-139">Uma coleção de [**certificados**](certificates.md) que contém todos os certificados no arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="82e4e-139">A [**Certificates**](certificates.md) collection that contains all the certificates in the signed executable file.</span></span><br/>             |
| [<span data-ttu-id="82e4e-140">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="82e4e-140">**Description**</span></span>](signedcode-description.md)<br/>       | <span data-ttu-id="82e4e-141">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="82e4e-141">Read/write</span></span><br/> | <span data-ttu-id="82e4e-142">Uma cadeia de caracteres que contém uma descrição do arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="82e4e-142">A string that contains a description of the signed executable file.</span></span><br/>                                                             |
| [<span data-ttu-id="82e4e-143">**DescriptionURL**</span><span class="sxs-lookup"><span data-stu-id="82e4e-143">**DescriptionURL**</span></span>](signedcode-descriptionurl.md)<br/> | <span data-ttu-id="82e4e-144">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="82e4e-144">Read/write</span></span><br/> | <span data-ttu-id="82e4e-145">Uma cadeia de caracteres que contém o endereço HTTP para uma descrição do arquivo executável assinado.</span><span class="sxs-lookup"><span data-stu-id="82e4e-145">A string that contains the HTTP address to a description of the signed executable file.</span></span><br/>                                         |
| [<span data-ttu-id="82e4e-146">**Nome do arquivo**</span><span class="sxs-lookup"><span data-stu-id="82e4e-146">**FileName**</span></span>](signedcode-filename.md)<br/>             | <span data-ttu-id="82e4e-147">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="82e4e-147">Read/write</span></span><br/> | <span data-ttu-id="82e4e-148">Uma cadeia de caracteres que contém o caminho para o arquivo de conteúdo que contém o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="82e4e-148">A string that contains the path to the content file that contains the executable file.</span></span><br/> <span data-ttu-id="82e4e-149">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="82e4e-149">This is the default property.</span></span><br/> |
| [<span data-ttu-id="82e4e-150">**Signatário**</span><span class="sxs-lookup"><span data-stu-id="82e4e-150">**Signer**</span></span>](signedcode-signer.md)<br/>                 | <span data-ttu-id="82e4e-151">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82e4e-151">Read-only</span></span><br/>  | <span data-ttu-id="82e4e-152">Um objeto de [**signatário**](signer.md) que fornece acesso ao signatário do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="82e4e-152">A [**Signer**](signer.md) object that provides access to the signer of the executable file.</span></span><br/>                                    |
| [<span data-ttu-id="82e4e-153">**Timestamper**</span><span class="sxs-lookup"><span data-stu-id="82e4e-153">**Timestamper**</span></span>](signedcode-timestamper.md)<br/>       | <span data-ttu-id="82e4e-154">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82e4e-154">Read-only</span></span><br/>  | <span data-ttu-id="82e4e-155">Um objeto de [**signatário**](signer.md) que fornece acesso ao Stamper de tempo do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="82e4e-155">A [**Signer**](signer.md) object that provides access to the time stamper of the executable file.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="82e4e-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="82e4e-156">Remarks</span></span>

<span data-ttu-id="82e4e-157">O objeto **SignedCode** pode ser criado e não é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="82e4e-157">The **SignedCode** object can be created, and is not safe for scripting.</span></span> <span data-ttu-id="82e4e-158">O ProgID do objeto **SignedCode** é CAPICOM. SignedCode. 1.</span><span class="sxs-lookup"><span data-stu-id="82e4e-158">The ProgID for the **SignedCode** object is CAPICOM.SignedCode.1.</span></span>

<span data-ttu-id="82e4e-159">O arquivo executável deve ser de um tipo que possa ser assinado com a tecnologia Authenticode, por exemplo, arquivos que têm uma extensão de nome de arquivo. cab,. Cat,. exe,. dll,. vbs ou. ocx.</span><span class="sxs-lookup"><span data-stu-id="82e4e-159">The executable file should be of a type that can be signed with Authenticode technology, for example, files that have a file name extension of .cab, .cat, .exe, .dll, .vbs, or .ocx.</span></span>

## <a name="requirements"></a><span data-ttu-id="82e4e-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82e4e-160">Requirements</span></span>



| <span data-ttu-id="82e4e-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="82e4e-161">Requirement</span></span> | <span data-ttu-id="82e4e-162">Valor</span><span class="sxs-lookup"><span data-stu-id="82e4e-162">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82e4e-163">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="82e4e-163">Redistributable</span></span><br/> | <span data-ttu-id="82e4e-164">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="82e4e-164">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="82e4e-165">DLL</span><span class="sxs-lookup"><span data-stu-id="82e4e-165">DLL</span></span><br/>             | <dl> <span data-ttu-id="82e4e-166"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82e4e-166"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
