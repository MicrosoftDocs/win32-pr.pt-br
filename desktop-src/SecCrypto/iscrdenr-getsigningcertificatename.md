---
description: Recupera o nome da entidade do certificado de autenticação.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: 'Método ISCrdEnr:: getSigningCertificateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 8d9a8a84067e82a18e5066721f3e7f39d075c339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370737"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a><span data-ttu-id="8a3e0-103">Método ISCrdEnr:: getSigningCertificateName</span><span class="sxs-lookup"><span data-stu-id="8a3e0-103">ISCrdEnr::getSigningCertificateName method</span></span>

<span data-ttu-id="8a3e0-104">O método **getSigningCertificateName** recupera o nome da entidade do certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="8a3e0-104">The **getSigningCertificateName** method retrieves the subject name from the signing certificate.</span></span>

<span data-ttu-id="8a3e0-105">Esse método também pode ser usado para exibir o certificado em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8a3e0-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="8a3e0-106">Esse método chama a [](../secgloss/c-gly.md) função CryptoAPI [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="8a3e0-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a3e0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a3e0-107">Syntax</span></span>


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="8a3e0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a3e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a3e0-109">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a3e0-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a3e0-110">Um valor que determina se o certificado é exibido em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8a3e0-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="8a3e0-111">Se esse valor for SCARTAR \_ não \_ registrar \_ nenhum \_ certificado de exibição (definido como 0x01), o certificado de autenticação não será exibido; todos os outros valores resultarão na exibição do certificado de autenticação na caixa de diálogo **certificado** .</span><span class="sxs-lookup"><span data-stu-id="8a3e0-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the signing certificate is not displayed; any other values result in the signing certificate being displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="8a3e0-112">*pbstrSigningCertName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8a3e0-112">*pbstrSigningCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a3e0-113">Um ponteiro para uma cadeia de caracteres que retorna o nome do certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="8a3e0-113">A pointer to a string that returns the name of the signing certificate.</span></span> <span data-ttu-id="8a3e0-114">O certificado de autenticação será usado para assinar a [*solicitação de certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8a3e0-114">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a3e0-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a3e0-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="8a3e0-116">C++</span><span class="sxs-lookup"><span data-stu-id="8a3e0-116">C++</span></span>

<span data-ttu-id="8a3e0-117">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a3e0-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="8a3e0-118">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="8a3e0-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="8a3e0-119">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="8a3e0-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="8a3e0-120">VB</span><span class="sxs-lookup"><span data-stu-id="8a3e0-120">VB</span></span>

<span data-ttu-id="8a3e0-121">Uma cadeia de caracteres que representa o nome do certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="8a3e0-121">A string that represents the name of the signing certificate.</span></span> <span data-ttu-id="8a3e0-122">O certificado de autenticação será usado para assinar a [*solicitação de certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8a3e0-122">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a3e0-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a3e0-123">Remarks</span></span>

<span data-ttu-id="8a3e0-124">O método **getSigningCertificateName** retorna o nome da entidade do certificado que você (ou outro administrador) selecionou em uma chamada bem-sucedida anterior para [**ISCrdEnr:: selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) ou [**ISCrdEnr:: setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="8a3e0-124">The **getSigningCertificateName** method returns the subject name of the certificate you (or another administrator) have selected in a previous successful call to [**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) or [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span> <span data-ttu-id="8a3e0-125">Esse método chama a função [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) para recuperar o nome da entidade de acordo com a sequência descrita para \_ o \_ \_ \_ valor de tipo de exibição simples do nome do certificado do parâmetro *dwType* do **CertGetNameString**.</span><span class="sxs-lookup"><span data-stu-id="8a3e0-125">This method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the subject name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a3e0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a3e0-126">Requirements</span></span>



| <span data-ttu-id="8a3e0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a3e0-127">Requirement</span></span> | <span data-ttu-id="8a3e0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="8a3e0-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a3e0-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a3e0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8a3e0-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8a3e0-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8a3e0-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a3e0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8a3e0-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8a3e0-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8a3e0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8a3e0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a3e0-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a3e0-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a3e0-135">IID</span><span class="sxs-lookup"><span data-stu-id="8a3e0-135">IID</span></span><br/>                      | <span data-ttu-id="8a3e0-136">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="8a3e0-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="8a3e0-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a3e0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a3e0-138">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="8a3e0-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="8a3e0-139">**ISCrdEnr::selectSigningCertificate**</span><span class="sxs-lookup"><span data-stu-id="8a3e0-139">**ISCrdEnr::selectSigningCertificate**</span></span>](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
