---
description: Enumera o nome dos CSPs (provedores de serviço de criptografia) disponíveis.
ms.assetid: d0dc8a8a-afff-4ccc-96e0-2c52913c3322
title: 'Método ISCrdEnr:: enumCSPName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCSPName
- SCrdEnr.enumCSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e7bba587b56300cd02efd81758288d3b77c65a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506174"
---
# <a name="iscrdenrenumcspname-method"></a><span data-ttu-id="511a6-103">Método ISCrdEnr:: enumCSPName</span><span class="sxs-lookup"><span data-stu-id="511a6-103">ISCrdEnr::enumCSPName method</span></span>

<span data-ttu-id="511a6-104">O método **enumCSPName** enumera o nome dos CSPs ( [*provedores de serviço de criptografia*](../secgloss/c-gly.md) ) disponíveis.</span><span class="sxs-lookup"><span data-stu-id="511a6-104">The **enumCSPName** method enumerates the name of the available [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs).</span></span>

## <a name="syntax"></a><span data-ttu-id="511a6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="511a6-105">Syntax</span></span>


```C++
HRESULT enumCSPName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCSPName
);
```


```VB

SCrdEnr.enumCSPName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCSPName _
)
```





## <a name="parameters"></a><span data-ttu-id="511a6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="511a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="511a6-107">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="511a6-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="511a6-108">O índice de base zero para a sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="511a6-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="511a6-109">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="511a6-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="511a6-110">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="511a6-110">Reserved for future use.</span></span> <span data-ttu-id="511a6-111">Defina esse valor como zero.</span><span class="sxs-lookup"><span data-stu-id="511a6-111">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="511a6-112">*pbstrCSPName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="511a6-112">*pbstrCSPName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="511a6-113">Um ponteiro para uma cadeia de caracteres que retorna o nome do CSP enumerado.</span><span class="sxs-lookup"><span data-stu-id="511a6-113">A pointer to a string that returns the name of the enumerated CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="511a6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="511a6-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="511a6-115">C++</span><span class="sxs-lookup"><span data-stu-id="511a6-115">C++</span></span>

<span data-ttu-id="511a6-116">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="511a6-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="511a6-117">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="511a6-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="511a6-118">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="511a6-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="511a6-119">VB</span><span class="sxs-lookup"><span data-stu-id="511a6-119">VB</span></span>

<span data-ttu-id="511a6-120">Uma cadeia de caracteres que representa o nome do CSP enumerado.</span><span class="sxs-lookup"><span data-stu-id="511a6-120">A string that represents the name of the enumerated CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="511a6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="511a6-121">Requirements</span></span>



| <span data-ttu-id="511a6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="511a6-122">Requirement</span></span> | <span data-ttu-id="511a6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="511a6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="511a6-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="511a6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="511a6-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="511a6-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="511a6-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="511a6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="511a6-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="511a6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="511a6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="511a6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="511a6-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="511a6-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="511a6-130">IID</span><span class="sxs-lookup"><span data-stu-id="511a6-130">IID</span></span><br/>                      | <span data-ttu-id="511a6-131">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="511a6-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="511a6-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="511a6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="511a6-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="511a6-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="511a6-134">**ISCrdEnr::CSPCount**</span><span class="sxs-lookup"><span data-stu-id="511a6-134">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="511a6-135">**ISCrdEnr:: CSPName**</span><span class="sxs-lookup"><span data-stu-id="511a6-135">**ISCrdEnr::CSPName**</span></span>](iscrdenr-cspname.md)
</dt> </dl>

 

 
