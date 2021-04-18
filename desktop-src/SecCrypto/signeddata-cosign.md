---
description: Cria uma assinatura digital no conteúdo assinado anteriormente.
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: Método SignedData. cosign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.CoSign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1ab2a24a20fd65fad9622b775bedc59cfa28301a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770327"
---
# <a name="signeddatacosign-method"></a><span data-ttu-id="a8879-103">Método SignedData. cosign</span><span class="sxs-lookup"><span data-stu-id="a8879-103">SignedData.CoSign method</span></span>

<span data-ttu-id="a8879-104">\[O método de **coassinatura** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a8879-104">\[The **CoSign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a8879-105">Em vez disso, use a [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="a8879-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="a8879-106">O método de **coassinatura** cria uma [*assinatura digital*](../secgloss/d-gly.md) no conteúdo assinado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a8879-106">The **CoSign** method creates a [*digital signature*](../secgloss/d-gly.md) on previously signed content.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8879-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8879-107">Syntax</span></span>


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a8879-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8879-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8879-109">*Signatário* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a8879-109">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8879-110">Uma referência ao objeto de [**signatário**](signer.md) do signatário dos dados.</span><span class="sxs-lookup"><span data-stu-id="a8879-110">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="a8879-111">O objeto de **signatário** deve ter acesso à chave privada do certificado usado para assinar.</span><span class="sxs-lookup"><span data-stu-id="a8879-111">The **Signer** object must have access to the private key of the certificate used to sign.</span></span> <span data-ttu-id="a8879-112">Esse parâmetro pode ser **nulo**; para obter mais informações, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="a8879-112">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a8879-113">*EncodingType* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a8879-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8879-114">Um valor da enumeração [**do \_ \_ tipo de codificação capicor**](capicom-encoding-type.md) que indica como os dados assinados serão codificados.</span><span class="sxs-lookup"><span data-stu-id="a8879-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="a8879-115">O valor padrão é CAPICOM de \_ codificação \_ base64.</span><span class="sxs-lookup"><span data-stu-id="a8879-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="a8879-116">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a8879-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a8879-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a8879-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="a8879-118">Significado</span><span class="sxs-lookup"><span data-stu-id="a8879-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="a8879-119"><dt>**CAPICOM \_ codificar \_ qualquer**</dt></span><span class="sxs-lookup"><span data-stu-id="a8879-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="a8879-120">Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a8879-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="a8879-121">Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="a8879-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="a8879-122">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a8879-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="a8879-123"><dt>**CAPICOM \_ codificar \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="a8879-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="a8879-124">Os dados são salvos como uma cadeia de caracteres codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="a8879-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="a8879-125"><dt>**capicote de \_ codificação \_ binário**</dt></span><span class="sxs-lookup"><span data-stu-id="a8879-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="a8879-126">Os dados são salvos como uma sequência binária pura.</span><span class="sxs-lookup"><span data-stu-id="a8879-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8879-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8879-127">Return value</span></span>

<span data-ttu-id="a8879-128">Esse método retorna uma cadeia de caracteres que contém os dados codificados e assinados.</span><span class="sxs-lookup"><span data-stu-id="a8879-128">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="a8879-129">Se esse método falhar, um erro será gerado.</span><span class="sxs-lookup"><span data-stu-id="a8879-129">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="a8879-130">O objeto **Err** conterá informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="a8879-130">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8879-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8879-131">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8879-132">Quando esse método é chamado de um script da Web, o script precisa usar sua [*chave privada*](../secgloss/p-gly.md) para criar uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="a8879-132">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to create a digital signature.</span></span> <span data-ttu-id="a8879-133">Permitir que sites não confiáveis usem sua chave privada é um risco de segurança.</span><span class="sxs-lookup"><span data-stu-id="a8879-133">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="a8879-134">Uma caixa de diálogo que pergunta se o site pode usar sua chave privada é exibida quando esse método é chamado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="a8879-134">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="a8879-135">Se você permitir que o script Use sua chave privada para criar uma assinatura digital e selecionar "não mostrar esta caixa de diálogo novamente", a caixa de diálogo não será mais exibida para nenhum script dentro desse domínio que use sua chave privada para criar uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="a8879-135">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="a8879-136">No entanto, os scripts fora desse domínio que tentarem usar sua chave privada para criar uma assinatura digital ainda farão com que essa caixa de diálogo seja exibida.</span><span class="sxs-lookup"><span data-stu-id="a8879-136">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="a8879-137">Se você não permitir que o script Use sua chave privada e selecionar "não mostrar esta caixa de diálogo novamente", os scripts nesse domínio serão recusados automaticamente a capacidade de usar sua chave privada para criar assinaturas digitais.</span><span class="sxs-lookup"><span data-stu-id="a8879-137">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="a8879-138">Não há garantia de que os coassinados estejam em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="a8879-138">Cosigners are not guaranteed to be in any particular order.</span></span>

<span data-ttu-id="a8879-139">Os seguintes resultados se aplicam ao valor do parâmetro de *signatário* :</span><span class="sxs-lookup"><span data-stu-id="a8879-139">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="a8879-140">Se o parâmetro de *signatário* não for **nulo**, esse método usará a chave privada apontada pelo certificado associado para criptografar a coassinatura.</span><span class="sxs-lookup"><span data-stu-id="a8879-140">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the cosignature.</span></span> <span data-ttu-id="a8879-141">Se a chave privada apontada pelo certificado não estiver disponível, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="a8879-141">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="a8879-142">Se o parâmetro de *signatário* for **nulo** e houver exatamente um certificado no usuário atual \_ meu repositório que tenha acesso a uma chave privada, esse certificado será usado para criar a coassinatura.</span><span class="sxs-lookup"><span data-stu-id="a8879-142">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the cosignature.</span></span>
-   <span data-ttu-id="a8879-143">Se o parâmetro de *signatário* for **nulo**, o valor da propriedade [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) for true e houver mais de um certificado no usuário atual \_ My Store com uma chave privada disponível, será exibida uma caixa de diálogo que permite ao usuário selecionar qual certificado será usado.</span><span class="sxs-lookup"><span data-stu-id="a8879-143">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="a8879-144">Se o parâmetro de *signatário* for **nulo** e a propriedade [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) for false, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="a8879-144">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="a8879-145">Se o parâmetro de *signatário* for **nulo** e não houver nenhum certificado no \_ usuário atual, meu repositório com uma chave privada disponível, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="a8879-145">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8879-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8879-146">Requirements</span></span>



| <span data-ttu-id="a8879-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8879-147">Requirement</span></span> | <span data-ttu-id="a8879-148">Valor</span><span class="sxs-lookup"><span data-stu-id="a8879-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8879-149">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a8879-149">Redistributable</span></span><br/> | <span data-ttu-id="a8879-150">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8879-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a8879-151">DLL</span><span class="sxs-lookup"><span data-stu-id="a8879-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="a8879-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8879-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8879-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8879-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8879-154">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="a8879-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="a8879-155">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="a8879-155">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
