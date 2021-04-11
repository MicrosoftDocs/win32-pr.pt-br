---
description: Uma função definida pelo aplicativo que manipula ACEs (entradas de controle de acesso) de retorno de chamada durante uma verificação de acesso.
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: Função de retorno de chamada AuthzAccessCheckCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 82e100092dd7c59e9cc689aa8723365fae8bed29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172324"
---
# <a name="authzaccesscheckcallback-callback-function"></a><span data-ttu-id="78733-103">Função de retorno de chamada AuthzAccessCheckCallback</span><span class="sxs-lookup"><span data-stu-id="78733-103">AuthzAccessCheckCallback callback function</span></span>

<span data-ttu-id="78733-104">A função **AuthzAccessCheckCallback** é uma função definida pelo aplicativo que manipula ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) de retorno de chamada durante uma verificação de acesso.</span><span class="sxs-lookup"><span data-stu-id="78733-104">The **AuthzAccessCheckCallback** function is an application-defined function that handles callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) during an access check.</span></span> <span data-ttu-id="78733-105">**AuthzAccessCheckCallback** é um espaço reservado para o nome da função definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="78733-105">**AuthzAccessCheckCallback** is a placeholder for the application-defined function name.</span></span> <span data-ttu-id="78733-106">O aplicativo registra esse retorno de chamada chamando [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).</span><span class="sxs-lookup"><span data-stu-id="78733-106">The application registers this callback by calling [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).</span></span>

## <a name="syntax"></a><span data-ttu-id="78733-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78733-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a><span data-ttu-id="78733-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78733-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78733-109">*hAuthzClientContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78733-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78733-110">Um identificador para um contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="78733-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="78733-111">*ritmo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78733-111">*pAce* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78733-112">Um ponteiro para a ACE a ser avaliada para inclusão na chamada à função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="78733-112">A pointer to the ACE to evaluate for inclusion in the call to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

</dd> <dt>

<span data-ttu-id="78733-113">*pArgs* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="78733-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="78733-114">Dados passados no parâmetro *DynamicGroupArgs* da chamada para [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) ou [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).</span><span class="sxs-lookup"><span data-stu-id="78733-114">Data passed in the *DynamicGroupArgs* parameter of the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) or [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).</span></span>

</dd> <dt>

<span data-ttu-id="78733-115">*pbAceApplicable* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="78733-115">*pbAceApplicable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78733-116">Um ponteiro para uma variável booliana que recebe os resultados da avaliação da lógica definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="78733-116">A pointer to a Boolean variable that receives the results of the evaluation of the logic defined by the application.</span></span>

<span data-ttu-id="78733-117">Os resultados serão **verdadeiros** se a lógica determinar que a ACE é aplicável e será incluída na chamada para [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); caso contrário, os resultados serão **falsos**.</span><span class="sxs-lookup"><span data-stu-id="78733-117">The results are **TRUE** if the logic determines that the ACE is applicable and will be included in the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); otherwise, the results are **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78733-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78733-118">Return value</span></span>

<span data-ttu-id="78733-119">Se a função for realizada com sucesso, a função retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="78733-119">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="78733-120">Se a função não puder executar a avaliação, ela retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="78733-120">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="78733-121">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para retornar um erro para a função de verificação de acesso.</span><span class="sxs-lookup"><span data-stu-id="78733-121">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="remarks"></a><span data-ttu-id="78733-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="78733-122">Remarks</span></span>

<span data-ttu-id="78733-123">As variáveis de atributo de segurança devem estar presentes no contexto do cliente, se referenciadas em uma expressão condicional, caso contrário, o termo de expressão condicional que as referenciará será avaliado como desconhecido.</span><span class="sxs-lookup"><span data-stu-id="78733-123">Security attribute variables must be present in the client context if referred to in a conditional expression, otherwise the conditional expression term referencing them will evaluate to unknown.</span></span>

<span data-ttu-id="78733-124">Para obter mais informações, consulte as visões gerais [sobre como o AccessCheck funciona](how-dacls-control-access-to-an-object.md) e a [política de autorização centralizada](centralized-authorization-policy.md) .</span><span class="sxs-lookup"><span data-stu-id="78733-124">For more information, see the [How AccessCheck Works](how-dacls-control-access-to-an-object.md) and [Centralized Authorization Policy](centralized-authorization-policy.md) overviews.</span></span>

## <a name="requirements"></a><span data-ttu-id="78733-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78733-125">Requirements</span></span>



| <span data-ttu-id="78733-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="78733-126">Requirement</span></span> | <span data-ttu-id="78733-127">Valor</span><span class="sxs-lookup"><span data-stu-id="78733-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="78733-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78733-128">Minimum supported client</span></span><br/> | <span data-ttu-id="78733-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="78733-129">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="78733-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78733-130">Minimum supported server</span></span><br/> | <span data-ttu-id="78733-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78733-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="78733-132">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="78733-132">Redistributable</span></span><br/>          | <span data-ttu-id="78733-133">Pacote de ferramentas de administração do Windows Server 2003 no Windows XP</span><span class="sxs-lookup"><span data-stu-id="78733-133">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78733-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="78733-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78733-135">Funções básicas de controle de acesso</span><span class="sxs-lookup"><span data-stu-id="78733-135">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="78733-136">Política de autorização centralizada</span><span class="sxs-lookup"><span data-stu-id="78733-136">Centralized Authorization Policy</span></span>](centralized-authorization-policy.md)
</dt> <dt>

[<span data-ttu-id="78733-137">Como a AccessCheck funciona</span><span class="sxs-lookup"><span data-stu-id="78733-137">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="78733-138">**AuthzAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="78733-138">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[<span data-ttu-id="78733-139">**AuthzCachedAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="78733-139">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="78733-140">**AuthzInitializeRemoteResourceManager**</span><span class="sxs-lookup"><span data-stu-id="78733-140">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="78733-141">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="78733-141">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

