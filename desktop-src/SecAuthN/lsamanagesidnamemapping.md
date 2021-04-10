---
UID: ''
title: Função LsaManageSidNameMapping
description: Adiciona ou remove mapeamentos de SID/nome do conjunto de mapeamento registrado com o serviço de pesquisa do LSA.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: fc0065c3964718d690149693f3c71ec4e9f676ec
ms.sourcegitcommit: 382c7259008374408368c173e0027fb641c848fe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2020
ms.locfileid: "104293845"
---
# <a name="lsamanagesidnamemapping-function"></a><span data-ttu-id="25b8e-103">Função LsaManageSidNameMapping</span><span class="sxs-lookup"><span data-stu-id="25b8e-103">LsaManageSidNameMapping function</span></span>

## <a name="description"></a><span data-ttu-id="25b8e-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="25b8e-104">Description</span></span>

<span data-ttu-id="25b8e-105">A função **LsaManageSidNameMapping** adiciona ou remove mapeamentos de Sid/nome do conjunto de mapeamento registrado com o serviço de pesquisa do LSA.</span><span class="sxs-lookup"><span data-stu-id="25b8e-105">The **LsaManageSidNameMapping** function adds or removes SID/name mappings from the mapping set registered with the LSA Lookup Service.</span></span>

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a><span data-ttu-id="25b8e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25b8e-106">Parameters</span></span>

### <a name="optype-in"></a><span data-ttu-id="25b8e-107">OpType [in]</span><span class="sxs-lookup"><span data-stu-id="25b8e-107">OpType [in]</span></span>

<span data-ttu-id="25b8e-108">Indica se uma função this está sendo chamada para adicionar ou remover um mapeamento de SID/nome.</span><span class="sxs-lookup"><span data-stu-id="25b8e-108">Indicates if a this function is being called to add or remove an SID/name mapping.</span></span>

### <a name="opinput-in"></a><span data-ttu-id="25b8e-109">OpInput [in]</span><span class="sxs-lookup"><span data-stu-id="25b8e-109">OpInput [in]</span></span>

<span data-ttu-id="25b8e-110">Indica o domínio, a conta e os valores de SID a serem usados durante esta operação.</span><span class="sxs-lookup"><span data-stu-id="25b8e-110">Indicates the domain, account, and SID values to use during this operation.</span></span> <span data-ttu-id="25b8e-111">Sinalizadores adicionais também podem ser definidos nessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="25b8e-111">Additional flags can also be set within this structure.</span></span>

### <a name="opoutput-out"></a><span data-ttu-id="25b8e-112">OpOutput [saída]</span><span class="sxs-lookup"><span data-stu-id="25b8e-112">OpOutput [out]</span></span>

<span data-ttu-id="25b8e-113">Contém um valor de [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) que indica êxito ou falha na operação.</span><span class="sxs-lookup"><span data-stu-id="25b8e-113">Contains a value of [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) that indicates operation success or failure.</span></span>

| <span data-ttu-id="25b8e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="25b8e-114">Value</span></span> | <span data-ttu-id="25b8e-115">Significado</span><span class="sxs-lookup"><span data-stu-id="25b8e-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="25b8e-116">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="25b8e-116">**Success**</span></span> | <span data-ttu-id="25b8e-117">A operação foi concluída sem erro.</span><span class="sxs-lookup"><span data-stu-id="25b8e-117">Operation is complete without error.</span></span> |
| <span data-ttu-id="25b8e-118">**NonMappingError**</span><span class="sxs-lookup"><span data-stu-id="25b8e-118">**NonMappingError**</span></span> | <span data-ttu-id="25b8e-119">Ocorreu um erro não relacionado ao mapeamento de nome de SID.</span><span class="sxs-lookup"><span data-stu-id="25b8e-119">An error unrelated to SID-name mapping has occurred.</span></span> |
| <span data-ttu-id="25b8e-120">**NameCollision**</span><span class="sxs-lookup"><span data-stu-id="25b8e-120">**NameCollision**</span></span> | <span data-ttu-id="25b8e-121">Falha na operação devido à colisão de nome.</span><span class="sxs-lookup"><span data-stu-id="25b8e-121">Operation failure due to name collision.</span></span> |
| <span data-ttu-id="25b8e-122">**SidCollision**</span><span class="sxs-lookup"><span data-stu-id="25b8e-122">**SidCollision**</span></span> | <span data-ttu-id="25b8e-123">Falha na operação devido à colisão de SID.</span><span class="sxs-lookup"><span data-stu-id="25b8e-123">Operation failure due to SID collision.</span></span> |
| <span data-ttu-id="25b8e-124">**DomainNotFound (Domínio não encontrado)**</span><span class="sxs-lookup"><span data-stu-id="25b8e-124">**DomainNotFound**</span></span> | <span data-ttu-id="25b8e-125">Domínio correspondente não encontrado.</span><span class="sxs-lookup"><span data-stu-id="25b8e-125">Corresponding domain not found.</span></span> |
| <span data-ttu-id="25b8e-126">**DomainSidPrefixMismatch**</span><span class="sxs-lookup"><span data-stu-id="25b8e-126">**DomainSidPrefixMismatch**</span></span> | <span data-ttu-id="25b8e-127">O SID fornecido não tem o prefixo de domínio correto.</span><span class="sxs-lookup"><span data-stu-id="25b8e-127">Provided SID doesn't have the correct domain prefix.</span></span> |
| <span data-ttu-id="25b8e-128">**MappingNotFound**</span><span class="sxs-lookup"><span data-stu-id="25b8e-128">**MappingNotFound**</span></span> | <span data-ttu-id="25b8e-129">Mapeamento não encontrado no cache.</span><span class="sxs-lookup"><span data-stu-id="25b8e-129">Mapping not found in the cache.</span></span> |

## <a name="returns"></a><span data-ttu-id="25b8e-130">Retornos</span><span class="sxs-lookup"><span data-stu-id="25b8e-130">Returns</span></span>

<span data-ttu-id="25b8e-131">Se o mapeamento for inserido com êxito, o valor de retorno será STATUS_SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="25b8e-131">If the mapping is inserted successfully, the return value is STATUS_SUCCESS.</span></span>
<span data-ttu-id="25b8e-132">Caso contrário, se a função falhar devido a conflitos de SID ou de nome, STATUS_INVALID_PARAMETER erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="25b8e-132">Otherwise, if the function fails due to SID or name conflicts, STATUS_INVALID_PARAMETER error will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="25b8e-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="25b8e-133">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="25b8e-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="25b8e-134">See also</span></span>
