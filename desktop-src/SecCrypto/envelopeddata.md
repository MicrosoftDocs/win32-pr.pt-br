---
description: O objeto EnvelopedData fornece propriedades e métodos para envelope dados para privacidade por criptografia.
ms.assetid: 7c5f3e3d-6a70-455d-8921-20495eec4b3e
title: Objeto EnvelopedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5309061c6ab315a089a1e1d8b9488556cae9f31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747641"
---
# <a name="envelopeddata-object"></a><span data-ttu-id="74ebe-103">Objeto EnvelopedData</span><span class="sxs-lookup"><span data-stu-id="74ebe-103">EnvelopedData object</span></span>

<span data-ttu-id="74ebe-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="74ebe-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="74ebe-105">Em vez disso, use a [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="74ebe-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="74ebe-106">O objeto **EnvelopedData** fornece propriedades e métodos para envelope dados para privacidade por criptografia.</span><span class="sxs-lookup"><span data-stu-id="74ebe-106">The **EnvelopedData** object provides properties and methods to envelop data for privacy by encryption.</span></span> <span data-ttu-id="74ebe-107">Para envelope dados, uma chave criptográfica da sessão é gerada.</span><span class="sxs-lookup"><span data-stu-id="74ebe-107">To envelop data, a session cryptographic key is generated.</span></span> <span data-ttu-id="74ebe-108">Essa [*chave de sessão*](../secgloss/s-gly.md) é criptografada para cada destinatário pretendido usando a [*chave pública*](../secgloss/p-gly.md) do destinatário pretendido do certificado do destinatário.</span><span class="sxs-lookup"><span data-stu-id="74ebe-108">That [*session key*](../secgloss/s-gly.md) is then encrypted for each intended recipient using the [*public key*](../secgloss/p-gly.md) of that intended recipient from the recipient's certificate.</span></span> <span data-ttu-id="74ebe-109">Os dados criptografados e o conjunto de chaves de sessão criptografadas podem ser enviados a todos os destinatários pretendidos.</span><span class="sxs-lookup"><span data-stu-id="74ebe-109">The encrypted data and the set of encrypted session keys can be sent to all intended recipients.</span></span> <span data-ttu-id="74ebe-110">A mensagem gerada está no \# formato PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="74ebe-110">The message generated is in PKCS \#7 format.</span></span>

## <a name="members"></a><span data-ttu-id="74ebe-111">Membros</span><span class="sxs-lookup"><span data-stu-id="74ebe-111">Members</span></span>

<span data-ttu-id="74ebe-112">O objeto **EnvelopedData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="74ebe-112">The **EnvelopedData** object has these types of members:</span></span>

-   [<span data-ttu-id="74ebe-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="74ebe-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="74ebe-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="74ebe-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="74ebe-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="74ebe-115">Methods</span></span>

<span data-ttu-id="74ebe-116">O objeto **EnvelopedData** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="74ebe-116">The **EnvelopedData** object has these methods.</span></span>



| <span data-ttu-id="74ebe-117">Método</span><span class="sxs-lookup"><span data-stu-id="74ebe-117">Method</span></span>                                   | <span data-ttu-id="74ebe-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="74ebe-118">Description</span></span>                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74ebe-119">**Descriptografar**</span><span class="sxs-lookup"><span data-stu-id="74ebe-119">**Decrypt**</span></span>](envelopeddata-decrypt.md) | <span data-ttu-id="74ebe-120">Descriptografa o conteúdo Envelopado.</span><span class="sxs-lookup"><span data-stu-id="74ebe-120">Decrypts enveloped content.</span></span><br/>                                                                      |
| [<span data-ttu-id="74ebe-121">**Encrypt**</span><span class="sxs-lookup"><span data-stu-id="74ebe-121">**Encrypt**</span></span>](envelopeddata-encrypt.md) | <span data-ttu-id="74ebe-122">Criptografa o conteúdo, criptografa uma chave de sessão para cada destinatário e retorna o BLOB criptografado.</span><span class="sxs-lookup"><span data-stu-id="74ebe-122">Encrypts the content, encrypts a session key for each recipient, and returns the encrypted BLOB.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="74ebe-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="74ebe-123">Properties</span></span>

<span data-ttu-id="74ebe-124">O objeto **EnvelopedData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="74ebe-124">The **EnvelopedData** object has these properties.</span></span>



| <span data-ttu-id="74ebe-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="74ebe-125">Property</span></span>                                                  | <span data-ttu-id="74ebe-126">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="74ebe-126">Access type</span></span>           | <span data-ttu-id="74ebe-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="74ebe-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74ebe-128">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="74ebe-128">**Algorithm**</span></span>](envelopeddata-algorithm.md)<br/>   | <span data-ttu-id="74ebe-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="74ebe-129">Read/write</span></span><br/> | <span data-ttu-id="74ebe-130">Algoritmo de criptografia e [*comprimento da chave*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="74ebe-130">Encryption algorithm and [*key length*](../secgloss/k-gly.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="74ebe-131">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="74ebe-131">**Content**</span></span>](envelopeddata-content.md)<br/>       | <span data-ttu-id="74ebe-132">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="74ebe-132">Read/write</span></span><br/> | <span data-ttu-id="74ebe-133">O conteúdo de texto não criptografado de uma mensagem a ser envelopada.</span><span class="sxs-lookup"><span data-stu-id="74ebe-133">The plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="74ebe-134">A definição dessa propriedade deve ser feita antes que o método [**Encrypt**](envelopeddata-encrypt.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="74ebe-134">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span><br/> <span data-ttu-id="74ebe-135">Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido e qualquer conteúdo criptografado no objeto é perdido.</span><span class="sxs-lookup"><span data-stu-id="74ebe-135">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="74ebe-136">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="74ebe-136">This is the default property.</span></span><br/> |
| [<span data-ttu-id="74ebe-137">**Destinatários**</span><span class="sxs-lookup"><span data-stu-id="74ebe-137">**Recipients**</span></span>](envelopeddata-recipients.md)<br/> | <span data-ttu-id="74ebe-138">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74ebe-138">Read-only</span></span><br/>  | <span data-ttu-id="74ebe-139">Coleção de objetos de [**certificado**](certificate.md) para receber a mensagem envelopada.</span><span class="sxs-lookup"><span data-stu-id="74ebe-139">Collection of [**Certificate**](certificate.md) objects to receive the enveloped message.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="74ebe-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="74ebe-140">Remarks</span></span>

