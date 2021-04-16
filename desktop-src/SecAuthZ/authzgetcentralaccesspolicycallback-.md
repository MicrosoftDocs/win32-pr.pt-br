---
description: A função AuthzGetCentralAccessPolicyCallback é uma função definida pelo aplicativo que recupera a política de acesso central. AuthzGetCentralAccessPolicyCallback é um espaço reservado para o nome da função definida pelo aplicativo.
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: Função de retorno de chamada AuthzGetCentralAccessPolicyCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b96832fa647fde920a70ac3d6608c8ebb0048892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750194"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a><span data-ttu-id="93de3-104">Função de retorno de chamada AuthzGetCentralAccessPolicyCallback</span><span class="sxs-lookup"><span data-stu-id="93de3-104">AuthzGetCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="93de3-105">A função *AuthzGetCentralAccessPolicyCallback* é uma função definida pelo aplicativo que recupera a política de acesso central.</span><span class="sxs-lookup"><span data-stu-id="93de3-105">The *AuthzGetCentralAccessPolicyCallback* function is an application-defined function that retrieves the central access policy.</span></span> <span data-ttu-id="93de3-106">*AuthzGetCentralAccessPolicyCallback* é um espaço reservado para o nome da função definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93de3-106">*AuthzGetCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="93de3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93de3-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="93de3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93de3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93de3-109">*hAuthzClientContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93de3-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93de3-110">Identificador para o contexto do cliente.</span><span class="sxs-lookup"><span data-stu-id="93de3-110">Handle to the client context.</span></span>

</dd> <dt>

<span data-ttu-id="93de3-111">*capid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93de3-111">*capid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93de3-112">ID da política de acesso central a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="93de3-112">ID of the central access policy to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="93de3-113">*pArgs* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="93de3-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93de3-114">Argumentos opcionais que foram passados para a função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) por meio do membro **OptionalArguments** da estrutura de [**solicitação de \_ acesso \_ do AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_access_request) .</span><span class="sxs-lookup"><span data-stu-id="93de3-114">Optional arguments that were passed to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function through the **OptionalArguments** member of the [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) structure.</span></span>

</dd> <dt>

<span data-ttu-id="93de3-115">*pCentralAccessPolicyApplicable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="93de3-115">*pCentralAccessPolicyApplicable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93de3-116">Ponteiro para um valor booliano que o Gerenciador de recursos usa para indicar se uma política de acesso central deve ser usada durante a avaliação do acesso.</span><span class="sxs-lookup"><span data-stu-id="93de3-116">Pointer to a Boolean value that the resource manager uses to indicate whether a central access policy should be used during access evaluation.</span></span>

</dd> <dt>

<span data-ttu-id="93de3-117">*ppCentralAccessPolicy* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="93de3-117">*ppCentralAccessPolicy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93de3-118">Ponteiro para a política de acesso central (CAP) a ser usado para avaliar o acesso.</span><span class="sxs-lookup"><span data-stu-id="93de3-118">Pointer to the central access policy (CAP) to be used for evaluating access.</span></span> <span data-ttu-id="93de3-119">Se esse valor for **NULL**, a extremidade padrão será aplicada.</span><span class="sxs-lookup"><span data-stu-id="93de3-119">If this value is **NULL**, the default CAP is applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93de3-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93de3-120">Return value</span></span>

<span data-ttu-id="93de3-121">Se a função for realizada com sucesso, a função retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="93de3-121">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="93de3-122">Se a função não puder executar a avaliação, ela retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="93de3-122">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="93de3-123">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para retornar um erro para a função de verificação de acesso.</span><span class="sxs-lookup"><span data-stu-id="93de3-123">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="requirements"></a><span data-ttu-id="93de3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93de3-124">Requirements</span></span>



| <span data-ttu-id="93de3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="93de3-125">Requirement</span></span> | <span data-ttu-id="93de3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="93de3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="93de3-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93de3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="93de3-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="93de3-128">Windows 8 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="93de3-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93de3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="93de3-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="93de3-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="93de3-131">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="93de3-131">Redistributable</span></span><br/>          | <span data-ttu-id="93de3-132">Pacote de ferramentas de administração do Windows Server 2003 no Windows XP</span><span class="sxs-lookup"><span data-stu-id="93de3-132">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93de3-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="93de3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93de3-134">**\_solicitação de acesso de AUTHZ \_**</span><span class="sxs-lookup"><span data-stu-id="93de3-134">**AUTHZ\_ACCESS\_REQUEST**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[<span data-ttu-id="93de3-135">**informações de todas as AUTHZ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93de3-135">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="93de3-136">**AuthzAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="93de3-136">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

