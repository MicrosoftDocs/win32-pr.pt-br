---
description: Recupera o número de modelos de certificado.
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: 'Método ISCrdEnr:: getCertTemplateCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateCount
- SCrdEnr.getCertTemplateCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 86a78f03929bc6cdcfc7b611944b81c59a1c9fc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836984"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a><span data-ttu-id="8734b-103">Método ISCrdEnr:: getCertTemplateCount</span><span class="sxs-lookup"><span data-stu-id="8734b-103">ISCrdEnr::getCertTemplateCount method</span></span>

<span data-ttu-id="8734b-104">O método **getCertTemplateCount** recupera o número de modelos de certificado.</span><span class="sxs-lookup"><span data-stu-id="8734b-104">The **getCertTemplateCount** method retrieves the number of certificate templates.</span></span>

## <a name="syntax"></a><span data-ttu-id="8734b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8734b-105">Syntax</span></span>


```C++
HRESULT getCertTemplateCount(
  [in]  DWORD     dwFlags,
  [out] LONG *pdwCertTemplateCount
);
```


```VB

SCrdEnr.getCertTemplateCount( _
  ByVal dwFlags, _
  ByRef pdwCertTemplateCount _
)
```





## <a name="parameters"></a><span data-ttu-id="8734b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8734b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8734b-107">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8734b-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8734b-108">Um valor que determina se o modelo é para certificados de usuário ou computador.</span><span class="sxs-lookup"><span data-stu-id="8734b-108">A value that determines whether the template is for user or machine certificates.</span></span> <span data-ttu-id="8734b-109">Se esse valor for SCARTAR \_ registrar \_ \_ \_ o modelo de certificado do usuário (definido como 1), a contagem retornada será para modelos de certificado do usuário.</span><span class="sxs-lookup"><span data-stu-id="8734b-109">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1) then the returned count will be for user certificate templates.</span></span> <span data-ttu-id="8734b-110">Se esse valor for SCARTAR \_ registrar \_ \_ \_ o modelo de certificado de máquina (definido como 2), a contagem retornada será para modelos de certificado de máquina.</span><span class="sxs-lookup"><span data-stu-id="8734b-110">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2) then the returned count will be for machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="8734b-111">*pdwCertTemplateCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8734b-111">*pdwCertTemplateCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8734b-112">Um ponteiro para um **longo** que retorna o número de modelos de certificado.</span><span class="sxs-lookup"><span data-stu-id="8734b-112">A pointer to a **LONG** that returns the number of certificate templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8734b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8734b-113">Return value</span></span>

### <a name="c"></a><span data-ttu-id="8734b-114">C++</span><span class="sxs-lookup"><span data-stu-id="8734b-114">C++</span></span>

<span data-ttu-id="8734b-115">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8734b-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="8734b-116">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="8734b-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="8734b-117">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="8734b-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="8734b-118">VB</span><span class="sxs-lookup"><span data-stu-id="8734b-118">VB</span></span>

<span data-ttu-id="8734b-119">Um valor **longo** que representa o número de modelos de certificado.</span><span class="sxs-lookup"><span data-stu-id="8734b-119">A **Long** value that represents the number of certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="8734b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8734b-120">Requirements</span></span>



| <span data-ttu-id="8734b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8734b-121">Requirement</span></span> | <span data-ttu-id="8734b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8734b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8734b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8734b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8734b-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8734b-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8734b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8734b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8734b-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8734b-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8734b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8734b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8734b-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8734b-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="8734b-129">IID</span><span class="sxs-lookup"><span data-stu-id="8734b-129">IID</span></span><br/>                      | <span data-ttu-id="8734b-130">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="8734b-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="8734b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8734b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8734b-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="8734b-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="8734b-133">**ISCrdEnr::enumCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="8734b-133">**ISCrdEnr::enumCertTemplateName**</span></span>](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 




