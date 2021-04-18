---
description: Gera uma chave de sessão e criptografa os dados e os envelopes.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: Método EnvelopedData. Encrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecdb665a8e70ff329f25398eb855ff3e82c96cfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751718"
---
# <a name="envelopeddataencrypt-method"></a><span data-ttu-id="c8015-103">Método EnvelopedData. Encrypt</span><span class="sxs-lookup"><span data-stu-id="c8015-103">EnvelopedData.Encrypt method</span></span>

<span data-ttu-id="c8015-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c8015-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c8015-105">Em vez disso, use a [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="c8015-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="c8015-106">O método **Encrypt** gera uma chave de sessão, usa essa chave para criptografar o conteúdo, envelops o conteúdo criptografado para cada destinatário criptografando a chave de sessão com a chave pública de cada destinatário e, em seguida, retorna o [*blob*](../secgloss/b-gly.md) que contém o conteúdo criptografado e as chaves de sessão criptografadas como uma cadeia de caracteres codificada.</span><span class="sxs-lookup"><span data-stu-id="c8015-106">The **Encrypt** method generates a session key, uses that key to encrypt the contents, envelops the encrypted content for each recipient by encrypting the session key with each recipient's public key, and then returns the [*BLOB*](../secgloss/b-gly.md) that contains the encrypted contents and the encrypted session keys as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8015-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8015-107">Syntax</span></span>


```VB
EnvelopedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c8015-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8015-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8015-109">*EncodingType* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c8015-109">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c8015-110">Um valor da enumeração [**do \_ \_ tipo de codificação capicor**](capicom-encoding-type.md) que indica o tipo de codificação usado para codificar os dados de envelope.</span><span class="sxs-lookup"><span data-stu-id="c8015-110">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the enveloped data.</span></span> <span data-ttu-id="c8015-111">O valor de codificação padrão é capicote Encoding \_ \_ base64.</span><span class="sxs-lookup"><span data-stu-id="c8015-111">The default encoding value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="c8015-112">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c8015-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c8015-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c8015-113">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="c8015-114">Significado</span><span class="sxs-lookup"><span data-stu-id="c8015-114">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="c8015-115"><dt>**CAPICOM \_ codificar \_ qualquer**</dt></span><span class="sxs-lookup"><span data-stu-id="c8015-115"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="c8015-116">Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c8015-116">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="c8015-117">Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="c8015-117">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="c8015-118">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="c8015-118">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="c8015-119"><dt>**CAPICOM \_ codificar \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="c8015-119"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="c8015-120">Os dados são salvos como uma cadeia de caracteres codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="c8015-120">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="c8015-121"><dt>**capicote de \_ codificação \_ binário**</dt></span><span class="sxs-lookup"><span data-stu-id="c8015-121"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="c8015-122">Os dados são salvos como uma sequência binária pura.</span><span class="sxs-lookup"><span data-stu-id="c8015-122">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8015-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8015-123">Return value</span></span>

<span data-ttu-id="c8015-124">Esse método retorna um BLOB que contém os dados de envelope em uma cadeia de caracteres codificada.</span><span class="sxs-lookup"><span data-stu-id="c8015-124">This method returns a BLOB that contains the enveloped data in an encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8015-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8015-125">Remarks</span></span>

<span data-ttu-id="c8015-126">O BLOB retornado contém o conteúdo criptografado e uma chave de sessão criptografada para cada destinatário pretendido.</span><span class="sxs-lookup"><span data-stu-id="c8015-126">The returned BLOB contains the encrypted content and an encrypted session key for each intended recipient.</span></span> <span data-ttu-id="c8015-127">Essas chaves de sessão são criptografadas usando a chave pública de cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="c8015-127">These session keys are encrypted using the public key of each recipient.</span></span> <span data-ttu-id="c8015-128">As chaves de sessão criptografadas podem ser descriptografadas somente com a chave privada de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="c8015-128">The encrypted session keys can be decrypted only with a recipient's private key.</span></span>

<span data-ttu-id="c8015-129">Se a propriedade [**Recipients**](envelopeddata-recipients.md) não contiver nenhuma informação, esse método pesquisará o repositório de certificados catálogo do usuário atual em busca de possíveis destinatários.</span><span class="sxs-lookup"><span data-stu-id="c8015-129">If the [**Recipients**](envelopeddata-recipients.md) property does not contain any information, this method searches the current user's AddressBook certificate store for potential recipients.</span></span> <span data-ttu-id="c8015-130">Se mais de um destinatário potencial for encontrado, será solicitado que o usuário selecione um destinatário em uma caixa de diálogo de seleção.</span><span class="sxs-lookup"><span data-stu-id="c8015-130">If more than one potential recipient is found, the user is prompted to select a recipient from a selection dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8015-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8015-131">Requirements</span></span>



| <span data-ttu-id="c8015-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8015-132">Requirement</span></span> | <span data-ttu-id="c8015-133">Valor</span><span class="sxs-lookup"><span data-stu-id="c8015-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8015-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c8015-134">End of client support</span></span><br/> | <span data-ttu-id="c8015-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8015-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c8015-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c8015-136">End of server support</span></span><br/> | <span data-ttu-id="c8015-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8015-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c8015-138">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c8015-138">Redistributable</span></span><br/>       | <span data-ttu-id="c8015-139">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c8015-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c8015-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c8015-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c8015-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8015-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8015-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8015-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8015-143">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="c8015-143">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="c8015-144">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="c8015-144">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