<span data-ttu-id="74ebe-141">O objeto **EnvelopedData** pode ser criado e é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="74ebe-141">The **EnvelopedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="74ebe-142">O ProgID do objeto **EnvelopedData** é CAPICOM. EnvelopedData. 1.</span><span class="sxs-lookup"><span data-stu-id="74ebe-142">The ProgID for the **EnvelopedData** object is CAPICOM.EnvelopedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="74ebe-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74ebe-143">Requirements</span></span>



| <span data-ttu-id="74ebe-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="74ebe-144">Requirement</span></span> | <span data-ttu-id="74ebe-145">Valor</span><span class="sxs-lookup"><span data-stu-id="74ebe-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74ebe-146">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="74ebe-146">End of client support</span></span><br/> | <span data-ttu-id="74ebe-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74ebe-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="74ebe-148">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="74ebe-148">End of server support</span></span><br/> | <span data-ttu-id="74ebe-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74ebe-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="74ebe-150">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="74ebe-150">Redistributable</span></span><br/>       | <span data-ttu-id="74ebe-151">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="74ebe-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="74ebe-152">DLL</span><span class="sxs-lookup"><span data-stu-id="74ebe-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="74ebe-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74ebe-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74ebe-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="74ebe-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74ebe-155">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="74ebe-155">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
