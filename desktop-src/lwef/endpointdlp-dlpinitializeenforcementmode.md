---
description: Notifica o sistema sobre os modos de imposição desejados para um conjunto de operações de DLP (prevenção de perda de dados) de ponto de extremidade.
title: Função DlpInitializeEnforcementMode (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cff3e1609f15f2cbbe6f6d9f76c6433ba3f4e5d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495350"
---
# <a name="dlpinitializeenforcementmode-function"></a><span data-ttu-id="51511-103">Função DlpInitializeEnforcementMode</span><span class="sxs-lookup"><span data-stu-id="51511-103">DlpInitializeEnforcementMode function</span></span>

<span data-ttu-id="51511-104">Notifica o sistema sobre os modos de imposição desejados para um conjunto de operações de DLP (prevenção de perda de dados) de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="51511-104">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="51511-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51511-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a><span data-ttu-id="51511-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51511-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51511-107">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="51511-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51511-108">Um **DWORD** especificando o número de operações incluídas na matriz *OperationEnforcement* .</span><span class="sxs-lookup"><span data-stu-id="51511-108">A **DWORD** specifying the number of operations included in the *OperationEnforcement* array.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="51511-109">*OperationEnforcement* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="51511-109">*OperationEnforcement* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51511-110">Uma matriz de estruturas [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) que especificam o nível de imposição para uma operação de DLP de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="51511-110">An array of [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structures that specify the enforcement level for an endpoint DLP operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="51511-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51511-111">Return value</span></span>

<span data-ttu-id="51511-112">Retorna um HRESULT que inclui, mas não se limita a, os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="51511-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="51511-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="51511-113">HRESULT</span></span> | <span data-ttu-id="51511-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="51511-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="51511-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="51511-115">S_OK</span></span> | <span data-ttu-id="51511-116">A função foi concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="51511-116">The function completed successfully</span></span> |
| <span data-ttu-id="51511-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="51511-117">E_INVALIDARG</span></span> | <span data-ttu-id="51511-118">Um ou mais dos parâmetros de função são inválidos.</span><span class="sxs-lookup"><span data-stu-id="51511-118">One or more of the function parameters are invalid.</span></span> |
| <span data-ttu-id="51511-119">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="51511-119">E_OUTOFMEMORY</span></span> | <span data-ttu-id="51511-120">Falha na alocação de memória para a operação.</span><span class="sxs-lookup"><span data-stu-id="51511-120">Memory allocation for the operation failed.</span></span> |



## <a name="remarks"></a><span data-ttu-id="51511-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="51511-121">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="51511-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51511-122">Requirements</span></span>



| <span data-ttu-id="51511-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="51511-123">Requirement</span></span>          |    <span data-ttu-id="51511-124">Valor</span><span class="sxs-lookup"><span data-stu-id="51511-124">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51511-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51511-125">Minimum supported client</span></span><br/> | <span data-ttu-id="51511-126">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="51511-126">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="51511-127">DLL</span><span class="sxs-lookup"><span data-stu-id="51511-127">DLL</span></span><br/>                      | <span data-ttu-id="51511-128">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="51511-128">EndpointDlp.dll</span></span> |