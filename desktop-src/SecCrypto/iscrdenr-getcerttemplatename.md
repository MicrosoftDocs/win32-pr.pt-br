---
description: Recupera o nome do modelo de certificado.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: 'Método ISCrdEnr:: getCertTemplateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4eee84140e0a23b8a0dd5d26099ca61b868a90fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171483"
---
# <a name="iscrdenrgetcerttemplatename-method"></a><span data-ttu-id="50632-103">Método ISCrdEnr:: getCertTemplateName</span><span class="sxs-lookup"><span data-stu-id="50632-103">ISCrdEnr::getCertTemplateName method</span></span>

<span data-ttu-id="50632-104">O método **getCertTemplateName** recupera o nome do modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="50632-104">The **getCertTemplateName** method retrieves the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="50632-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50632-105">Syntax</span></span>


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="50632-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50632-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50632-107">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50632-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50632-108">Um valor que determina se o nome real ou o nome de exibição do modelo de certificado é retornado.</span><span class="sxs-lookup"><span data-stu-id="50632-108">A value that determines whether the certificate template's real name or display name is returned.</span></span> <span data-ttu-id="50632-109">Se *dwFlags* tiver o valor scartar \_ registrar \_ o \_ \_ nome de exibição do modelo de certificado \_ , o nome de exibição do modelo de certificados será recuperado; caso contrário, o nome real do modelo de certificado será exibido.</span><span class="sxs-lookup"><span data-stu-id="50632-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is retrieved; otherwise, the real name of the certificate template is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="50632-110">*pbstrCertTemplateName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="50632-110">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50632-111">Um ponteiro para uma cadeia de caracteres que retorna o nome do modelo de certificado que será usado na [*solicitação de certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="50632-111">A pointer to a string that returns the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50632-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50632-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="50632-113">C++</span><span class="sxs-lookup"><span data-stu-id="50632-113">C++</span></span>

<span data-ttu-id="50632-114">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="50632-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="50632-115">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="50632-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="50632-116">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="50632-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="50632-117">VB</span><span class="sxs-lookup"><span data-stu-id="50632-117">VB</span></span>

<span data-ttu-id="50632-118">Uma cadeia de caracteres que representa o nome do modelo de certificado que será usado na [*solicitação de certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="50632-118">A string that represents the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="50632-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="50632-119">Remarks</span></span>

<span data-ttu-id="50632-120">Se você não definir o nome do modelo de certificado chamando [**ISCrdEnr:: setCertTemplateName**](iscrdenr-setcerttemplatename.md), o nome será padronizado como o nome na lista de modelos de certificado disponíveis.</span><span class="sxs-lookup"><span data-stu-id="50632-120">If you do not set the certificate template name by calling [**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md), the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="50632-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50632-121">Requirements</span></span>



| <span data-ttu-id="50632-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="50632-122">Requirement</span></span> | <span data-ttu-id="50632-123">Valor</span><span class="sxs-lookup"><span data-stu-id="50632-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50632-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50632-124">Minimum supported client</span></span><br/> | <span data-ttu-id="50632-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="50632-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="50632-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50632-126">Minimum supported server</span></span><br/> | <span data-ttu-id="50632-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50632-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50632-128">DLL</span><span class="sxs-lookup"><span data-stu-id="50632-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50632-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50632-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="50632-130">IID</span><span class="sxs-lookup"><span data-stu-id="50632-130">IID</span></span><br/>                      | <span data-ttu-id="50632-131">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="50632-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="50632-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="50632-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50632-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="50632-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="50632-134">**ISCrdEnr::setCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="50632-134">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
