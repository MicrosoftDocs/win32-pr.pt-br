---
description: Limpa o nome de usuário do controle de cartão inteligente.
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: 'Método ISCrdEnr:: resetUser'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.resetUser
- SCrdEnr.resetUser
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3b00721229890f82b00e7e7a41ccb8796a81b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756677"
---
# <a name="iscrdenrresetuser-method"></a><span data-ttu-id="09af8-103">Método ISCrdEnr:: resetUser</span><span class="sxs-lookup"><span data-stu-id="09af8-103">ISCrdEnr::resetUser method</span></span>

<span data-ttu-id="09af8-104">O método **resetUser** limpa o nome de usuário do controle de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="09af8-104">The **resetUser** method clears the user name from the smart card control.</span></span>

## <a name="syntax"></a><span data-ttu-id="09af8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09af8-105">Syntax</span></span>


```C++
HRESULT resetUser();
```



## <a name="parameters"></a><span data-ttu-id="09af8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09af8-106">Parameters</span></span>

<span data-ttu-id="09af8-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="09af8-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="09af8-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="09af8-108">Remarks</span></span>

<span data-ttu-id="09af8-109">Esse método limpa qualquer nome de usuário existente e certificado registrado anteriormente da memória.</span><span class="sxs-lookup"><span data-stu-id="09af8-109">This method clears any existing user name and previously enrolled certificate from memory.</span></span> <span data-ttu-id="09af8-110">No entanto, o certificado registrado anteriormente não é removido do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="09af8-110">The previously enrolled certificate is not removed from the smart card, however.</span></span>

## <a name="requirements"></a><span data-ttu-id="09af8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09af8-111">Requirements</span></span>



| <span data-ttu-id="09af8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="09af8-112">Requirement</span></span> | <span data-ttu-id="09af8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="09af8-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09af8-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09af8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="09af8-115">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="09af8-115">None supported</span></span><br/>                                                               |
| <span data-ttu-id="09af8-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09af8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="09af8-117">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="09af8-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="09af8-118">DLL</span><span class="sxs-lookup"><span data-stu-id="09af8-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09af8-119"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09af8-119"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="09af8-120">IID</span><span class="sxs-lookup"><span data-stu-id="09af8-120">IID</span></span><br/>                      | <span data-ttu-id="09af8-121">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="09af8-121">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="09af8-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="09af8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09af8-123">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="09af8-123">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="09af8-124">**ISCrdEnr:: GetUserName**</span><span class="sxs-lookup"><span data-stu-id="09af8-124">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="09af8-125">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="09af8-125">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="09af8-126">**ISCrdEnr:: SetUserName**</span><span class="sxs-lookup"><span data-stu-id="09af8-126">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




