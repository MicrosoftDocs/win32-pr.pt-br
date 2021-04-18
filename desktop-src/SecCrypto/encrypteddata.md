---
description: Fornece propriedades e métodos para criptografar e descriptografar dados usando uma chave de sessão derivada de um segredo.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: Objeto EncryptedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 123e0973343e4990dd2d49cfb321d739085358f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764623"
---
# <a name="encrypteddata-object"></a><span data-ttu-id="f7b15-103">Objeto EncryptedData</span><span class="sxs-lookup"><span data-stu-id="f7b15-103">EncryptedData object</span></span>

<span data-ttu-id="f7b15-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f7b15-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f7b15-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções de API do Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para criptografar e descriptografar mensagens.</span><span class="sxs-lookup"><span data-stu-id="f7b15-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="f7b15-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="f7b15-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="f7b15-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="f7b15-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="f7b15-108">O objeto **EncryptedData** fornece propriedades e métodos para criptografar e descriptografar dados usando uma [*chave de sessão*](../secgloss/s-gly.md) derivada de um segredo.</span><span class="sxs-lookup"><span data-stu-id="f7b15-108">The **EncryptedData** object provides properties and methods to encrypt and decrypt data using a [*session key*](../secgloss/s-gly.md) derived from a secret.</span></span>

> [!Note]  
> <span data-ttu-id="f7b15-109">O CAPICOM não oferece suporte ao \# tipo de conteúdo ENCRYPTEDDATA PKCS 7, mas usa uma estrutura ASN não padrão para **EncryptedData**.</span><span class="sxs-lookup"><span data-stu-id="f7b15-109">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for **EncryptedData**.</span></span> <span data-ttu-id="f7b15-110">Portanto, somente o capicor pode descriptografar um objeto capicot **EncryptedData** .</span><span class="sxs-lookup"><span data-stu-id="f7b15-110">Therefore, only CAPICOM can decrypt a CAPICOM **EncryptedData** object.</span></span>

 

## <a name="members"></a><span data-ttu-id="f7b15-111">Membros</span><span class="sxs-lookup"><span data-stu-id="f7b15-111">Members</span></span>

<span data-ttu-id="f7b15-112">O objeto **EncryptedData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f7b15-112">The **EncryptedData** object has these types of members:</span></span>

-   [<span data-ttu-id="f7b15-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="f7b15-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="f7b15-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f7b15-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f7b15-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="f7b15-115">Methods</span></span>

<span data-ttu-id="f7b15-116">O objeto **EncryptedData** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f7b15-116">The **EncryptedData** object has these methods.</span></span>



| <span data-ttu-id="f7b15-117">Método</span><span class="sxs-lookup"><span data-stu-id="f7b15-117">Method</span></span>                                       | <span data-ttu-id="f7b15-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7b15-118">Description</span></span>                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7b15-119">**Descriptografar**</span><span class="sxs-lookup"><span data-stu-id="f7b15-119">**Decrypt**</span></span>](encrypteddata-decrypt.md)     | <span data-ttu-id="f7b15-120">Descriptografa o conteúdo criptografado usando o segredo.</span><span class="sxs-lookup"><span data-stu-id="f7b15-120">Decrypts encrypted content using the secret.</span></span><br/>                                 |
| [<span data-ttu-id="f7b15-121">**Encrypt**</span><span class="sxs-lookup"><span data-stu-id="f7b15-121">**Encrypt**</span></span>](encrypteddata-encrypt.md)     | <span data-ttu-id="f7b15-122">Criptografa o conteúdo usando o segredo atual e o algoritmo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="f7b15-122">Encrypts the content using the current secret and encryption algorithm.</span></span><br/>      |
| [<span data-ttu-id="f7b15-123">**Setsecret**</span><span class="sxs-lookup"><span data-stu-id="f7b15-123">**SetSecret**</span></span>](encrypteddata-setsecret.md) | <span data-ttu-id="f7b15-124">Define o segredo do qual a chave de sessão de criptografia/descriptografia é derivada.</span><span class="sxs-lookup"><span data-stu-id="f7b15-124">Sets the secret from which the encryption/decryption session key is derived.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f7b15-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f7b15-125">Properties</span></span>

<span data-ttu-id="f7b15-126">O objeto **EncryptedData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f7b15-126">The **EncryptedData** object has these properties.</span></span>



| <span data-ttu-id="f7b15-127">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f7b15-127">Property</span></span>                                                | <span data-ttu-id="f7b15-128">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="f7b15-128">Access type</span></span>           | <span data-ttu-id="f7b15-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7b15-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7b15-130">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="f7b15-130">**Algorithm**</span></span>](encrypteddata-algorithm.md)<br/> | <span data-ttu-id="f7b15-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7b15-131">Read-only</span></span><br/>  | <span data-ttu-id="f7b15-132">Algoritmo usado para criptografia/descriptografia.</span><span class="sxs-lookup"><span data-stu-id="f7b15-132">Algorithm used for encryption/decryption.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="f7b15-133">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="f7b15-133">**Content**</span></span>](encrypteddata-content.md)<br/>     | <span data-ttu-id="f7b15-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7b15-134">Read/write</span></span><br/> | <span data-ttu-id="f7b15-135">O conteúdo a ser criptografado ou descriptografado.</span><span class="sxs-lookup"><span data-stu-id="f7b15-135">The content to be encrypted or decrypted.</span></span> <span data-ttu-id="f7b15-136">A definição dessa propriedade deve ser feita antes que o método [**Encrypt**](encrypteddata-encrypt.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="f7b15-136">Setting this property must be done before the [**Encrypt**](encrypteddata-encrypt.md) method is called.</span></span> <br/> <span data-ttu-id="f7b15-137">Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido e qualquer conteúdo criptografado no objeto é perdido.</span><span class="sxs-lookup"><span data-stu-id="f7b15-137">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="f7b15-138">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="f7b15-138">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7b15-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7b15-139">Remarks</span></span>

<span data-ttu-id="f7b15-140">O objeto **EncryptedData** pode ser criado e é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="f7b15-140">The **EncryptedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="f7b15-141">O ProgID do objeto **EncryptedData** é CAPICOM. EncryptedData. 1.</span><span class="sxs-lookup"><span data-stu-id="f7b15-141">The ProgID for the **EncryptedData** object is CAPICOM.EncryptedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b15-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7b15-142">Requirements</span></span>



| <span data-ttu-id="f7b15-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7b15-143">Requirement</span></span> | <span data-ttu-id="f7b15-144">Valor</span><span class="sxs-lookup"><span data-stu-id="f7b15-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b15-145">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f7b15-145">End of client support</span></span><br/> | <span data-ttu-id="f7b15-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7b15-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f7b15-147">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="f7b15-147">End of server support</span></span><br/> | <span data-ttu-id="f7b15-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7b15-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f7b15-149">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f7b15-149">Redistributable</span></span><br/>       | <span data-ttu-id="f7b15-150">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="f7b15-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f7b15-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f7b15-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f7b15-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b15-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7b15-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7b15-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b15-154">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="f7b15-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
