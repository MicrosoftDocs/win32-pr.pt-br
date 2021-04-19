---
description: Especifica o nível de imposição de uma operação de DLP (prevenção de perda de dados) de ponto de extremidade.
title: Enumeração DlpAppEnforceLevel (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpAppEnforceLevel
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d0ccc8d0d39bc4022899deaeb9e8a81eae1f720f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495361"
---
# <a name="dlpappenforcelevel-enumeration"></a><span data-ttu-id="a2ea4-103">Enumeração DlpAppEnforceLevel</span><span class="sxs-lookup"><span data-stu-id="a2ea4-103">DlpAppEnforceLevel enumeration</span></span>

<span data-ttu-id="a2ea4-104">Especifica o nível de imposição de uma operação de DLP (prevenção de perda de dados) de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a2ea4-104">Specifies the enforcement level of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2ea4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2ea4-105">Syntax</span></span>


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a><span data-ttu-id="a2ea4-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a2ea4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a2ea4-107">*DlpAppEnforceLevelNone* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2ea4-107">*DlpAppEnforceLevelNone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ea4-108">Nenhuma imposição pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a2ea4-108">No enforcement by the app.</span></span> <span data-ttu-id="a2ea4-109">O sistema DLP irá impor a operação.</span><span class="sxs-lookup"><span data-stu-id="a2ea4-109">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a2ea4-110">*DlpAppEnforceLevelNotify* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2ea4-110">*DlpAppEnforceLevelNotify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ea4-111">O aplicativo TNE usará as APIs DLP para notificar o sistema DLP sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="a2ea4-111">Tne app will use the DLP APIs to notify the DLP system about the operation.</span></span> <span data-ttu-id="a2ea4-112">O sistema DLP irá impor a operação.</span><span class="sxs-lookup"><span data-stu-id="a2ea4-112">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a2ea4-113">*DlpAppEnforceLevelPrevent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2ea4-113">*DlpAppEnforceLevelPrevent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ea4-114">Sem suporte na versão atual.</span><span class="sxs-lookup"><span data-stu-id="a2ea4-114">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a2ea4-115">*DlpAppEnforceLevelFull* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2ea4-115">*DlpAppEnforceLevelFull* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ea4-116">Sem suporte na versão atual.</span><span class="sxs-lookup"><span data-stu-id="a2ea4-116">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a2ea4-117">*DlpAppEnforceLevelCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2ea4-117">*DlpAppEnforceLevelCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ea4-118">O valor máximo da enumeração.</span><span class="sxs-lookup"><span data-stu-id="a2ea4-118">The maximum value of the enumeration.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="a2ea4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2ea4-119">Remarks</span></span>

<span data-ttu-id="a2ea4-120">Os valores dessa enumeração são usados pela estrutura de [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) .</span><span class="sxs-lookup"><span data-stu-id="a2ea4-120">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>


## <a name="requirements"></a><span data-ttu-id="a2ea4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2ea4-121">Requirements</span></span>



| <span data-ttu-id="a2ea4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2ea4-122">Requirement</span></span>          |    <span data-ttu-id="a2ea4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a2ea4-123">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ea4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2ea4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ea4-125">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="a2ea4-125">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

