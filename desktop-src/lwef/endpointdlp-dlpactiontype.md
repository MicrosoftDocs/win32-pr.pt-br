---
description: Especifica o tipo de ação de uma operação de DLP (prevenção de perda de dados) de ponto de extremidade.
title: Enumeração DlpActionType (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 7900e79536cc9ac45037e205962a563bcde8878a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495362"
---
# <a name="dlpactiontype-enumeration"></a><span data-ttu-id="c560a-103">Enumeração DlpActionType</span><span class="sxs-lookup"><span data-stu-id="c560a-103">DlpActionType enumeration</span></span>

<span data-ttu-id="c560a-104">Especifica o tipo de ação de uma operação de DLP (prevenção de perda de dados) de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c560a-104">Specifies the action type of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c560a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c560a-105">Syntax</span></span>


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a><span data-ttu-id="c560a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c560a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c560a-107">*DlpActionTypeCopyToRemovableMedia*</span><span class="sxs-lookup"><span data-stu-id="c560a-107">*DlpActionTypeCopyToRemovableMedia*</span></span>
</dt> <dd>

<span data-ttu-id="c560a-108">Uma operação de cópia para mídia removível.</span><span class="sxs-lookup"><span data-stu-id="c560a-108">A copy operation to removable media.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c560a-109">*DlpActionTypeCopyToNetworkShare*</span><span class="sxs-lookup"><span data-stu-id="c560a-109">*DlpActionTypeCopyToNetworkShare*</span></span>
</dt> <dd>

<span data-ttu-id="c560a-110">Uma operação de cópia para uma pasta de rede compartilhada.</span><span class="sxs-lookup"><span data-stu-id="c560a-110">A copy operation to a shared network folder.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c560a-111">*DlpActionTypeCopyToClipboard*</span><span class="sxs-lookup"><span data-stu-id="c560a-111">*DlpActionTypeCopyToClipboard*</span></span>
</dt> <dd>

<span data-ttu-id="c560a-112">Uma operação de cópia para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="c560a-112">A copy operation to the clipboard.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c560a-113">*DlpActionTypePrint*</span><span class="sxs-lookup"><span data-stu-id="c560a-113">*DlpActionTypePrint*</span></span>
</dt> <dd>

<span data-ttu-id="c560a-114">Uma operação de impressão.</span><span class="sxs-lookup"><span data-stu-id="c560a-114">A print operation.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="c560a-115">*DlpActionTypeScreenClip*</span><span class="sxs-lookup"><span data-stu-id="c560a-115">*DlpActionTypeScreenClip*</span></span>
</dt> <dd>

<span data-ttu-id="c560a-116">Uma operação de captura de tela.</span><span class="sxs-lookup"><span data-stu-id="c560a-116">A screen capture operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c560a-117">*DlpActionTypeAccessByUnallowedApp*</span><span class="sxs-lookup"><span data-stu-id="c560a-117">*DlpActionTypeAccessByUnallowedApp*</span></span>
</dt> <dd>

<span data-ttu-id="c560a-118">Uma operação executada por um aplicativo não permitido.</span><span class="sxs-lookup"><span data-stu-id="c560a-118">An operation performed by an unallowed app.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="c560a-119">*DlpActionTypeCloudAppEgress*</span><span class="sxs-lookup"><span data-stu-id="c560a-119">*DlpActionTypeCloudAppEgress*</span></span>
</dt> <dd>

<span data-ttu-id="c560a-120">Uma operação direcionada a um local de nuvem.</span><span class="sxs-lookup"><span data-stu-id="c560a-120">An operation targeted to a cloud location.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c560a-121">*DlpActionTypeAccessByBluetoothApp*</span><span class="sxs-lookup"><span data-stu-id="c560a-121">*DlpActionTypeAccessByBluetoothApp*</span></span>
</dt> <dd>

<span data-ttu-id="c560a-122">Uma operação que inclui o acesso por um aplicativo Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="c560a-122">An operation that includes access by a bluetooth app.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c560a-123">*DlpActionTypeAccessByRDPApp*</span><span class="sxs-lookup"><span data-stu-id="c560a-123">*DlpActionTypeAccessByRDPApp*</span></span>
</dt> <dd>

<span data-ttu-id="c560a-124">Uma operação que inclui o acesso por uma área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="c560a-124">An operation that includes access by a remote desktop.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c560a-125">*DlpActionTypeCount*</span><span class="sxs-lookup"><span data-stu-id="c560a-125">*DlpActionTypeCount*</span></span>
</dt> <dd>

<span data-ttu-id="c560a-126">O valor máximo da enumeração.</span><span class="sxs-lookup"><span data-stu-id="c560a-126">The maximum value of the enumeration.</span></span>

</dd> </dl>
 

## <a name="remarks"></a><span data-ttu-id="c560a-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c560a-127">Remarks</span></span>

<span data-ttu-id="c560a-128">Os valores dessa enumeração são usados pela estrutura de [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) .</span><span class="sxs-lookup"><span data-stu-id="c560a-128">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c560a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c560a-129">Requirements</span></span>



| <span data-ttu-id="c560a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c560a-130">Requirement</span></span>          |    <span data-ttu-id="c560a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c560a-131">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c560a-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c560a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c560a-133">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="c560a-133">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

