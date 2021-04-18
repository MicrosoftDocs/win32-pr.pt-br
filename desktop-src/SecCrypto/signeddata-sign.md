---
description: Cria uma assinatura digital no conteúdo a ser assinado. Uma assinatura digital consiste em um hash do conteúdo a ser assinado que é criptografado usando a chave privada do Assinante.
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: Método SignedData. Sign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9f885bb110b51264bc6108ca8c0f881cc48f7710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810506"
---
# <a name="signeddatasign-method"></a><span data-ttu-id="e0822-104">Método SignedData. Sign</span><span class="sxs-lookup"><span data-stu-id="e0822-104">SignedData.Sign method</span></span>

<span data-ttu-id="e0822-105">\[O método **Sign** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e0822-105">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e0822-106">Em vez disso, use a [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="e0822-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="e0822-107">O método **Sign** cria uma [*assinatura digital*](../secgloss/d-gly.md) no conteúdo a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="e0822-107">The **Sign** method creates a [*digital signature*](../secgloss/d-gly.md) on the content to be signed.</span></span> <span data-ttu-id="e0822-108">Uma assinatura digital consiste em um [*hash*](../secgloss/h-gly.md) do conteúdo a ser assinado que é criptografado usando a chave privada do Assinante.</span><span class="sxs-lookup"><span data-stu-id="e0822-108">A digital signature consists of a [*hash*](../secgloss/h-gly.md) of the content to be signed that is encrypted by using the private key of the signer.</span></span> <span data-ttu-id="e0822-109">Este método só pode ser usado depois que a propriedade [**SignedData. Content**](signeddata-content.md) tiver sido inicializada.</span><span class="sxs-lookup"><span data-stu-id="e0822-109">This method can only be used after the [**SignedData.Content**](signeddata-content.md) property has been initialized.</span></span> <span data-ttu-id="e0822-110">Se o método **Sign** for chamado em um objeto que já tem uma assinatura, a assinatura antiga será substituída.</span><span class="sxs-lookup"><span data-stu-id="e0822-110">If the **Sign** method is called on an object that already has a signature, the old signature is replaced.</span></span> <span data-ttu-id="e0822-111">A assinatura é criada usando o algoritmo de assinatura SHA1.</span><span class="sxs-lookup"><span data-stu-id="e0822-111">The signature is created by using the SHA1 signing algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0822-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0822-112">Syntax</span></span>


```VB
SignedData.Sign( _
  [ ByVal Signer ], _
  [ ByVal bDetached ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e0822-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0822-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0822-114">*Signatário* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e0822-114">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0822-115">Uma referência ao objeto de [**signatário**](signer.md) do signatário dos dados.</span><span class="sxs-lookup"><span data-stu-id="e0822-115">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="e0822-116">O objeto de **signatário** deve ter acesso à [*chave privada*](../secgloss/p-gly.md) do [*certificado*](../secgloss/c-gly.md) usado para assinar.</span><span class="sxs-lookup"><span data-stu-id="e0822-116">The **Signer** object must have access to the [*private key*](../secgloss/p-gly.md) of the [*certificate*](../secgloss/c-gly.md) used to sign.</span></span> <span data-ttu-id="e0822-117">Esse parâmetro pode ser **nulo**; para obter mais informações, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="e0822-117">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e0822-118">*bDetached* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e0822-118">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0822-119">Se **for true**, os dados a serem assinados serão desanexados; ou seja, o conteúdo assinado não é incluído como parte do objeto assinado.</span><span class="sxs-lookup"><span data-stu-id="e0822-119">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="e0822-120">Para verificar a assinatura no conteúdo desanexado, um aplicativo deve ter uma cópia do conteúdo original.</span><span class="sxs-lookup"><span data-stu-id="e0822-120">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="e0822-121">O conteúdo desanexado é geralmente usado para diminuir o tamanho de um objeto assinado a ser enviado pela Web, se o destinatário da mensagem assinada tiver uma cópia original dos dados assinados.</span><span class="sxs-lookup"><span data-stu-id="e0822-121">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="e0822-122">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="e0822-122">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="e0822-123">*EncodingType* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e0822-123">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0822-124">Um valor da enumeração [do \_ \_ tipo de codificação capicor](capicom-encoding-type.md) que indica como os dados assinados serão codificados.</span><span class="sxs-lookup"><span data-stu-id="e0822-124">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="e0822-125">O valor padrão é CAPICOM de \_ codificação \_ base64.</span><span class="sxs-lookup"><span data-stu-id="e0822-125">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="e0822-126">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0822-126">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e0822-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e0822-127">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="e0822-128">Significado</span><span class="sxs-lookup"><span data-stu-id="e0822-128">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="e0822-129"><dt>**CAPICOM \_ codificar \_ qualquer**</dt></span><span class="sxs-lookup"><span data-stu-id="e0822-129"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="e0822-130">Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e0822-130">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="e0822-131">Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="e0822-131">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="e0822-132">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e0822-132">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="e0822-133"><dt>**CAPICOM \_ codificar \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="e0822-133"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="e0822-134">Os dados são salvos como uma cadeia de caracteres codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="e0822-134">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="e0822-135"><dt>**capicote de \_ codificação \_ binário**</dt></span><span class="sxs-lookup"><span data-stu-id="e0822-135"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="e0822-136">Os dados são salvos como uma sequência binária pura.</span><span class="sxs-lookup"><span data-stu-id="e0822-136">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0822-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0822-137">Return value</span></span>

<span data-ttu-id="e0822-138">Esse método retorna uma cadeia de caracteres que contém os dados codificados e assinados.</span><span class="sxs-lookup"><span data-stu-id="e0822-138">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="e0822-139">Se esse método falhar, um erro será gerado.</span><span class="sxs-lookup"><span data-stu-id="e0822-139">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="e0822-140">O objeto **Err** conterá informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="e0822-140">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0822-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0822-141">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0822-142">Quando esse método é chamado de um script da Web, o script precisa usar sua chave privada para criar uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="e0822-142">When this method is called from a web script, the script needs to use your private key to create a digital signature.</span></span> <span data-ttu-id="e0822-143">Permitir que sites não confiáveis usem sua chave privada é um risco de segurança.</span><span class="sxs-lookup"><span data-stu-id="e0822-143">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="e0822-144">Uma caixa de diálogo que pergunta se o site pode usar sua chave privada é exibida quando esse método é chamado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="e0822-144">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="e0822-145">Se você permitir que o script Use sua chave privada para criar uma assinatura digital e selecionar "não mostrar esta caixa de diálogo novamente", a caixa de diálogo não será mais exibida para nenhum script dentro desse domínio que use sua chave privada para criar uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="e0822-145">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="e0822-146">No entanto, os scripts fora desse domínio que tentarem usar sua chave privada para criar uma assinatura digital ainda farão com que essa caixa de diálogo seja exibida.</span><span class="sxs-lookup"><span data-stu-id="e0822-146">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="e0822-147">Se você não permitir que o script Use sua chave privada e selecionar "não mostrar esta caixa de diálogo novamente", os scripts nesse domínio serão recusados automaticamente a capacidade de usar sua chave privada para criar assinaturas digitais.</span><span class="sxs-lookup"><span data-stu-id="e0822-147">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="e0822-148">Como a criação de uma [*assinatura digital*](../secgloss/d-gly.md) requer o uso de uma [*chave privada*](../secgloss/p-gly.md), os aplicativos baseados na Web que tentarem usar esse método exigirão prompts de interface do usuário que permitam ao usuário aprovar o uso da chave privada, por motivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="e0822-148">Because creating a [*digital signature*](../secgloss/d-gly.md) requires the use of a [*private key*](../secgloss/p-gly.md), web-based applications that attempt to use this method will require user interface prompts that allow the user to approve the use of the private key, for security reasons.</span></span>

<span data-ttu-id="e0822-149">Os seguintes resultados se aplicam ao valor do parâmetro de *signatário* :</span><span class="sxs-lookup"><span data-stu-id="e0822-149">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="e0822-150">Se o parâmetro de *signatário* não for **nulo**, esse método usará a chave privada apontada pelo certificado associado para criptografar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e0822-150">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="e0822-151">Se a chave privada apontada pelo certificado não estiver disponível, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="e0822-151">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="e0822-152">Se o parâmetro de *signatário* for **nulo** e houver exatamente um certificado no usuário atual \_ meu repositório que tenha acesso a uma chave privada, esse certificado será usado para criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e0822-152">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="e0822-153">Se o parâmetro de *signatário* for **nulo**, o valor da propriedade [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) for true e houver mais de um certificado no usuário atual \_ My Store com uma chave privada disponível, será exibida uma caixa de diálogo que permite ao usuário selecionar qual certificado será usado.</span><span class="sxs-lookup"><span data-stu-id="e0822-153">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="e0822-154">Se o parâmetro de *signatário* for **nulo** e a propriedade [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) for false, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="e0822-154">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="e0822-155">Se o parâmetro de *signatário* for **nulo** e não houver nenhum certificado no \_ usuário atual, meu repositório com uma chave privada disponível, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="e0822-155">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0822-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0822-156">Requirements</span></span>



| <span data-ttu-id="e0822-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0822-157">Requirement</span></span> | <span data-ttu-id="e0822-158">Valor</span><span class="sxs-lookup"><span data-stu-id="e0822-158">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0822-159">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e0822-159">Redistributable</span></span><br/> | <span data-ttu-id="e0822-160">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e0822-160">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e0822-161">DLL</span><span class="sxs-lookup"><span data-stu-id="e0822-161">DLL</span></span><br/>             | <dl> <span data-ttu-id="e0822-162"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0822-162"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0822-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0822-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0822-164">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="e0822-164">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="e0822-165">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="e0822-165">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
