---
description: Associa uma ação de DLP (prevenção de perda de dados) de ponto de extremidade com um nível de imposição.
title: Estrutura de DLP_APP_OP_ENLIGHTENED_LEVEL (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_APP_OP_ENLIGHTENED_LEVEL
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 2d9c1aa8335078cad71832c6090cada1669641cb
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495365"
---
# <a name="dlp_app_op_enlightened_level-structure"></a><span data-ttu-id="7a2eb-103">Estrutura de DLP_APP_OP_ENLIGHTENED_LEVEL</span><span class="sxs-lookup"><span data-stu-id="7a2eb-103">DLP_APP_OP_ENLIGHTENED_LEVEL structure</span></span>

<span data-ttu-id="7a2eb-104">Associa uma ação de DLP (prevenção de perda de dados) de ponto de extremidade com um nível de imposição.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-104">Associates an endpoint Data Loss Prevention (DLP) action with an enforcement level.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a2eb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a2eb-105">Syntax</span></span>


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a><span data-ttu-id="7a2eb-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7a2eb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a2eb-107">*Operação* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7a2eb-107">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a2eb-108">Um valor da enumeração [DlpActionType](endpointdlp-dlpactiontype.md) especificando o tipo de ação de DLP do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-108">A value from the [DlpActionType](endpointdlp-dlpactiontype.md) enumeration specifying the endpoint DLP action type.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="7a2eb-109">*AppEnforcementLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a2eb-109">*AppEnforcementLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a2eb-110">Um valor de [DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md) que especifica o nível de imposição para o tipo de ação de DLP de ponto de extremidade associado.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-110">A value from the [DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md) specifying the level of enforcement for the associated endpoint DLP action type.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="7a2eb-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a2eb-111">Remarks</span></span>

<span data-ttu-id="7a2eb-112">Passe uma matriz dessas estruturas em [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) para definir o modo de imposição para um conjunto de operações de DLP de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-112">Pass an array of these structures into [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) to set the enforcement mode for a set of endpoint DLP operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a2eb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a2eb-113">Requirements</span></span>



| <span data-ttu-id="7a2eb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a2eb-114">Requirement</span></span>          |    <span data-ttu-id="7a2eb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7a2eb-115">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a2eb-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a2eb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7a2eb-117">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="7a2eb-117">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

