---
description: Usado para determinar se um modelo de certificado contém o \_ uso da chave de proteção de email szOID PKIX \_ KP \_ \_ .
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: 'Método ISCrdEnr:: getCertTemplateSMIME'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4ed66af6a8a91855fbfc5a972a8bf00358314663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829529"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a><span data-ttu-id="f6fc6-103">Método ISCrdEnr:: getCertTemplateSMIME</span><span class="sxs-lookup"><span data-stu-id="f6fc6-103">ISCrdEnr::getCertTemplateSMIME method</span></span>

<span data-ttu-id="f6fc6-104">O método **getCertTemplateSMIME** é usado para determinar se um modelo de certificado contém o \_ uso da chave de proteção de email szOID PKIX \_ KP \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f6fc6-104">The **getCertTemplateSMIME** method is used to determine whether a certificate template contains the szOID\_PKIX\_KP\_EMAIL\_PROTECTION key usage.</span></span>

<span data-ttu-id="f6fc6-105">Se esse uso de chave fizer parte do modelo de certificado, o modelo de certificado dará suporte a operações de S/MIME ( [*Internet Mail Extensions) seguras/multipropósitos*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f6fc6-105">If this key usage is part of the certificate template, the certificate template supports [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6fc6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6fc6-106">Syntax</span></span>


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a><span data-ttu-id="f6fc6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6fc6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6fc6-108">*bstrCertTemplateName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6fc6-108">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6fc6-109">O nome do certificado que está sendo consultado para o uso da chave S/MIME.</span><span class="sxs-lookup"><span data-stu-id="f6fc6-109">The name of the certificate being queried for the S/MIME key usage.</span></span>

</dd> <dt>

<span data-ttu-id="f6fc6-110">*pdwCertTemplateSMIME* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f6fc6-110">*pdwCertTemplateSMIME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6fc6-111">Um ponteiro para um **DWORD** que retorna um valor de um se *bstrCertTemplateName* dá suporte a S/MIME; caso contrário, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="f6fc6-111">A pointer to a **DWORD** that returns a value of one if *bstrCertTemplateName* supports S/MIME; otherwise it returns zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6fc6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6fc6-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="f6fc6-113">C++</span><span class="sxs-lookup"><span data-stu-id="f6fc6-113">C++</span></span>

<span data-ttu-id="f6fc6-114">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f6fc6-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="f6fc6-115">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="f6fc6-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="f6fc6-116">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="f6fc6-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="f6fc6-117">VB</span><span class="sxs-lookup"><span data-stu-id="f6fc6-117">VB</span></span>

<span data-ttu-id="f6fc6-118">Valor **longo** de um se *bstrCertTemplateName* dá suporte a S/MIME; caso contrário, zero.</span><span class="sxs-lookup"><span data-stu-id="f6fc6-118">**Long** value of one if *bstrCertTemplateName* supports S/MIME; otherwise zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6fc6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6fc6-119">Remarks</span></span>

<span data-ttu-id="f6fc6-120">A constante para szOID \_ PKIX \_ KP \_ email \_ Protection é definida em Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="f6fc6-120">The constant for szOID\_PKIX\_KP\_EMAIL\_PROTECTION is defined in Wincrypt.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6fc6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6fc6-121">Requirements</span></span>



| <span data-ttu-id="f6fc6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6fc6-122">Requirement</span></span> | <span data-ttu-id="f6fc6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f6fc6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6fc6-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6fc6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f6fc6-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f6fc6-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f6fc6-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6fc6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f6fc6-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f6fc6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f6fc6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f6fc6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6fc6-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6fc6-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6fc6-130">IID</span><span class="sxs-lookup"><span data-stu-id="f6fc6-130">IID</span></span><br/>                      | <span data-ttu-id="f6fc6-131">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="f6fc6-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f6fc6-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6fc6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6fc6-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="f6fc6-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="f6fc6-134">[**ISCrdEnr:: inscrever**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6fc6-134">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 
