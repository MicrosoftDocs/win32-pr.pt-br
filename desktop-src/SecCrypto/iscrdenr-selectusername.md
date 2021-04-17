---
description: Exibe uma interface do usuário selecionada, permitindo que um nome de usuário seja selecionado.
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: 'Método ISCrdEnr:: selectUserName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectUserName
- SCrdEnr.selectUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 13059775abc8520c39a0ad3dea2d604fc8d65455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755044"
---
# <a name="iscrdenrselectusername-method"></a><span data-ttu-id="d526b-103">Método ISCrdEnr:: selectUserName</span><span class="sxs-lookup"><span data-stu-id="d526b-103">ISCrdEnr::selectUserName method</span></span>

<span data-ttu-id="d526b-104">O método **selectUserName** exibe uma interface do **usuário** selecionada, permitindo que um nome de usuário seja selecionado.</span><span class="sxs-lookup"><span data-stu-id="d526b-104">The **selectUserName** method displays a **Select User** interface, allowing a user name to be selected.</span></span>

<span data-ttu-id="d526b-105">O nome de usuário se aplica ao usuário em cujo nome o registro de certificado é pretendido.</span><span class="sxs-lookup"><span data-stu-id="d526b-105">The user name applies to the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="d526b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d526b-106">Syntax</span></span>


```C++
HRESULT selectUserName(
  [in] DWORD dwFlags
);
```


```VB

SCrdEnr.selectUserName( _
  ByVal dwFlags _
)
```





## <a name="parameters"></a><span data-ttu-id="d526b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d526b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d526b-108">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d526b-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d526b-109">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d526b-109">Reserved for future use.</span></span> <span data-ttu-id="d526b-110">Defina esse valor como zero.</span><span class="sxs-lookup"><span data-stu-id="d526b-110">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d526b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d526b-111">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="d526b-112">VB</span><span class="sxs-lookup"><span data-stu-id="d526b-112">VB</span></span>

<span data-ttu-id="d526b-113">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d526b-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="d526b-114">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="d526b-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="d526b-115">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="d526b-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d526b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d526b-116">Remarks</span></span>

<span data-ttu-id="d526b-117">Use esse método para selecionar o nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="d526b-117">Use this method to select the name of the user.</span></span> <span data-ttu-id="d526b-118">Depois que um nome de usuário tiver sido selecionado, seu valor poderá ser recuperado chamando o método [**ISCrdEnr:: GetUserName**](iscrdenr-getusername.md) .</span><span class="sxs-lookup"><span data-stu-id="d526b-118">After a user name has been selected, its value can be retrieved by calling the [**ISCrdEnr::getUserName**](iscrdenr-getusername.md) method.</span></span>

<span data-ttu-id="d526b-119">Uma alternativa ao uso da interface ' Selecionar usuário ' é especificar um usuário chamando o método [**ISCrdEnr:: SetUserName**](iscrdenr-setusername.md) .</span><span class="sxs-lookup"><span data-stu-id="d526b-119">An alternative to using the 'Select User' interface is to specify a user by calling the [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d526b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d526b-120">Requirements</span></span>



| <span data-ttu-id="d526b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d526b-121">Requirement</span></span> | <span data-ttu-id="d526b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d526b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d526b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d526b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d526b-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d526b-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d526b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d526b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d526b-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d526b-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d526b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d526b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d526b-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d526b-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="d526b-129">IID</span><span class="sxs-lookup"><span data-stu-id="d526b-129">IID</span></span><br/>                      | <span data-ttu-id="d526b-130">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="d526b-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d526b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d526b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d526b-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="d526b-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="d526b-133">**ISCrdEnr:: GetUserName**</span><span class="sxs-lookup"><span data-stu-id="d526b-133">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="d526b-134">**ISCrdEnr::resetUser**</span><span class="sxs-lookup"><span data-stu-id="d526b-134">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="d526b-135">**ISCrdEnr:: SetUserName**</span><span class="sxs-lookup"><span data-stu-id="d526b-135">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




