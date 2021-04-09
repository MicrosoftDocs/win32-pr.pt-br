---
description: Recupera o nome da autoridade de certificação (CA) especificada para um determinado modelo de certificado.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: 'Método ISCrdEnr:: getCAName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b62b0a7e871a29ff0a8edd28eb8cd5e18e97c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171485"
---
# <a name="iscrdenrgetcaname-method"></a><span data-ttu-id="ff092-103">Método ISCrdEnr:: getCAName</span><span class="sxs-lookup"><span data-stu-id="ff092-103">ISCrdEnr::getCAName method</span></span>

<span data-ttu-id="ff092-104">O método **getCAName** recupera o nome da autoridade de [*certificação*](../secgloss/c-gly.md) (CA) especificada para um determinado modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="ff092-104">The **getCAName** method retrieves the name of the specified [*certification authority*](../secgloss/c-gly.md) (CA) for a given certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff092-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff092-105">Syntax</span></span>


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="ff092-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff092-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff092-107">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff092-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff092-108">Um valor que determina se o nome refere-se ao nome da autoridade de certificação ou ao nome da máquina da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="ff092-108">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="ff092-109">Se esse valor for SCARTAR \_ , registre o \_ \_ nome da máquina CA \_ (definido como 0x01) e o nome se referirá ao nome da máquina da autoridade de certificação; caso contrário, o nome se referirá ao nome da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="ff092-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01) then the name refers to the CA's machine name; otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="ff092-110">*bstrCertTemplateName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff092-110">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff092-111">O nome do modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="ff092-111">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="ff092-112">*pbstrCAName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ff092-112">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff092-113">Um ponteiro para uma cadeia de caracteres que retorna o nome da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="ff092-113">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff092-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff092-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="ff092-115">C++</span><span class="sxs-lookup"><span data-stu-id="ff092-115">C++</span></span>

<span data-ttu-id="ff092-116">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ff092-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="ff092-117">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="ff092-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="ff092-118">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="ff092-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="ff092-119">VB</span><span class="sxs-lookup"><span data-stu-id="ff092-119">VB</span></span>

<span data-ttu-id="ff092-120">Uma cadeia de caracteres que representa o nome da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="ff092-120">A string that represents the name of the CA.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff092-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff092-121">Remarks</span></span>

<span data-ttu-id="ff092-122">O nome da autoridade de certificação padrão é o nome da lista de CAs disponível.</span><span class="sxs-lookup"><span data-stu-id="ff092-122">The default CA name is the first name in the available list of CAs.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff092-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff092-123">Requirements</span></span>



| <span data-ttu-id="ff092-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff092-124">Requirement</span></span> | <span data-ttu-id="ff092-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ff092-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff092-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff092-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ff092-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ff092-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ff092-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff092-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ff092-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ff092-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff092-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ff092-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff092-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff092-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff092-132">IID</span><span class="sxs-lookup"><span data-stu-id="ff092-132">IID</span></span><br/>                      | <span data-ttu-id="ff092-133">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="ff092-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="ff092-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff092-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff092-135">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="ff092-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="ff092-136">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="ff092-136">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="ff092-137">**ISCrdEnr::getCACount**</span><span class="sxs-lookup"><span data-stu-id="ff092-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="ff092-138">**ISCrdEnr::setCAName**</span><span class="sxs-lookup"><span data-stu-id="ff092-138">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 
