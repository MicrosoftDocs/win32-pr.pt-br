---
description: Enumera o nome das autoridades de certificação (CAs) para um determinado nome de modelo de certificado.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: 'Método ISCrdEnr:: enumCAName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: c23df2f74cdf3791f1280e38cbff8ddd48f924b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758163"
---
# <a name="iscrdenrenumcaname-method"></a><span data-ttu-id="ef1cc-103">Método ISCrdEnr:: enumCAName</span><span class="sxs-lookup"><span data-stu-id="ef1cc-103">ISCrdEnr::enumCAName method</span></span>

<span data-ttu-id="ef1cc-104">O método **enumCAName** enumera o nome das CAS ( [*autoridades de certificação*](../secgloss/c-gly.md) ) para um determinado nome de modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-104">The **enumCAName** method enumerates the name of the [*certification authorities*](../secgloss/c-gly.md) (CAs) for a given certificate template name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1cc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef1cc-105">Syntax</span></span>


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="ef1cc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef1cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef1cc-107">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ef1cc-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1cc-108">O índice de base zero para a sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="ef1cc-109">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ef1cc-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1cc-110">Um valor que determina se o nome refere-se ao nome da autoridade de certificação ou ao nome da máquina da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-110">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="ef1cc-111">Se esse valor for SCARTAR \_ , registre o \_ \_ nome da máquina CA \_ (definido como 0x01), o nome se referirá ao nome da máquina da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-111">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="ef1cc-112">Caso contrário, o nome se refere ao nome da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-112">Otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="ef1cc-113">*bstrCertTemplateName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ef1cc-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1cc-114">O nome do modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-114">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="ef1cc-115">*pbstrCAName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ef1cc-115">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1cc-116">Um ponteiro para uma cadeia de caracteres que retorna o nome da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-116">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef1cc-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ef1cc-117">Return value</span></span>

### <a name="c"></a><span data-ttu-id="ef1cc-118">C++</span><span class="sxs-lookup"><span data-stu-id="ef1cc-118">C++</span></span>

<span data-ttu-id="ef1cc-119">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-119">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="ef1cc-120">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-120">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="ef1cc-121">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="ef1cc-121">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="ef1cc-122">VB</span><span class="sxs-lookup"><span data-stu-id="ef1cc-122">VB</span></span>

<span data-ttu-id="ef1cc-123">Uma cadeia de caracteres que representa o nome da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="ef1cc-123">A string that represents the name of the CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef1cc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef1cc-124">Requirements</span></span>



| <span data-ttu-id="ef1cc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef1cc-125">Requirement</span></span> | <span data-ttu-id="ef1cc-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ef1cc-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1cc-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef1cc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1cc-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ef1cc-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ef1cc-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef1cc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1cc-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef1cc-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ef1cc-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ef1cc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef1cc-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef1cc-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="ef1cc-133">IID</span><span class="sxs-lookup"><span data-stu-id="ef1cc-133">IID</span></span><br/>                      | <span data-ttu-id="ef1cc-134">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="ef1cc-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="ef1cc-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef1cc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef1cc-136">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="ef1cc-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="ef1cc-137">**ISCrdEnr::getCACount**</span><span class="sxs-lookup"><span data-stu-id="ef1cc-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="ef1cc-138">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="ef1cc-138">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> <dt>

[<span data-ttu-id="ef1cc-139">**ISCrdEnr::setCAName**</span><span class="sxs-lookup"><span data-stu-id="ef1cc-139">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 
