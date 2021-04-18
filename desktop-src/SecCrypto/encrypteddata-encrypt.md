---
description: Deriva uma chave de sessão do segredo e criptografa o valor da propriedade Content usando essa chave. Ele retorna o conteúdo criptografado como uma cadeia de caracteres codificada.
ms.assetid: aa6f6e6a-208b-4e9c-b530-08673ab9d794
title: Método EncryptedData. Encrypt (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 04d7bf8a337c1bcfa0a024b84304fe50c035f9dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757474"
---
# <a name="encrypteddataencrypt-method"></a><span data-ttu-id="7fb08-104">Método EncryptedData. Encrypt</span><span class="sxs-lookup"><span data-stu-id="7fb08-104">EncryptedData.Encrypt method</span></span>

<span data-ttu-id="7fb08-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7fb08-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7fb08-106">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções de API do Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para criptografar e descriptografar mensagens.</span><span class="sxs-lookup"><span data-stu-id="7fb08-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="7fb08-107">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="7fb08-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="7fb08-108">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="7fb08-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="7fb08-109">O método **Encrypt** deriva uma chave de sessão do segredo e criptografa o valor da propriedade [**Content**](encrypteddata-content.md) usando essa chave.</span><span class="sxs-lookup"><span data-stu-id="7fb08-109">The **Encrypt** method derives a session key from the secret and encrypts the [**Content**](encrypteddata-content.md) property value using that key.</span></span> <span data-ttu-id="7fb08-110">Ele retorna o conteúdo criptografado como uma cadeia de caracteres codificada.</span><span class="sxs-lookup"><span data-stu-id="7fb08-110">It returns the encrypted content as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fb08-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7fb08-111">Syntax</span></span>


```VB
EncryptedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7fb08-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fb08-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fb08-113">*EncodingType* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7fb08-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb08-114">Um valor da enumeração [**do \_ \_ tipo de codificação capicor**](capicom-encoding-type.md) que indica o tipo de codificação usado para codificar os dados criptografados.</span><span class="sxs-lookup"><span data-stu-id="7fb08-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the encrypted data.</span></span> <span data-ttu-id="7fb08-115">O valor padrão é CAPICOM de \_ codificação \_ base64.</span><span class="sxs-lookup"><span data-stu-id="7fb08-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="7fb08-116">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7fb08-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7fb08-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7fb08-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="7fb08-118">Significado</span><span class="sxs-lookup"><span data-stu-id="7fb08-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="7fb08-119"><dt>**CAPICOM \_ codificar \_ qualquer**</dt></span><span class="sxs-lookup"><span data-stu-id="7fb08-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="7fb08-120">Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido.</span><span class="sxs-lookup"><span data-stu-id="7fb08-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="7fb08-121">Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="7fb08-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="7fb08-122">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="7fb08-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="7fb08-123"><dt>**CAPICOM \_ codificar \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="7fb08-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="7fb08-124">Os dados são salvos como uma cadeia de caracteres codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="7fb08-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="7fb08-125"><dt>**capicote de \_ codificação \_ binário**</dt></span><span class="sxs-lookup"><span data-stu-id="7fb08-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="7fb08-126">Os dados são salvos como uma sequência binária pura.</span><span class="sxs-lookup"><span data-stu-id="7fb08-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fb08-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7fb08-127">Return value</span></span>

<span data-ttu-id="7fb08-128">Uma cadeia de caracteres que contém os dados criptografados e codificados.</span><span class="sxs-lookup"><span data-stu-id="7fb08-128">A string that contains the encrypted, encoded data.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fb08-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fb08-129">Remarks</span></span>

<span data-ttu-id="7fb08-130">Antes de chamar o método **Encrypt** , defina a propriedade [**Content**](encrypteddata-content.md) e chame o método [**setsecret**](encrypteddata-setsecret.md) .</span><span class="sxs-lookup"><span data-stu-id="7fb08-130">Before calling the **Encrypt** method, set the [**Content**](encrypteddata-content.md) property and call the [**SetSecret**](encrypteddata-setsecret.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fb08-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fb08-131">Requirements</span></span>



| <span data-ttu-id="7fb08-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fb08-132">Requirement</span></span> | <span data-ttu-id="7fb08-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7fb08-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fb08-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7fb08-134">End of client support</span></span><br/> | <span data-ttu-id="7fb08-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7fb08-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7fb08-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="7fb08-136">End of server support</span></span><br/> | <span data-ttu-id="7fb08-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fb08-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7fb08-138">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7fb08-138">Redistributable</span></span><br/>       | <span data-ttu-id="7fb08-139">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="7fb08-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7fb08-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7fb08-140">Header</span></span><br/>                | <dl> <span data-ttu-id="7fb08-141"><dt>InfoCard. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fb08-141"><dt>Infocard.h</dt></span></span> </dl>  |
| <span data-ttu-id="7fb08-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7fb08-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7fb08-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fb08-143"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fb08-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fb08-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fb08-145">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="7fb08-145">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="7fb08-146">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="7fb08-146">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
