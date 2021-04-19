---
description: Fornece o sistema com informações de status após a conclusão de uma operação de área de transferência de stash.
title: Função DlpNotifyPostStashClipboard (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e549593acab6d74edf838a0f82952d8f3034bfcc
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495326"
---
# <a name="dlpnotifypoststashclipboard-function"></a><span data-ttu-id="534c3-103">Função DlpNotifyPostStashClipboard</span><span class="sxs-lookup"><span data-stu-id="534c3-103">DlpNotifyPostStashClipboard function</span></span>

<span data-ttu-id="534c3-104">Fornece o sistema com informações de status após a conclusão de uma operação de área de transferência de stash.</span><span class="sxs-lookup"><span data-stu-id="534c3-104">Provides the system with status information after a stash clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="534c3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="534c3-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="534c3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="534c3-106">Parameters</span></span>


<dl> <dt>

<span data-ttu-id="534c3-107">*OpStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="534c3-107">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="534c3-108">Um ponteiro para uma estrutura de [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contém informações de status sobre a operação de área de transferência de stash.</span><span class="sxs-lookup"><span data-stu-id="534c3-108">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the stash clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="534c3-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="534c3-109">Return value</span></span>

<span data-ttu-id="534c3-110">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="534c3-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="534c3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="534c3-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="534c3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="534c3-112">Requirements</span></span>



| <span data-ttu-id="534c3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="534c3-113">Requirement</span></span>          |    <span data-ttu-id="534c3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="534c3-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="534c3-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="534c3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="534c3-116">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="534c3-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="534c3-117">DLL</span><span class="sxs-lookup"><span data-stu-id="534c3-117">DLL</span></span><br/>                      | <span data-ttu-id="534c3-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="534c3-118">EndpointDlp.dll</span></span> |