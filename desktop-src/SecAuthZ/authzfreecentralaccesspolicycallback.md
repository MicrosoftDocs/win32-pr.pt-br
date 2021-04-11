---
description: A função AuthzFreeCentralAccessPolicyCallback é uma função definida pelo aplicativo que libera a memória alocada pela função AuthzGetCentralAccessPolicyCallback.
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: Função de retorno de chamada AuthzFreeCentralAccessPolicyCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: d2139c9fa106b6070a3c043d417bdbf23379084b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172322"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a><span data-ttu-id="26929-103">Função de retorno de chamada AuthzFreeCentralAccessPolicyCallback</span><span class="sxs-lookup"><span data-stu-id="26929-103">AuthzFreeCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="26929-104">A função *AuthzFreeCentralAccessPolicyCallback* é uma função definida pelo aplicativo que libera a memória alocada pela função [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) .</span><span class="sxs-lookup"><span data-stu-id="26929-104">The *AuthzFreeCentralAccessPolicyCallback* function is an application-defined function that frees memory allocated by the [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) function.</span></span> <span data-ttu-id="26929-105">*AuthzFreeCentralAccessPolicyCallback* é um espaço reservado para o nome da função definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26929-105">*AuthzFreeCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="26929-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26929-106">Syntax</span></span>


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="26929-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26929-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26929-108">*pCentralAccessPolicy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26929-108">*pCentralAccessPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26929-109">Ponteiro para a política de acesso central a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="26929-109">Pointer to the central access policy to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26929-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26929-110">Return value</span></span>

<span data-ttu-id="26929-111">Se a função for realizada com sucesso, a função retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="26929-111">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="26929-112">Se a função não puder executar a avaliação, ela retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="26929-112">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="26929-113">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para retornar um erro para a função de verificação de acesso.</span><span class="sxs-lookup"><span data-stu-id="26929-113">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="see-also"></a><span data-ttu-id="26929-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="26929-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26929-115">**informações de todas as AUTHZ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="26929-115">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="26929-116">*AuthzGetCentralAccessPolicyCallback*</span><span class="sxs-lookup"><span data-stu-id="26929-116">*AuthzGetCentralAccessPolicyCallback*</span></span>](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
