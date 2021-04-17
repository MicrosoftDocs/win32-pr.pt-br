---
description: Retorna o número de autoridades de certificação (CAs) que desejam emitir um certificado com base no modelo de certificado especificado.
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: 'Método ISCrdEnr:: getCACount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780468"
---
# <a name="iscrdenrgetcacount-method"></a><span data-ttu-id="2fd83-103">Método ISCrdEnr:: getCACount</span><span class="sxs-lookup"><span data-stu-id="2fd83-103">ISCrdEnr::getCACount method</span></span>

<span data-ttu-id="2fd83-104">O método **getCACount** retorna o número de [*autoridades de certificação*](../secgloss/c-gly.md) (CAS) que desejam emitir um certificado com base no modelo de certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="2fd83-104">The **getCACount** method returns the number of [*certification authorities*](../secgloss/c-gly.md) (CAs) willing to issue a certificate based on the specified certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd83-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2fd83-105">Syntax</span></span>


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a><span data-ttu-id="2fd83-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2fd83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fd83-107">*bstrCertTemplateName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2fd83-107">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fd83-108">Uma cadeia de caracteres que representa o nome do modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="2fd83-108">A string that represents the name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="2fd83-109">*pdwCACount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2fd83-109">*pdwCACount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fd83-110">Um ponteiro para um **longo** que retorna o número de CAS disponíveis que emitirão um certificado para o modelo de certificado especificado em *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="2fd83-110">A pointer to a **LONG** that returns the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fd83-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2fd83-111">Return value</span></span>

### <a name="c"></a><span data-ttu-id="2fd83-112">C++</span><span class="sxs-lookup"><span data-stu-id="2fd83-112">C++</span></span>

<span data-ttu-id="2fd83-113">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2fd83-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="2fd83-114">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="2fd83-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="2fd83-115">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="2fd83-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="2fd83-116">VB</span><span class="sxs-lookup"><span data-stu-id="2fd83-116">VB</span></span>

<span data-ttu-id="2fd83-117">Um valor **longo** que representa o número de CAS disponíveis que emitirão um certificado para o modelo de certificado especificado em *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="2fd83-117">A **Long** value that represents the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fd83-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fd83-118">Requirements</span></span>



| <span data-ttu-id="2fd83-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fd83-119">Requirement</span></span> | <span data-ttu-id="2fd83-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2fd83-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd83-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2fd83-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2fd83-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2fd83-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2fd83-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2fd83-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2fd83-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2fd83-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2fd83-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2fd83-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fd83-126"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fd83-126"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="2fd83-127">IID</span><span class="sxs-lookup"><span data-stu-id="2fd83-127">IID</span></span><br/>                      | <span data-ttu-id="2fd83-128">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="2fd83-128">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="2fd83-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2fd83-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fd83-130">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="2fd83-130">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="2fd83-131">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="2fd83-131">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="2fd83-132">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="2fd83-132">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 
