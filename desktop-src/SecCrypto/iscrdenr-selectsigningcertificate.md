---
description: Exibe uma caixa de diálogo Selecionar certificado, permitindo que um certificado de autenticação (também conhecido como certificado do agente de registro) seja selecionado.
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: 'Método ISCrdEnr:: selectSigningCertificate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectSigningCertificate
- SCrdEnr.selectSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a4ef3be0ef16797597f57c12e90736ba50109601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836983"
---
# <a name="iscrdenrselectsigningcertificate-method"></a><span data-ttu-id="d0f6e-103">Método ISCrdEnr:: selectSigningCertificate</span><span class="sxs-lookup"><span data-stu-id="d0f6e-103">ISCrdEnr::selectSigningCertificate method</span></span>

<span data-ttu-id="d0f6e-104">O método **selectSigningCertificate** exibe uma caixa de diálogo **Selecionar certificado** , permitindo que um certificado de autenticação (também conhecido como *certificado do agente de registro*) seja selecionado.</span><span class="sxs-lookup"><span data-stu-id="d0f6e-104">The **selectSigningCertificate** method displays a **Select Certificate** dialog box, allowing a signing certificate (also known as the *enrollment agent certificate*) to be selected.</span></span>

<span data-ttu-id="d0f6e-105">Antes de registrar em nome dos usuários, você deve selecionar um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d0f6e-105">Before enrolling on behalf of users, you must select a signing certificate.</span></span> <span data-ttu-id="d0f6e-106">A [*chave privada*](../secgloss/p-gly.md) associada a esse certificado de autenticação é usada para assinar uma \# solicitação PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="d0f6e-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="d0f6e-107">O PKCS \# 7, por sua vez, contém a solicitação PKCS \# 10 do usuário (que é assinada com a chave privada do usuário).</span><span class="sxs-lookup"><span data-stu-id="d0f6e-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f6e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0f6e-108">Syntax</span></span>


```C++
HRESULT selectSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.selectSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="d0f6e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0f6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0f6e-110">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0f6e-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f6e-111">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d0f6e-111">Reserved for future use.</span></span> <span data-ttu-id="d0f6e-112">Defina esse valor como zero.</span><span class="sxs-lookup"><span data-stu-id="d0f6e-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="d0f6e-113">*bstrCertTemplateName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0f6e-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f6e-114">Uma cadeia de caracteres que representa o nome do modelo de certificado para o certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d0f6e-114">A string that represents the name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="d0f6e-115">Você pode usar o valor "EnrollmentAgent" se tiver obtido um certificado EnrollmentAgent.</span><span class="sxs-lookup"><span data-stu-id="d0f6e-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0f6e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0f6e-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="d0f6e-117">VB</span><span class="sxs-lookup"><span data-stu-id="d0f6e-117">VB</span></span>

<span data-ttu-id="d0f6e-118">Se o método for bem sucedido, o método retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d0f6e-118">If the method succeeds, the method returns **S\_OK**.</span></span>

<span data-ttu-id="d0f6e-119">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="d0f6e-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="d0f6e-120">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="d0f6e-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0f6e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0f6e-121">Remarks</span></span>

<span data-ttu-id="d0f6e-122">Antes de registrar em nome de um usuário, primeiro você deve obter um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d0f6e-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="d0f6e-123">Você pode obter um certificado de autenticação usando o snap-in do MMC do Gerenciador de certificados.</span><span class="sxs-lookup"><span data-stu-id="d0f6e-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="d0f6e-124">O método **selectSigningCertificate** não obtém o certificado de autenticação, mas exibe uma caixa de diálogo de certificados de assinatura obtidos anteriormente, permitindo que você escolha qual certificado será usado para assinar as solicitações de registro em nome.</span><span class="sxs-lookup"><span data-stu-id="d0f6e-124">The **selectSigningCertificate** method does not obtain the signing certificate but displays a dialog box of previously obtained signing certificates, allowing you to choose which certificate will be used to sign the enroll-on-behalf requests.</span></span>

<span data-ttu-id="d0f6e-125">Uma alternativa para **selectSigningCertificate** é [**ISCrdEnr:: setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="d0f6e-125">An alternative to **selectSigningCertificate** is [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span>

<span data-ttu-id="d0f6e-126">Depois que um certificado de assinatura é selecionado, seu nome pode ser recuperado chamando [**ISCrdEnr:: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span><span class="sxs-lookup"><span data-stu-id="d0f6e-126">After a signing certificate is selected, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0f6e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0f6e-127">Requirements</span></span>



| <span data-ttu-id="d0f6e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0f6e-128">Requirement</span></span> | <span data-ttu-id="d0f6e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d0f6e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f6e-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0f6e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d0f6e-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d0f6e-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d0f6e-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0f6e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d0f6e-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0f6e-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d0f6e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d0f6e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0f6e-135"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0f6e-135"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0f6e-136">IID</span><span class="sxs-lookup"><span data-stu-id="d0f6e-136">IID</span></span><br/>                      | <span data-ttu-id="d0f6e-137">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="d0f6e-137">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d0f6e-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0f6e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f6e-139">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="d0f6e-139">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="d0f6e-140">**ISCrdEnr::getSigningCertificateName**</span><span class="sxs-lookup"><span data-stu-id="d0f6e-140">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
