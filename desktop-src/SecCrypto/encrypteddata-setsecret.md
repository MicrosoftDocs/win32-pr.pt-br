---
description: Define o valor do segredo usado para derivar a chave de sessão criptográfica usada para criptografar e descriptografar dados.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: Método EncryptedData. setsecret
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c8d30355b022a593ca17519e3ccfa876a5b07b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787460"
---
# <a name="encrypteddatasetsecret-method"></a><span data-ttu-id="b5ed0-103">Método EncryptedData. setsecret</span><span class="sxs-lookup"><span data-stu-id="b5ed0-103">EncryptedData.SetSecret method</span></span>

<span data-ttu-id="b5ed0-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b5ed0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b5ed0-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções de API do Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para criptografar e descriptografar mensagens.</span><span class="sxs-lookup"><span data-stu-id="b5ed0-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="b5ed0-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="b5ed0-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="b5ed0-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="b5ed0-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="b5ed0-108">O método **setsecret** define o valor do segredo usado para derivar a [*chave de sessão*](../secgloss/s-gly.md) criptográfica usada para criptografar e descriptografar dados.</span><span class="sxs-lookup"><span data-stu-id="b5ed0-108">The **SetSecret** method sets the value of the secret used to derive the cryptographic [*session key*](../secgloss/s-gly.md) used to encrypt and decrypt data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ed0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5ed0-109">Syntax</span></span>


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b5ed0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5ed0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ed0-111">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5ed0-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ed0-112">Uma cadeia de caracteres que contém um segredo usado para criar uma chave de criptografia de sessão.</span><span class="sxs-lookup"><span data-stu-id="b5ed0-112">A string that contains a secret used to create a session cryptographic key.</span></span>

</dd> <dt>

<span data-ttu-id="b5ed0-113">*Segredo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b5ed0-113">*SecretType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ed0-114">Um valor da enumeração [**de \_ \_ tipo de segredo de CAPICOM**](capicom-secret-type.md) que indica o tipo de segredo usado para gerar a chave de sessão.</span><span class="sxs-lookup"><span data-stu-id="b5ed0-114">A value of the [**CAPICOM\_SECRET\_TYPE**](capicom-secret-type.md) enumeration that indicates the kind of secret used to generate the session key.</span></span> <span data-ttu-id="b5ed0-115">O valor padrão é CAPICOM de \_ senha de segredo \_ .</span><span class="sxs-lookup"><span data-stu-id="b5ed0-115">The default value is CAPICOM\_SECRET\_PASSWORD.</span></span> <span data-ttu-id="b5ed0-116">Esse parâmetro pode ser o valor a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5ed0-116">This parameter can be the following value.</span></span>



| <span data-ttu-id="b5ed0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b5ed0-117">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="b5ed0-118">Significado</span><span class="sxs-lookup"><span data-stu-id="b5ed0-118">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <span data-ttu-id="b5ed0-119"><dt>**CAPICOM \_ \_ senha secreta**</dt></span><span class="sxs-lookup"><span data-stu-id="b5ed0-119"><dt>**CAPICOM\_SECRET\_PASSWORD**</dt></span></span> </dl> | <span data-ttu-id="b5ed0-120">A chave de criptografia deve ser derivada de uma senha.</span><span class="sxs-lookup"><span data-stu-id="b5ed0-120">The encryption key is to be derived from a password.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ed0-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5ed0-121">Return value</span></span>

<span data-ttu-id="b5ed0-122">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b5ed0-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5ed0-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5ed0-123">Remarks</span></span>

<span data-ttu-id="b5ed0-124">O segredo é usado para criar a chave de sessão para criptografia ou descriptografia.</span><span class="sxs-lookup"><span data-stu-id="b5ed0-124">The secret is used to create the session key for encryption or decryption.</span></span> <span data-ttu-id="b5ed0-125">O mesmo segredo deve ser usado para ambas as operações.</span><span class="sxs-lookup"><span data-stu-id="b5ed0-125">The same secret must be used for both operations.</span></span> <span data-ttu-id="b5ed0-126">Se o segredo usado para criptografar dados for perdido, os dados criptografados não poderão ser descriptografados.</span><span class="sxs-lookup"><span data-stu-id="b5ed0-126">If the secret used to encrypt data is lost, the encrypted data cannot be decrypted.</span></span>

<span data-ttu-id="b5ed0-127">Se apropriado para seu aplicativo, considere o uso de [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) ou [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) para proteger o segredo antes e depois do uso.</span><span class="sxs-lookup"><span data-stu-id="b5ed0-127">If appropriate for your application, consider using [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) or [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) to protect the secret before and after use.</span></span> <span data-ttu-id="b5ed0-128">Limpe a memória associada ao segredo quando terminar.</span><span class="sxs-lookup"><span data-stu-id="b5ed0-128">Clear the memory associated with the secret when done.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ed0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5ed0-129">Requirements</span></span>



| <span data-ttu-id="b5ed0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5ed0-130">Requirement</span></span> | <span data-ttu-id="b5ed0-131">Valor</span><span class="sxs-lookup"><span data-stu-id="b5ed0-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ed0-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b5ed0-132">End of client support</span></span><br/> | <span data-ttu-id="b5ed0-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5ed0-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b5ed0-134">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b5ed0-134">End of server support</span></span><br/> | <span data-ttu-id="b5ed0-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5ed0-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b5ed0-136">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b5ed0-136">Redistributable</span></span><br/>       | <span data-ttu-id="b5ed0-137">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5ed0-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b5ed0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b5ed0-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b5ed0-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5ed0-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5ed0-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5ed0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ed0-141">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="b5ed0-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="b5ed0-142">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="b5ed0-142">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
