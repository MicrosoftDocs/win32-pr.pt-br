---
description: Especifica o nome do usuário em cujo nome o registro de certificado é pretendido.
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: 'Método ISCrdEnr:: SetUserName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setUserName
- SCrdEnr.setUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: cc2d3157e41fc7ffd9fc0bf7f607de137559e751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758010"
---
# <a name="iscrdenrsetusername-method"></a><span data-ttu-id="6555d-103">Método ISCrdEnr:: SetUserName</span><span class="sxs-lookup"><span data-stu-id="6555d-103">ISCrdEnr::setUserName method</span></span>

<span data-ttu-id="6555d-104">O método **SetUserName** especifica o nome do usuário em cujo nome o registro de certificado é pretendido.</span><span class="sxs-lookup"><span data-stu-id="6555d-104">The **setUserName** method specifies the name of the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="6555d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6555d-105">Syntax</span></span>


```C++
HRESULT setUserName(
  [in] DWORD dwFlags,
  [in] BSTR bstrUserName
);
```


```VB

SCrdEnr.setUserName( _
  ByVal dwFlags, _
  ByVal bstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="6555d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6555d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6555d-107">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6555d-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6555d-108">Esse valor deve ser SCARTAR \_ \_ \_ nome UPN de registro (definido como 1) ou scartar \_ registrar \_ \_ nome compatível com Sam \_ (definido como 2).</span><span class="sxs-lookup"><span data-stu-id="6555d-108">This value must be either SCARD\_ENROLL\_UPN\_NAME (defined as 1) or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME (defined as 2).</span></span>

<span data-ttu-id="6555d-109">Defina esse valor como SCARTAR \_ registrar \_ \_ nome UPN, se o nome especificado em *bstrUserName* for o nome da entidade universal do usuário, como " someone@example.com ".</span><span class="sxs-lookup"><span data-stu-id="6555d-109">Set this value to SCARD\_ENROLL\_UPN\_NAME, if the name specified in *bstrUserName* is the user's Universal Principal Name, such as "someone@example.com".</span></span> <span data-ttu-id="6555d-110">O nome UPN do usuário deve corresponder a um nome de SAM (Gerenciador de acesso de segurança) existente.</span><span class="sxs-lookup"><span data-stu-id="6555d-110">The user's UPN name must correspond to an existing security access manager (SAM) name.</span></span>

<span data-ttu-id="6555d-111">Defina esse valor como SCARTAR \_ registrar \_ \_ nome compatível com Sam \_ , se o nome especificado em *bstrUserName* for o nome Sam do usuário no formato "domínio \\ usuário".</span><span class="sxs-lookup"><span data-stu-id="6555d-111">Set this value to SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, if the name specified in *bstrUserName* is the user's SAM name in the format of "DOMAIN\\USER".</span></span>

</dd> <dt>

<span data-ttu-id="6555d-112">*bstrUserName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6555d-112">*bstrUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6555d-113">Nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="6555d-113">Name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6555d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6555d-114">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="6555d-115">VB</span><span class="sxs-lookup"><span data-stu-id="6555d-115">VB</span></span>

<span data-ttu-id="6555d-116">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6555d-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="6555d-117">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="6555d-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="6555d-118">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="6555d-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6555d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6555d-119">Remarks</span></span>

<span data-ttu-id="6555d-120">Chame esse método para especificar o nome de usuário a ser emitido pelo [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6555d-120">Call this method to specify the user name to be issued the [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="6555d-121">Uma alternativa para **SetUserName** é [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md).</span><span class="sxs-lookup"><span data-stu-id="6555d-121">An alternative to **setUserName** is [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span>

<span data-ttu-id="6555d-122">Depois que um nome de usuário tiver sido especificado, seu valor poderá ser recuperado chamando [**GetUserName**](iscrdenr-getusername.md).</span><span class="sxs-lookup"><span data-stu-id="6555d-122">After a user name has been specified, its value can be retrieved by calling [**getUserName**](iscrdenr-getusername.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6555d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6555d-123">Requirements</span></span>



| <span data-ttu-id="6555d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6555d-124">Requirement</span></span> | <span data-ttu-id="6555d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6555d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6555d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6555d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6555d-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6555d-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6555d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6555d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6555d-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6555d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6555d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6555d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6555d-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6555d-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="6555d-132">IID</span><span class="sxs-lookup"><span data-stu-id="6555d-132">IID</span></span><br/>                      | <span data-ttu-id="6555d-133">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="6555d-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="6555d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6555d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6555d-135">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="6555d-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="6555d-136">**ISCrdEnr:: GetUserName**</span><span class="sxs-lookup"><span data-stu-id="6555d-136">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="6555d-137">**ISCrdEnr::resetUser**</span><span class="sxs-lookup"><span data-stu-id="6555d-137">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="6555d-138">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="6555d-138">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> </dl>

 

 
