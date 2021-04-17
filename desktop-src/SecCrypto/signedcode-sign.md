---
description: Cria uma assinatura digital Authenticode e assina o arquivo executável especificado na propriedade SignedCode. FileName.
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: Método SignedCode. Sign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36e5c813b997ae452d44764ed88f51b273c75528
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779941"
---
# <a name="signedcodesign-method"></a><span data-ttu-id="8df8c-103">Método SignedCode. Sign</span><span class="sxs-lookup"><span data-stu-id="8df8c-103">SignedCode.Sign method</span></span>

<span data-ttu-id="8df8c-104">\[O método **Sign** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="8df8c-104">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8df8c-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="8df8c-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="8df8c-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="8df8c-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="8df8c-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="8df8c-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="8df8c-108">O método **Sign** cria uma assinatura digital Authenticode e assina o arquivo executável especificado na propriedade [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="8df8c-108">The **Sign** method creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df8c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8df8c-109">Syntax</span></span>


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8df8c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8df8c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df8c-111">*Signatário* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8df8c-111">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8df8c-112">Um objeto de [**signatário**](signer.md) que tem acesso à chave privada do certificado usado para assinar o código.</span><span class="sxs-lookup"><span data-stu-id="8df8c-112">A [**Signer**](signer.md) object that has access to the private key of the certificate used to sign the code.</span></span> <span data-ttu-id="8df8c-113">O valor padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8df8c-113">The default value is **Null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df8c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8df8c-114">Return value</span></span>

<span data-ttu-id="8df8c-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8df8c-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8df8c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8df8c-116">Remarks</span></span>

<span data-ttu-id="8df8c-117">Antes que o método **Sign** seja chamado, o arquivo que contém o código deve ser especificado na propriedade [**filename**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="8df8c-117">Before the **Sign** method is called, the file that contains the code must be specified in the [**FileName**](signedcode-filename.md) property.</span></span>

<span data-ttu-id="8df8c-118">Se o arquivo executável já estiver assinado, esse método substituirá a assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="8df8c-118">If the executable file is already signed, this method overwrites the existing signature.</span></span>

<span data-ttu-id="8df8c-119">Os seguintes resultados se aplicam ao valor do parâmetro de *signatário* :</span><span class="sxs-lookup"><span data-stu-id="8df8c-119">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="8df8c-120">Se o parâmetro de *signatário* não for **nulo**, esse método usará a chave privada apontada pelo certificado associado para criptografar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="8df8c-120">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="8df8c-121">Se a chave privada apontada pelo certificado não estiver disponível, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="8df8c-121">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="8df8c-122">Se o parâmetro de *signatário* for **nulo** e houver exatamente um certificado no usuário atual \_ meu repositório que tenha acesso a uma chave privada com capacidade de assinatura de código, esse certificado será usado para criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="8df8c-122">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key with code signing capability, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="8df8c-123">Se o parâmetro de *signatário* for **nulo**, o valor da propriedade [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) for true e houver mais de um certificado no usuário atual \_ My Store com uma chave privada disponível com o recurso de assinatura de código, será exibida uma caixa de diálogo que permite ao usuário selecionar qual certificado será usado.</span><span class="sxs-lookup"><span data-stu-id="8df8c-123">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key with code signing capability, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="8df8c-124">Se o parâmetro de *signatário* for **nulo** e a propriedade [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) for false, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="8df8c-124">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="8df8c-125">Se o parâmetro de *signatário* for **nulo** e não houver certificados no usuário atual \_ meu repositório com uma chave privada disponível com capacidade de assinatura de código, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="8df8c-125">If the *Signer* parameter is **NULL** and there are no certificates in the CURRENT\_USER MY store with an available private key with code signing capability, the method fails.</span></span>

<span data-ttu-id="8df8c-126">Esse método usa o algoritmo de hash SHA-1.</span><span class="sxs-lookup"><span data-stu-id="8df8c-126">This method uses the SHA-1 hashing algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="8df8c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8df8c-127">Requirements</span></span>



| <span data-ttu-id="8df8c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8df8c-128">Requirement</span></span> | <span data-ttu-id="8df8c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8df8c-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8df8c-130">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="8df8c-130">Redistributable</span></span><br/> | <span data-ttu-id="8df8c-131">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="8df8c-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8df8c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8df8c-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="8df8c-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8df8c-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
