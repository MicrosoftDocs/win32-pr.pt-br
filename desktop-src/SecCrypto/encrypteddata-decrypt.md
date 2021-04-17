---
description: Descriptografa uma cadeia de caracteres de dados criptografada e codificada.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: Método EncryptedData. Decrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aa702a5cefc46f6d0cbe5d7e0fba17ff03596b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747843"
---
# <a name="encrypteddatadecrypt-method"></a><span data-ttu-id="4a77b-103">Método EncryptedData. Decrypt</span><span class="sxs-lookup"><span data-stu-id="4a77b-103">EncryptedData.Decrypt method</span></span>

<span data-ttu-id="4a77b-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4a77b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4a77b-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções de API do Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para criptografar e descriptografar mensagens.</span><span class="sxs-lookup"><span data-stu-id="4a77b-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="4a77b-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a77b-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="4a77b-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="4a77b-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="4a77b-108">O método **Decrypt** descriptografa uma cadeia de caracteres de dados criptografada e codificada.</span><span class="sxs-lookup"><span data-stu-id="4a77b-108">The **Decrypt** method decrypts an encrypted and encoded data string.</span></span> <span data-ttu-id="4a77b-109">Os dados de texto sem formatação resultantes se tornam a propriedade [**Content**](encrypteddata-content.md) do objeto [**EncryptedData**](encrypteddata.md) .</span><span class="sxs-lookup"><span data-stu-id="4a77b-109">The resulting plaintext data becomes the [**Content**](encrypteddata-content.md) property of the [**EncryptedData**](encrypteddata.md) object.</span></span> <span data-ttu-id="4a77b-110">A descriptografia do conteúdo falha a menos que o segredo, definido pelo método [**setsecret**](encrypteddata-setsecret.md) , seja exatamente o mesmo que o segredo usado para derivar a chave usada para criptografar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4a77b-110">Decryption of the content fails unless the secret, set by the [**SetSecret**](encrypteddata-setsecret.md) method, is exactly the same as the secret used to derive the key used to encrypt the content.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a77b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a77b-111">Syntax</span></span>


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="4a77b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a77b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a77b-113">*EncryptedMessage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a77b-113">*EncryptedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a77b-114">Cadeia de caracteres que contém os dados codificados e criptografados a serem descriptografados.</span><span class="sxs-lookup"><span data-stu-id="4a77b-114">String that contains the encoded, encrypted data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a77b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a77b-115">Return value</span></span>

<span data-ttu-id="4a77b-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4a77b-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a77b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a77b-117">Remarks</span></span>

<span data-ttu-id="4a77b-118">A chave de sessão derivada do segredo atual é usada para a descriptografia.</span><span class="sxs-lookup"><span data-stu-id="4a77b-118">The session key derived from the current secret is used for the decryption.</span></span> <span data-ttu-id="4a77b-119">Esse método não produzirá o texto não criptografado correto, a menos que o segredo atual corresponda exatamente ao segredo usado para criptografar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="4a77b-119">This method will not produce the correct plaintext unless the current secret exactly matches the secret used to encrypt the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a77b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a77b-120">Requirements</span></span>



| <span data-ttu-id="4a77b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a77b-121">Requirement</span></span> | <span data-ttu-id="4a77b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4a77b-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a77b-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4a77b-123">End of client support</span></span><br/> | <span data-ttu-id="4a77b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a77b-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4a77b-125">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4a77b-125">End of server support</span></span><br/> | <span data-ttu-id="4a77b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a77b-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4a77b-127">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4a77b-127">Redistributable</span></span><br/>       | <span data-ttu-id="4a77b-128">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a77b-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4a77b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4a77b-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4a77b-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a77b-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a77b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a77b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a77b-132">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="4a77b-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="4a77b-133">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="4a77b-133">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
