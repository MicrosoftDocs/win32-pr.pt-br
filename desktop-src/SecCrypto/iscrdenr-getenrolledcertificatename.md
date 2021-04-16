---
description: 'Recupera o nome do certificado resultante de uma chamada bem-sucedida anterior para ISCrdEnr:: inscrever.'
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: 'Método ISCrdEnr:: getEnrolledCertificateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getEnrolledCertificateName
- SCrdEnr.getEnrolledCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3c9640e7719d2b5ac0e576384246cda5e1b2bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758162"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a><span data-ttu-id="24a5a-103">Método ISCrdEnr:: getEnrolledCertificateName</span><span class="sxs-lookup"><span data-stu-id="24a5a-103">ISCrdEnr::getEnrolledCertificateName method</span></span>

<span data-ttu-id="24a5a-104">O método **getEnrolledCertificateName** recupera o nome do certificado resultante de uma chamada bem-sucedida anterior para [**ISCrdEnr:: Enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="24a5a-104">The **getEnrolledCertificateName** method retrieves the name of the certificate resulting from an earlier successful call to [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).</span></span>

<span data-ttu-id="24a5a-105">Esse método também pode ser usado para exibir o certificado em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="24a5a-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="24a5a-106">Esse método chama a [](../secgloss/c-gly.md) função CryptoAPI [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="24a5a-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="24a5a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24a5a-107">Syntax</span></span>


```C++
HRESULT getEnrolledCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pBstrCertName
);
```


```VB

SCrdEnr.getEnrolledCertificateName( _
  ByVal dwFlags, _
  ByRef pBstrCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="24a5a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24a5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24a5a-109">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="24a5a-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a5a-110">Um valor que determina se o certificado é exibido em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="24a5a-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="24a5a-111">Se esse valor for SCARTAR não \_ registrar \_ nenhum certificado de \_ exibição \_ (definido como 0x01), o certificado registrado não será exibido; qualquer outro valor fará com que o certificado registrado seja exibido na caixa de diálogo **certificado** .</span><span class="sxs-lookup"><span data-stu-id="24a5a-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the enrolled certificate is not displayed; any other values cause the enrolled certificate to be displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="24a5a-112">*pBstrCertName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="24a5a-112">*pBstrCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24a5a-113">Um ponteiro para uma cadeia de caracteres que retorna o nome do certificado recuperado.</span><span class="sxs-lookup"><span data-stu-id="24a5a-113">A pointer to a string that returns the retrieved certificate name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24a5a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24a5a-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="24a5a-115">C++</span><span class="sxs-lookup"><span data-stu-id="24a5a-115">C++</span></span>

<span data-ttu-id="24a5a-116">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="24a5a-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="24a5a-117">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="24a5a-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="24a5a-118">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="24a5a-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="24a5a-119">VB</span><span class="sxs-lookup"><span data-stu-id="24a5a-119">VB</span></span>

<span data-ttu-id="24a5a-120">Uma cadeia de caracteres que representa o nome do certificado recuperado.</span><span class="sxs-lookup"><span data-stu-id="24a5a-120">A string that represents the retrieved certificate name.</span></span>

## <a name="remarks"></a><span data-ttu-id="24a5a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="24a5a-121">Remarks</span></span>

<span data-ttu-id="24a5a-122">Como esse método opera em um certificado existente, você deve ter chamado [**ISCrdEnr:: registro**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) com êxito para poder chamar **getEnrolledCertificateName**.</span><span class="sxs-lookup"><span data-stu-id="24a5a-122">Because this method operates on an existing certificate, you must have successfully called [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) before you can call **getEnrolledCertificateName**.</span></span>

<span data-ttu-id="24a5a-123">O método **getEnrolledCertificateName** chama a função [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) para recuperar o nome do certificado de acordo com a sequência descrita para \_ o \_ \_ \_ valor de tipo de exibição simples de nome de certificado do parâmetro *dwType* de **CertGetNameString**.</span><span class="sxs-lookup"><span data-stu-id="24a5a-123">The **getEnrolledCertificateName** method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the certificate name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="24a5a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24a5a-124">Requirements</span></span>



| <span data-ttu-id="24a5a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="24a5a-125">Requirement</span></span> | <span data-ttu-id="24a5a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="24a5a-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24a5a-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24a5a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="24a5a-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="24a5a-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="24a5a-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24a5a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="24a5a-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24a5a-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24a5a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="24a5a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24a5a-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24a5a-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="24a5a-133">IID</span><span class="sxs-lookup"><span data-stu-id="24a5a-133">IID</span></span><br/>                      | <span data-ttu-id="24a5a-134">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="24a5a-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="24a5a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="24a5a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a5a-136">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="24a5a-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="24a5a-137">[**ISCrdEnr:: inscrever**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24a5a-137">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 
