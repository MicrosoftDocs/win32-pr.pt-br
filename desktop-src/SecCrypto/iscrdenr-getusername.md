---
description: Recupera o nome do usuário em cujo nome o registro de certificado é pretendido.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: 'Método ISCrdEnr:: GetUserName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getUserName
- SCrdEnr.getUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 51f551a704f3a98b932e646c95810f928e73bac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297350"
---
# <a name="iscrdenrgetusername-method"></a><span data-ttu-id="dc998-103">Método ISCrdEnr:: GetUserName</span><span class="sxs-lookup"><span data-stu-id="dc998-103">ISCrdEnr::getUserName method</span></span>

<span data-ttu-id="dc998-104">O método **GetUserName** recupera o nome do usuário em cujo nome o registro de certificado é pretendido.</span><span class="sxs-lookup"><span data-stu-id="dc998-104">The **getUserName** method retrieves the name of the user on whose behalf the certificate enrollment is intended.</span></span>

<span data-ttu-id="dc998-105">Antes de chamar esse método, você deve especificar o nome de usuário em uma chamada para [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md) ou [**ISCrdEnr:: SetUserName**](iscrdenr-setusername.md).</span><span class="sxs-lookup"><span data-stu-id="dc998-105">Before calling this method, you must specify the user name in a call to [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md) or [**ISCrdEnr::setUserName**](iscrdenr-setusername.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc998-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc998-106">Syntax</span></span>


```C++
HRESULT getUserName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrUserName
);
```


```VB

SCrdEnr.getUserName( _
  ByVal dwFlags, _
  ByRef pbstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="dc998-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc998-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc998-108">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dc998-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc998-109">Esse valor deve ser zero (0), SCARTAR \_ \_ \_ nome UPN de registro ou scartar \_ registrar \_ \_ nome compatível com Sam \_ .</span><span class="sxs-lookup"><span data-stu-id="dc998-109">This value must be either zero (0), SCARD\_ENROLL\_UPN\_NAME, or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME.</span></span>

<span data-ttu-id="dc998-110">Se esse valor for SCARTAR \_ registrar \_ \_ nome UPN, **GetUserName** retornará o nome UPN (Universal principal Name) do usuário, como " someone@example.com ".</span><span class="sxs-lookup"><span data-stu-id="dc998-110">If this value is SCARD\_ENROLL\_UPN\_NAME, **getUserName** returns the user's Universal Principal Name (UPN), such as "someone@example.com".</span></span>

<span data-ttu-id="dc998-111">Se esse valor for SCARTAR \_ registrar \_ \_ nome compatível com Sam \_ , o método retornará o nome Sam (Security Access Manager) do usuário no formato "domínio \\ usuário".</span><span class="sxs-lookup"><span data-stu-id="dc998-111">If this value is SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, the method returns the user's security access manager (SAM) name in the format "DOMAIN\\USER".</span></span>

<span data-ttu-id="dc998-112">Se esse valor for zero, o método retornará o nome UPN do usuário, se ele existir.</span><span class="sxs-lookup"><span data-stu-id="dc998-112">If this value is zero, the method returns the user's UPN name if it exists.</span></span> <span data-ttu-id="dc998-113">Se o usuário não tiver um nome UPN, o método retornará o nome SAM do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc998-113">If the user does not have a UPN name, the method returns the user's SAM name.</span></span>

</dd> <dt>

<span data-ttu-id="dc998-114">*pbstrUserName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dc998-114">*pbstrUserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc998-115">Um ponteiro para uma cadeia de caracteres que retorna o nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc998-115">A pointer to a string that returns the name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc998-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dc998-116">Return value</span></span>

### <a name="c"></a><span data-ttu-id="dc998-117">C++</span><span class="sxs-lookup"><span data-stu-id="dc998-117">C++</span></span>

<span data-ttu-id="dc998-118">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dc998-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="dc998-119">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="dc998-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="dc998-120">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="dc998-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="dc998-121">VB</span><span class="sxs-lookup"><span data-stu-id="dc998-121">VB</span></span>

<span data-ttu-id="dc998-122">Cadeia de caracteres que representa o nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc998-122">String that represents the name of the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc998-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc998-123">Remarks</span></span>

<span data-ttu-id="dc998-124">Você pode especificar o nome do usuário para o qual o [*cartão inteligente*](../secgloss/s-gly.md) é emitido chamando [**ISCrdEnr:: SetUserName**](iscrdenr-setusername.md) ou [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md).</span><span class="sxs-lookup"><span data-stu-id="dc998-124">You can specify the name of the user to whom the [*smart card*](../secgloss/s-gly.md) is issued by calling either [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) or [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span> <span data-ttu-id="dc998-125">Depois que um nome de usuário tiver sido especificado, seu valor poderá ser recuperado chamando **GetUserName**.</span><span class="sxs-lookup"><span data-stu-id="dc998-125">After a user name has been specified, its value can be retrieved by calling **getUserName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc998-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc998-126">Requirements</span></span>



| <span data-ttu-id="dc998-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc998-127">Requirement</span></span> | <span data-ttu-id="dc998-128">Valor</span><span class="sxs-lookup"><span data-stu-id="dc998-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc998-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc998-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dc998-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dc998-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="dc998-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc998-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dc998-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dc998-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dc998-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dc998-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc998-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc998-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="dc998-135">IID</span><span class="sxs-lookup"><span data-stu-id="dc998-135">IID</span></span><br/>                      | <span data-ttu-id="dc998-136">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="dc998-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="dc998-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc998-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc998-138">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="dc998-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="dc998-139">**ISCrdEnr::resetUser**</span><span class="sxs-lookup"><span data-stu-id="dc998-139">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="dc998-140">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="dc998-140">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="dc998-141">**ISCrdEnr:: SetUserName**</span><span class="sxs-lookup"><span data-stu-id="dc998-141">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 
