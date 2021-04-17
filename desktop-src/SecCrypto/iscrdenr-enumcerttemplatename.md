---
description: Enumera os nomes de modelo de certificado.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: 'Método ISCrdEnr:: enumCertTemplateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCertTemplateName
- SCrdEnr.enumCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a0a4850143cac48ef9b9b853f99153d4daeb4366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754596"
---
# <a name="iscrdenrenumcerttemplatename-method"></a><span data-ttu-id="61cc7-103">Método ISCrdEnr:: enumCertTemplateName</span><span class="sxs-lookup"><span data-stu-id="61cc7-103">ISCrdEnr::enumCertTemplateName method</span></span>

<span data-ttu-id="61cc7-104">O método **enumCertTemplateName** enumera os nomes de modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="61cc7-104">The **enumCertTemplateName** method enumerates the certificate template names.</span></span>

## <a name="syntax"></a><span data-ttu-id="61cc7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61cc7-105">Syntax</span></span>


```C++
HRESULT enumCertTemplateName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.enumCertTemplateName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="61cc7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61cc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61cc7-107">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61cc7-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61cc7-108">O índice de base zero para a sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="61cc7-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="61cc7-109">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61cc7-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61cc7-110">Um valor que determina se o modelo de certificado enumerado se aplica a certificados de usuário ou computador.</span><span class="sxs-lookup"><span data-stu-id="61cc7-110">A value that determines whether the enumerated certificate template applies to user or machine certificates.</span></span> <span data-ttu-id="61cc7-111">Se esse valor for SCARTAR \_ registrar \_ o \_ modelo de certificado \_ do usuário (definido como 1), a enumeração se aplicará aos modelos de certificado do usuário.</span><span class="sxs-lookup"><span data-stu-id="61cc7-111">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1), the enumeration applies to user certificate templates.</span></span> <span data-ttu-id="61cc7-112">Se esse valor for SCARTAR \_ registrar \_ o \_ modelo de certificado \_ de máquina (definido como 2), a enumeração se aplicará aos modelos de certificado do computador.</span><span class="sxs-lookup"><span data-stu-id="61cc7-112">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2), the enumeration applies to machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="61cc7-113">*pbstrCertTemplateName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="61cc7-113">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61cc7-114">Um ponteiro para uma cadeia de caracteres que retorna o nome do modelo de certificado enumerado.</span><span class="sxs-lookup"><span data-stu-id="61cc7-114">A pointer to a string that returns the name of the enumerated certificate template.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61cc7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61cc7-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="61cc7-116">C++</span><span class="sxs-lookup"><span data-stu-id="61cc7-116">C++</span></span>

<span data-ttu-id="61cc7-117">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="61cc7-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="61cc7-118">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="61cc7-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="61cc7-119">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="61cc7-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="61cc7-120">VB</span><span class="sxs-lookup"><span data-stu-id="61cc7-120">VB</span></span>

<span data-ttu-id="61cc7-121">Uma cadeia de caracteres que contém o nome do modelo de certificado enumerado.</span><span class="sxs-lookup"><span data-stu-id="61cc7-121">A string that contains the name of the enumerated certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="61cc7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61cc7-122">Requirements</span></span>



| <span data-ttu-id="61cc7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="61cc7-123">Requirement</span></span> | <span data-ttu-id="61cc7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="61cc7-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61cc7-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61cc7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="61cc7-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="61cc7-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="61cc7-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61cc7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="61cc7-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="61cc7-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="61cc7-129">DLL</span><span class="sxs-lookup"><span data-stu-id="61cc7-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61cc7-130"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61cc7-130"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="61cc7-131">IID</span><span class="sxs-lookup"><span data-stu-id="61cc7-131">IID</span></span><br/>                      | <span data-ttu-id="61cc7-132">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="61cc7-132">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="61cc7-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="61cc7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61cc7-134">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="61cc7-134">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="61cc7-135">**ISCrdEnr::getCertTemplateCount**</span><span class="sxs-lookup"><span data-stu-id="61cc7-135">**ISCrdEnr::getCertTemplateCount**</span></span>](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[<span data-ttu-id="61cc7-136">**ISCrdEnr::getCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="61cc7-136">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[<span data-ttu-id="61cc7-137">**ISCrdEnr::setCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="61cc7-137">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




