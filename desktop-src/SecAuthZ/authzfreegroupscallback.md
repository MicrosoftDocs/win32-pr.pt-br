---
description: Uma função definida pelo aplicativo que libera a memória alocada pela função AuthzComputeGroupsCallback. AuthzFreeGroupsCallback é um espaço reservado para o nome da função definida pelo aplicativo.
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: Função de retorno de chamada AuthzFreeGroupsCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7d8942acbc67f122ea79f0b9e98793628b5f21f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663597"
---
# <a name="authzfreegroupscallback-callback-function"></a><span data-ttu-id="19162-104">Função de retorno de chamada AuthzFreeGroupsCallback</span><span class="sxs-lookup"><span data-stu-id="19162-104">AuthzFreeGroupsCallback callback function</span></span>

<span data-ttu-id="19162-105">A função **AuthzFreeGroupsCallback** é uma função definida pelo aplicativo que libera a memória alocada pela função [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md) .</span><span class="sxs-lookup"><span data-stu-id="19162-105">The **AuthzFreeGroupsCallback** function is an application-defined function that frees memory allocated by the [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md) function.</span></span> <span data-ttu-id="19162-106">**AuthzFreeGroupsCallback** é um espaço reservado para o nome da função definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="19162-106">**AuthzFreeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="19162-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19162-107">Syntax</span></span>


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a><span data-ttu-id="19162-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19162-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19162-109">*pSidAttrArray* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19162-109">*pSidAttrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19162-110">Um ponteiro para a memória alocada por [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md).</span><span class="sxs-lookup"><span data-stu-id="19162-110">A pointer to memory allocated by [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19162-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19162-111">Return value</span></span>

<span data-ttu-id="19162-112">Essa função de retorno de chamada não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="19162-112">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19162-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="19162-113">Remarks</span></span>

<span data-ttu-id="19162-114">As variáveis de atributo devem estar na forma de uma expressão quando usadas com operadores lógicos; caso contrário, eles serão avaliados como desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="19162-114">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="19162-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19162-115">Requirements</span></span>



| <span data-ttu-id="19162-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="19162-116">Requirement</span></span> | <span data-ttu-id="19162-117">Valor</span><span class="sxs-lookup"><span data-stu-id="19162-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="19162-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19162-118">Minimum supported client</span></span><br/> | <span data-ttu-id="19162-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="19162-119">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="19162-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19162-120">Minimum supported server</span></span><br/> | <span data-ttu-id="19162-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19162-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="19162-122">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="19162-122">Redistributable</span></span><br/>          | <span data-ttu-id="19162-123">Pacote de ferramentas de administração do Windows Server 2003 no Windows XP</span><span class="sxs-lookup"><span data-stu-id="19162-123">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19162-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="19162-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19162-125">Funções básicas de controle de acesso</span><span class="sxs-lookup"><span data-stu-id="19162-125">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="19162-126">**AuthzComputeGroupsCallback**</span><span class="sxs-lookup"><span data-stu-id="19162-126">**AuthzComputeGroupsCallback**</span></span>](authzcomputegroupscallback.md)
</dt> </dl>

 

 




