---
description: Uma função definida pelo aplicativo que cria uma lista de SIDs (identificadores de segurança) que se aplicam a um cliente. AuthzComputeGroupsCallback é um espaço reservado para o nome da função definida pelo aplicativo.
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: Função de retorno de chamada AuthzComputeGroupsCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3728f8114d87d07ddb33dd77a6fda5db30d07cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663598"
---
# <a name="authzcomputegroupscallback-callback-function"></a><span data-ttu-id="f2cf8-104">Função de retorno de chamada AuthzComputeGroupsCallback</span><span class="sxs-lookup"><span data-stu-id="f2cf8-104">AuthzComputeGroupsCallback callback function</span></span>

<span data-ttu-id="f2cf8-105">A função **AuthzComputeGroupsCallback** é uma função definida pelo aplicativo que cria uma lista de SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) que se aplicam a um cliente.</span><span class="sxs-lookup"><span data-stu-id="f2cf8-105">The **AuthzComputeGroupsCallback** function is an application-defined function that creates a list of [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that apply to a client.</span></span> <span data-ttu-id="f2cf8-106">**AuthzComputeGroupsCallback** é um espaço reservado para o nome da função definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f2cf8-106">**AuthzComputeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2cf8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2cf8-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a><span data-ttu-id="f2cf8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2cf8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2cf8-109">*hAuthzClientContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2cf8-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cf8-110">Um identificador para um contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="f2cf8-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="f2cf8-111">*Argumentos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2cf8-111">*Args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cf8-112">Dados passados no parâmetro *DynamicGroupArgs* de uma chamada para a função [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)ou [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) .</span><span class="sxs-lookup"><span data-stu-id="f2cf8-112">Data passed in the *DynamicGroupArgs* parameter of a call to the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid), or [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function.</span></span>

</dd> <dt>

<span data-ttu-id="f2cf8-113">*pSidAttrArray* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f2cf8-113">*pSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cf8-114">Um ponteiro para uma variável de ponteiro que recebe o endereço de uma matriz de [**Sid e estruturas de \_ \_ atributos**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) .</span><span class="sxs-lookup"><span data-stu-id="f2cf8-114">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="f2cf8-115">Essas estruturas representam os grupos aos quais o cliente pertence.</span><span class="sxs-lookup"><span data-stu-id="f2cf8-115">These structures represent the groups to which the client belongs.</span></span>

</dd> <dt>

<span data-ttu-id="f2cf8-116">*pSidCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f2cf8-116">*pSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cf8-117">O número de estruturas em *pSidAttrArray*.</span><span class="sxs-lookup"><span data-stu-id="f2cf8-117">The number of structures in *pSidAttrArray*.</span></span>

</dd> <dt>

<span data-ttu-id="f2cf8-118">*pRestrictedSidAttrArray* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f2cf8-118">*pRestrictedSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cf8-119">Um ponteiro para uma variável de ponteiro que recebe o endereço de uma matriz de [**Sid e estruturas de \_ \_ atributos**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) .</span><span class="sxs-lookup"><span data-stu-id="f2cf8-119">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="f2cf8-120">Essas estruturas representam os grupos dos quais o cliente é restrito.</span><span class="sxs-lookup"><span data-stu-id="f2cf8-120">These structures represent the groups from which the client is restricted.</span></span>

</dd> <dt>

<span data-ttu-id="f2cf8-121">*pRestrictedSidCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f2cf8-121">*pRestrictedSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cf8-122">O número de estruturas em *pSidRestrictedAttrArray*.</span><span class="sxs-lookup"><span data-stu-id="f2cf8-122">The number of structures in *pSidRestrictedAttrArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2cf8-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2cf8-123">Return value</span></span>

<span data-ttu-id="f2cf8-124">Se a função retornar com êxito uma lista de SIDs, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="f2cf8-124">If the function successfully returns a list of SIDs, the return value is **TRUE**.</span></span>

<span data-ttu-id="f2cf8-125">Se a função falhar, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="f2cf8-125">If the function fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2cf8-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2cf8-126">Remarks</span></span>

<span data-ttu-id="f2cf8-127">Os aplicativos também podem adicionar SIDs ao contexto do cliente chamando [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).</span><span class="sxs-lookup"><span data-stu-id="f2cf8-127">Applications can also add SIDs to the client context by calling [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).</span></span>

<span data-ttu-id="f2cf8-128">As variáveis de atributo devem estar na forma de uma expressão quando usadas com operadores lógicos; caso contrário, eles serão avaliados como desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="f2cf8-128">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2cf8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2cf8-129">Requirements</span></span>



| <span data-ttu-id="f2cf8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2cf8-130">Requirement</span></span> | <span data-ttu-id="f2cf8-131">Valor</span><span class="sxs-lookup"><span data-stu-id="f2cf8-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="f2cf8-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2cf8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f2cf8-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f2cf8-133">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f2cf8-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2cf8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f2cf8-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2cf8-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="f2cf8-136">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f2cf8-136">Redistributable</span></span><br/>          | <span data-ttu-id="f2cf8-137">Pacote de ferramentas de administração do Windows Server 2003 no Windows XP</span><span class="sxs-lookup"><span data-stu-id="f2cf8-137">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2cf8-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2cf8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2cf8-139">Funções básicas de controle de acesso</span><span class="sxs-lookup"><span data-stu-id="f2cf8-139">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="f2cf8-140">**AuthzAddSidsToContext**</span><span class="sxs-lookup"><span data-stu-id="f2cf8-140">**AuthzAddSidsToContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[<span data-ttu-id="f2cf8-141">**AuthzCachedAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="f2cf8-141">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="f2cf8-142">**AuthzInitializeContextFromAuthzContext**</span><span class="sxs-lookup"><span data-stu-id="f2cf8-142">**AuthzInitializeContextFromAuthzContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[<span data-ttu-id="f2cf8-143">**AuthzInitializeContextFromSid**</span><span class="sxs-lookup"><span data-stu-id="f2cf8-143">**AuthzInitializeContextFromSid**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[<span data-ttu-id="f2cf8-144">**AuthzInitializeContextFromToken**</span><span class="sxs-lookup"><span data-stu-id="f2cf8-144">**AuthzInitializeContextFromToken**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[<span data-ttu-id="f2cf8-145">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="f2cf8-145">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[<span data-ttu-id="f2cf8-146">**SID \_ e \_ atributos**</span><span class="sxs-lookup"><span data-stu-id="f2cf8-146">**SID\_AND\_ATTRIBUTES**</span></span>](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

