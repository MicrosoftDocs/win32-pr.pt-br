---
description: Determina se as assinaturas em dados assinados no objeto SignedData são válidas.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: Método SignedData. Verify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3cb48943a826296c13df80130171442fc29435f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769271"
---
# <a name="signeddataverify-method"></a><span data-ttu-id="50555-103">Método SignedData. Verify</span><span class="sxs-lookup"><span data-stu-id="50555-103">SignedData.Verify method</span></span>

<span data-ttu-id="50555-104">\[O método **Verify** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="50555-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="50555-105">Em vez disso, use a [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="50555-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="50555-106">O método **Verify** determina se as [*assinaturas*](../secgloss/d-gly.md) em dados assinados no objeto [**SignedData**](signeddata.md) são válidas.</span><span class="sxs-lookup"><span data-stu-id="50555-106">The **Verify** method determines whether the [*signatures*](../secgloss/d-gly.md) on signed data in the [**SignedData**](signeddata.md) object are valid.</span></span> <span data-ttu-id="50555-107">Para verificar uma assinatura, o [*hash*](../secgloss/h-gly.md) criptografado do conteúdo é descriptografado usando a chave pública do assinante do certificado do Assinante.</span><span class="sxs-lookup"><span data-stu-id="50555-107">To verify a signature, the encrypted [*hash*](../secgloss/h-gly.md) of the contents is decrypted by using the signer's public key from the signer's certificate.</span></span> <span data-ttu-id="50555-108">O hash descriptografado é comparado com um novo hash do conteúdo de dados.</span><span class="sxs-lookup"><span data-stu-id="50555-108">The decrypted hash is compared to a new hash of the data content.</span></span> <span data-ttu-id="50555-109">Uma assinatura será válida se os hashes corresponderem.</span><span class="sxs-lookup"><span data-stu-id="50555-109">A signature is valid if the hashes match.</span></span> <span data-ttu-id="50555-110">Além disso, esse método também cria uma cadeia de certificados para determinar a validade do certificado que fornece a [*chave pública*](../secgloss/p-gly.md) usada para descriptografar o hash.</span><span class="sxs-lookup"><span data-stu-id="50555-110">In addition, this method also builds a certificate chain to determine the validity of the certificate that provides the [*public key*](../secgloss/p-gly.md) used to decrypt the hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="50555-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50555-111">Syntax</span></span>


```VB
SignedData.Verify( _
  ByVal SignedMessage, _
  [ ByVal bDetached ], _
  [ ByVal VerifyFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="50555-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50555-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50555-113">*SignedMessage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50555-113">*SignedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50555-114">Uma cadeia de caracteres que contém a mensagem assinada a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="50555-114">A string that contains the signed message to be verified.</span></span>

</dd> <dt>

<span data-ttu-id="50555-115">*bDetached* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="50555-115">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50555-116">Se **for true**, os dados a serem assinados serão desanexados; ou seja, o conteúdo assinado não é incluído como parte do objeto assinado.</span><span class="sxs-lookup"><span data-stu-id="50555-116">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="50555-117">Para verificar a assinatura no conteúdo desanexado, um aplicativo deve ter uma cópia do conteúdo original.</span><span class="sxs-lookup"><span data-stu-id="50555-117">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="50555-118">O conteúdo desanexado é geralmente usado para diminuir o tamanho de um objeto assinado a ser enviado pela Web, se o destinatário da mensagem assinada tiver uma cópia original dos dados assinados.</span><span class="sxs-lookup"><span data-stu-id="50555-118">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="50555-119">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="50555-119">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="50555-120">*VerifyFlag* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="50555-120">*VerifyFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50555-121">Um valor da enumeração [de \_ \_ sinalizador de \_ verificação \_ de dados assinados capicor](capicom-signed-data-verify-flag.md) que indica a política de verificação.</span><span class="sxs-lookup"><span data-stu-id="50555-121">A value of the [CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG](capicom-signed-data-verify-flag.md) enumeration that indicates the verification policy.</span></span> <span data-ttu-id="50555-122">O valor padrão é capicot \_ verificar \_ assinatura \_ e \_ certificado.</span><span class="sxs-lookup"><span data-stu-id="50555-122">The default value is CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE.</span></span> <span data-ttu-id="50555-123">Usando esse valor, a validade do certificado e a validade da assinatura são verificadas.</span><span class="sxs-lookup"><span data-stu-id="50555-123">Using this value, both the validity of the certificate and the validity of the signature are checked.</span></span> <span data-ttu-id="50555-124">Esse parâmetro pode ser definido para verificar a assinatura e não o certificado.</span><span class="sxs-lookup"><span data-stu-id="50555-124">This parameter may be set to verify the signature and not the certificate.</span></span> <span data-ttu-id="50555-125">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="50555-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="50555-126">Valor</span><span class="sxs-lookup"><span data-stu-id="50555-126">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="50555-127">Significado</span><span class="sxs-lookup"><span data-stu-id="50555-127">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <span data-ttu-id="50555-128"><dt>**CAPICOM \_ verificar \_ \_ somente assinatura**</dt></span><span class="sxs-lookup"><span data-stu-id="50555-128"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</dt></span></span> </dl>                                   | <span data-ttu-id="50555-129">Somente a assinatura é verificada.</span><span class="sxs-lookup"><span data-stu-id="50555-129">Only the signature is checked.</span></span><br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <span data-ttu-id="50555-130"><dt>**CAPICOM \_ verificar \_ assinatura \_ e \_ certificado**</dt></span><span class="sxs-lookup"><span data-stu-id="50555-130"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</dt></span></span> </dl> | <span data-ttu-id="50555-131">A assinatura e a validade do certificado usado para criar a assinatura são verificadas.</span><span class="sxs-lookup"><span data-stu-id="50555-131">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50555-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50555-132">Return value</span></span>

<span data-ttu-id="50555-133">Esse método retorna uma cadeia de caracteres que contém os dados codificados e assinados.</span><span class="sxs-lookup"><span data-stu-id="50555-133">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="50555-134">Se esse método falhar, um erro será gerado.</span><span class="sxs-lookup"><span data-stu-id="50555-134">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="50555-135">O objeto **Err** conterá informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="50555-135">The **Err** object will contain additional information about the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="50555-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50555-136">Requirements</span></span>



| <span data-ttu-id="50555-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="50555-137">Requirement</span></span> | <span data-ttu-id="50555-138">Valor</span><span class="sxs-lookup"><span data-stu-id="50555-138">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50555-139">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="50555-139">Redistributable</span></span><br/> | <span data-ttu-id="50555-140">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="50555-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="50555-141">DLL</span><span class="sxs-lookup"><span data-stu-id="50555-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="50555-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50555-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50555-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="50555-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50555-144">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="50555-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="50555-145">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="50555-145">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
