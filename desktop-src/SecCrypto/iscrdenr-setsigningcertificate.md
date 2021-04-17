---
description: Especifica um certificado de autenticação (também conhecido como o certificado do agente de registro).
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: 'Método ISCrdEnr:: setSigningCertificate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: dd00ba19872cb0ba2b21981c79e8f7be03aa4937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755043"
---
# <a name="iscrdenrsetsigningcertificate-method"></a><span data-ttu-id="6835c-103">Método ISCrdEnr:: setSigningCertificate</span><span class="sxs-lookup"><span data-stu-id="6835c-103">ISCrdEnr::setSigningCertificate method</span></span>

<span data-ttu-id="6835c-104">O método **setSigningCertificate** especifica um certificado de autenticação (também conhecido como o *certificado do agente de registro*).</span><span class="sxs-lookup"><span data-stu-id="6835c-104">The **setSigningCertificate** method specifies a signing certificate (also known as the *enrollment agent certificate*).</span></span>

<span data-ttu-id="6835c-105">Antes de registrar em nome dos usuários, você deve selecionar ou definir um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="6835c-105">Before enrolling on behalf of users, you must select or set a signing certificate.</span></span> <span data-ttu-id="6835c-106">A [*chave privada*](../secgloss/p-gly.md) associada a esse certificado de autenticação é usada para assinar uma \# solicitação PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="6835c-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="6835c-107">O PKCS \# 7, por sua vez, contém a solicitação PKCS \# 10 do usuário (que é assinada com a chave privada do usuário).</span><span class="sxs-lookup"><span data-stu-id="6835c-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="6835c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6835c-108">Syntax</span></span>


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="6835c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6835c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6835c-110">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6835c-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6835c-111">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6835c-111">Reserved for future use.</span></span> <span data-ttu-id="6835c-112">Defina esse valor como zero.</span><span class="sxs-lookup"><span data-stu-id="6835c-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6835c-113">*bstrCertTemplateName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6835c-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6835c-114">Nome do modelo de certificado para o certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="6835c-114">Name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="6835c-115">Você pode usar o valor "EnrollmentAgent" se tiver obtido um certificado EnrollmentAgent.</span><span class="sxs-lookup"><span data-stu-id="6835c-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6835c-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6835c-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="6835c-117">VB</span><span class="sxs-lookup"><span data-stu-id="6835c-117">VB</span></span>

<span data-ttu-id="6835c-118">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6835c-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="6835c-119">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="6835c-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="6835c-120">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="6835c-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6835c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="6835c-121">Remarks</span></span>

<span data-ttu-id="6835c-122">Antes de registrar em nome de um usuário, primeiro você deve obter um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="6835c-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="6835c-123">Você pode obter um certificado de autenticação usando o snap-in do MMC do Gerenciador de certificados.</span><span class="sxs-lookup"><span data-stu-id="6835c-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="6835c-124">O método **setSigningCertificate** não obtém o certificado de autenticação, mas informa ao controle de registro de cartão inteligente que anteriormente obteve o certificado de autenticação a ser usado.</span><span class="sxs-lookup"><span data-stu-id="6835c-124">The **setSigningCertificate** method does not obtain the signing certificate but informs the Smart Card Enrollment Control which previously obtained signing certificate to use.</span></span> <span data-ttu-id="6835c-125">O método **setSigningCertificate** pesquisa o repositório "My" do chamador para o certificado de autenticação mais recente correspondente ao modelo de certificado especificado por *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="6835c-125">The **setSigningCertificate** method searches the caller's "My" store for the most recent signing certificate corresponding to the certificate template specified by *bstrCertTemplateName*.</span></span>

<span data-ttu-id="6835c-126">Uma alternativa para **setSigningCertificate** é **ISCrdEnr:: setSigningCertificate**.</span><span class="sxs-lookup"><span data-stu-id="6835c-126">An alternative to **setSigningCertificate** is **ISCrdEnr::setSigningCertificate**.</span></span>

<span data-ttu-id="6835c-127">Depois que um certificado de assinatura é definido, seu nome pode ser recuperado chamando [**ISCrdEnr:: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span><span class="sxs-lookup"><span data-stu-id="6835c-127">After a signing certificate is set, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6835c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6835c-128">Requirements</span></span>



| <span data-ttu-id="6835c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6835c-129">Requirement</span></span> | <span data-ttu-id="6835c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="6835c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6835c-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6835c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6835c-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6835c-132">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6835c-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6835c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6835c-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6835c-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6835c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6835c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6835c-136"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6835c-136"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="6835c-137">IID</span><span class="sxs-lookup"><span data-stu-id="6835c-137">IID</span></span><br/>                      | <span data-ttu-id="6835c-138">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="6835c-138">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="6835c-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="6835c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6835c-140">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="6835c-140">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="6835c-141">**ISCrdEnr::getSigningCertificateName**</span><span class="sxs-lookup"><span data-stu-id="6835c-141">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
