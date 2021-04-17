---
description: Especifica o nome do modelo de certificado.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: 'Método ISCrdEnr:: setCertTemplateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 53ba18626a7d2bb703ed4d11953fb4872cf9257c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758011"
---
# <a name="iscrdenrsetcerttemplatename-method"></a><span data-ttu-id="07d57-103">Método ISCrdEnr:: setCertTemplateName</span><span class="sxs-lookup"><span data-stu-id="07d57-103">ISCrdEnr::setCertTemplateName method</span></span>

<span data-ttu-id="07d57-104">O método **setCertTemplateName** especifica o nome do modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="07d57-104">The **setCertTemplateName** method specifies the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d57-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07d57-105">Syntax</span></span>


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="07d57-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07d57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d57-107">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07d57-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d57-108">Valor que determina se o nome real ou o nome de exibição do modelo de certificado está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="07d57-108">Value which determines if the certificate template's real name or display name is being set.</span></span> <span data-ttu-id="07d57-109">Se *dwFlags* tiver o valor scartar \_ registrar \_ o \_ \_ \_ nome de exibição do modelo de certificado, o nome de exibição do modelo será definido.</span><span class="sxs-lookup"><span data-stu-id="07d57-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is set.</span></span> <span data-ttu-id="07d57-110">Caso contrário, o nome real do modelo de certificado será definido.</span><span class="sxs-lookup"><span data-stu-id="07d57-110">Otherwise, the real name of the certificate template is set.</span></span>

</dd> <dt>

<span data-ttu-id="07d57-111">*bstrCertTemplateName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07d57-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d57-112">Nome do modelo de certificado que será usado na solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="07d57-112">Name of the certificate template which will be used in the certificate request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d57-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07d57-113">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="07d57-114">VB</span><span class="sxs-lookup"><span data-stu-id="07d57-114">VB</span></span>

<span data-ttu-id="07d57-115">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="07d57-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="07d57-116">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="07d57-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="07d57-117">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="07d57-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="07d57-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="07d57-118">Remarks</span></span>

<span data-ttu-id="07d57-119">Se você não definir o nome do modelo de certificado chamando **ISCrdEnr:: setCertTemplateName**, o nome será padronizado como o nome na lista de modelos de certificado disponíveis.</span><span class="sxs-lookup"><span data-stu-id="07d57-119">If you do not set the certificate template name by calling **ISCrdEnr::setCertTemplateName**, the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="07d57-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07d57-120">Requirements</span></span>



| <span data-ttu-id="07d57-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="07d57-121">Requirement</span></span> | <span data-ttu-id="07d57-122">Valor</span><span class="sxs-lookup"><span data-stu-id="07d57-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07d57-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07d57-123">Minimum supported client</span></span><br/> | <span data-ttu-id="07d57-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="07d57-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="07d57-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07d57-125">Minimum supported server</span></span><br/> | <span data-ttu-id="07d57-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="07d57-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="07d57-127">DLL</span><span class="sxs-lookup"><span data-stu-id="07d57-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07d57-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07d57-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="07d57-129">IID</span><span class="sxs-lookup"><span data-stu-id="07d57-129">IID</span></span><br/>                      | <span data-ttu-id="07d57-130">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="07d57-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="07d57-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="07d57-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d57-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="07d57-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="07d57-133">**ISCrdEnr::getCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="07d57-133">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




